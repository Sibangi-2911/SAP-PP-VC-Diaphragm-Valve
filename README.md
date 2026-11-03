# SAP S/4HANA PP & Variant Configuration - Configurable Diaphragm Valve

## Project Overview

This project demonstrates an **end-to-end configurable manufacturing scenario** for a diaphragm valve using **SAP S/4HANA Production Planning (PP)** and **Variant Configuration (VC)**.

The objective of this project was to understand how customer-specific product requirements can be captured through Variant Configuration and translated into production planning and production execution.

The project covers the complete process from creating the configuration model and manufacturing master data through **Sales Order Configuration, MRP, Planned Order, Production Order, Goods Issue, Production Confirmation, and Goods Receipt**.

---

## Business Scenario

A diaphragm valve can be manufactured in different configurations depending on customer requirements.

Instead of creating and maintaining a separate product structure for every possible product combination, a **Configurable Material (KMAT)** can be used to represent the product family.

The required product specification is captured through characteristic values during configuration. The configuration model then determines the relevant manufacturing requirements for the selected product configuration.

### High-Level Business Flow

**Customer Requirement**  
↓  
**Sales Order**  
↓  
**Variant Configuration**  
↓  
**Production Planning**  
↓  
**Production Execution**  
↓  
**Finished Configured Diaphragm Valve**

---

## Project Objectives

The main objectives of this project were:

* Build a configurable diaphragm valve scenario in SAP S/4HANA
* Understand the relationship between Characteristics, Classes, and Configurable Materials
* Create a Configurable Material (KMAT)
* Maintain a Configuration Profile
* Create a Super BOM
* Understand and apply Object Dependencies
* Create the required Production Planning master data
* Integrate Variant Configuration with Production Planning
* Capture configurable product requirements through a Sales Order
* Execute Material Requirements Planning (MRP)
* Process a Planned Order
* Create and execute a Production Order
* Perform Goods Issue
* Perform Production Confirmation
* Post Goods Receipt
* Analyze and troubleshoot configuration and production-related issues

---

## SAP Areas Covered

### SAP Variant Configuration (VC)

The project provided practical exposure to:

* Characteristics
* Variant Class
* Configurable Material (KMAT)
* Configuration Profile
* Super BOM
* Object Dependencies
* Sales Order Configuration
* Configuration-dependent component selection
* Variant Matching exploration

### SAP Production Planning (PP)

The project covered:

* Material Master
* Bill of Material (BOM)
* Work Centers
* Routing
* Production Version
* Material Requirements Planning (MRP)
* Planned Order
* Production Order
* Component Availability
* Production Order Release
* Goods Issue
* Production Confirmation
* Goods Receipt

---

## End-to-End Process Flow

**Customer Requirement**  
↓  
**Sales Order**  
↓  
**Configurable Material**  
↓  
**Characteristic Value Selection**  
↓  
**Variant Configuration**  
↓  
**Configuration Logic**  
↓  
**Relevant Components**  
↓  
**MRP**  
↓  
**Planned Order**  
↓  
**Production Order**  
↓  
**Production Order Release**  
↓  
**Goods Issue**  
↓  
**Production Confirmation**  
↓  
**Goods Receipt**  
↓  
**Finished Configured Diaphragm Valve**

---

## 1. Material Master

The Material Master forms the foundation of the manufacturing scenario.

The project includes a configurable finished material together with the components required to manufacture the diaphragm valve.

Material Master information supports different areas of the manufacturing process, including:

* Material Planning
* Procurement
* Production
* Inventory Management
* Production Execution

The configurable finished product acts as the central material around which the Variant Configuration and Production Planning processes are built.

---

## 2. Characteristics

Characteristics represent the selectable properties of the configurable diaphragm valve.

They are used to represent the different options available when configuring the product.

### Concept

**Customer Requirement**  
↓  
**Characteristic Values**  
↓  
**Product Configuration**

