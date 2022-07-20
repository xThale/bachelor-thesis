# Bachelor Thesis

### Aggregation design of a checkout software with hexagonal architecture and domain-driven design

#### Abstract
In the e-commerce sector software projects fulfill complex business requirements and therefore demand a stable architecture as their foundation. This thesis examines an online shop checkout domain and how the bounded context can be implemented utilizing hexagonal architecture and domain-driven design. The focus is placed on the design of the aggregates. Various data models are analyzed and evaluated based on their complexity, performance, parallelism and client-friendliness. Generally, big aggregates suffer from lower parallelism, however can be implemented more easily since all required information is loaded at once from the database. Splitting the data model into different aggregates entails the usage of eventual consistency or force transactions to modify more than one aggregate at the same time. Eventual consistency increases the complexity of the checkout software, on the other hand cross-aggregate transactions make the operation of multiple database hosts within one application more difficult. The performance of individual aggregate designs are measured with a load test. On average, applications with one cohesive aggregate process more requests per second than a model using separated aggregates. Conclusively, the checkout software profits from a higher performance and reduced complexity by implementing only one aggregate. If a common use case is the mutation of one resource by distinct processes simultaneously then the affected objects need to be placed in different aggregates.

#### Zusammenfassung

Softwareprojekte im E-Commerce-Bereich erfullen komplexe Businessanforderungen ¨ und ben¨otigen aufgrund dessen eine stabile Architektur. Dieses Projekt untersucht die Domain eines Onlineshop-Checkouts und wie der Bounded-Context mithilfe einer Hexagonalen Architektur und Domain-Driven Design implementiert werden kann. Besonders liegt der Aggregationsschnitt im Fokus, wobei unterschiedliche Datenmodelle analysiert und anhand von Komplexit¨at, Performance, Parallelit¨at und Client-Freundlichkeit bewertet werden. Große Aggregates leiden generell unter verringerter Parallelit¨at, jedoch bietet ein zusammengeh¨origes Datenmodell eine vereinfachte Umsetzung von Businessanforderungen, da stets alle Informationen aus der Datenbank geladen werden. Die Aufteilung in mehrere Aggregates erzwingt die Anwendung von Eventueller Konsistenz oder einer Transaktion uber mehrere Aggregates. ¨ Eventuelle Konsistenz erh¨oht die Komplexit¨at der Checkout-Software, wohingegen eine aggregate-ubergreifende Transaktion die Verwendung von unterschiedlichen ¨ Datenbank-Hosts erschwert. Anhand eines Lasttests wird die Performance der Designans¨atze betrachtet. Im Durchschnitt verarbeitet die Applikation mit einem zusammengeh¨origen Datenmodell mehr Anfragen pro Sekunde als unter Verwendung getrennter Aggregates. Als Fazit dieser Arbeit wird argumentativ begrundet, dass ¨ innerhalb einer Checkout-Software die Vorteile eines Designs mit einem einzigen Aggregate dank der erh¨ohten Performance und reduzierten Komplexit¨at uberwiegen. ¨ Falls eine zeitgleiche Bearbeitung einer Ressource durch unterschiedliche Prozesse ein g¨angiger Anwendungsfall ist, mussen die betroffenen Objekte in separate Aggregates ¨ verlagert werden.