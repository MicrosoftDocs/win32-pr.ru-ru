---
description: Использует протокол EAP-TLS для проверки подлинности в сети.
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: Пример WPA-Enterprise с профилем TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5300f8886d55ac713b0206b45f20857f22b2772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999314"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a>Пример WPA-Enterprise с профилем TLS

В этом примере профиля используется протокол EAP-TLS с сертификатами для проверки подлинности в сети.

Этот пример настроен для использования Wi-Fi безопасности защищенного доступа, работающей в режиме предприятия (WPA-Enterprise). Тип безопасности WPA-Enterprise использует 802.1 X для обмена аутентификацией с серверной частью. Для шифрования используется протокол TKIP.

Учетные данные EAP-TLS получаются из хранилища сертификатов. Если проверка подлинности на основе учетных данных в хранилище сертификатов завершается неудачно, пользователю предлагается ввести допустимые учетные данные. Если первая попытка завершается неудачей, для проверки подлинности не используются альтернативные серверы, корневые центры сертификации или имена пользователей.

Конфигурация EAPHost, используемая в этом примере профиля беспроводной связи, была получена из образца [свойств подключения EAP-TLS](../eaphost/eap-tls-connection-properties.md) .

**Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети:** Изменения реализуются в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети для оптимизации производительности беспроводных сетей. Параметр по умолчанию для [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) , если этот элемент не задан в профиле беспроводной локальной сети, изменился. Значение по умолчанию изменено на "false" в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети. Значение по умолчанию — true в Windows Server 2008 и Windows Vista. Дополнительные сведения см. в описании элемента схемы [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) .

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Протокол EAP-TLS не поддерживается.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAEnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAEnterpriseTLS</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA</authentication>
                <encryption>TKIP</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
 
                        <EapMethod>
                            <eapCommon:Type>13</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                        </EapMethod>
                        <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                                xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">

                            <baseEap:Eap>
                                <baseEap:Type>13</baseEap:Type> 
                                <eapTls:EapType>
                                    <eapTls:CredentialsSource>
                                        <eapTls:CertificateStore />
                                    </eapTls:CredentialsSource>
                                    <eapTls:ServerValidation>
                                        <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation> 
                                        <eapTls:ServerNames /> 
                                    </eapTls:ServerValidation> 
                                   <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
                               </eapTls:EapType>
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

 

 
