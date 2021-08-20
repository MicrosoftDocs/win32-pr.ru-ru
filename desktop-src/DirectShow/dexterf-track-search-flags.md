---
description: В \_ \_ \_ перечислении флагов поиска декстерф Track указываются граничные условия для поиска объекта на временной шкале.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: Перечисление DEXTERF_TRACK_SEARCH_FLAGS (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 55d7c70dffbf57ae4d9788a10dfea02911a998e21ab5ea8e3d9ad7fffcf91624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952943"
---
# <a name="dexterf_track_search_flags-enumeration"></a>\_ \_ \_ Перечисление флагов поиска декстерф Track

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`DEXTERF_TRACK_SEARCH_FLAGS`Перечисление задает граничные условия для поиска объекта на временной шкале.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**ДЕКСТЕРФное \_ ограничение**
</dt> <dd>

Поиск объекта, охватывающего указанное время.

</dd> <dt>

<span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**ДЕКСТЕРФ \_ \_ в точности**
</dt> <dd>

Поиск объекта, который запускается точно в указанное время.

</dd> <dt>

<span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**Пересылка ДЕКСТЕРФ \_**
</dt> <dd>

Поиск объекта, запускаемого в указанное время или позже.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эти условия границ приведены в следующей таблице.



| Значение перечисления    | Условие границы                        |
|----------------------|-------------------------------------------|
| ДЕКСТЕРФное \_ ограничение    | <запуска = время > Тиместоп<br/> |
| ДЕКСТЕРФ \_ \_ в точности | Начало = = время                             |
| Пересылка ДЕКСТЕРФ \_    | >запуска = время                          |



 

-   Начало: время начала полученного объекта.
-   Прерывать: время окончания полученного объекта.
-   Время: указанное время поиска.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Кедит. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Иамтимелинетракк:: Жетсркаттиме**](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




