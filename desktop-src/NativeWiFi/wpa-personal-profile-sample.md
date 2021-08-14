---
description: Использует общий ключ для проверки подлинности сети. Этот пример профиля использует Wi-Fi безопасность защищенного доступа в личном режиме (WPA-личное).
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: Пример профиля WPA-Personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d196a327672ae31cb52d275be79193860fd89fff29f169be63018f5b848a4268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797424"
---
# <a name="wpa-personal-profile-sample"></a>Пример профиля WPA-Personal

Этот пример профиля использует общий ключ для проверки подлинности сети. Ключ используется совместно с клиентом и точкой доступа. Этот пример профиля настроен для использования защиты Wi-Fi защищенного доступа, работающей в личном режиме (WPA-Personal). Для шифрования используется протокол TKIP.

**Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети:** изменения реализуются на Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети для оптимизации производительности беспроводных сетей. Параметр по умолчанию для [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) , если этот элемент не задан в профиле беспроводной локальной сети, изменился. значение по умолчанию изменено на "false" на Windows 7 и Windows сервере 2008 R2 с установленной службой беспроводной локальной сети. значение по умолчанию — true на Windows Server 2008 и Windows Vista. Дополнительные сведения см. в описании элемента схемы [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) .

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Дочерний элемент [**Name**](wlan-profileschema-name-wlanprofile-element.md) элемента [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) игнорируется. Имя профиля, хранящееся в хранилище профилей, является производным от дочернего элемента [**имени**](wlan-profileschema-name-ssid-element.md) [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAPSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAPSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPAPSK</authentication>
                <encryption>TKIP</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

Общий ключ пропущен в этом примере профиля. Если вы попытаетесь использовать этот пример профиля для подключения к сети, вам будет предложено ввести общий ключ. Этот запрос можно избежать, добавив дочерний элемент [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) в элемент [**безопасности**](wlan-profileschema-security-msm-element.md) сразу после элемента [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .

В следующем фрагменте кода показан элемент [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) , содержащий незашифрованный ключ. `<!-- insert key here -->`Перед использованием этого фрагмента в профиле необходимо заменить комментарий фактическим незашифрованным ключом.

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Образцы профиля беспроводной связи](wireless-profile-samples.md)
</dt> </dl>

 

 



