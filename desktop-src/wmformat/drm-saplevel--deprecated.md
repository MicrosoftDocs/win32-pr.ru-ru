---
title: DRM_SAPLEVEL (не рекомендуется)
description: Указывает уровень защищенного звукового пути (SAP), поддерживаемый приложением.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (не рекомендуется) формат Windows Media
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80b43cfcf0c89283237f8ff2d3e4f8612050296d7462f54890c3efa908fa9be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930894"
---
# <a name="drm_saplevel-deprecated"></a>DRM \_ саплевел (не рекомендуется)

\[**DRM \_ саплевел** больше не доступен для использования в Windows Vista. Вместо этого используйте звук защищенного пользовательского режима (PUMA) в библиотеке Media Foundation. \]

Свойство **DRM \_ саплевел** указывает уровень защищенного звукового пути (SAP), поддерживаемого приложением.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмдрм \_ саплевел

## <a name="data-type"></a>Тип данных

**\_Строка типа \_ ВМТ**

## <a name="remarks"></a>Remarks

Это свойство доступно только для записи и устанавливается путем вызова [**ивмдрмреадер:: сетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty). Значение представляет собой строковое представление уровня SAP с расширенными символами, например L "200". Текущие поддерживаемые значения: 200 и 300.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|--------------------------------|
| Окончание поддержки клиента<br/> | Windows XP<br/>          |
| Поддержка конца сервера<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Свойства DRM**](drm-properties.md)
</dt> </dl>

 

 





