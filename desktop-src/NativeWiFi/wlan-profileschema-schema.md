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
ms.openlocfilehash: 91bd1a5d04bcc265f2b9ba7c0533bb0beb4e2c861f01c8b5e286d59f8b4bcfc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619071"
---
# <a name="wlan_profile-schema"></a>\_Схема профиля WLAN

\_Схема профиля WLAN определяет профиль WLAN, используемый собственной службой автонастройки WiFi.

Служба автонастройки принимает профили беспроводной связи от агента групповая политика, интерфейса сценариев (**netsh**), пользовательского интерфейса или интерфейса USB Flash.

Профиль, полученный от одной из этих систем, сопоставляется со \_ схемой профиля WLAN и хранится в хранилище профилей. Профили можно экспортировать из хранилища профилей с помощью команд netsh или с помощью таких элементов API, как [**вланжетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).

Корневым элементом профиля WLAN является элемент [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) . Каждый профиль будет иметь только один корневой элемент. Элемент **вланпрофиле** находится в пространстве имен `https://www.microsoft.com/networking/WLAN/profile/v1` .

Чтобы просмотреть примеры профилей WLAN, см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).

-   [\_Элементы схемы профиля WLAN](wlan-profileschema-elements.md)
-   [\_Простые типы схемы профиля WLAN](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Команды Netsh для беспроводной локальной сети (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))
</dt> </dl>

 

 