Characteristics make it possible to capture product requirements systematically within the SAP configuration model.

---

## 3. Variant Class

The relevant Characteristics are grouped into a Variant Class.

### Relationship

**Characteristics**  
↓  
**Variant Class**  
↓  
**Configurable Material**

The Variant Class provides a structured way of grouping the Characteristics required to describe the configurable product.

---

## 4. Configurable Material (KMAT)

The diaphragm valve was modeled as a **Configurable Material (KMAT)**.

The Configurable Material enables different product variations to be represented through a common configurable product model.

### Configuration Flow

**Configurable Material**  
↓  
**Configuration**  
↓  
**Characteristic Selection**  
↓  
**Specific Product Configuration**

This creates a connection between the configurable product and the required product specification.

---

## 5. Configuration Profile

A Configuration Profile was maintained for the configurable diaphragm valve.

The Configuration Profile forms an important part of the Variant Configuration setup for the configurable material.

### Conceptual Relationship

**Configurable Material**  
↓  
**Configuration Profile**  
↓  
**Variant Configuration**  
↓  
**Characteristic Selection**

---

## 6. Super BOM

A **Super BOM** was used to represent the possible components associated with different configurations of the diaphragm valve.

The Super BOM provides a common component structure from which the relevant components for a particular configuration can be determined.

### Concept

**Configurable Diaphragm Valve**  
↓  
**Super BOM**  
↓  
**Possible Components**  
↓  
**Configuration Logic**  
↓  
**Relevant Components**

This approach supports configurable manufacturing without maintaining a completely independent product structure for every configuration.

---

## 7. Object Dependencies

Object Dependencies were used as part of the Variant Configuration model.

Dependencies introduce configuration logic that connects selected Characteristic values with the appropriate configuration behavior and product structure.

### Concept

**Characteristic Values**  
↓  
**Object Dependencies**  
↓  
**Configuration Evaluation**  
↓  
**Relevant Components**  
↓  
**Manufacturing Requirement**

This demonstrates how Variant Configuration can influence the manufacturing requirements of a configurable product.

---

## 8. Bill of Material (BOM)

The **Bill of Material (BOM)** defines the components required to manufacture the product.

For a configurable product, the BOM works together with the Variant Configuration model to determine the appropriate component structure.

### Simple Definition

**BOM = WHAT components are required to manufacture the product**

The BOM provides component information required during Production Planning and Production Execution.

---

## 9. Work Centers

Work Centers represent the production resources associated with manufacturing operations.

Operations defined in the Routing are assigned to the appropriate Work Centers.

### Concept

**Routing Operation**  
↓  
**Work Center**  
↓  
**Production Resource**

Work Centers provide information relevant to:

* Scheduling
* Capacity Planning
* Costing
* Production Execution

---

## 10. Routing

The **Routing** defines the sequence of operations required to manufacture the diaphragm valve.

While the BOM describes the required components, the Routing describes how the product is manufactured.

### Key Difference

**BOM = WHAT components are required**

**Routing = HOW the product is manufactured**

### Manufacturing Flow

**Product**  
↓  
**Operation 1**  
↓  
**Operation 2**  
↓  
**Operation 3**  
↓  
**Finished Product**

The relevant operations are assigned to appropriate Work Centers.

---

## 11. Production Version

The **Production Version** provides the relevant combination of BOM and Routing for production.

### Concept

**Production Version**  
↓  
**BOM + Routing**  
↓  
**Components + Operations**  
↓  
**Production Process**

The Production Version creates an important connection between the product structure and manufacturing process.

---

## Manufacturing Master Data Relationship

### Product Structure

**Material**  
↓  
**BOM**  
↓  
**Components**

### Manufacturing Process

**Material**  
↓  
**Routing**  
↓  
**Operations**  
↓  
**Work Centers**

### Production Version

**Material**  
↓  
**Production Version**  
↓  
**BOM + Routing**

