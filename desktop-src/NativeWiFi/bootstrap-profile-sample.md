---
description: Используется для проверки подлинности беспроводной сети в первый раз перед присоединением компьютера к домену.
ms.assetid: e1a5ce76-9761-4c65-8b26-a44bf2eb1835
title: Образец профиля начальной загрузки
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 96c7daa6bdc72146400973d08c9e5780092b214a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265031"
---
# <a name="bootstrap-profile-sample"></a><span data-ttu-id="aaf64-103">Образец профиля начальной загрузки</span><span class="sxs-lookup"><span data-stu-id="aaf64-103">Bootstrap Profile Sample</span></span>

<span data-ttu-id="aaf64-104">Образец профиля начальной загрузки можно использовать для проверки подлинности беспроводной сети в первый раз, прежде чем компьютер будет присоединен к домену.</span><span class="sxs-lookup"><span data-stu-id="aaf64-104">The Bootstrap profile sample can be used to authenticate to a wireless network for the first time before the computer has joined a domain.</span></span>

<span data-ttu-id="aaf64-105">Этот профиль не проверяет сертификаты, представленные сервером протокол RADIUS (RADIUS), и не должен использоваться после присоединения компьютера к домену.</span><span class="sxs-lookup"><span data-stu-id="aaf64-105">This profile does not validate the certificates presented by the Remote Authentication Dial-In User Service (RADIUS) server, and should not be used after the machine is joined to a domain.</span></span>

<span data-ttu-id="aaf64-106">Этот пример настроен для использования защиты Wi-Fi защищенного доступа 2, работающей в режиме предприятия (WPA2-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="aaf64-106">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="aaf64-107">Другие типы безопасности можно использовать при условии, что используется метод проверки подлинности PEAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="aaf64-107">Other security types can be used as long as the authentication method is PEAP-MSCHAPv2.</span></span>

<span data-ttu-id="aaf64-108">**Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети:** Изменения реализуются в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети для оптимизации производительности беспроводных сетей.</span><span class="sxs-lookup"><span data-stu-id="aaf64-108">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="aaf64-109">Параметр по умолчанию для [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) , если этот элемент не задан в профиле беспроводной локальной сети, изменился.</span><span class="sxs-lookup"><span data-stu-id="aaf64-109">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="aaf64-110">Значение по умолчанию изменено на "false" в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="aaf64-110">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="aaf64-111">Значение по умолчанию — true в Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="aaf64-111">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="aaf64-112">Дополнительные сведения см. в описании элемента схемы [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="aaf64-112">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="aaf64-113">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Дочерний элемент [**Name**](wlan-profileschema-name-wlanprofile-element.md) элемента [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="aaf64-113">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="aaf64-114">Имя профиля, хранящееся в хранилище профилей, является производным от дочернего элемента [**имени**](wlan-profileschema-name-ssid-element.md) [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="aaf64-114">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="aaf64-115">Дочерние элементы [**качеусердата**](onexschema-cacheuserdata-onex-element.md), [**аусмоде**](onexschema-authmode-onex-element.md)и [**singleSignOn**](onexschema-singlesignon-onex-element.md) элемента [**OneX**](onexschema-onex-element.md) не поддерживаются, и их следует удалить из профиля перед использованием.</span><span class="sxs-lookup"><span data-stu-id="aaf64-115">The [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**authMode**](onexschema-authmode-onex-element.md), and [**singleSignOn**](onexschema-singlesignon-onex-element.md) children of the [**OneX**](onexschema-onex-element.md) element are not supported, and should be removed from the profile before use.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleBootstrap</name>
    <SSIDConfig>
        <SSID>
            <name>SampleBootstrap</name>
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
                <authMode>machineOrUser</authMode>
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
               </EAPConfig>
           </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="aaf64-116">См. также</span><span class="sxs-lookup"><span data-stu-id="aaf64-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaf64-117">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="aaf64-117">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="aaf64-118">Присоединение беспроводного клиента Windows Vista к домену</span><span class="sxs-lookup"><span data-stu-id="aaf64-118">Joining a Windows Vista Wireless Client to a Domain</span></span>](https://www.microsoft.com/technet/network/wifi/vista_bootstrap_wireless.mspx)
</dt> </dl>

 

 



