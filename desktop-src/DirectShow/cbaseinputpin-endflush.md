---
description: 'Метод Ендфлуш завершает операцию очистки. Реализует метод Ипин:: Ендфлуш.'
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Кбасеинпутпин. Ендфлуш, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fba4c82679ebe96827cd45c9045080fb354cdab25eb562523869e97d533c5f2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056354"
---
# <a name="cbaseinputpinendflush-method"></a>Кбасеинпутпин. Ендфлуш, метод

`EndFlush`Метод завершает операцию очистки. Реализует метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод задает для флага [**кбасеинпутпин:: m \_ Бфлушинг**](cbaseinputpin-m-bflushing.md) **значение true**, что позволяет методу [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) принимать выборки.

Производный класс должен переопределить этот метод и выполнить следующие действия:

1.  Освободите все буферизованные данные и дождитесь отмены всех примеров в очереди.
2.  Удалите все ожидающие уведомления [**EC о \_ завершении**](ec-complete.md) .
3.  Вызовите метод базового класса.
4.  Вызовите [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) на нижестоящих входных контактах. Если ПИН-код еще не доставил никаких образцов мультимедиа, этот шаг можно пропустить. Если выходные контакты являются производными от класса [**кбасеаутпутпин**](cbaseoutputpin.md) , можно вызвать метод [**Кбасеаутпутпин::D еливерендфлуш**](cbaseoutputpin-deliverendflush.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеинпутпин**](cbaseinputpin.md)
</dt> </dl>

 

 




