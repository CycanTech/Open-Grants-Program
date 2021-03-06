# Open Grant Proposal

* **Project Name:** GVM Bridge
* **Team Name:** Cycan Technologies
* **Payment Address:** 0x04822c1E25c9C8F4ce4980bc1E3e91b2dD4E6A91


## Project Overview :page_facing_up: 

### Overview
* There are many projects on Ethereum that are developed in solidity and run on EVM. To take advantage of these legacy resources, an EVM implementation has been integrated in Polkadot. However, the challenge now is that WASM contracts and EVM contracts cannot call each other. This limits the integration between WASM contract resources and EVM contract resources.
* As the technology develops, Polkadot is likely to support more smart contract VMs which will create challenges for resource integration with the original VM contracts.
* Therefore, there is a need to develop a system (Generic VM Bridge - GVM Bridge) and a standard (VM General ABI - VM GABI) to achieve resource integration through VM inter-modulation protocols. This will allow the resources of various VMs to be used with each other immediately without migration which will improve the utilization of resources.

### Project Details
Through the GVM Bridge system and the VM interconnection protocol, smart contracts between VMs can be invoked to achieve resource consolidation. Resources from different VMs can be used immediately without migration which will improve resource utilization. 
#### Technical Design Overview
GVM Bridge will provide a GVM Bridge Framework component and ABI conversion tools, Trans4WABI and Trans4EABI, for converting WASM ABI to VM GABI and EVM ABI to VM GABI. The WASM-Proxy pallet and the EVM-Proxy pallet specifically implement WASM VM and EVM calls.
The functions of these components are:

#### GVM Bridge Framework
1. Build inter-call framework for different VM contracts to provide the interface for virtual machine proxy access.
2. Implement VM proxy registration.
3. Provide encapsulation of public standard components like AccountId, Block, etc.
4. Provide an ABI conversion access interface.
5. Provide access to the contract invocation interface.

#### WASM-Proxy pallet
1. Implement the GVM Bridge Framework interface.
2. Implement the inter-conversion of VM GABI parameters and WASM ABI parameters.
3. Implement the inter-conversion between public standard components and WASM components.
4. Implement the host function for contract inter-call.

#### EVM-Proxy pallet
1. Implement the GVM Bridge Framework interface.
2. Implement the inter-conversion of VM GABI parameters and EVM ABI parameters.
3. Implement the inter-conversion between public standard components and EVM components.
4. Implement the pre-compiled contract for contract inter-calls.

#### Trans4WABI
1. Implement WASM ABI to VM GABI conversion.
2. Implement VM GABI to WASM ABI conversion.

#### Trans4EABI
1. Implement EVM ABI to VM GABI conversion.
2. Implement VM GABI to EVM ABI conversion.

#### Other
To facilitate developers to develop contract inter-call functions, we will provide sample codes for WASM contract and EVM contract inter-calling, such as inter-calling ERC20 contracts, etc. 

### Ecosystem Fit
The project will enable integration of the WASM application and EVM application ecology on the Cycan/ELP parachain.
As a Polkadot Parachain project, we understand in the foreseeable future it will be necessary to not only vigorously develop the WASM contract application ecology, but also to quickly introduce the application ecology of Ethereum for migration.
When the demand begins for assembly DeFi components such as "Lego blocks" in the same chain and across the ecology, it is particularly important to achieve seamless integration and intermodulation between WASM and EVM.
This project will be fully open-source and strive to become one of the common modules of the Substrate to be independently cited by Polkadot / Kusama's parachain project parties. This will aid in our quest to achieve seamless integration between EVM and WASM contract applications.

## Team 👥
The team behind GVM Bridge is the Cycan team, an early-stage core team of experts from around the world with a background in finance, blockchain development and large-scale software architectures serving multiple industries, business development and media. Cycan has a core team of ten developers including a development leader, seven Rust developers, one product manager, and one front-end engineer.

### Team members
Cycan led by:
* **Donald Gao**: Founder and Financial Model Designer
* **Benoit Lavorata**: Global Tech Partner and IT architect

### Contact
* **Contact Name:** Donald Gao
* **Contact Email:** Donald@cycan.network
* **Website:** https://cycan.network

