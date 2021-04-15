---
description: Метод OnDeactivate вызывается при уничтожении окна диалогового окна.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: Метод Кбасепропертипаже. OnDeactivate (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669361"
---
# <a name="cbasepropertypageondeactivate-method"></a>Кбасепропертипаже. OnDeactivate, метод

`OnDeactivate`Метод вызывается при уничтожении окна диалогового окна.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Реализация базового класса возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Метод [**кбасепропертипаже::D еактивате**](cbasepropertypage-deactivate.md) вызывает `OnDeactivate` метод. Переопределите, `OnDeactivate` чтобы освободить все ресурсы, полученные производным классом в методе [**кбасепропертипаже:: OnActivate**](cbasepropertypage-onactivate.md) , или для выполнения других задач по мере необходимости.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кпроп. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




