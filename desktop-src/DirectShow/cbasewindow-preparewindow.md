---
description: Метод Препаревиндов создает окно.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Кбасевиндов. Препаревиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657954"
---
# <a name="cbasewindowpreparewindow-method"></a>Кбасевиндов. Препаревиндов, метод

`PrepareWindow`Метод создает окно.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                            | Описание         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/> |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Ошибка.<br/> |



 

## <a name="remarks"></a>Комментарии

Вызовите этот метод после создания объекта. Этот метод выполняет некоторый первоначальный бухгалтерский вызов, а затем вызывает метод [**кбасевиндов::D окреатевиндов**](cbasewindow-docreatewindow.md) для создания окна.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




