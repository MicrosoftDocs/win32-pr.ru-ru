---
description: Метод размещения \_ виндовстиликс задает расширенные стили окна.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: Метод CBaseControlWindow.put_WindowStyleEx (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658061"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a>Кбасеконтролвиндов. размещение \_ метода виндовстиликс

`put_WindowStyleEx`Метод задает расширенные стили окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Виндовстиликс* \[ окне\]
</dt> <dd>

Значение, указывающее стиль окна элемента управления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение "ошибка".

## <a name="remarks"></a>Комментарии

Этот метод использует расширенные стили окна. Полный список расширенных стилей окон см. в разделе функция Microsoft Win32 **CreateWindowEx** . Чтобы изменить стиль окна, извлеките текущий стиль окна, а затем добавьте или удалите необходимые битовые поля.

Не используйте следующие стили окна, так как они не проверены.

-   протокол WS \_ отключен
-   \_HSCROLL WS
-   \_значок WS
-   \_развернуть WS
-   WS \_ Minimize
-   \_VSCROLL WS

С некоторыми исключениями (отмеченными здесь) допустимые флаги совпадают с допустимыми для функции Win32 **CreateWindow** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




