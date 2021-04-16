---
description: Использует общий ключ для проверки подлинности сети.
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: Пример профиля WPA-Personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d4a69fffcb0432e420121ed76c76889eb8bb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684228"
---
# <a name="wpa-personal-profile-sample"></a>Пример профиля WPA-Personal

Этот пример профиля использует общий ключ для проверки подлинности сети. Ключ используется совместно с клиентом и точкой доступа. Этот пример профиля настроен для использования защиты Wi-Fi защищенного доступа, работающей в личном режиме (WPA-Personal). Для шифрования используется протокол TKIP.

**Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети:** Изменения реализуются в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети для оптимизации производительности беспроводных сетей. Параметр по умолчанию для [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) , если этот элемент не задан в профиле беспроводной локальной сети, изменился. Значение по умолчанию изменено на "false" в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети. Значение по умолчанию — true в Windows Server 2008 и Windows Vista. Дополнительные сведения см. в описании элемента схемы [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) .

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Образцы профиля беспроводной связи](wireless-profile-samples.md)
</dt> </dl>

 

 



