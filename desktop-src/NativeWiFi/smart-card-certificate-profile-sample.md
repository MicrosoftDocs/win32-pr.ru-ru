---
description: Используется для подключения к сети, использующей сертификаты протокола EAP-TLS, которые хранятся на смарт-карте для проверки подлинности 802.1 X.
ms.assetid: cb6758fc-1cce-4e62-adf7-0976957a49b0
title: Пример профиля сертификата смарт-карты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13373ea66a7ed93ad527715de9f32d4f72705be5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674364"
---
# <a name="smart-card-certificate-profile-sample"></a>Пример профиля сертификата смарт-карты

В этом примере профиля показан профиль проводной сети, используемый для подключения к сети, в которой используются сертификаты протокола EAP-TLS, хранящиеся на смарт-карте для проверки подлинности 802.1 X. Чтобы просмотреть профиль, использующий сертификаты EAP-TLS, хранящиеся на локальном компьютере, см. [пример профиля сертификата компьютера](machine-certificate-profile-sample.md).

Конфигурация EAPHost, используемая в этом примере профиля беспроводной связи, была получена из образца [свойств подключения EAP-TLS](../eaphost/eap-tls-connection-properties.md) .

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<LANProfile xmlns="https://www.microsoft.com/networking/LAN/profile/v1">
    <MSM>
        <security>
            <OneXEnforced>false</OneXEnforced>
            <OneXEnabled>true</OneXEnabled>
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
                                        <eapTls:SmartCard />
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
</LANProfile>
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Примеры проводных профилей](wired-profile-samples.md)
</dt> </dl>

 

 
