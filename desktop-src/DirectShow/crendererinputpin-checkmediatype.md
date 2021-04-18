---
description: 'Метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя. Этот метод переопределяет метод Кбасепин:: Чеккмедиатипе.'
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: Крендереринпутпин. Чеккмедиатипе, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d3229d1431e45a6177c454f94bf9873aaceaca5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657381"
---
# <a name="crendererinputpincheckmediatype-method"></a>Крендереринпутпин. Чеккмедиатипе, метод

`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя. Этот метод переопределяет метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*состоит* 
</dt> <dd>

Указатель на объект типа мультимедиа, который содержит предложенный тип мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Крендереринпутпин**](crendererinputpin.md)
</dt> </dl>

 

 




