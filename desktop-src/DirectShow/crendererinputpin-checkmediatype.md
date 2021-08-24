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
ms.openlocfilehash: d47f69c72ab2dab366b42d6dc80100508c0b1608d25abdcbfb1bb49c4177a278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687704"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Крендереринпутпин**](crendererinputpin.md)
</dt> </dl>

 

 




