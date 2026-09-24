# Cloud Storage Types Research

Cloud storage is commonly divided into three main types: **Block Storage, File Storage, and Object Storage**. Each type has a different structure and is suitable for specific applications and workloads.

| Storage Type       | Description                                                                                                               | Primary Use Case                                                                                     | Cloud Provider Example |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------- |
| **Block Storage**  | Divides data into fixed-size blocks that an operating system can use similar to a virtual hard drive.                     | Suitable for virtual machines, databases, and applications that require fast and direct disk access. | AWS EBS                |
| **File Storage**   | Organizes data into files and folders that can be accessed by multiple users or systems through a shared file system.     | Commonly used for shared documents, files, and applications that require shared storage.             | AWS EFS                |
| **Object Storage** | Stores data as individual objects along with metadata and a unique identifier inside a storage container called a bucket. | Useful for storing images, videos, backups, documents, and other large amounts of unstructured data. | AWS S3                 |

## Why Object Storage for the Client?

Object Storage is suitable for the client's photo-sharing application because it is designed to handle large amounts of unstructured data, especially images and other media files. It can also grow as more photos are uploaded, making it practical for applications where the amount of stored data can increase over time.

