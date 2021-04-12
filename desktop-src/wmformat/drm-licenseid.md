---
title: DRM_LicenseID
description: '\_Свойство ЛИЦЕНСЕИД DRM содержит строку, полученную из лицензии, связанной с текущим открытым файлом, который однозначно идентифицирует эту лицензию.'
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID формат Windows Media
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336423"
---
# <a name="drm_licenseid"></a>\_ЛИЦЕНСЕИД DRM

Свойство **\_ лиценсеид DRM** содержит строку, полученную из лицензии, связанной с текущим открытым файлом, который однозначно идентифицирует эту лицензию.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмдрм \_ лиценсеид

## <a name="data-type"></a>Тип данных

**\_Строка типа \_ ВМТ**

## <a name="remarks"></a>Комментарии

Этот атрибут имеется только в содержимом DRM версии 7. Его можно задать с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , и его можно получить при помощи [**Ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

Идентификатор лицензии хранится в лицензии, а не в файле ASF. Каждая отдельная лицензия имеет уникальный идентификатор, который назначается генератором лицензий во время создания лицензии. Например, если вы получаете две лицензии для одного и того же содержимого, у каждого из них будет свой атрибут Лиценсеид. Как правило, приложениям не нужно получать это значение.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




