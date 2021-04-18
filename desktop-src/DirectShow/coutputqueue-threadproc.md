---
description: Метод Среадпрок извлекает образцы из очереди и доставляет их во входной ПИН-код.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Каутпуткуеуе. Среадпрок, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665145"
---
# <a name="coutputqueuethreadproc-method"></a>Каутпуткуеуе. Среадпрок, метод

`ThreadProc`Метод извлекает образцы из очереди и доставляет их во входной ПИН-код.

## <a name="syntax"></a>Синтаксис


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль.

## <a name="remarks"></a>Комментарии

Метод [**каутпуткуеуе:: инитиалсреадпрок**](coutputqueue-initialthreadproc.md) вызывает этот метод, который реализует главный цикл потока. В цикле метод выполняет следующие действия:

1.  Извлекает пример для очереди.
2.  Если пример представляет собой управляющее сообщение, то поток выполняет действие элемента управления. В противном случае он помещает пример в массив [**каутпуткуеуе:: m \_ ппсамплес**](coutputqueue-m-ppsamples.md) .
3.  Если массив заполнен (или если [**каутпуткуеуе:: m \_ Ббатчексакт**](coutputqueue-m-bbatchexact.md) имеет **значение false**), поток вызывает метод [**имеминпутпин:: рецеивемултипле**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) для доставки образцов.
4.  Если ни один из образцов не поставлен в очередь, поток ожидает семафор [**\_ хсем каутпуткуеуе:: m**](coutputqueue-m-hsem.md) .

Поток завершается, когда переменная члена [**каутпуткуеуе:: m \_ Бтерминате**](coutputqueue-m-bterminate.md) принимает **значение true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Аутпутк. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




