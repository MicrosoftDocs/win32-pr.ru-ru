---
description: Метод Онрецеивемессаже обрабатывает сообщения окна.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Кбасевиндов. Онрецеивемессаже, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a5dbfb84edef1f5257cfda8cae08d27b219909f47a7d88fd29580ae12e48b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657967"
---
# <a name="cbasewindowonreceivemessage-method"></a>Кбасевиндов. Онрецеивемессаже, метод

`OnReceiveMessage`Метод обрабатывает сообщения окна.

## <a name="syntax"></a>Синтаксис


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Дескриптор для окна.

</dd> <dt>

*Uiacp* 
</dt> <dd>

Идентификатор сообщения.

</dd> <dt>

*wParam* 
</dt> <dd>

Первый параметр сообщения.

</dd> <dt>

*lParam* 
</dt> <dd>

Второй параметр сообщения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0, если сообщение было обработано, или значение 1, если сообщение не было обработано.

## <a name="remarks"></a>Remarks

Базовый класс обрабатывает следующие сообщения:

-   \_Закрыть WM
-   \_Перемещение WM
-   WM \_ палеттечанжед
-   WM \_ куериневпалетте
-   \_Размер WM
-   WM \_ сисколорчанже

Производный класс может переопределить этот метод для управления другими сообщениями. Производный класс должен вызвать метод базового класса, чтобы обрабатывать все сообщения, которые пропускаются производным классом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




