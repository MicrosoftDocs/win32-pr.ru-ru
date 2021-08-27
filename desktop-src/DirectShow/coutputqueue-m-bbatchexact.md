---
description: Флаг, указывающий, доставляет ли объект выборки в точных пакетах.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Элемент Каутпуткуеуе:: m_bBatchExact (Аутпутк. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5859744c3670ccc789ae5d87a619b3b32c3731580d473ff8cc6d775348771f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087254"
---
# <a name="coutputqueuem_bbatchexact-member"></a>Элемент Каутпуткуеуе:: m \_ ббатчексакт

Флаг, указывающий, доставляет ли объект выборки в точных пакетах.

## <a name="syntax"></a>Синтаксис


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a>Remarks

Если значение равно **true**, объект ожидает, пока не будет выполнен полный пакет примеров мультимедиа перед доставкой. В противном случае он доставляет образцы по мере их поступления. Переменная члена [**каутпуткуеуе:: m \_ лбатчсизе**](coutputqueue-m-lbatchsize.md) определяет размер пакета.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>аутпутк. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




