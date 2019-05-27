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
When we do such big system planning there are whole bunch of supply planners who will review orders on a daily basis. In order to meet certain timeline it is common to split the processing workload into planning zones such as 3 zones, grouping 5000 stores in each and run it based on local time zones, east cost first then central and then west coast.

## Soda Items Planning
Interesting aspect about Soda drink sale is that customer gets a cup and we don't know what specific drink he/she purchased, in other words we sold something but we don't know what item we sold !!!. To solve this riddle we need to track usage pattern for a period at each store on different syrups and come up with split % and use this split % for demand forecasting of such syrups and usage depletion in order to accurately do supply planning.

## Perpetual Inventory Systems
Unlike other industries restaurants cannot do stock counting on a daily basis, simply too much labor, so we needed a perpetual inventory system which will calculate based on transactions what is the daily onhand in theory. This gets feed into supply planning as a starting inventory. Calculating accurate on hand gets complicated with recipe usage variations, unreported waste, date sensitive inventory and missing sales information.

## Supply Planning Master Data 
For both supply and demand planning we need various master data such as what locations we are planning, what items, BOM and its active dates, sourcing, network, delivery schedule and substitute item info.

## Supply Planning Transactoin Data 
Transaction data include demand forecast, delivery confirmation to the store, in-transit to store, past sales from store, stock count from store and order approval from store

## Order Cycles
Orders are created for DC to deliver items to Store. Typically orders are created and send to store manager for approval, approved orders are send to DC for filfullment, DC will send in-transits, either store or DC has to send delivery confirmation and any adjustments and orders get closed out. Different cycle variations exists when DC generates its order based on adhoc restaurant special orders

## Food Promotional Items Planning
Food Promotional Items are limited in supply so it gets special handling by Limited Supply Specialists. Restaurant cannot order what they want unlike other items. Sometimes stores that are on the borders in different planning zones could source limited supply items from DC that are not their primary DC, this complicates planning, in the sense 'Constrainted Inventory' planning need to be planned together which leads to store migration between planning zones. This becomes its own module to do accurate planning. 

## Toys Promotional Items Planning
This is one of the big system within supply planning. There could be 12 promotions in a year, each for 4 weeks duration, each week can a different toy design. Each promotion gets planned 9 months ahead, each toy need to be designed, given to manufactrers in China and other countries, ship planning over sea routes need to be done, hub and master warehosue gets involved, controled movement from master warehouse to DC need to be planned and then DC to store. Store will not have control over delivery quantities due to fair distribution rules, even run out requirement, ensuring store does not skip a design, small store big store management, toy first substitute management, fall back toys management and generic promotion to clear out strandad toys. 

## Sales Filling Concept
Sometimes due to system failure stores prior day sales will not get reported, yet we need previous day sales data to plan for the coming days. To address this we can use past forecast as filler for previous day sales. 

## New Store Handling 
New store will not have any past history to predict future sales, everything need to be setup, some need to be modeled after a model store. New Store handling is a set of process to bring a store live for planning. 

## Date Sensitive Inventory Management
Food items are perishable items with shelflife of 2 to 3 days. In order to do accurate supply planning we need what goes waste everyday. Store will not report all waste due to labor, time and other reasons. To address this issue inventory system need to compute what is unreported waste. To do this we need to know inventory at lot (delivery) level and each lots expiration date. Based on expiry date we can compute unreported waste. Also for DSI planning we need to on hand info by lot with its expiry date. All in-transits need to be have expiry date. Safety stock will also go waste, so on each delivery we will have to add safety stock. 

## Recipe Management
In restaurant industry Recipe management is a big process and it is done by many groups, Sold Menu Item is set up by some group, Base Menu Item to Assembly Item to PPO is setup and managed a different group and PPO-SU is managed by the distribution center. For planning all these need to be reconciled and come together. Recipe flattening process is involved for process performance improvement, example sales coming in at BMI need to be converted to PPO for planning. The effective date adjustement also happens at various point in the process to open up early and extend beyond end date, plus fill gaps if any, all these are done because restaurant get their product earlier than effective date and keep selling after the end is reached, all these transactions will flow and need to be handled. 

## Supply Chain Statistics Management
Transactions information that comes to supply planning system may not be accurate. Forecast will not be accurate, Recipe usage will not be accurate, Inventory reporting will not be accurate, Product Promo need to be factored in, Employee meals need to be factored. In order to all these we compute SSCOV in duration and qty, Yield Correction Factor to address Recipe usage vairance, Waste not get reported need to be address using Waste Factor, Giveaways and Employee meal need to be addressed via Promo Factor and incorrect inventory counts need to be factored with IDIFF factor

## Supply Chain Parameter Planning 
Planning for 15000 stores, average 300 items is not easy, we need tools to manage at different hierarchy levels. Planning parameter management itself is a module to address this. 3X3 matrix is one typical solution, 3 levels of geography and 3 levels of items which include Market-Region-Store and Item-Item Group-All Items. This 3X3 will give the planners to set planning configuration parameters and the system will blow it down to rest@item for planning purposes.

## Forecast Error Tracking
This is one of the important process in supply planning, in order to not to get into a stock low or stock out at the store. Typically Forecast errors are computed for each delivery period of what we forecasted and what we actually sold. Each such two data points can produce error and over a 10 data points we can arrive a forecast error, based on this we can add safety stock which will address to the stock low and stock out issues 

## How to plan for Napkins 
In restaurant industry supplying napkins type items, tray liners, ketchups  are a challenge, these are not part of Bills of Material, so it won't come under any base menu item planning. In order to solve this there is an non real item called Transaction Count item, for each store we compute it for each day and this becomes a fake base menu item with many assembly items part of it, for all these assembly items planning will be carried out using this fictitious item similar other real items

