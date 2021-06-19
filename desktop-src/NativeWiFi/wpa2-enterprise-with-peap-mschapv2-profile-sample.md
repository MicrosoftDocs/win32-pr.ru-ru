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
# <a name="wpa2-enterprise-with-peap-mschapv2-profile-sample"></a><span data-ttu-id="17a4f-103">Пример WPA2-Enterprise с PEAP-MSCHAPv2 профилем</span><span class="sxs-lookup"><span data-stu-id="17a4f-103">WPA2-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>

<span data-ttu-id="17a4f-104">Этот пример профиля использует защищенный протокол расширенной проверки подлинности с использованием протокола проверки подлинности Microsoft Challenge версии 2 (PEAP-MSCHAPv2) с **/** _паролем_ \* username \* для проверки подлинности в сети.</span><span class="sxs-lookup"><span data-stu-id="17a4f-104">This sample profile uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ to authenticate to the network.</span></span> <span data-ttu-id="17a4f-105">Пользователю предлагается ввести учетные данные.</span><span class="sxs-lookup"><span data-stu-id="17a4f-105">The user is prompted to enter credentials.</span></span>

<span data-ttu-id="17a4f-106">Этот пример настроен для использования защиты Wi-Fi защищенного доступа 2, работающей в режиме предприятия (WPA2-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="17a4f-106">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="17a4f-107">Тип безопасности WPA2-Enterprise использует 802.1 X для обмена аутентификацией с серверной частью.</span><span class="sxs-lookup"><span data-stu-id="17a4f-107">The WPA2-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="17a4f-108">Для шифрования используется тип шифра AES (AES).</span><span class="sxs-lookup"><span data-stu-id="17a4f-108">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="17a4f-109">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Дочерний элемент [**Name**](wlan-profileschema-name-wlanprofile-element.md) элемента [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="17a4f-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="17a4f-110">Имя профиля, хранящееся в хранилище профилей, является производным от дочернего элемента [**имени**](wlan-profileschema-name-ssid-element.md) [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="17a4f-110">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="17a4f-111">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="17a4f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17a4f-112">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="17a4f-112">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



