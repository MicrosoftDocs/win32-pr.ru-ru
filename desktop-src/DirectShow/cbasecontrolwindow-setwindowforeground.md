---
description: Метод Сетвиндовфореграунд перемещает окно видео на передний план и при необходимости дает ему фокус.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Кбасеконтролвиндов. Сетвиндовфореграунд, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 87a6768c8864de45d50dc630773b756dfad43759adbf4b09ed8070febd37f4d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635474"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a>Кбасеконтролвиндов. Сетвиндовфореграунд, метод

`SetWindowForeground`Метод перемещает окно видео на передний план и при необходимости дает ему фокус.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Фокус* 
</dt> <dd>

Значение, указывающее, будет ли окно видео получать фокус. Значение 1 задает фокус окна, а 0 — нет.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений.



| Код возврата                                                                                           | Описание                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NOERROR**</dt> </dl>                | Метод выполнен успешно.<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Фокус не равен 1 или 0.<br/>                                   |
| <dl> <dt>**VFW \_ E \_ не \_ подключен**</dt> </dl> | Текущий фильтр не подключен к полному графу фильтра.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




