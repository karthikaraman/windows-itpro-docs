---
title: WindowsAdvancedThreatProtection DDF file
description: WindowsAdvancedThreatProtection DDF file
ms.assetid: 0C62A790-4351-48AF-89FD-7D46C42D13E0
ms.author: maricia
ms.topic: article
ms.prod: w10
ms.technology: windows
author: nickbrower
---

# WindowsAdvancedThreatProtection DDF file

This topic shows the OMA DM device description framework (DDF) for the **WindowsAdvancedThreatProtection** configuration service provider. DDF files are used only with OMA DM provisioning XML.

You can download the DDF files from the links below:

- [Download all the DDF files for Windows 10, version 1703](http://download.microsoft.com/download/C/7/C/C7C94663-44CF-4221-ABCA-BC895F42B6C2/Windows10_1703_DDF_download.zip)
- [Download all the DDF files for Windows 10, version 1607](http://download.microsoft.com/download/2/3/E/23E27D6B-6E23-4833-B143-915EDA3BDD44/Windows10_1607_DDF.zip)

The XML below is the current version for this CSP.

``` syntax
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE MgmtTree PUBLIC " -//OMA//DTD-DM-DDF 1.2//EN"
  "http://www.openmobilealliance.org/tech/DTD/DM_DDF-V1_2.dtd"
  [<?oma-dm-ddf-ver supported-versions="1.2"?>]>
<MgmtTree xmlns:MSFT="http://schemas.microsoft.com/MobileDevice/DM">
  <VerDTD>1.2</VerDTD>
      <Node>
        <NodeName>WindowsAdvancedThreatProtection</NodeName>
        <Path>./Device/Vendor/MSFT</Path>
        <DFProperties>
          <AccessType>
            <Get />
          </AccessType>
          <Description>Windows Defender Advanced Threat Protection</Description>
          <DFFormat>
            <node />
          </DFFormat>
          <Occurrence>
            <One />
          </Occurrence>
          <Scope>
            <Permanent />
          </Scope>
          <DFType>
            <MIME>com.microsoft/1.1/MDM/WindowsAdvancedThreatProtection</MIME>
          </DFType>
        </DFProperties>
        <Node>
          <NodeName>Onboarding</NodeName>
          <DFProperties>
            <AccessType>
              <Replace />
              <Get />
            </AccessType>
            <Description>Set Windows Defender Advanced Threat Protection Onboarding blob and initiate onboarding to Windows Defender Advanced Threat Protection</Description>
            <DFFormat>
              <chr />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>HealthState</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Represents Windows Defender Advanced Threat Protection Health State</Description>
            <DFFormat>
              <node />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <DDFName></DDFName>
            </DFType>
          </DFProperties>
          <Node>
            <NodeName>LastConnected</NodeName>
            <DFProperties>
              <AccessType>
                <Get />
              </AccessType>
              <Description>The last successful connection.</Description>
              <DFFormat>
                <time />
              </DFFormat>
              <Occurrence>
                <One />
              </Occurrence>
              <Scope>
                <Permanent />
              </Scope>
              <DFType>
                <MIME>text/plain</MIME>
              </DFType>
            </DFProperties>
          </Node>
          <Node>
            <NodeName>SenseIsRunning</NodeName>
            <DFProperties>
              <AccessType>
                <Get />
              </AccessType>
              <DefaultValue>false</DefaultValue>
              <Description>Return Windows Defender Advanced Threat Protection service running state</Description>
              <DFFormat>
                <bool />
              </DFFormat>
              <Occurrence>
                <One />
              </Occurrence>
              <Scope>
                <Permanent />
              </Scope>
              <DFType>
                <MIME>text/plain</MIME>
              </DFType>
            </DFProperties>
          </Node>
          <Node>
            <NodeName>OnboardingState</NodeName>
            <DFProperties>
              <AccessType>
                <Get />
              </AccessType>
              <DefaultValue>0</DefaultValue>
              <Description>Return Windows Defender Advanced Threat Protection onboarding state: 0 – not onboarded; 1 - onboarded</Description>
              <DFFormat>
                <int />
              </DFFormat>
              <Occurrence>
                <One />
              </Occurrence>
              <Scope>
                <Permanent />
              </Scope>
              <DFType>
                <MIME>text/plain</MIME>
              </DFType>
            </DFProperties>
          </Node>
          <Node>
            <NodeName>OrgId</NodeName>
            <DFProperties>
              <AccessType>
                <Get />
              </AccessType>
              <Description>Onboarded Org ID.</Description>
              <DFFormat>
                <chr />
              </DFFormat>
              <Occurrence>
                <One />
              </Occurrence>
              <Scope>
                <Permanent />
              </Scope>
              <DFType>
                <MIME>text/plain</MIME>
              </DFType>
            </DFProperties>
          </Node>
        </Node>
        <Node>
          <NodeName>Configuration</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Represents Windows Defender Advanced Threat Protection Configuration</Description>
            <DFFormat>
              <node />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <DDFName></DDFName>
            </DFType>
          </DFProperties>
          <Node>
            <NodeName>SampleSharing</NodeName>
            <DFProperties>
              <AccessType>
                <Get />
                <Replace />
              </AccessType>
              <DefaultValue>1</DefaultValue>
              <Description>Return or set Windows Defender Advanced Threat Protection Sample Sharing configuration parameter: 0 - none, 1 - All</Description>
              <DFFormat>
                <int />
              </DFFormat>
              <Occurrence>
                <One />
              </Occurrence>
              <Scope>
                <Permanent />
              </Scope>
              <DFType>
                <MIME>text/plain</MIME>
              </DFType>
            </DFProperties>
          </Node>
          <Node>
            <NodeName>TelemetryReportingFrequency</NodeName>
            <DFProperties>
              <AccessType>
                <Get />
                <Replace />
              </AccessType>
              <DefaultValue>1</DefaultValue>
              <Description>Return or set Windows Defender Advanced Threat Protection telemetry reporting frequency. Allowed values are: 1 - Normal, 2 - Expedite</Description>
              <DFFormat>
                <int />
              </DFFormat>
              <Occurrence>
                <One />
              </Occurrence>
              <Scope>
                <Permanent />
              </Scope>
              <DFTitle>Telemetry reporting frequency</DFTitle>
              <DFType>
                <MIME>text/plain</MIME>
              </DFType>
            </DFProperties>
          </Node>
        </Node>
        <Node>
          <NodeName>Offboarding</NodeName>
          <DFProperties>
            <AccessType>
              <Replace />
              <Get />
            </AccessType>
            <Description>Set Windows Defender Advanced Threat Protection Offboarding blob and initiate offboarding</Description>
            <DFFormat>
              <chr />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
      </Node>
</MgmtTree>
```

## Related topics


[Configuration service provider reference](configuration-service-provider-reference.md)

 

 






