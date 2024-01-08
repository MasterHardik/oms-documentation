# Data Manager Configurations Guide

The Data Manager Configurations page in the OMS empowers users to effectively manage data flow into and out of the OMS. This guide provides step-by-step instructions on adding and editing configurations, as well as integrating SFTP details into the configurations.

## Accessing the Data Manager Configurations Page

1. Go to the Hamburger menu.
2. Select `Settings`.
3. Click on `Data manager configurations`.

## Add a New Configuration

Adding a new data configuration in OMS enables users to specify how data is imported and exported.

### Steps:

1. Click the `Add` button on the configurations page.
2. In the modal that appears, provide information for fields such as Config ID, Description, Import Service, Import Path, Export Content ID, Export Service, Export Path, File Name Pattern, and Multi-threading.
3. Click `Add` again to save the new configuration.

### Configuration Information Table:

| Field               | Description                                         |
|---------------------|-----------------------------------------------------|
| **Config ID**       | A unique identifier for the configuration.           |
| **Description**     | A brief description of the configuration.            |
| **Import Service**  | The OMS service for importing data into OMS.         |
| **Import Path**     | The path from which the data is kept for OMS to import.|
| **Export Content ID**| Content ID for exporting data.                       | 
| **Export Service**  | The OMS service or workflow for exporting data.      |
| **Export Path**     | The path to which the data will be exported.         |
| **File Name Pattern**| A pattern for naming files.                          |
| **Multi-threading** | Y/N configuration for processing multiple files.    |

### Use Cases of some configurations:

1. **File Name Pattern:**
   - *Scenario:* Multiple file types share the same path on an SFTP server.
   - *Purpose:* Uniquely identify and categorize files for accurate processing by the import service.

2. **Multi-threading:**
   - *Scenario:* Large data imports, e.g., product inventory resets with files exceeding 20 MB.
   - *Purpose:* Speed up processing by grouping data and allocating multiple threads simultaneously.
   - *Note:* Default value is 'N' (No)

3. **Export Content ID:**
   - *Scenario:* HotWax uses content templates for exporting data with specific field values.
   - *Purpose:* Specify a unique identifier (Content ID) to ensure the export service selects the correct template for accurate data rendering and export.

4. **Export/Import Path:**
   - *Scenario:* Data communication between OMS and external systems through SFTP.
   - *Purpose:* Specify accurate paths for file import/export; incorrect paths can result in failed data communication.


## Edit Configurations

Editing an existing Data Manager Configuration allows users to update configurations based on evolving business needs or changing data sources.

### Steps:

- Search for the desired configuration by name or ID.
- Click the `Edit` button at the end of the search result.

{% hint style="info" %}
Config ID cannot be changed after creation. Create a new Config if a new Config ID is needed.
{% endhint %}

# SFTP User Integration in Data Configuration

In the OMS data import/export process, setting up SFTP users is essential for smooth operations. Server paths, beginning with the SFTP username (e.g., `dummySftpUser/HotWax/SalesOrders/`), follow a consistent convention. HotWax simplifies user integration, minimizing manual errors. This streamlined setup is crucial for bulk user integration, allowing easy association with diverse import paths. By incorporating specific SFTP users into configurations, users can efficiently manage data flow, ensuring secure and error-free transactions within the OMS.

### Steps:

1. Select `Add SFTP User to Config`.
2. Choose the SFTP user configuration path.
3. Select the `FTP Config` and `Config ID`.
4. Save the configuration.

By following these steps, users can manage data configurations within the OMS, ensuring efficient data flow and integration.