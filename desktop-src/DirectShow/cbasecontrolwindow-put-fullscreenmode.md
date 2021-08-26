---
description: Метод размещения \_ фуллскринмоде задает полноэкранный режим модуля подготовки отчетов.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: Метод CBaseControlWindow.put_FullScreenMode (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e7aa121ce78198fe6b2ca0b88109183665f0cd93dd95294a848a2b2d0c03548
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983684"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a>Кбасеконтролвиндов. размещение \_ метода фуллскринмоде

`put_FullScreenMode`Метод задает полноэкранный режим для модуля подготовки отчетов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фуллскринмоде* 
</dt> <dd>

Полноэкранный режим для применения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Текущая реализация возвращает E \_ нотимпл.

## <a name="remarks"></a>Remarks

Модуль подготовки видео, реализующий полноэкранный режим, должен переопределять эту функцию-член и реализовывать все поддерживаемые им режимы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




