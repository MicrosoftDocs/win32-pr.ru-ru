---
description: Определяет профиль WLAN, используемый собственной службой автонастройки WiFi.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: Схема WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d484215ca53ddcd97dbef4adf4aac17cd8457b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144536"
---
# <a name="wlan_profile-schema"></a>\_Схема профиля WLAN

\_Схема профиля WLAN определяет профиль WLAN, используемый собственной службой автонастройки WiFi.

Служба автонастройки принимает профили беспроводной связи от агента групповая политика, интерфейса сценариев (**netsh**), пользовательского интерфейса или интерфейса USB Flash.

Профиль, полученный от одной из этих систем, сопоставляется со \_ схемой профиля WLAN и хранится в хранилище профилей. Профили можно экспортировать из хранилища профилей с помощью команд netsh или с помощью таких элементов API, как [**вланжетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).

Корневым элементом профиля WLAN является элемент [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) . Каждый профиль будет иметь только один корневой элемент. Элемент **вланпрофиле** находится в пространстве имен `https://www.microsoft.com/networking/WLAN/profile/v1` .

Чтобы просмотреть примеры профилей WLAN, см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).

-   [\_Элементы схемы профиля WLAN](wlan-profileschema-elements.md)
-   [\_Простые типы схемы профиля WLAN](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Команды Netsh для беспроводной локальной сети (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))
</dt> </dl>

 

 