### Legal Structure
* **Registered Address:** 3 Fraser Street, #05-25 Duo Tower, 189352, Singapore
* **Registered Legal Entity:** Cycan Foundation Ltd.

### Team's experience
Cycan’s team has a deep experience in blockchain technology development and financial model design.

The team has developed public chains similar to Ethereum, cross-chain bridges connecting DPOS-based side chain and the notary network, and an open consortium chain with rPBFT consensus mechanism. 
The team also has rich experience in smart contract development including our Bancor-based decentralized transaction protocol, decentralized identity, distributed domain registration and auction, decentralized stable coin protocols.

Our developers are proficient in Rust, Java, C++, Solidity, Go and other development languages and we are familiar with the Substrate development framework.

The team also has extensive experience in financial model designs especially for the trust instruments and relevant model designs.

The team has submitted our Everlasting Cash project to the Web3 Open Grants Program and delivered Milestone one.

Lastly, the team has a consolidated architectural and developmental experience with both experimental and real-world large-scale deployments.

### Team Code Repos
* https://github.com/CycanTech/GVM-Bridge

### Team LinkedIn Profiles
* https://www.linkedin.com/in/donald-gao-6bab74206/
* https://www.linkedin.com/in/benoitlavorata/

## Development Roadmap :nut_and_bolt: 

### Overview
* **Total Estimate Duration:** 14 weeks
* **Full-time Equivalent(FTE):** 5
* **Total cost:** 30,000 USD  (we accept up to 100% of payment in crypto currencies that are equivalent to $ including DAI)


### Milestone 1 – GVM Bridge V0.1
* **Total Estimate Duration:** 4 weeks
* **Full-time Equivalent(FTE):** 2
* **Total cost:** 6,000 USD
* **Task:** Design a minimal system for the GVM Bridge to enable simple interconnection and inter-call between WASM and EVM contracts.

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- |
| 0a.	| License	| Apache 2.0 |
| 0b.	| Documentation	| We will provide both inline documentation of the code and a tutorial that explains how a user can use GVM Bridge. |
| 0c.	| Testing Guide	| The code will have proper unit-test coverage to ensure functionality and robustness. In the guide we will describe how to run these tests. |
| 1.	| GVM Bridge Framework V0.1 	| Develop GVM Bridge Framework as a minimal system for the GVM Bridge to enable simple interconnection and inter-call. |
| 2.  | Exmaple of ERC20 contract calling | An example of calling ERC20 contract of other virtual machine types. |

### Milestone 2 – GVM Bridge V0.2
* **Total Estimate Duration:** 10 weeks
* **Full-time Equivalent(FTE):** 3
* **Total cost:** 24,000 USD
* **Task:** Design the initial standard of VM GABI; design the structure and interface of GVM Bridge Framework; initial implementation of WASM-Proxy pallet and EVM-Proxy pallet interface; initial implementation of Trans4WABI and Trans4EABI.

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- |
| 0a.	| License	| Apache 2.0 |
| 0b.	| Documentation	| We will provide both inline documentation of the code and a tutorial that explains how a user can use GVM Bridge. |
| 0c.	| Testing Guide	| The code will have proper unit-test coverage to ensure functionality and robustness. In the guide we will describe how to run these tests. |
| 1.	| GVM Bridge Framework V0.2	| The Framework V0.2 will contain WASM-Proxy pallet, EVM-Proxy pallet, Trans4WABI and Trans4EABI. |

## Future Plans
Further refining components and add supports for new VMs.
1. Tidy up and refactor the code.
2. Add support for new features of WASM and EVM.
3. Add support for new VMs.

## Additional Information :heavy_plus_sign: 

* What work has been done so far?<br>
1. Completed the development feasibility verification of the intermodulation between WASM contract and EVM contract. 
2. Completed the debugging of the WASM contract calling the EVM contract V0.1 code test.
3. Completed the debugging of the EVM contract calling the WASM contract V0.1 code test.
4. The next step is to complete the testing of the contract mutual calling function V0.1 code.

* Are there are any teams who have already contributed (financially) to the project?<br>
No
  
* Have you applied for other grants so far?<br>
Yes. We have submitted Everlasting Cash project to the Web3 Open Grants Program and delivered Milestone 1.
  
* Are there any other project similar to yours?<br>
No, we haven’t heard of a similar project yet.
