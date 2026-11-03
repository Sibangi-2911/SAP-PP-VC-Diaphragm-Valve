# SAP S/4HANA PP & Variant Configuration - Configurable Diaphragm Valve

## Project Overview

This project demonstrates an **end-to-end configurable manufacturing scenario** for a diaphragm valve using **SAP S/4HANA Production Planning (PP)** and **Variant Configuration (VC)**.

The objective of this project was to understand how customer-specific product requirements can be captured through Variant Configuration and translated into production planning and production execution.

The project covers the complete process from creating the configuration model and manufacturing master data through **Sales Order Configuration, MRP, Planned Order, Production Order, Goods Issue, Production Confirmation, and Goods Receipt**.

---

## Business Scenario

A diaphragm valve can be manufactured in different configurations depending on customer requirements.

Instead of creating and maintaining a completely separate product structure for every possible product combination, a **Configurable Material (KMAT)** can be used to represent the product family.

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

- Build a configurable diaphragm valve scenario in SAP S/4HANA
- Understand the relationship between Characteristics, Classes, and Configurable Materials
- Create a Configurable Material (KMAT)
- Maintain a Configuration Profile
- Create a Super BOM
- Understand and apply Object Dependencies
- Create the required Production Planning master data
- Integrate Variant Configuration with Production Planning
- Capture configurable product requirements through a Sales Order
- Execute Material Requirements Planning (MRP)
- Process a Planned Order
- Create and execute a Production Order
- Perform Goods Issue
- Perform Production Confirmation
- Post Goods Receipt
- Analyze and troubleshoot configuration and production-related issues

---

## SAP Areas Covered

### SAP Variant Configuration (VC)

The project provided practical exposure to:

- Characteristics
- Variant Class
- Configurable Material (KMAT)
- Configuration Profile
- Super BOM
- Object Dependencies
- Sales Order Configuration
- Configuration-dependent component selection
- Variant Matching exploration

### SAP Production Planning (PP)

The project covered:

- Material Master
- Bill of Material (BOM)
- Work Centers
- Routing
- Production Version
- Material Requirements Planning (MRP)
- Planned Order
- Production Order
- Component Availability
- Production Order Release
- Goods Issue
- Production Confirmation
- Goods Receipt

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

# 1. Material Master

The Material Master forms the foundation of the manufacturing scenario.

The project includes a configurable finished material together with the components required to manufacture the diaphragm valve.

Material Master information supports different areas of the manufacturing process, including:

- Material Planning
- Procurement
- Production
- Inventory Management
- Production Execution

The configurable finished product acts as the central material around which the Variant Configuration and Production Planning processes are built.

---

# 2. Characteristics

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

# 3. Variant Class

The relevant Characteristics are grouped into a Variant Class.

### Relationship

**Characteristics**  
↓  
**Variant Class**  
↓  
**Configurable Material**

The Variant Class provides a structured way of grouping the Characteristics required to describe the configurable product.

---

# 4. Configurable Material (KMAT)

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

# 5. Configuration Profile

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

# 6. Super BOM

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

# 7. Object Dependencies

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

# 8. Bill of Material (BOM)

The **Bill of Material (BOM)** defines the components required to manufacture the product.

For a configurable product, the BOM works together with the Variant Configuration model to determine the appropriate component structure.

### Simple Definition

**BOM = WHAT components are required to manufacture the product**

The BOM provides component information required during Production Planning and Production Execution.

---

# 9. Work Centers

Work Centers represent the production resources associated with manufacturing operations.

Operations defined in the Routing are assigned to the appropriate Work Centers.

### Concept

**Routing Operation**  
↓  
**Work Center**  
↓  
**Production Resource**

Work Centers provide information relevant to areas such as:

- Scheduling
- Capacity Planning
- Costing
- Production Execution

---

# 10. Routing

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

# 11. Production Version

The **Production Version** provides the relevant combination of BOM and Routing for production.

### Concept

**Production Version**  
↓  
**BOM + Routing**  
↓  
**Components + Operations**  
↓  
**Production Process**

The Production Version therefore creates an important connection between the product structure and manufacturing process.

---

## Manufacturing Master Data Relationship

The Production Planning master-data relationship can be summarized as follows:

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

# 12. Sales Order Configuration

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

# 13. Material Requirements Planning (MRP)

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

# 14. Planned Order

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

# 15. Production Order

The **Production Order** represents the manufacturing requirement used during production execution.

It brings together important production information such as:

- Material to be produced
- Production quantity
- Required components
- Manufacturing operations
- Work Centers
- Scheduling information

This demonstrated why accurate upstream master data is important for successful Production Order processing.

---

# 16. Production Order Release

The Production Order was released as part of the production execution process.

This stage provided practical experience in understanding relationships between:

- Production Order
- Master Data
- Component Requirements
- Component
