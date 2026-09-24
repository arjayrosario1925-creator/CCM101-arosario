# MinIO Deployment

## 1. Deploy MinIO Using Docker

I used Docker to download and start the MinIO object storage server. The following command was used to create the MinIO container:

`docker run -d -p 9000:9000 -p 9001:9001 --name minio-server -e "MINIO_ROOT_USER=cloudadmin" -e "MINIO_ROOT_PASSWORD=CloudNova2026!" minio/minio server /data --console-address ":9001"`

This command creates a MinIO container and runs it in the background using detached mode.

## 2. Verify the Container

To check if the MinIO container was successfully started, I used:

`docker ps`

This command lists the Docker containers that are currently running. The MinIO container should appear in the list with a running status.

## 3. Access the MinIO Web Console

The MinIO Web Console can be accessed through:

`Port: 9001`

Port 9001 is connected to the MinIO Web Console, allowing users to access the storage management interface.

## 4. MinIO Login Credentials

The login information was configured through environment variables included in the Docker command.

`Username: cloudadmin`
`Password: CloudNova2026!`

These credentials are used to log in to the MinIO Web Console.

## 5. Environment Variables

The `-e` option is used to provide environment variables to the MinIO container.

`-e "MINIO_ROOT_USER=cloudadmin"`

This sets the administrator username for MinIO.

`-e "MINIO_ROOT_PASSWORD=CloudNova2026!"`

This sets the administrator password.

Using environment variables makes it possible to provide the required MinIO settings when the container starts.

## 6. Bucket Created

The bucket I created for the client was:

`client-photos`

I created the bucket through the MinIO Web Console and successfully uploaded a sample file to it.

## 7. Ports Used

| Port | Purpose           |
| ---- | ----------------- |
| 9000 | MinIO API         |
| 9001 | MinIO Web Console |

## 8. Result

The MinIO server was successfully set up using Docker. I was able to open the Web Console, create the `client-photos` bucket, and upload a sample file. This activity helped me understand how MinIO can be used as an S3-compatible object storage solution.

