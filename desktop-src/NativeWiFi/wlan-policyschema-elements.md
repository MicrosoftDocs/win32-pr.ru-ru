---
description: Профиль политики беспроводной локальной сети Wi-Fi (WLAN) состоит из следующих элементов схемы.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: WLAN_policy элементы схемы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541042"
---
# <a name="wlan_policy-schema-elements"></a>\_Элементы схемы политики WLAN

Профиль политики беспроводной локальной сети Wi-Fi (WLAN) состоит из следующих элементов схемы. Все именованные элементы находятся в пространстве имен `https://www.microsoft.com/networking/WLAN/policy/v1` .

В следующем списке показаны определенные элементы в порядке, в котором элементы отображаются в профиле. Упорядочение элементов выполняется принудительно. Не все элементы находятся в каждом профиле, поскольку некоторые элементы являются необязательными.

В этом списке не отображаются все возможные элементы, которые могут отображаться в профиле, так как элементы можно добавлять в **xs: любые** точки вставки.

-   [**вланполици**](wlan-policyschema-wlanpolicy-element.md)
    -   [**имя (Вланполици)**](wlan-policyschema-name-wlanpolicy-element.md)
    -   [**Описание (Вланполици)**](wlan-policyschema-description-wlanpolicy-element.md)
    -   [**Глобалфлагс (Вланполици)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [**Енаблеаутоконфиг (Глобалфлагс)**](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [**Шовдениеднетворк (Глобалфлагс)**](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [**Алловеверйонетокреатеаллусерпрофилес (Глобалфлагс)**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [**Нетворкфилтер (Вланполици)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [**Разрешенных (Нетворкфилтер)**](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [**сеть (разрешенных)**](wlan-policyschema-network-allowlist-element.md)
                -   [**networkName (Нетворкитемтипе)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**Нетворктипе (Нетворкитемтипе)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**Списка блокировки (Нетворкфилтер)**](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [**сеть (списка блокировки)**](wlan-policyschema-network-blocklist-element.md)
                -   [**networkName (Нетворкитемтипе)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**Нетворктипе (Нетворкитемтипе)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**Деняллибсс (Нетворкфилтер)**](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [**Деняллесс (Нетворкфилтер)**](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [**Профилелист (Вланполици)**](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