### Variant Configuration Layer

**Characteristics**  
↓  
**Variant Class**  
↓  
**Configurable Material**  
↓  
**Configuration Profile**  
↓  
**Variant Configuration**  
↓  
**Super BOM**  
↓  
**Object Dependencies**  
↓  
**Relevant Manufacturing Requirements**

---

## 12. Sales Order Configuration

A Sales Order was used to represent the requirement for the configurable diaphragm valve.

During configuration, Characteristic values can be selected according to the required product specification.

### Sales Configuration Flow

**Customer Requirement**  
↓  
**Sales Order**  
↓  
**Configurable Material**  
↓  
**Characteristic Selection**  
↓  
**Configured Diaphragm Valve**

This demonstrates how a customer-specific product requirement can become an input into the manufacturing process.

---

## 13. Material Requirements Planning (MRP)

Material Requirements Planning was executed after the required demand and master data were available.

MRP evaluates material requirements associated with the requirement.

### Planning Flow

**Demand**  
↓  
**MRP**  
↓  
**Material Requirements**  
↓  
**Component Requirements**  
↓  
**Planning Proposals**

This stage demonstrated the importance of accurate manufacturing master data.

The product structure, configuration, procurement settings, and planning data can influence the production planning process.

---

## 14. Planned Order

For an in-house manufacturing requirement, the planning process can generate a **Planned Order**.

### Flow

**Demand**  
↓  
**MRP**  
↓  
**Planned Order**  
↓  
**Production Order**

The Planned Order represents the planning stage before production execution.

---

## 15. Production Order

The **Production Order** represents the manufacturing requirement used during production execution.

It brings together important production information such as:

* Material to be produced
* Production quantity
* Required components
* Manufacturing operations
* Work Centers
* Scheduling information

This demonstrated why accurate upstream master data is important for successful Production Order processing.

---

## 16. Production Order Release

The Production Order was released as part of the production execution process.

This stage provided practical experience in understanding relationships between:

* Production Order
* Master Data
* Component Requirements
* Component Availability
* Manufacturing Execution

### Troubleshooting Approach

When the Production Order could not proceed as expected, the following areas were considered:

1. Material Master
2. BOM
3. Routing
4. Work Centers
5. Production Version
6. Component Requirements
7. Component Availability
8. Production Order Status

This helped develop a structured, business-process-oriented troubleshooting approach.

---

## 17. Goods Issue

Goods Issue represents the consumption of components for the Production Order.

### Flow

**Component Inventory**  
↓  
**Goods Issue**  
↓  
**Production Order**  
↓  
**Component Consumption**

This step demonstrates the connection between inventory management and production execution.

---

## 18. Production Confirmation

Production Confirmation records manufacturing execution associated with the Production Order.

### Flow

**Production Order**  
↓  
**Release**  
↓  
**Production Execution**  
↓  
**Confirmation**

This provides a link between the manufacturing activities performed and the Production Order.

---

## 19. Goods Receipt

After the diaphragm valve has been produced, Goods Receipt records the finished product entering inventory.

### Production Execution Flow

**Production Order**  
↓  
**Release**  
↓  
**Goods Issue**  
↓  
**Production Execution**  
↓  
**Confirmation**  
↓  
**Goods Receipt**  
↓  
**Finished Product Inventory**

---

# Complete Project Flow

## Phase 1: Product Configuration

**Customer Requirement**  
↓  
**Configurable Material**  
↓  
**Characteristic Selection**  
↓  
**Configuration**  
↓  
**Object Dependency Evaluation**  
↓  
**Relevant Product Structure**

### Outcome

A product configuration representing the required diaphragm valve specification.

---

## Phase 2: Production Planning

**Product Requirement**  
↓  
**MRP**  
↓  
**Component Requirements**  
↓  
**Planned Order**

### Outcome

Production and component requirements are identified for manufacturing.

---

## Phase 3: Production Execution

