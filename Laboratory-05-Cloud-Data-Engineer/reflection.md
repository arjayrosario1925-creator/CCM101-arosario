# Reflection

This activity helped me understand the purpose of object storage and why it is useful for applications that handle a lot of data. For a photo-sharing application, the number of images can become very large over time, making traditional storage harder to manage. Object storage is suitable for this type of data because it can handle unstructured files such as photos, videos, and backups while allowing them to be stored and accessed easily.

I also learned that Docker can make deploying MinIO more convenient. Instead of going through a long manual installation process, I was able to start the storage server using a Docker command with the necessary configuration. The container was able to run quickly, and I could access the MinIO Web Console through its assigned port. This also gave me more practice with Docker after working with it in the previous activity.

Another thing I learned was the purpose of a bucket in object storage. A bucket acts as a storage container where objects or files can be organized. In this activity, I created the `client-photos` bucket and uploaded a sample file, which helped me understand how an application could store user-uploaded files.

For larger organizations, I learned that protecting stored data requires proper backup and redundancy strategies. Data can be replicated across different servers or locations so that it can still be available if one server experiences a failure. These practices can help reduce the risk of losing important files.

My experience with the Linux command line also improved during this activity. Some Docker commands were unfamiliar to me at first, but using commands such as `docker run` and `docker ps` helped me become more comfortable with the terminal. Overall, this activity helped me connect the concepts of Linux, Docker, object storage, MinIO, and GitHub documentation.

