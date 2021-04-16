---
description: Метод GetIDsOfNames сопоставляет набор имен с соответствующим набором идентификаторов DISPID.
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
ms.openlocfilehash: dc2c7eee4304bb32ac1af2759bc2f094aca1d592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679830"
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
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиапоситион**](cmediaposition.md)
</dt> </dl>

 

 




