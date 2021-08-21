---
description: 'Метод Ваитфоррецеиветокомплете ожидает завершения метода Кбасерендерер:: Receive.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Кбасерендерер. Ваитфоррецеиветокомплете, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1f63efa53cc8e8829aba825e831f95595b16faf97bdf29777918c599aadade1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016792"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a>Кбасерендерер. Ваитфоррецеиветокомплете, метод

`WaitForReceiveToComplete`Метод ожидает завершения метода [**кбасерендерер:: Receive**](cbaserenderer-receive.md) .

## <a name="syntax"></a>Синтаксис


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Методы [**кбасерендерер:: останавливают**](cbaserenderer-stop.md) и [**Кбасерендерер:: бегинфлуш**](cbaserenderer-beginflush.md) вызывают этот метод, чтобы синхронизировать изменение состояния с методом **Receive** .

В частности, этот метод отправляет сообщения, пока он ожидает, пока флаг [**кбасерендерер:: m \_ бинрецеиве**](cbaserenderer-m-binreceive.md) не станет равным **false**. Флаг принимает **значение true** в методе [**Кбасерендерер::P репаререцеиве**](cbaserenderer-preparereceive.md) и возвращается в **значение false** после того, как метод **Receive** вызовет метод [**кбасерендерер::P репаререндер**](cbaserenderer-preparerender.md) . Производный класс может использовать **препаререндер** для установки палитры. Ожидание завершения **препаререндер** гарантирует, что сообщения о смене палитры будут отправлены, прежде чем произойдет изменение состояния. Это позволяет избежать возможной взаимоблокировки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




