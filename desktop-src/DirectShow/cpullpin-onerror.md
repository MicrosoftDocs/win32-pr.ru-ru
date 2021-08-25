---
description: Метод OnError вызывается при возникновении ошибки во время потоковой передачи. Производный класс должен реализовывать этот метод.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: Метод Кпуллпин. OnError (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0d9873e2d327c424b2cd1ffda7112676f53399a63d2a9ca92dca1f50a02f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908884"
---
# <a name="cpullpinonerror-method"></a>Кпуллпин. OnError, метод

`OnError`Метод вызывается при возникновении ошибки во время потоковой передачи. Производный класс должен реализовывать этот метод.

## <a name="syntax"></a>Синтаксис


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ч* 
</dt> <dd>

Указывает значение **HRESULT** , возвращаемое методом, который завершился ошибкой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Объект вызывает этот метод каждый раз, когда возникает ошибка, которая останавливает поток извлечения данных. Фильтр может использовать этот метод для корректного устранения ошибок потоковой передачи. в большинстве случаев ошибка возвращается из вышестоящего фильтра, поэтому вышестоящей фильтр отвечает за передачу отчета в фильтр Graph Manager. Если ошибка возникает в методе [**кпуллпин:: Receive**](cpullpin-receive.md) , то фильтр должен отправить событие [**EC \_ еррораборт**](ec-errorabort.md) . (См. [**имедиаевентсинк:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Пуллпин. h</dt> </dl>                                                                                                       |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпуллпин**](cpullpin.md)
</dt> </dl>

 

 




