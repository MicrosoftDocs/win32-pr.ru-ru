---
title: Структура WMDRM_LICENSE_FILTER (Вмдрмсдк. h)
description: '\_ \_ Структура фильтра лицензий WMDRM определяет параметры фильтрации для использования при создании перечисления лицензий.'
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- Формат WMDRM_LICENSE_FILTER структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dc65758c7c5a25d31dd9fdb2d0fcd5cfa65debfff3defab4b88280a5ff3b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698142"
---
# <a name="wmdrm_license_filter-structure"></a>\_ \_ Структура фильтра лицензий WMDRM

Структура **\_ \_ фильтра лицензий WMDRM** определяет параметры фильтрации для использования при создании перечисления лицензий.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**двверсион**
</dt> <dd>

Указывает минимальный номер версии для возвращенных лицензий.

</dd> <dt>

**бстркид**
</dt> <dd>

Указывает идентификатор ключа для фильтрации лицензий. В перечисление будут включаться только лицензии с указанным ИДЕНТИФИКАТОРом ключа.

</dd> <dt>

**бстрригхтс**
</dt> <dd>

Задает набор прав для фильтрации лицензий. В перечисление будут включаться только лицензии, предоставляющие все указанные права.

</dd> <dt>

**бстралловедсаурцеидс**
</dt> <dd>

Указывает источники защищенного содержимого для включения в Поиск лицензий.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура используется методом [**ивмдрмлиценсеманажемент:: креателиценсинумератион**](iwmdrmlicensemanagement-createlicenseenumeration.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





