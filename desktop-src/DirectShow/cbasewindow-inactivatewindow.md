---
description: Метод Инактиватевиндов деактивирует окно. В базовом классе этот метод скрывает окно.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Кбасевиндов. Инактиватевиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1c5e925a3d9b510918636a221d5ad6e1b7da736
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675470"
---
# <a name="cbasewindowinactivatewindow-method"></a>Кбасевиндов. Инактиватевиндов, метод

`InactivateWindow`Метод деактивирует окно. В базовом классе этот метод скрывает окно.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                             | Описание                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>                    |
| <dl> <dt>**S \_ false**</dt> </dl> | Окно уже неактивно.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




