---
description: '\_Перечисление основных типов временной шкалы \_ задает основной тип объекта.'
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: Перечисление TIMELINE_MAJOR_TYPE (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: b18088a9d01b263c80a4ff941a6b7720043da708eaeaebf4f79a2084d1ed258f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501724"
---
# <a name="timeline_major_type-enumeration"></a>\_Перечисление основных типов временной шкалы \_

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`TIMELINE_MAJOR_TYPE`Перечисление указывает основной тип объекта.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**\_ \_ составной основной тип временной шкалы \_**
</dt> <dd>

Составной объект. Содержит одну или несколько дорожек.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**\_Основная \_ запись типа \_ временной шкалы**
</dt> <dd>

Объект Track. Содержит один или несколько источников.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**\_источник основных \_ типов временной шкалы \_**
</dt> <dd>

Исходный объект. Содержит ссылку на источник мультимедиа.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**\_Переход на основной \_ тип \_ временной шкалы**
</dt> <dd>

Объект перехода. Определяет переход между составными элементами, дорожками или источниками.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_результат основного \_ типа временной шкалы \_**
</dt> <dd>

Объект Effect. Определяет однонаправленный результат, применяемый к составному, отслеживающему или исходному объекту.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**\_Основная \_ группа типов \_ временной шкалы**
</dt> <dd>

Объект группы. Содержит одну или несколько дорожек заданного типа.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Кедит. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иамтимелине**](iamtimeline.md)
</dt> <dt>

[**Иамтимелинекомп:: Жеткаунтофтипе**](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[**Иамтимелинеобж:: Жеттимелинетипе**](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




