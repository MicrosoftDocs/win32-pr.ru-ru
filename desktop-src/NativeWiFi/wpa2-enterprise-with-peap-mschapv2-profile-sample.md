---
description: Использует защищенный протокол расширенной проверки подлинности с протоколом проверки подлинности Microsoft Challenge версии 2 с WPA2-Enterprise.
ms.assetid: fcbc74a6-1990-45a0-af2e-1c343a84497a
title: Пример WPA2-Enterprise с PEAP-MSCHAPv2 профилем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd05ac34992244eedae08f9c76becd5b2c95564e
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394809"
---
# <a name="wpa2-enterprise-with-peap-mschapv2-profile-sample"></a>Пример WPA2-Enterprise с PEAP-MSCHAPv2 профилем

Этот пример профиля использует защищенный протокол расширенной проверки подлинности с использованием протокола проверки подлинности Microsoft Challenge версии 2 (PEAP-MSCHAPv2) с **/** _паролем_ * username * для проверки подлинности в сети. Пользователю предлагается ввести учетные данные.

Этот пример настроен для использования защиты Wi-Fi защищенного доступа 2, работающей в режиме предприятия (WPA2-Enterprise). Тип безопасности WPA2-Enterprise использует 802.1 X для обмена аутентификацией с серверной частью. Для шифрования используется тип шифра AES (AES).

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Дочерний элемент [**Name**](wlan-profileschema-name-wlanprofile-element.md) элемента [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) игнорируется. Имя профиля, хранящееся в хранилище профилей, является производным от дочернего элемента [**имени**](wlan-profileschema-name-ssid-element.md) [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2EnterprisePEAPMSCHAP</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2EnterprisePEAPMSCHAP</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
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
                                           <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Образцы профиля беспроводной связи](wireless-profile-samples.md)
</dt> </dl>

 

 



