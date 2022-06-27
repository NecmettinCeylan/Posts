# How to Install MinIO on Linux
## Simple steps to start you own MinIO server

# 1. Download and install MinIO 

    wget https://dl.min.io/server/minio/release/linux-amd64/minio_20220625155016.0.0_amd64.deb -O minio.deb
    sudo dpkg -i minio.deb

# 2. Start minio server

    mkdir ~/minio
    minio server ~/minio --console-address :9090

# 3. Connect to MinIO server using defautl credentials

    RootUser: minioadmin
    RootPass: minioadmin

# 4. Start server with custom admin username and password

Set following variables before starting the server

    MINIO_ROOT_USER
	MINIO_ROOT_PASSWORD

# 5. Create User

First you need to get MinIO Client

    wget https://dl.min.io/client/mc/release/linux-amd64/mc
    chmod +x mc
    ./mc --help

Create user with:

    mc admin user add ALIAS ACCESSKEY SECRETKEY

Set policy of user:

    mc admin policy set ALIAS readwrite user=USERNAME


# Ref:

[https://docs.min.io/minio/baremetal/quickstart/linux.html#quickstart-linux](https://docs.min.io/minio/baremetal/quickstart/linux.html#quickstart-linux)

[https://docs.min.io/docs/minio-multi-user-quickstart-guide.html](https://docs.min.io/docs/minio-multi-user-quickstart-guide.html)

[https://docs.min.io/minio/baremetal/security/minio-identity-management/user-management.html](https://docs.min.io/minio/baremetal/security/minio-identity-management/user-management.html)