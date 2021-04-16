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
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658058"
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
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




