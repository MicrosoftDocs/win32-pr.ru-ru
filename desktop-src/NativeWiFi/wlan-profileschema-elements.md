---
description: '\_Схема профиля WLAN определяет следующие элементы.'
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: WLAN_profile элементы схемы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810379"
---
# <a name="wlan_profile-schema-elements"></a>\_Элементы схемы профиля WLAN

\_Схема профиля WLAN определяет следующие элементы. Большинство элементов находятся в пространстве имен `https://www.microsoft.com/networking/WLAN/profile/v1` , за исключением [**Фипсмоде (аусенкриптион)**](wlan-profileschema-fipsmode-authencryption-element.md), который находится в пространстве имен `https://www.microsoft.com/networking/WLAN/profile/v2` .

В следующем списке показаны определенные элементы в порядке, в котором элементы отображаются в профиле. Упорядочение элементов выполняется принудительно. Не все элементы находятся в каждом профиле, поскольку некоторые элементы являются необязательными.

В этом списке не отображаются все возможные элементы, которые могут отображаться в профиле беспроводной связи, так как элементы можно добавлять в **xs: любые** точки вставки.

-   [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
    -   [**имя (Вланпрофиле)**](wlan-profileschema-name-wlanprofile-element.md)
    -   [**Ссидконфиг (Вланпрофиле)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [**SSID (Ссидконфиг)**](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [**Hex (SSID)**](wlan-profileschema-hex-ssid-element.md)
            -   [**имя (SSID)**](wlan-profileschema-name-ssid-element.md)
        -   [**Нешироковещательная (Ссидконфиг)**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [**Hotspot2 (Вланпрофиле)**](wlan-profileschema-hotspot2-element.md)
        -   [**Имя_домена (Hotspot2)**](wlan-profileschema-hotspot2-domainname-element.md)
        -   [**Наиреалм (Hotspot2)**](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [**Network3GPP (Hotspot2)**](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [**Роамингконсортиум (Hotspot2)**](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [**connectionType (Вланпрофиле)**](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [**connectionMode (Вланпрофиле)**](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [**Автопереключение (Вланпрофиле)**](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [**MSM (Вланпрофиле)**](wlan-profileschema-msm-wlanprofile-element.md)
        -   [**подключение (MSM)**](wlan-profileschema-connectivity-msm-element.md)
            -   [**Фитипе (подключение)**](wlan-profileschema-phytype-connectivity-element.md)
        -   [**безопасность (MSM)**](wlan-profileschema-security-msm-element.md)
            -   [**Аусенкриптион (безопасность)**](wlan-profileschema-authencryption-security-element.md)
                -   [**Проверка подлинности (Аусенкриптион)**](wlan-profileschema-authentication-authencryption-element.md)
                -   [**шифрование (Аусенкриптион)**](wlan-profileschema-encryption-authencryption-element.md)
                -   [**Усеонекс (Аусенкриптион)**](wlan-profileschema-useonex-authencryption-element.md)
                -   [**Фипсмоде (Аусенкриптион)**](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [**sharedKey (безопасность)**](wlan-profileschema-sharedkey-security-element.md)
                -   [**keyType (sharedKey)**](wlan-profileschema-keytype-sharedkey-element.md)
                -   [**защищено (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)
                -   [**Кэйматериал (sharedKey)**](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [**Кэйиндекс (безопасность)**](wlan-profileschema-keyindex-security-element.md)
            -   [**Пмккачемоде (безопасность)**](wlan-profileschema-pmkcachemode-security-element.md)
            -   [**Пмккачеттл (безопасность)**](wlan-profileschema-pmkcachettl-security-element.md)
            -   [**Пмккачесизе (безопасность)**](wlan-profileschema-pmkcachesize-security-element.md)
            -   [**Преаусмоде (безопасность)**](wlan-profileschema-preauthmode-security-element.md)
            -   [**Преауссроттле (безопасность)**](wlan-profileschema-preauththrottle-security-element.md)
    -   [**IHV (Вланпрофиле)**](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [**Ауихеадер (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
            -   [**OUI (Ауихеадер)**](wlan-profileschema-oui-ouiheader-element.md)
            -   [**тип (Ауихеадер)**](wlan-profileschema-type-ouiheader-element.md)
        -   [**подключение (IHV)**](wlan-profileschema-connectivity-ihv-element.md)
        -   [**безопасность (IHV)**](wlan-profileschema-security-ihv-element.md)
        -   [**Усемсонекс (IHV)**](wlan-profileschema-usemsonex-ihv-element.md)

 

 



