# Felix Project Proposals

## Problem

There is currently food collected from supermarkets and delivered to charities around London. As all this food is mostly barcoded and trackable it would be good to efficiently collect the data. And use it to work out how much value the Charity is providing.

## Proposal

Multi-phase project to gradually implement a technical solution. The phases on this document become increasingly higher-level as scope would change based on continuous feedback from the Felix Project.

### Phase 1 - Feasilibility of data source.

In order to identify the products and their prices from a barcode we will require a database or API containing this information. There are a few options for this data source:

* Preferrably we could use the charity's relationship with the supermarket to request we have an API to, or a perodic snapshot of the supermarket's own database. This would require us having a communication channel to their Software Engineering team.
* Alternatively there are open-source databases on the internet that should (hopefully) provide us with adequate data. We would need to use a small sample of goods to confirm that they can provide the information needed.
* Otherwise we can build our own database, this would require the item's details being entered into the system by the driver the first time the item is seen - this is a last resort as would require a significant amount of time at the roll-out of the system.

### Phase 2 - Minimal Roll-Out.

If Phase 1 has made the project seem feasible, initially we purchase the equipment and make the simplest possible system to collect barcode numbers. This data will be unusable in its raw form but would enable us to back-fill data once the rest of the system has been bulked out. It would also require us to start collecting feedback from drivers about how they are getting on with the system enabling us to shape end end product.

### Phase 3 - First Product Version

Build out the server-side application of the product. This should allow goods to be resolved against a product database and stored. It should collect data on goods being picked up and from where, and also where they were delivered to. It should be designed in such a way to allow for future expansion in below possible "Future Use Cases".

The software on the scanner devices should be bulked out based on initial feedback from Phase 2, it should allow the data to be quickly collected and sent from source.

### Phase 4 - Web UI

Create basic web UI to explore the data collected, with an emphasis on providing metrics on value the charity is providing to is beneficiaries.

## Future Use Cases

This system should provide useful data straight away, but the data it is collecting could have many other uses, especially once the dataset grows.

Ideas include:

* Live inventory: There could be a live inventory of food that has been picked-up and delivered to a warehouse. This may help with planning and even distributing excess goods between the different food-bank depot's.
* Identifying Trends: Being able to pick up on any natural trends in what excess food might be available to pick up different days of the week or times of the year may help with planning.
* Just-in-time delivery: If/Once trends are identified in food colleciton and delivery. Warehouse space might be saved by predicting pick-ups and deliveries and missing out warehouses.
* Tracking of fresh goods: Once bedded in, the system will show it can help reliably track fresh goods in such a way that it may help with the legislation behind transporting meat produce.


## Costs

### For Development:

| Requirement | Periodicity | Cost |
| ----------- | ----------- | ----:|
| Domain name | Annual | £20 |
| Server Hosting | Annual | £300 |
| Dev Handheld Scanner (*) | One off | £400 |

(*) something like [this](http://www.jmprime.co.uk/product_info.php/android-44-rugged-handheld-terminal-with-2d-barcode-scanner-wifi-bluetooth-3g-gps-p-89?gclid=CKDHvYHKwc8CFbQy0wodWKoGEQ)

### Per van/device:

| Requirement | Periodicity | Cost |
| ----------- | ----------- | ----:|
| Data SIM | Annual | £60 |
| Handheld Scanner | One off | £400 |

## Risks:

* Will access to supermarket barcode data always be available.
* At some point we will need to handover ongoing maintenance back to you. This may involve logging onto systems and restarting or reconfiguring. Part-time IT sysadmin or similar may be required at this point.
* Technical ability is required to generate reports and metrics from the collected data.
