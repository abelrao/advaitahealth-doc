#### advaitahealth-doc
AdvaitaHealth doc

#### 项目的架构
![avatar](./image/arch.jpg)

####  项目模块 
![avatar](./image/module.jpg)

#### 合约逻辑
* 传统问卷上链
* 现代问卷上链

#### 合约代码

* [Contract Code](https://github.com/abortrao/ink-example/blob/main/advaita_health_contract/lib.rs)
* [polkadot-js-contract](https://polkadot.js.org/docs/api-contract/start/contract.tx)


#### 合约方法说明
合约名称: `advaita_health_contrac`

方法说明:

    // 添加现代问卷 
    pub fn add_modern_survey(&mut self, info: Survey) {}
    // 获取现代问卷列表
    pub fn modern_survey_list(&self) -> Vec<Survey> {}
    // 获取现代问卷
    pub fn get_modern_survey(&self, index: u64) -> Survey {}


    // 添加传统问卷
    pub fn add_tradition_survey(&mut self, info: Survey) {}
    // 获取传统问卷
    pub fn get_tradition_survey(&self, index: u64) -> Survey {}
    // 传统问卷列表
    pub fn tradition_survey_list(&self) -> Vec<Survey> {}

    // 添加处方
    pub fn add_prescription(&mut self, info: Prescription) {}
    // 查看单个处方
    pub fn get_prescription(&self, index: u64) -> Prescription {}
    // 处方列表 
    pub fn prescription_list(&self) -> Vec<Prescription> {}





tips: 
* 暂时先提供基础功能，具体的业务逻辑确定，随时沟通
* 具体怎调用合约请参考 [polkadot-js-contract](https://polkadot.js.org/docs/api-contract/start/contract.tx) 这部分的API
* [canvas-ui](https://github.com/paritytech/canvas-ui) 使用这个工具可以部署调用合约
* 这里提供一个合约文件，可以直接部署，[合约文件](https://github.com/abortrao/ink-example/tree/main/contract/advaita_health)
* 必须部署包含合约模块的 substrate 节点，substrate 全节点和 substrate-contract-node 都支持 