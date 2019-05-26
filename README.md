# My Supply Chain Experience
I had the privilege to work for the number one restaurant chain in the world with 34,000 restaurants, an iconic fast food American brand having operations in 119 countries. Gartner listed its supply chain solution as one of the top 3 and I happen to be one of the Subject Matter Expert helping them for years. In this README I have gathered my learnings on many of the Advanced Supply Chain solutions and concepts  

# Supply Planning Concepts 

## Supply Chain Network
The end goal is to supply items to  restaurants, in order to fulfill this there are many entities involved based on the item. Most of these entities are independently operated (called as Owner Operators). Local and Foriegn suppliers who mamanufacture or produce items. Hubs are the locations where items are gathered before redistributed. Master Warehouses which store huge volumns of in-transit inventory. Distribution Center who work closely with Restaurant Owner Operators for day to day distribution of items. Bakery and Commissary also work closely with Restaurant Owner Operators for day to day deliveires. 

Each one of these entities need to plan supply for its demand. Demand, Supply and Transportation planning systems are involved at each entity level. 

## Demand Forecasting
In order to come up with what to deliver to store we need to know the daily demand at store for each Item. Everything will go wrong if we cannot predict accurate demand forecast at store level. Forecast will never be perfect, but it should be close to actual sales. In this solution Demand Forecasting is a major module with many concepts that I have laidout below. 

## Supply Planning
Supply planning system is the second pillar in this solution. Each restaurant item need to be planned daily. Restaurant participation is involved, what is sold in which location. There are many pieces of information need to be come together in order to accurately plan the supply

## Transportation Management
This is the third pillar which addresses what are the means of transportation, mainly Trunc and Ship (Containers). Managing pickup and delivery schedule between locations and how to arrange items optimally in a container. Transportation is closely tied with Supply Planning. This does not play much role in Demand Forecasting. 

## Item Sourcing
Each Item need to have Item/Source Loc/Dest Loc information in order for planning. This is one of the important input for supply planning. For example Bun is sourced from bakery, some of the morning breakfast items are sourced from commissary and rest of the items are sourced from distribution centers. The client that I helped had 40 DC and 15000 stores just in the US. 

## Item Bills of Material
In restaurant industry BOM levels are used based on task or transaction processing at hand, for example there could be 5 level BOM (Sold Menu Item, Base Menu Item, Assembly Item (AI), Product/Package/Ops (PPO) Supply Item and Raw Item) but for supply planning Sold Menu Item such as combo meal plays very less role, we need sales at base menu item level. What restaurant expect from supply planning system is only Raw Item quantities, so we could bring the demand to Assembly Item or Product/Packaging/Ops Supply level and come up with Raw Material requirements for a store. 
- Sales could come in at base menu item level
- Deliveries will come at raw item level
- Forecast will come in at base menu item level
- Planning can start from AI or PPO

## Delivery Schedule
Planning involves at item/source loc/destination loc. For each this combination we need delivery schedule for the planning horizon. When you plan for 15000 stores with average 300 items we are talking about about 4.5 million delivery schedule information for a period of 30 days. If you have an average delivery frequncy of 3 days we are taking about 45 million delivery schedule information we need on a daily basis. In order to manage such huge volume we would do delivery patten matching and sharing. 

## Planning Zone Concepts
When we do such big system planning there are whole supply planners who will review orders on a daily basis. In order to meet certain timeline it is common to split the processing workload into planning zones such as 3 zones, grouping 5000 stores in each and run it based on local time zones, east cost first then centeral and then west coast.

## Soda Items Planning


## Perpetual Inventory Systems

## Supply Planning Master Data 

## Supply Planning Transactoin Data 

## Order Cycles

## Food Promotional Items Planning

## Toys Promotional Items Planning

## Sales Filling Concept

## New Store Handling 

## Date Sensitive Inventory Management

## Recipe Management

## Supply Chain Statistics Management

## Supply Chain Parameter Planning 

## Forecast Error Tracking

## Transaction Count Phantom Items

## Manage by Exceptions

## Substitute Item Management 

## Transaction Count Phantom Item 

------------------- ------------------- ------------------- ------------------- ------------------- ------------------- ------------------- ------------------- -------------------

# Demand Planning Concepts

## Demand Forecasting Units  (DFUs)

## Demand Lift Management

## Promotional Event Management

## Digital Event Management

## Forecast Override Management

## Proxy Item and Loc

## Demand Master Data

## Demand Transaction Data

## Bills of Material for Demand Planning

## Forecast Level Value and Adjustment 

## Item and Loc Masking 

## Forecast Merging within Entities

## Demand Planning Algorithms 

## Revenue Item Based Forecast Model

## Manage by Exceptions


## US DP
- Digital Promotions Forecast Lift Management 
- Event Forecast Lift Management
- Lift Calculation
- Forecast Override Management
- Management Level on Item and Loc Hierarcy
- Proxy Item or Loc Management
- Digital Promotion Management
- Master Data Management
- Transaction Data Management
- Bill of Material for Planning 
- Forecast Level Value Calculation simple and complex methods
- Item Loc Masking
- Forecast Merging from Rest to DC


## EU ROPDP/SP
- MLR algorithms for forecasting
- Demand Exception Management
- Supply Exception Management
- Custom Supersession (Substitute Item Management)
- Revenue Item Based Forecast Model

## Restaurant Demand Planning
- Supply Chain Network and Sourcing
- Supply Chain Demand and Fillment
- Promotional Item Planning DC Perp Inv. and Waving 
- BMI Agg
- Toys Report
- Perpetual Inventory System 
- Contingency Order Concepts
- Forecast Transformations
- Master Data
- Transaction Data
- Promotional Planning Post Processor 
- Proposed Order Cycle
- Sales Filling Concepts
- Sales History Processing for New Stores
- Date Sensitive Inventory 
- Delivery Schedule Patterns
- Recipe Management
- Supply Chain Statistics Module
- Supply Chain Planning Parameter Management
- Forecast Error
- PZ management
- Transaction Count Phantom Item 

