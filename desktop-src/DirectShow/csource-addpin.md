---
description: Метод Аддпин добавляет новый выходной ПИН-код в фильтр.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: Метод Ксаурце. Аддпин (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665140"
---
# <a name="csourceaddpin-method"></a>Ксаурце. Аддпин, метод

`AddPin`Метод добавляет новый выходной ПИН-код в фильтр.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстреам* 
</dt> <dd>

Указатель на объект [**ксаурцестреам**](csourcestream.md) , который реализует ПИН-код.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                   | Описание                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти<br/> |



 

## <a name="remarks"></a>Комментарии

При создании нового ПИН-кода, производного от **ксаурцестреам**, конструктор **ксаурцестреам** автоматически вызывает этот метод для добавления выходного контакта в фильтр.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурце**](csource.md)
</dt> </dl>

 

 




