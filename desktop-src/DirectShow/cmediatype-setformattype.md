---
description: Метод Сетформаттипе задает тип формата.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Кмедиатипе. Сетформаттипе, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6a0582a882ffe40a9bd889ff48e70a52a4048bad57e01077263e607f13d9898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954423"
---
# <a name="cmediatypesetformattype-method"></a>Кмедиатипе. Сетформаттипе, метод

Метод Сетформаттипе задает тип формата.

## <a name="syntax"></a>Синтаксис


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пформаттипе* 
</dt> <dd>

Указатель на **идентификатор GUID** , указывающий тип формата.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод задает элемент **форматтипе** . Тип формата определяет макет блока форматирования. Например, если тип формата — FORMAT \_ видеоинфо, блок формата должен содержать структуру **видеоинфохеадер** . Чтобы задать блок формата, вызовите метод [**кмедиатипе:: сетформат**](cmediatype-setformat.md) . Вызывающий объект отвечает за обеспечение соответствия блока формата типу формата.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 


``
