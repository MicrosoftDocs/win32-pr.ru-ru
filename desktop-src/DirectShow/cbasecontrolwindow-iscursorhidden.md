---
description: Метод Искурсорхидден извлекает текущее состояние \_ элемента данных m бкурсорхидден.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Кбасеконтролвиндов. Искурсорхидден, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658109"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a>Кбасеконтролвиндов. Искурсорхидден, метод

`IsCursorHidden`Метод получает текущее состояние элемента данных **m \_ бкурсорхидден** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*курсорхидден* 
</dt> <dd>

Указатель на значение **m \_ бкурсорхидден**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При вызове без параметра возвращает ОАТРУЕ, если курсор скрыт, или ОАФАЛСЕ, если курсор является видимым.

## <a name="remarks"></a>Комментарии

Внутренние объекты должны вызывать эту функцию члена без параметра *курсорхидден* , чтобы избежать блокировки критической секции. Внешние объекты обращаются к этой функции-члену с помощью параметра *курсорхидден* с помощью метода [**Ивидеовиндов:: искурсорхидден**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