**Planned Order**  
↓  
**Production Order**  
↓  
**Production Order Release**  
↓  
**Goods Issue**  
↓  
**Production Confirmation**  
↓  
**Goods Receipt**

### Final Result

**Finished Configured Diaphragm Valve**

---

# Challenges and Troubleshooting

Troubleshooting formed an important part of this project because it helped demonstrate how SAP master data, configuration, planning, component availability, and production execution depend on each other.

## Challenge 1: Component Availability

Component availability became an important consideration during Production Order processing.

This demonstrated the relationship between:

* BOM Requirements
* Component Stock
* Material Planning
* Component Availability
* Production Order Execution

### Key Learning

Creating a Production Order does not automatically mean that all required components are available for production.

The material availability situation must also support manufacturing execution.

---

## Challenge 2: Routing and Master Data

Routing-related issues provided practical experience in analyzing manufacturing master data.

The troubleshooting relationship can be summarized as:

**Material**  
↓  
**BOM**  
↓  
**Routing**  
↓  
**Work Center**  
↓  
**Production Version**  
↓  
**Production Order**

### Key Learning

An issue observed during Production Order processing may originate from upstream master data.

Troubleshooting should therefore consider the complete manufacturing structure instead of focusing only on the final system message.

---

## Challenge 3: Production Order Execution

Production Order processing provided practical understanding of how manufacturing execution steps are connected.

The process includes:

* Production Order Creation
* Component Requirements
* Component Availability
* Production Order Release
* Goods Issue
* Production Confirmation
* Goods Receipt

### Key Learning

Production execution depends on correct master data together with the required component availability and production information.

---

## Challenge 4: Variant Matching Exploration

Variant Matching was explored to better understand the relationship between a selected configuration and an existing material variant.

This provided additional exposure to how configurable products and material variants can interact within a Variant Configuration scenario.

---

# Key Learnings

## Variant Configuration Learnings

* Understanding Characteristics
* Understanding Variant Classes
* Working with Configurable Materials
* Understanding Configuration Profiles
* Creating a configurable product structure
* Understanding Super BOMs
* Understanding Object Dependencies
* Connecting product requirements with Variant Configuration
* Understanding configuration-dependent manufacturing requirements

## Production Planning Learnings

* Understanding Material Master requirements
* Understanding BOM structures
* Understanding the difference between BOM and Routing
* Understanding Work Centers
* Understanding Production Versions
* Executing MRP
* Understanding Planned Orders
* Processing Production Orders

## Production Execution Learnings

* Understanding Component Availability
* Releasing Production Orders
* Performing Goods Issue
* Performing Production Confirmation
* Posting Goods Receipt
* Understanding the transition from Production Planning to Production Execution

## Troubleshooting Learnings

This project helped develop the following structured troubleshooting approach:

**Problem**  
↓  
**Understand the Business Requirement**  
↓  
**Check Master Data**  
↓  
**Check Variant Configuration**  
↓  
**Check Planning Result**  
↓  
**Check Material Availability**  
↓  
**Check Production Order**  
↓  
**Identify Root Cause**  
↓  
**Correct and Retest**

---

# Business Process Understanding

One of the most important learnings from this project was understanding that individual SAP objects do not operate independently.

The complete configurable manufacturing scenario connects:

**Customer Requirement**  
↓  
**Sales Order**  
↓  
**Variant Configuration**  
↓  
**Product Structure**  
↓  
**Production Planning**  
↓  
**Material Requirements**  
↓  
**Production Order**  
↓  
**Production Execution**  
↓  
**Finished Product**

This project therefore focuses not only on individual SAP activities but also on understanding the **business logic behind the complete end-to-end manufacturing process**.

---

# PP and VC Integration

An important aspect of this project was understanding how **Variant Configuration and Production Planning work together**.

## Variant Configuration Answers

**What exactly does the customer require?**

Variant Configuration captures the required product specification through the configurable product model.

