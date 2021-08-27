---
title: Перечисление DRM_ATTR_DATATYPE (Вмдрмсдк. h)
description: '\_ \_ Перечисление DATATYPE attr DRM определяет типы данных, используемые для атрибутов и свойств DRM.'
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- Формат Windows Media DRM_ATTR_DATATYPE перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_ATTR_DATATYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f55c3d218aa86c33f699d4cb762e752a0bf4e1029e8ca42eee797aaf8ac721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110534"
---
# <a name="drm_attr_datatype-enumeration"></a>\_ \_ Перечисление DATATYPE атрибутов DRM

Перечисление **\_ \_ DATATYPE attr DRM** определяет типы данных, используемые для атрибутов и свойств DRM.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum DRM_ATTR_DATATYPE { 
  DRM_TYPE_DWORD   = 0,
  DRM_TYPE_STRING  = 1,
  DRM_TYPE_BINARY  = 2,
  DRM_TYPE_BOOL    = 3,
  DRM_TYPE_QWORD   = 4,
  DRM_TYPE_WORD    = 5,
  DRM_TYPE_GUID    = 6
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**\_тип DRM типа \_ DWORD**
</dt> <dd>

Свойство является 4-байтовым значением **типа DWORD** .

</dd> <dt>

<span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**\_Строка типа \_ DRM**
</dt> <dd>

Свойство является строкой в Юникоде, завершающейся нулем.

</dd> <dt>

<span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**\_ \_ двоичный тип DRM**
</dt> <dd>

Свойство представляет собой массив байтов.

</dd> <dt>

<span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**\_тип логического типа DRM \_**
</dt> <dd>

Свойство является 4-байтовым логическим значением.

</dd> <dt>

<span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**Тип управления цифровыми правами ( \_ \_ QWORD)**
</dt> <dd>

Свойство является 8-байтовым значением **QWORD** .

</dd> <dt>

<span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**\_слово типа \_ DRM**
</dt> <dd>

Свойство является 2-байтовым значением **слова** .

</dd> <dt>

<span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**\_GUID типа \_ DRM**
</dt> <dd>

Свойство является 128-битным (6-байтовым) значением GUID.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Типы перечислений**](drm-enumeration-types.md)
</dt> </dl>

 

 





