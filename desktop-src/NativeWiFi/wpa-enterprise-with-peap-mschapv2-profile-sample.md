---
description: Использует защищенный протокол расширенной проверки подлинности с протоколом проверки подлинности Microsoft Challenge версии 2 с WPA-Enterprise.
ms.assetid: e344c360-4ab5-4a5f-a1b2-b0fa890b8666
title: Пример WPA-Enterprise с PEAP-MSCHAPv2 профилем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364cc7a9cc85e4c5e2ef908c0ac2a4726d6c5a96
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395049"
---
# <a name="wpa-enterprise-with-peap-mschapv2-profile-sample"></a><span data-ttu-id="3cb7f-103">Пример WPA-Enterprise с PEAP-MSCHAPv2 профилем</span><span class="sxs-lookup"><span data-stu-id="3cb7f-103">WPA-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>

<span data-ttu-id="3cb7f-104">Этот пример профиля использует защищенный протокол расширенной проверки подлинности с использованием протокола проверки подлинности Microsoft Challenge версии 2 (PEAP-MSCHAPv2) с **/** _паролем_ \* username \* для проверки подлинности в сети.</span><span class="sxs-lookup"><span data-stu-id="3cb7f-104">This sample profile uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ to authenticate to the network.</span></span> <span data-ttu-id="3cb7f-105">Пользователю предлагается ввести учетные данные.</span><span class="sxs-lookup"><span data-stu-id="3cb7f-105">The user is prompted to enter credentials.</span></span>

<span data-ttu-id="3cb7f-106">Этот пример настроен для использования Wi-Fi безопасности защищенного доступа, работающей в режиме предприятия (WPA-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="3cb7f-106">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="3cb7f-107">Тип безопасности WPA-Enterprise использует 802.1 X для обмена аутентификацией с серверной частью.</span><span class="sxs-lookup"><span data-stu-id="3cb7f-107">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="3cb7f-108">Для шифрования используется протокол TKIP.</span><span class="sxs-lookup"><span data-stu-id="3cb7f-108">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="3cb7f-109">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Дочерний элемент [**Name**](wlan-profileschema-name-wlanprofile-element.md) элемента [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3cb7f-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="3cb7f-110">Имя профиля, хранящееся в хранилище профилей, является производным от дочернего элемента [**имени**](wlan-profileschema-name-ssid-element.md) [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3cb7f-110">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAEnterprisePEAPMSCHAP</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAEnterprisePEAPMSCHAP</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
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

## <a name="related-topics"></a><span data-ttu-id="3cb7f-111">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3cb7f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cb7f-112">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="3cb7f-112">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



