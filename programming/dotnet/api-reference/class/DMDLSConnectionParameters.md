---
layout: default-layout
title: Dynamsoft Barcode Reader .NET API Reference - DMDLSConnectionParameters Class
description: This page shows the DMDLSConnectionParameters Class of Dynamsoft Barcode Reader for .NET SDK.
keywords: DMDLSConnectionParameters, class, api reference, .Net
needAutoGenerateSidebar: false
---


# DMDLSConnectionParameters
Defines a struct to configure the parameters to connect to license server.  

```csharp
public class DMDLSConnectionParameters
```  


## Attributes
    
| Attribute | Type |
|---------- | ---- |
| [`MainServerURL`](#mainserverurl) | *string* |
| [`StandbyServerURL`](#standbyserverurl) | *string* |
| [`HandshakeCode`](#handshakecode) | *string* |
| [`SessionPassword`](#sessionpassword) | *string* |
| [`DeploymentType`](#deploymenttype) | *EnumDMDeploymentType* |
| [`ChargeWay`](#chargeway) | *EnumDMChargeWay* |
| [`UUIDGenerationMethod`](#uuidgenerationmethod) | *EnumDMUUIDGenerationMethod* |
| [`MaxBufferDays`](#maxbufferdays) | *int* |
| [`LimitedLicenseModules`](#limitedlicensemodules) | *EnumDMLicenseModule[]* |
| [`MaxConcurrentInstanceCount`](#maxconcurrentinstancecount) | *int* |
| [`OrganizationID`](#organizationid) | *string* |
| [`Products`](#products) | *int* |


### MainServerURL

The URL of the license server.

```csharp
string Dynamsoft.DMDLSConnectionParameters.MainServerURL
```

- **Value range**   
    Any string value   
      
- **Default value**   
    null
    
- **Remarks**  
    If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to null (default value), it will connect to Dynamsoft's license servers for online verification.

- **Remarks**   
    If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to null (default value), it will connect to Dynamsoft's license servers for online verification.   


### StandbyServerURL

The URL of the standby license server.

```csharp
string Dynamsoft.DMDLSConnectionParameters.StandbyServerURL
```

- **Value range**   
    Any string value   
      
- **Default value**   
    null
    
- **Remarks**  
    If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to null (default value), it will connect to Dynamsoft's license servers for online verification.

- **Remarks**   
    If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to null (default value), it will connect to Dynamsoft's license servers for online verification.   


### HandshakeCode

The handshake code.

```csharp
string Dynamsoft.DMDLSConnectionParameters.HandshakeCode
```

- **Value range**   
    Any string value   
      
- **Default value**   
    null

### SessionPassword

The session password of the handshake code set in license server.

```csharp
string Dynamsoft.DMDLSConnectionParameters.SessionPassword
```

- **Value range**   
    Any string value   
      
- **Default value**   
    null


### DeploymentType

Sets the deployment type.

```csharp
EnumDMDeploymentType Dynamsoft.DMDLSConnectionParameters.DeploymentType
```

- **Value range**   
    Any one of the [`EnumDMDeploymentType`]({{ site.enumerations }}other-enums.html#dm_deploymenttype) Enumeration items.   
      
- **Default value**   
    DM_DT_DESKTOP   
    
- **See also**  
    [`EnumDMDeploymentType`]({{ site.enumerations }}other-enums.html#dm_deploymenttype)    

### ChargeWay

Sets the charge way.

```csharp
EnumDMChargeWay Dynamsoft.DMDLSConnectionParameters.ChargeWay
```

- **Value range**   
    Any one of the [`EnumDMChargeWay`]({{ site.enumerations }}other-enums.html#dm_chargeWay) Enumeration items.   
      
- **Default value**   
    DM_CW_AUTO   
    
- **See also**  
    [`EnumDMChargeWay`]({{ site.enumerations }}other-enums.html#dm_chargeWay)    


### UUIDGenerationMethod

Sets the method to generate UUID.

```csharp
EnumDMUUIDGenerationMethod Dynamsoft.DMDLSConnectionParameters.UUIDGenerationMethod
```

- **Value range**   
    Any one of the [`EnumDMUUIDGenerationMethod`]({{ site.enumerations }}other-enums.html#dm_uuidgenerationmethod) Enumeration items.   
      
- **Default value**   
    DM_UUIDGM_RANDOM   
    
- **See also**  
    [`EnumDMUUIDGenerationMethod`]({{ site.enumerations }}other-enums.html#dm_uuidgenerationmethod)    

### MaxBufferDays

Sets the max days to buffer the license info.

```csharp
int Dynamsoft.DMDLSConnectionParameters.MaxBufferDays
```

- **Value range**   
    [7,0x7fffffff]  
      
- **Default value**   
    7  
    

### LimitedLicenseModules

Sets the license modules to use.

```csharp
EnumDMLicenseModule[] Dynamsoft.DMDLSConnectionParameters.LimitedLicenseModules
```

- **Value range**   
    Each array item can be any one of the [`EnumDMLicenseModule`]({{ site.enumerations }}other-enums.html#dm_licensemodule) Enumeration items.   
      
- **Default value**   
    null   
    
- **See also**  
    [`EnumDMLicenseModule`]({{ site.enumerations }}other-enums.html#dm_licensemodule)    


### MaxConcurrentInstanceCount
Sets the max concurrent instance count.
```csharp
int Dynamsoft.DMDLSConnectionParameters.MaxConcurrentInstanceCount
```
- **Value range**   
    [1,0x7fffffff]   
      
- **Default value**   
    1
- **Remarks**   
    It works only when [ChargeWay](#chargeway) is setting to DM_CW_CONCURRENT_INSTANCE_COUNT
    It is the total number of instances used by multiple processes. For example, if there are two .EXE are running on the server and each .EXE may have 10 instances at most, then you should set maxConcurrentInstanceCount to 20.


### OrganizationID
The organization ID got from Dynamsoft.

```csharp
string Dynamsoft.DMDLSConnectionParameters.OrganizationID
```

- **Value range**   
    Any string value   
      
- **Default value**   
    null


### Products
Sets the products to get the license for. Product values can be combined.
```csharp
int Dynamsoft.DMDLSConnectionParameters.Products
```
- **Value range**   
    A combined value of [`Product`]({{ site.enumerations }}other-enums.html#product) Enumeration items
      
- **Default value**   
    `PROD_ALL`
