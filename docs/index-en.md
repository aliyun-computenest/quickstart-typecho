# Typecho Compute Nest Quick Deployment

## Overview

Typecho is a lightweight, open-source blogging program developed in PHP. It supports multiple databases and features a robust kernel, convenient extensibility, user-friendly experience, and smooth performance. For more information, please refer to the [Typecho Official Documentation](https://docs.typecho.org/doku.php).

This document describes how to quickly deploy Typecho using Alibaba Cloud Compute Nest.

## Prerequisites

To deploy a Typecho Community Edition service instance, you need permission to access and create certain Alibaba Cloud resources. Therefore, your account must have permissions for the following resources.

**Note:** These permissions are only required if your account is a RAM (Resource Access Management) user.

| Permission Policy Name              | Description                                  |
|-------------------------------------|----------------------------------------------|
| AliyunECSFullAccess                 | Permissions to manage Elastic Compute Service (ECS) |
| AliyunVPCFullAccess                 | Permissions to manage Virtual Private Cloud (VPC)   |
| AliyunROSFullAccess                 | Permissions to manage Resource Orchestration Service (ROS) |
| AliyunComputeNestUserFullAccess     | User-side permissions to manage Compute Nest services |

## Parameter Descriptions

| Parameter Group      | Parameter Item       | Description                                                                                                                                                               |
|----------------------|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Service Instance     | Service Instance Name | Must not exceed 64 characters. Must start with an English letter. Can contain numbers, English letters, hyphens (-), and underscores (_).                                 |
|                      | Region               | The region where the service instance will be deployed.                                                                                                                   |
| Network Configuration| Zone                 | The zone where the ECS instance resides.                                                                                                                                  |
|                      | VPC ID               | The VPC where the resources reside.                                                                                                                                       |
|                      | vSwitch ID           | The vSwitch where the resources reside.                                                                                                                                   |
| ECS Instance Config  | Instance Type        | The specification of the ECS instance.                                                                                                                                    |
|                      | Billing Method       | The billing method for resources: Pay-As-You-Go or Subscription.                                                                                                          |
|                      | System Disk Size     | The size of the system disk. Value range: [40, 500]. Unit: GB.                                                                                                            |
|                      | Traffic Billing Type | Pay-by-bandwidth or Pay-by-traffic.                                                                                                                                       |
|                      | Instance Password    | The login password for the server. Length: 8–30 characters. Must include at least three of the following categories: uppercase letters, lowercase letters, numbers, and special symbols (`()~!@#$%^&*_-+={}[]:;'<>,.?/`). |
| Database Configuration| Database Password    | The password for the Typecho database account (`root`) for the database `typecho_db`. Consists of letters, numbers, and underscores (_). Length: 8–32 characters.          |

## Deployment Process

1. Visit the Compute Nest Typecho Community Edition [deployment link](https://computenest.console.aliyun.com/service/instance/create/cn-hangzhou?type=user&ServiceId=service-db7c899d37c04551b61e) and fill in the deployment parameters as prompted.

2. After filling in the parameters, you will see the corresponding price inquiry details. Confirm the parameters, click **Next: Confirm Order**, agree to the service agreement, and then click **Create Now** to enter the deployment phase.

3. Once the deployment is successful, go to the service instance details page and click `typechoUrl` to install Typecho.

4. The default database username is `root`, the database password is the one specified during deployment, and the database name is `typecho_db`.

5. Set the administrator username, password, and email address. Typecho installation is now complete.
