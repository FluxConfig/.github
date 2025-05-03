# FluxConfig - Remote Configuration Storage System

FluxConfig is self-hosted configuration storage and management service aimed at optimizing the process of application maintenance and development.

Provides isolated storage for application configuration data by versions - tags, configuration data management, feature flag support, system user management, permissions separation in the system and within the configuration by roles via a web client, automated retrieval and update of configuration of the already deployed application without the need to restart the application or interact with the deployment environment via provided SDK clients for various programming languages ​​and frameworks.

## How does it work

- You install the system in your own controlled environment

- Manage the configuration parameters and feature flags of the application using the web client.

  - Each application configuration can have multiple version-tags with corresponding requirements for the configuration participant role. 
  - Each version-tag of the configuration  is divided into 2 parts - RealTime section, which allows automatic data modification during application runtime and is intended for use of feature flags and dynamic data and Vault section, the data of which is loaded by the application once at startup and cannot be modified during application runtime, intended for storing sensitive data and infrastructure parameters of the application environment.

- Using the system-provided SDK clients, the application receives up-to-date data and updates the application configuration parameters in runtime.

<div style="display: flex; justify-content: center; align-items: center; ">
  <img src="../docs/img/fluxconfig_arch.jpg" 
  style="width: 90%; height: auto;" alt="Sign In Guide">
</div>

## Get started with FluxConfig


### 1. Deploy system according to provided [Guidance](https://github.com/FluxConfig/Deployment)

FluxConfig is modular, so you can deploy all its parts on one system or each part separately.


### 2. Manage applications configurations with web-client

#### 2.1 Sign-in into account or create one

#### 2.2 Create or join configuration for your project

**Create if allowed**

<div style="display: flex; justify-content: center; align-items: center; margin-bottom: 10px">
  <img src="../docs/img/guidance_2_1_create.png" 
  style="width: 60%; height: auto;" alt="Sign In Guide">
</div>

<div style="text-align: center;">
  <img 
    src="../docs/img/guidance_2_2_create.png" 
    style="width: 60%; display: block; margin: 0 auto;" 
    alt="Guidance_2_2 create"
  >
</div>

**Invite members**

<div style="text-align: center;">
  <img 
    src="../docs/img/guidance_2_3_invite.png" 
    style="width: 60%; display: block; margin: 0 auto;" 
    alt="Guidance_2_3 invite"
  >
</div>

#### 2.3 Create configuration Tag if needed and allowed for your role

<div style="text-align: center; margin-bottom: 10px">
  <img 
    src="../docs/img/guidance_3_1_tags.png" 
    style="width: 60%; display: block; margin: 0 auto;" 
    alt="Guidance_2_3 invite"
  >
</div>

<div style="display: flex; justify-content: center; align-items: center; margin-bottom: 10px">
  <img src="../docs/img/guidance_3_1_tag_create.png" 
  style="width: 60%; height: auto;" alt="Sign In Guide">
</div>

#### 2.4 Create or update configuration data for Tag allowed for your role

<div style="text-align: center; margin-bottom: 10px">
  <img 
    src="../docs/img/guidance_4_1_tag_data.png" 
    style="width: 60%; display: block; margin: 0 auto;" 
    alt="Guidance_2_3 invite"
  >
</div>

<div style="display: flex; justify-content: center; align-items: center;">
  <img src="../docs/img/guidance_4_2_tag_data.png" 
  style="width: 60%; height: auto;" alt="Sign In Guide">
</div>

#### 2.5 Get an API-key for configuration Tag allowed for your role

<div style="display: flex; justify-content: center; align-items: center;">
  <img src="../docs/img/guidance_5_api-key.png" 
  style="width: 60%; height: auto;" alt="Sign In Guide">
</div>

### 3. Use provided SDK-clients in your application to retrieve configuration data.


## List of avaliable open-source SDK-clients

| **SDK-client** | Package | Repository |
| -------- | -------- | -------- |
| .NET  |  [NuGet](https://www.nuget.org/packages/FluxConfig.Provider)   |  [FluxConfig.Provider](https://github.com/FluxConfig/FluxConfig.Provider)  |