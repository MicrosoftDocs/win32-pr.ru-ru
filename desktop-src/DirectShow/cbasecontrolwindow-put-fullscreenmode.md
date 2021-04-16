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
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657348"
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

## <a name="remarks"></a>Комментарии

Модуль подготовки видео, реализующий полноэкранный режим, должен переопределять эту функцию-член и реализовывать все поддерживаемые им режимы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




