# AWS Multi-Tier VPC Architecture

VPC or  VIrtual Private Cloud is a service used to create private networks inside AWS you can provision other services like EC2, EFS etc to run from a VPC.
VPC are also the service used to connect your AWS private networks from your on premises network when you're creating a hybrid environment or it is a service which lets you connect your other cloud platforms,
when you're creating a multi cloud deployment.

There are two types of VPC S, default VPC and custom VPC. Default VPC is created by AWS on your behalf and you can have one default VPC per region.
But for custom VPC you need to configure everything end to end in detail and there are 100% private by default.You can have multiple custom VPCs per region.

VPC is private and isolated.Services deployed into the VPC can communicate with each other, but it will not be able to communicate with anything outside VPC until you explicitly configured.

1.	# Create Custom VPC

![2024-02-25 22_42_38-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/1340fe43-47f2-4916-80db-1e90c4102056)

![2024-02-25 22_42_56-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/37b29512-206b-4e3e-a317-1f4587b3846b)


2.	# Create Subnets inside custom VPC

![2024-02-25 22_43_01-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/629d4df4-1958-40cc-9520-fa4eb04d74a7)


3.	# Configuring one tier in VPC to be Public
![2024-02-25 22_43_14-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/7faffcbd-1104-4a03-aa8d-7a72ab96f778)

![2024-02-25 22_43_21-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/78862f89-6a37-4dae-9322-3047d8765ffe)

![2024-02-25 22_43_26-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/8ec6a022-1b65-49be-9ba2-b5f86cb4b06a)

![2024-02-25 22_43_29-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/aa7fd1de-208e-456b-a62a-4c2a8d19dff7)

![2024-02-25 22_43_55-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/2b771b14-b4e8-4b95-b003-ab34d2079fdf)

![2024-02-25 22_44_58-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/34779a09-b744-4169-bfd2-8c056acfffcd)

![2024-02-25 22_46_28-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/024907cc-0e2e-4c3c-89b2-7f3dd4f467b6)

![2024-02-25 22_47_19-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/b50fd013-e52a-4c39-9883-b3f833b2f777)



4.	# Create NAT Gateway

![2024-02-25 22_51_18-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/118bf32b-9a71-4515-a44f-d5623e1f3227)

![2024-02-25 22_52_45-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/19c810a3-4ed9-4573-bd9c-575735118f9a)

![2024-02-25 22_54_39-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/3c9e8352-8ad2-4b31-9aeb-b4aa73a3e5e5)

5.	# Create Bastion Host and Clean up 

![2024-02-25 22_54_55-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/1d0c1bd3-dd3c-4820-9eb7-1dda79fd8d27)

![2024-02-25 22_55_01-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/16d1c9c7-0fee-4050-9e18-5804475efefc)

![2024-02-25 22_55_09-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/f3c76a2e-47f8-478e-bb3e-7fa979d7747f)

![2024-02-25 22_56_58-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/1b02b965-b8ae-40e7-b8b2-57ae93969a16)

![2024-02-25 22_57_05-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/ea73712a-d7ed-4197-9006-6a4c69750b36)

![2024-02-25 22_57_54-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/75e3d291-8b90-4590-b0c7-6d0443ff9391)
![2024-02-25 22_59_38-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/15606eb8-3dba-4f53-9043-241e9f8dd975)
![2024-02-25 22_59_58-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/ed144a73-629a-4885-929d-736169e35514)

![2024-02-25 23_05_27-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/ce64ea82-ae82-4a05-9702-c897766019ec)

![2024-02-25 23_06_19-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/7f239492-46b5-4455-bf33-4e2cf0a02557)
![2024-02-25 23_09_46-Greenshot](https://github.com/Anshul3vishwakarmma6/Aws/assets/159995520/d4af9fc4-fee7-46ef-a817-408ca7b49ff6)

