<h1>SQL Joins for Data Analysis and Cybersecurity</h1>

### [YouTube Demonstration](https://youtu.be/your_youtube_link_here)

<h2>Description</h2>
This repository demonstrates the different types of SQL JOIN operations used to combine data from multiple tables. Each JOIN type has a specific use case, particularly in cybersecurity, where these operations help ensure data integrity, monitor access, and detect potential threats. Below are examples of INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL OUTER JOIN, each with an explanation of their purpose.

<h2>Languages and Utilities Used</h2>

- <b>SQL</b>

<h2>Environments Used</h2>

- <b>Windows 10</b>

<h2>Program Walk-through:</h2>

<h3>1. INNER JOIN - Match Employees to their Machines</h3>
In this example, we perform an <code>INNER JOIN</code> between the `machines` and `employees` tables. This JOIN returns only the records where the <code>device_id</code> exists in both tables, ensuring that we retrieve only employees who have assigned machines.
<br/>
<code>SELECT *</code><br/>
<code>FROM machines</code><br/>
<code>INNER JOIN employees ON machines.device_id = employees.device_id;</code><br/>

**Cybersecurity Application:** The <code>INNER JOIN</code> ensures that only relevant and authorized data is returned. This prevents unauthorized data access by retrieving only the necessary records, reducing the risk of data breaches.

<p align="center">
<img src="https://i.imgur.com/Uby72K6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p align="center">
Only records with matching device_id values in both machines and employees tables are returned.
</p>
 
<h3>2. LEFT JOIN - Return More Data</h3>
A <code>LEFT JOIN</code> retrieves all records from the `machines` table, even if there is no matching employee. This is useful to ensure we see all machines, including those not yet assigned to an employee.
<br/>
<code>SELECT *</code><br/>
<code>FROM machines</code><br/>
<code>LEFT JOIN employees ON machines.device_id = employees.device_id;</code><br/>

**Cybersecurity Application:** <code>LEFT JOIN</code> ensures comprehensive analysis, helping to audit unassigned devices. This can prevent security gaps by identifying unused or unaccounted-for devices that may pose a risk to the organization.

<p align="center">
<img src="https://i.imgur.com/1zcF6Bg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p align="center">
All rows from the machines table are returned, including those without matching device_id values in the employees table (with NULL values for unmatched rows).
</p>

<h3>3. RIGHT JOIN - Ensure Full Employee Data</h3>
The <code>RIGHT JOIN</code> ensures that all records from the `employees` table are included, even if they don’t have assigned machines. This helps in cases where we need complete employee information regardless of machine assignments.
<br/>
<code>SELECT *</code><br/>
<code>FROM machines</code><br/>
<code>RIGHT JOIN employees ON machines.device_id = employees.device_id;</code><br/>

**Cybersecurity Application:** In cybersecurity, this can help track employees who lack assigned devices, ensuring that no individual is overlooked during audits or system checks.

<p align="center">
<img src="https://i.imgur.com/hMLjUFx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p align="center">
All rows from the employees table are included, even those without a matching device_id in the machines table (with NULL values for unmatched rows).
</p>

<h3>4. FULL OUTER JOIN - Retrieve All Data with No Gaps</h3>
A <code>FULL OUTER JOIN</code> returns all records from both tables, whether there is a match or not. This is useful to identify any discrepancies between the machines and employees data.
<br/>
<code>SELECT *</code><br/>
<code>FROM machines</code><br/>
<code>FULL OUTER JOIN employees ON machines.device_id = employees.device_id;</code><br/>

**Cybersecurity Application:** <code>FULL OUTER JOIN</code> helps identify anomalies by showing both assigned and unassigned machines as well as employees with or without devices. This is particularly valuable for detecting potential security issues, such as unaccounted-for assets or unusual data patterns.

<p align="center">
<img src="https://i.imgur.com/Ia8jIZn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p align="center">
All rows from both machines and employees tables are included, with NULL values where no matching data exists in the other table.
</p>

<h2>Conclusion</h2>
SQL JOINS are critical for combining data across multiple tables in a way that supports cybersecurity efforts. By using <code>INNER JOIN</code>, <code>LEFT JOIN</code>, <code>RIGHT JOIN</code>, and <code>FULL OUTER JOIN</code> effectively, organizations can maintain data integrity, detect security gaps, and prevent unauthorized access. These techniques are essential for cybersecurity professionals seeking to secure and manage complex datasets.