## Manage by Exceptions
When supply planner review plan output it is impossible to review each and every item at restaurant, so to manage this they rely on exception reports which will report incorrect safety stock, stock low, stock out, very low forecast, high coverage days, high leftover at the store etc. 

## Item Transition Management 
There are different scenarios broadly hard cutover and softcutover. Hard Cutover is when old item need to be stopped on a specific day and new item need to start. Soft Cutover is where restaurant can have old and new item and sell old item until everything is depleted and start the new item. For both we need to handle supersession logic. 

## Substitute Item Management
Substitute items are where both items are active but if store runs out they substitute primary with substitute item. This is a standard supply chain feature, but there are more complex scenario where deployment need to be 
- Primary Item at store
- Primary Item at DC
- Substitute Item at store 
- Substitute Item at DC

The complication is store ran out on primary, they have sub but DC still has primary, planning system should deploy DC primary before store can use sub which is at the store. 

------------------- ------------------- ------------------- ------------------- ------------------- ------------------- ------------------- ------------------- -------------------

# Demand Planning Concepts
The client that I worked used JDA Demand Planning product for demand forecasting. This JDA solution supports many alogorithms which include Lewandowski, moving average and  Multiple Linear Regression. US markets used Lew and Moving Avg and Europe markets used MLR. 

## Demand Forecasting Units  (DFUs)
This is the basic unit used for forecasting, each DFU represents a unique combination of demand loc/item/group/model. Model represent the choosen alogorithm and history stream. History stream is predominantly Sales history but it can be anything that is time series data such as past shipments from DC or past arrivals at store or store daily total revenue.  Typically DFUs will have relationship via DFU maps, higher level DFU can be reconcilled to lower level DFUs. DFUs will have two dimentional hierarchies, location hierarchy can be store, advertisement co-op, DC, Region, National, item hierarchy can be base menu item to demand planning item aggregates (DPIAs). Mostly demand is forecasted at the DPIA level and gets reconcilled to Base Menu Item level. 

## Demand Lift Management
JDA can use the total history which include regular sales, seasonality adjustments and any lifts due to promotions. But if there are too many events and event types have too much difference then out-of-box JDA feature will not predict the forecast accurately. This is mainly due to event weights cannot be fed into the standard alogrithms. Due to this product limitation we had to come up with custom lift calclation with various client specific rules. Lift management is a big topic because of the fact that total history need to be split to identify the past event performance and come up with new lifts for the future. 

## Promotional Event Management
For the client that I worked there are too many events going on in the country. Stores are grouped into advertisement co-ops which pool AD money and primarilly TV ADs. Events are run at Ad Coop but individual stores can exclude from participation. Because there are too many events managing each event's lift is not possible, so similar events in the same geog are grouped into what is called Managed Events. Base Menu Items are also grouped into DPIAs. 

## Digital Event Management
Digital events are getting very popular as I write this note in 2019, these are called Digital Campaigns which are sent directly to the mobile app and redumption is using the app. These campaigns are grouped together Managed Digital Events, similar other TV promotional events base menu item are aggregated to DPIAs and store are grouped into ad-coop. Redumption data could be used to predict future lifts. 

## Forecast Override Management
This is one of the imporant tool for demand planners. They could do overrides at any level and the process will blow it down to the management level based on store participation. Overrides can be % change override or qty override. If Qty override then it get blown down to lower level DFUs based on its forecast proportion. 

## Proxy Item and Loc
Stores that are new have to modeled with an another store, this is accomplished via proxy location setup. Proxy item features is used to introduce new item to the market using similar proxy item. 

## Demand Master Data
Like supply planning demand planning also needs master data such as processing locations, processing items, location item participation, location item item to do transfer forecast for supply planning, higher level DFUs to lower level DFUs map creation

## Demand Transaction Data
Transaction data include sales or similar time series data history. In some markets forecast is generated by the store on a fictitous (revenue item) item and it gets blown down to base menu item based on maps. In some cases other location forecast will be reconcilied for shorter duration, for example for DC Demand planning first 30 days restaurant level forecast is more accurate, so 30 days of restaurant forecast get rolled up to DC, i.e., short term forecast merge

## Forecast Level Value and Adjustment 
The client that I worked has this very very import Forecast Level Value Calculation process. Basically last three weeks of sales trend need to be applied to the immediate 2 weeks future forecast. Forecast is based on 2 and half years history, JDA may come up with long term trend forecast but immediate happenings at the store is more important for the next two weeks. This process could a simple last 3 weeks, figure out the difference between forecast and actuals, figure out level % and apply this to the next two weeks, this is what is used in EU markets at the client I worked for. 

In US this process is far more complex due to various events that are going on, this level calculation process need to be aware of these events and determine whether we should do level value adjustment or not, in some cases the past level calucation period will be adjustement to more long term or short term or no level value calucation at all. In some cases look back period could have exclusion days based on highly popular events that is running. Besides the level factor is based on weighted average, giving more weight to the most recent day than the older days. This can be further complicated with application on top of future event lifts and overrides.  

## Manage by Exceptions
There are many demand forecasting exceptions that be automatically caught such as missing forecast, negative forecast, incorrect forecast override records, higher level to lower level DFU relationship does not exists, in an MLR algorithm there need to be causal factor in order to come up with accurate forecast; if this is missing report it etc. 

# Summary
Supply Chain can be complex based on how corporations carry out their business and relationship to entities. The concepts that I have laid out in this are generally applicable to any retail chains or fast food chains such as McDonald's, Burger King, Arbys, Subway etc. All though I gained significant amount of knowledge there is plenty more to learn, in my humble opinion one life time is not enough especially with the technology landscape is changing. 

