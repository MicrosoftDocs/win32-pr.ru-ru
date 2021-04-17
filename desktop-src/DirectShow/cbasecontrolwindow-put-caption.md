---
description: Метод вставить \_ заголовок задает заголовок окна или заголовок.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: Метод CBaseControlWindow.put_Caption (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657349"
---
# <a name="cbasecontrolwindowput_caption-method"></a>Метод Кбасеконтролвиндов. размещение \_ субтитров

`put_Caption`Метод задает заголовок окна или заголовок.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стркаптион* 
</dt> <dd>

Новый заголовок окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Большинство окон верхнего уровня на рабочем столе под управлением Windows имеют заголовок (заголовок), связанный с ними. Это свойство можно запрашивать и задавать с помощью интерфейса [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) . Любой набор заголовков будет виден только в том случае, если для окна \_ применен стиль «заголовок WS». Если это не так, заголовок можно по-прежнему задать (и получить), хотя он не будет виден пользователю.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




