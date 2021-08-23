---
description: Кмедиапоситион. GetIDsOfNames, метод GetIDsOfNames сопоставляет набор имен с соответствующим набором идентификаторов DISPID.
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Кмедиапоситион. GetIDsOfNames, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eebd32638afdf957024f54f6a601e95bae274dc4ab9a8265e9a618d635a23530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634804"
---
# <a name="cmediapositiongetidsofnames-method"></a>Кмедиапоситион. GetIDsOfNames, метод

`GetIDsOfNames`Метод сопоставляет набор имен с соответствующим набором идентификаторов DISPID.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*riid* 
</dt> <dd>

Зарезервировано. Используйте IID \_ null.

</dd> <dt>

*ргсзнамес* 
</dt> <dd>

Адрес массива строк расширенных символов, содержащих имена для сопоставления.

</dd> <dt>

*Записи CNAME* 
</dt> <dd>

Размер массива, заданного параметром *ргсзнамес* .

</dd> <dt>

*lcid* 
</dt> <dd>

Контекст языкового стандарта, в котором следует интерпретировать имена. Может иметь **значение NULL**.

</dd> <dt>

*ргдиспид* 
</dt> <dd>

Указатель на массив, который получает идентификаторы DISPID. Каждый элемент получает идентификатор, соответствующий одному из имен, переданных в параметре *ргсзнамес* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                                         | Описание                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                | Успешно.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Недостаточно памяти.<br/>                     |
| <dl> <dt>**\_выункновннаме E \_**</dt> </dl> | Одно или несколько имен не были известны.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиапоситион**](cmediaposition.md)
</dt> </dl>

 

 




