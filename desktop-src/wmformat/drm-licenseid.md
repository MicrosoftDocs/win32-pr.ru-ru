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
ms.openlocfilehash: d9dea32903de18dd1bde8f132b8acf993d3eba2deb0d45c814f0572ce8591ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930954"
---
# <a name="drm_licenseid"></a>\_ЛИЦЕНСЕИД DRM

Свойство **\_ лиценсеид DRM** содержит строку, полученную из лицензии, связанной с текущим открытым файлом, который однозначно идентифицирует эту лицензию.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмдрм \_ лиценсеид

## <a name="data-type"></a>Тип данных

**\_Строка типа \_ ВМТ**

## <a name="remarks"></a>Remarks

Этот атрибут имеется только в содержимом DRM версии 7. Его можно задать с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , и его можно получить при помощи [**Ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

Идентификатор лицензии хранится в лицензии, а не в файле ASF. Каждая отдельная лицензия имеет уникальный идентификатор, который назначается генератором лицензий во время создания лицензии. Например, если вы получаете две лицензии для одного и того же содержимого, у каждого из них будет свой атрибут Лиценсеид. Как правило, приложениям не нужно получать это значение.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




