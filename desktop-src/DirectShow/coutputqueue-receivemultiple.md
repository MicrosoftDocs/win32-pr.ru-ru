---
description: Метод Рецеивемултипле доставляет пакет образцов мультимедиа во входной ПИН-код.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Каутпуткуеуе. Рецеивемултипле, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674880"
---
# <a name="coutputqueuereceivemultiple-method"></a>Каутпуткуеуе. Рецеивемултипле, метод

`ReceiveMultiple`Метод доставляет пакет образцов мультимедиа во входной ПИН-код.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппсамплес* 
</dt> <dd>

Адрес указателя на массив выборок.

</dd> <dt>

*нсамплес* 
</dt> <dd>

Число выборок в массиве.

</dd> <dt>

*нсамплеспроцессед* 
</dt> <dd>

Указатель на переменную, которая получает количество успешно доставленных выборок.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                             | Описание                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Перед обработкой этого примера получено уведомление о завершении потока.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>                                                           |



 

## <a name="remarks"></a>Комментарии

Если объект использует поток, этот метод помещает все образцы, переданные в массив, в очередь. В противном случае метод вызывает метод [**имеминпутпин:: рецеивемултипле**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) для входного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Аутпутк. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




