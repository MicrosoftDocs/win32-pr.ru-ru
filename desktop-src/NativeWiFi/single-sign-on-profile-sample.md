---
description: Используется для сценариев, требующих проверки подлинности 802.1 X перед входом в Windows.
ms.assetid: 76c8d416-3912-41b1-ac9d-3e6e86a76ceb
title: Пример профиля с одним Sign-On
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 077ed95095150e81ad9a3d7412d1940dcb1b33e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674365"
---
# <a name="single-sign-on-profile-sample"></a>Пример профиля с одним Sign-On

Образец профиля единого входа (SSO) можно использовать для сценариев, требующих проверки подлинности 802.1 X перед входом в Windows.

Этот пример настроен для использования защиты Wi-Fi защищенного доступа 2, работающей в режиме предприятия (WPA2-Enterprise). Для сетевой проверки подлинности используется защищенный протокол расширенной проверки подлинности с протоколом проверки подлинности Microsoft Challenge версии 2 (PEAP-MSCHAPv2). Учетные данные входа Windows используются для PEAP-MSCHAPv2 проверки подлинности.

Хотя этот пример настроен для использования WPA2-Enterprise и протокола PEAP-MSCHAPv2, для профилей единого входа можно настроить другие типы безопасности и проверки подлинности.

**Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети:** Изменения реализуются в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети для оптимизации производительности беспроводных сетей. Параметр по умолчанию для [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) , если этот элемент не задан в профиле беспроводной локальной сети, изменился. Значение по умолчанию изменено на "false" в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети. Значение по умолчанию — true в Windows Server 2008 и Windows Vista. Дополнительные сведения см. в описании элемента схемы [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) .

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Дочерний элемент [**Name**](wlan-profileschema-name-wlanprofile-element.md) элемента [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) игнорируется. Имя профиля, хранящееся в хранилище профилей, является производным от дочернего элемента [**имени**](wlan-profileschema-name-ssid-element.md) [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) . Дочерние элементы [**качеусердата**](onexschema-cacheuserdata-onex-element.md), [**максаусфаилурес**](onexschema-maxauthfailures-onex-element.md), [**аусмоде**](onexschema-authmode-onex-element.md)и [**singleSignOn**](onexschema-singlesignon-onex-element.md) элемента [**OneX**](onexschema-onex-element.md) не поддерживаются, и их следует удалить из профиля перед использованием.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleSingleSignOn</name>
    <SSIDConfig>
        <SSID>
            <name>SampleSingleSignOn</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <cacheUserData>true</cacheUserData>
                <maxAuthFailures>3</maxAuthFailures>
                <authMode>user</authMode>
                <singleSignOn>
                    <type>preLogon</type>
                    <maxDelay>10</maxDelay>
                </singleSignOn>
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
                        <EapMethod>
                            <eapCommon:Type>25</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                       </EapMethod>
                       <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                               xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
                               xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
                           <baseEap:Eap>
                               <baseEap:Type>25</baseEap:Type> 
                               <msPeap:EapType>
                                   <msPeap:ServerValidation>
                                       <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
                                       <msPeap:TrustedRootCA /> 
                                   </msPeap:ServerValidation>
                                   <msPeap:FastReconnect>true</msPeap:FastReconnect> 
                                   <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
                                   <baseEap:Eap>
                                       <baseEap:Type>26</baseEap:Type> 
                                       <msChapV2:EapType>
                                           <msChapV2:UseWinLogonCredentials>true</msChapV2:UseWinLogonCredentials> 
                                       </msChapV2:EapType>
                                   </baseEap:Eap>
                                   <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
                                   <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
                                   <msPeap:PeapExtensions /> 
                               </msPeap:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Образцы профиля беспроводной связи](wireless-profile-samples.md)
</dt> </dl>

 

 



