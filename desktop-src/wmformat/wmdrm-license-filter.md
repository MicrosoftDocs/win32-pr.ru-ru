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
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694862"
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

## <a name="remarks"></a>Комментарии

Эта структура используется методом [**ивмдрмлиценсеманажемент:: креателиценсинумератион**](iwmdrmlicensemanagement-createlicenseenumeration.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





