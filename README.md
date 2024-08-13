# Pharmaceutical-Distribution-Logistics

## Database Design

The logistics pipeline in a pharmaceutical organization centers around key entities, with the ‘Drug’ entity being the primary product. Manufacturing drugs requires raw materials, primarily chemicals, leading to the crucial ‘Chemical’ entity. Each drug must receive legal and safety approvals, represented by the ‘Approvals’ entity. To simulate sales and purchases, the database includes ‘Distributors’ (who purchase drugs) and ‘Vendors’ (who sell chemicals), along with their respective ‘Inventory’. The ‘Shipper’ entity manages product transportation, while the ‘Order’ entity tracks sales and purchase details, including items, pricing, and involved distributors or vendors.

The design focuses on essential fields to accurately simulate processes and gain analytical insights while avoiding redundancy. The Not Null constraint is applied to ensure data consistency, preventing columns from having undefined or missing values. Data integrity is maintained through primary keys, foreign keys, unique constraints, and check constraints.

To avoid violating database normalization, related entities with similar attributes are handled using separate tables. For example, ‘Chemicals in Drug’ and ‘Drugs in Order’ tables manage relationships between entities without redundancy. This approach ensures the accurate representation of relationships and maintains database normalcy.

## Application Description

To facilitate seamless communication between a MySQL database and Python, the MySQL Connector Python driver was employed. This driver enables the retrieval and storage of data between the MySQL tables and Python scripts. Data stored in MySQL tables can be retrieved using SQL queries executed through the MySQL Connector Python driver. This retrieved data is crucial for feeding information to applications, ensuring that the latest and relevant data is utilized.
In addition to interacting with MySQL, the Python script employs Pandas DataFrames providing a convenient structure for storing, manipulating, and analyzing tabular data.
Some of the features of the application include:

### Order Placement
An admin-driven order placement system plays a pivotal role in pharmaceutical inventory management. It empowers administrators to initiate orders for drugs from distributors or procure raw chemicals from vendors. This process triggers internal procedures, orchestrating the update of stock levels in the inventory system. By seamlessly integrating order placement with inventory management, pharmaceutical companies ensure efficient control over their supply chain, enabling timely replenishment of essential pharmaceutical components. This streamlined approach enhances operational resilience and supports the continuous availability of critical materials for drug manufacturing.

### Get Best Vendor
This feature is a critical component of the procurement process, aiding in the strategic selection of vendors based on a company's specific needs. It considers the urgency of raw material requirements. In situations where immediate supply is crucial, the system identifies vendors capable of prompt delivery. Simultaneously, for scenarios where cost reduction is a priority, it evaluates vendors offering the best pricing structures and favorable terms.

### Low Stock Alert
This feature plays a crucial role in pharmaceutical and chemical inventory management by promptly notifying administrators when specific drugs and chemicals fall below a predefined threshold. This proactive alert mechanism ensures that the administrative team remains vigilant about the inventory levels. By preventing stocks from reaching critically low levels, the system facilitates seamless inventory management and safeguards against potential disruptions in the manufacturing or distribution processes. Ultimately this enables timely actions to replenish essential pharmaceutical components and maintain the continuity of production and distribution.

### Lab Approvals
Lab approvals in the pharmaceutical industry are a critical step in ensuring the compliance of drugs with stringent quality standards. After undergoing rigorous lab tests, this process verifies the validity, reliability, and high quality of pharmaceutical products. By preventing the release of inaccurate or substandard drugs into the market, lab approvals play a pivotal role in safeguarding public health. Moreover, the documentation and evidence generated through this approval process are invaluable in making legal decisions for the company, providing a robust foundation for regulatory adherence and fostering trust with regulatory bodies.

### Shipper Tracking
Shipper tracking provides customers with essential details such as the shipper's information, estimated time of arrival (ETA), and the tracking number for their shipments. This transparency in logistics empowers customers with real-time insights into the status and location of their packages, contributing to a positive customer experience. By ensuring customers are well-informed and confident about their deliveries, shipper tracking plays a pivotal role in enhancing overall customer satisfaction.

### Analytical Decisions
Using analytics to derive insights from data to optimize operations and maximize profit. By analyzing total sales and purchases, businesses can make informed decisions for resource allocation and process improvement. Additionally, identifying top-selling drugs provides pharmaceutical companies with crucial market insights, aiding strategic planning. Vendor optimization, considering factors like minimum delivery periods, ensures efficient supply chain management, minimizing delays and enhancing overall productivity. Detailed sales analysis by drugs allows businesses to tailor marketing strategies and product offerings, aligning with customer preferences and market trends.
