---
description: Метод размещения \_ WindowStyle задает стандартные стили окна.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: Метод CBaseControlWindow.put_WindowStyle (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658062"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a>Кбасеконтролвиндов. размещение \_ метода WindowStyle

`put_WindowStyle`Метод задает стандартные стили окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*WindowStyle* 
</dt> <dd>

Новые стили окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Следите за изменениями стилей окна. В большинстве случаев приложение должно получить текущий стиль, а затем добавить или удалить недопустимые биты. Эта процедура позволяет не менять различные внутренние стили окна, используемые Windows.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




