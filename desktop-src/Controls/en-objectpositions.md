---
title: Код уведомления EN_OBJECTPOSITIONS (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, когда элемент управления считывает объекты. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- EN_OBJECTPOSITIONS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892030"
---
# <a name="en_objectpositions-notification-code"></a>\_Код уведомления EN обжектпоситионс

Сообщает родительскому окну элемента управления Rich Edit, когда элемент управления считывает объекты. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Структура [**обжектпоситионс**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль, чтобы продолжить операцию **чтения** .

Для завершения операции **чтения** возвращается ненулевое значение.

## <a name="remarks"></a>Комментарии

Чтобы получить \_ код уведомления EN обжектпоситионс, укажите флаг [**енм \_ обжектпоситионс**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**обжектпоситионс**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[**\_уведомление WM**](wm-notify.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

