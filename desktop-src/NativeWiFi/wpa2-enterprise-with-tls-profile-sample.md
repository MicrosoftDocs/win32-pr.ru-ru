---
description: Использует протокол расширенной проверки подлинности (EAP-TLS) с сертификатами для проверки подлинности в сети (WPA2-Enterprise).
ms.assetid: ded07fda-ea7f-4c5a-9433-60196c3f14af
title: Пример WPA2-Enterprise с профилем TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba561f552614896ca5da1522180a53146dc5ce54
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394828"
---
# <a name="wpa2-enterprise-with-tls-profile-sample"></a><span data-ttu-id="10210-103">Пример WPA2-Enterprise с профилем TLS</span><span class="sxs-lookup"><span data-stu-id="10210-103">WPA2-Enterprise with TLS Profile Sample</span></span>

<span data-ttu-id="10210-104">В этом примере профиля используется протокол EAP-TLS с сертификатами для проверки подлинности в сети.</span><span class="sxs-lookup"><span data-stu-id="10210-104">This sample profile uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) with certificates to authenticate to the network.</span></span>

<span data-ttu-id="10210-105">Этот пример настроен для использования защиты Wi-Fi защищенного доступа 2, работающей в режиме предприятия (WPA2-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="10210-105">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="10210-106">Тип безопасности WPA2-Enterprise использует 802.1 X для обмена аутентификацией с серверной частью.</span><span class="sxs-lookup"><span data-stu-id="10210-106">The WPA2-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="10210-107">Для шифрования используется тип шифра AES (AES).</span><span class="sxs-lookup"><span data-stu-id="10210-107">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="10210-108">Учетные данные EAP-TLS получаются из хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="10210-108">The EAP-TLS credentials are obtained from the certificate store.</span></span> <span data-ttu-id="10210-109">Если проверка подлинности на основе учетных данных в хранилище сертификатов завершается неудачно, пользователю предлагается ввести допустимые учетные данные.</span><span class="sxs-lookup"><span data-stu-id="10210-109">If authentication based on the credentials in the certificate store fails, the user is prompted to provide valid credentials.</span></span> <span data-ttu-id="10210-110">Если первая попытка завершается неудачей, для проверки подлинности не используются альтернативные серверы, корневые центры сертификации или имена пользователей.</span><span class="sxs-lookup"><span data-stu-id="10210-110">No alternate servers, root certificate authorities, or user names are used for authentication if the first attempt fails.</span></span>

<span data-ttu-id="10210-111">Конфигурация EAPHost, используемая в этом примере профиля беспроводной связи, была получена из образца [свойств подключения EAP-TLS](../eaphost/eap-tls-connection-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="10210-111">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

<span data-ttu-id="10210-112">**Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети:** Изменения реализуются в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети для оптимизации производительности беспроводных сетей.</span><span class="sxs-lookup"><span data-stu-id="10210-112">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="10210-113">Параметр по умолчанию для [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) , если этот элемент не задан в профиле беспроводной локальной сети, изменился.</span><span class="sxs-lookup"><span data-stu-id="10210-113">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="10210-114">Значение по умолчанию изменено на "false" в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="10210-114">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="10210-115">Значение по умолчанию — true в Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="10210-115">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="10210-116">Дополнительные сведения см. в описании элемента схемы [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="10210-116">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="10210-117">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Протокол EAP-TLS не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="10210-117">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** EAP-TLS is not supported.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2EnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2EnterpriseTLS</name>
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

## <a name="related-topics"></a><span data-ttu-id="10210-118">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="10210-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10210-119">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="10210-119">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
