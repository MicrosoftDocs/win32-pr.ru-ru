---
description: Метод «вставить \_ Автоотображение» задает флаг состояния «Автоотображение».
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: Метод CBaseControlWindow.put_AutoShow (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8e24686baa3cf1f2ad570394acd7a290ac374043b8564566dc1e89668d3f6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017282"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a>Кбасеконтролвиндов. размещение \_ метода автоотображения

`put_AutoShow`Метод задает флаг состояния автоотображения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Автоотображение* 
</dt> <dd>

Логический флаг автоматизации (0 — отключено, 1 — включено).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Это свойство упрощает доступ к окнам для приложений. Если задано значение 1 (включено), то окно, которое обычно скрыто после подключения фильтра, будет отображаться автоматически при приостановке или запуске фильтра. Однако окно не должно быть скрыто при остановке фильтра. Если задано значение 0 (выключено), окно становится видимым только тогда, когда приложение вызывает [**кбасеконтролвиндов::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) или [**кбасеконтролвиндов::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) с соответствующими параметрами.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