## Production Planning Answers

**What is required to manufacture that product?**

Production Planning provides the master data, planning process, and production execution structure required for manufacturing.

### Combined Process

**Customer Requirement**  
↓  
**Variant Configuration**  
↓  
**Configured Product**  
↓  
**Manufacturing Requirements**  
↓  
**MRP**  
↓  
**Production Order**  
↓  
**Production Execution**

The integration between PP and VC was one of the primary learning outcomes of the project.

---

# Skills Demonstrated

## SAP Functional Skills

* SAP S/4HANA
* SAP Production Planning (PP)
* SAP Variant Configuration (VC)
* Configurable Product Modeling
* Manufacturing Master Data
* Material Requirements Planning
* Production Order Processing
* Production Execution

## Variant Configuration Skills

* Characteristics
* Classes
* Configurable Material (KMAT)
* Configuration Profile
* Super BOM
* Object Dependencies
* Sales Order Configuration
* Variant Matching Concepts

## Production Planning Skills

* Material Master
* Bill of Material
* Routing
* Work Centers
* Production Version
* MRP
* Planned Orders
* Production Orders

## Production Execution Skills

* Component Availability
* Production Order Release
* Goods Issue
* Production Confirmation
* Goods Receipt

## Business Process Skills

* End-to-End Manufacturing Process Understanding
* SAP Master Data Analysis
* Functional Troubleshooting
* Business Process Mapping
* PP and VC Integration Understanding

---

# What I Learned from This Project

This project helped me move beyond understanding individual SAP transactions and develop a broader understanding of how an end-to-end configurable manufacturing scenario works.

The most important learning was understanding the relationship between:

**Customer Requirement**  
↓  
**Variant Configuration**  
↓  
**Manufacturing Master Data**  
↓  
**Production Planning**  
↓  
**Production Execution**

The project also strengthened my understanding of how configuration and production issues can be investigated by identifying which upstream business object or master-data element is influencing the process.

---

# Future Enhancements

The diaphragm valve scenario can be extended further with:

* SAP Quality Management (QM) integration
* Quality Inspection during or after production
* More advanced Variant Configuration logic
* Material Variant scenarios
* Production costing analysis
* Advanced planning and scheduling
* ePP/DS integration
* Additional manufacturing scenarios
* SAP Fiori-based manufacturing processes
* Additional visual process documentation

---

# Project Summary

This project provided hands-on experience in understanding how a customer requirement for a configurable product can be connected with SAP manufacturing processes.

The complete project journey can be summarized as:

**Customer Requirement**  
↓  
**Variant Configuration**  
↓  
**Manufacturing Master Data**  
↓  
**MRP**  
↓  
**Planned Order**  
↓  
**Production Order**  
↓  
**Goods Issue**  
↓  
**Production Confirmation**  
↓  
**Goods Receipt**

The project strengthened my understanding of the relationship between **SAP PP, Variant Configuration, master data, production planning, manufacturing execution, and functional troubleshooting**.

---

# Documentation Approach

This repository documents the **business process, SAP functional concepts, configuration relationships, troubleshooting approach, and learning outcomes** from the project.

The focus is on understanding why different SAP objects are required and how those objects interact across the complete configurable manufacturing process.

---

# Disclaimer

This repository is a **personal SAP learning and portfolio case study** created to demonstrate my understanding of SAP S/4HANA manufacturing concepts.

The documentation focuses on general SAP functional concepts and personal learning outcomes.

No confidential organizational information, customer information, credentials, internal system details, proprietary documentation, or restricted project data is intended to be included in this repository.

---

# Author

**Sibangi Boxipatro**

## SAP Manufacturing Learning Portfolio

### Focus Areas

* SAP Production Planning (PP)
* SAP Quality Management (QM)
* SAP Variant Configuration (VC)
* SAP S/4HANA Manufacturing
* SAP Digital and Development Technologies
