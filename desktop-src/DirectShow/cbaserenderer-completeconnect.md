---
description: Метод Комплетеконнект завершает подключение входного контакта к другому ПИН-коду.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Кбасерендерер. Комплетеконнект, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 833e19a6e7b100aac5322a54455c04c263569e33b3422d5957e5eeee15bbd283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157845"
---
# <a name="cbaserenderercompleteconnect-method"></a>Кбасерендерер. Комплетеконнект, метод

`CompleteConnect`Метод завершает подключение входного контакта к другому ПИН-коду.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прецеивепин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) выходного контакта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Входной ПИН-код фильтра вызывает этот метод из собственного `CompleteConnect` метода, который вызывается для завершения соединения с ПИН-кодом. (Дополнительные сведения см. в разделе [**кбасепин:: комплетеконнект**](cbasepin-completeconnect.md).) Фильтр вызывает метод [**кбасерендерер:: сетрепаинтстатус**](cbaserenderer-setrepaintstatus.md) , чтобы включить события [**\_ перерисовки EC**](ec-repaint.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




