---
description: 'Метод Cancel отменяет ранее поставленный в очередь запрос Кдеферредкомманд:: Invoke.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Метод Кдеферредкомманд. Cancel (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa7e957fe97e06c6fb14fe3a9048048e351ac1baf4ff8f4dae25b3cf5863776e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043714"
---
# <a name="cdeferredcommandcancel-method"></a>Кдеферредкомманд. Cancel, метод

`Cancel`Метод отменяет ранее поставленный в очередь запрос [**кдеферредкомманд:: Invoke**](cdeferredcommand-invoke.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает VFW \_ E \_ уже \_ отменено, если **m \_ пкуеуе** имеет **значение NULL**. Возвращает **значение HRESULT** из [**ккмдкуеуе:: Remove**](ccmdqueue-remove.md) , если вызов создает ошибку. \_При успешном выполнении возвращает значение ОК.

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**идеферредкомманд:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдеферредкомманд**](cdeferredcommand.md)
</dt> </dl>

 

 




