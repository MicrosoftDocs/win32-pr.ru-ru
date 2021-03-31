---
title: Код уведомления EN_PROTECTED (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что пользователь предпринимает действие, которое изменит защищенный диапазон текста. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- EN_PROTECTED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490869"
---
# <a name="en_protected-notification-code"></a>\_Код уведомления, защищенного коротким кодом

Сообщает родительскому окну элемента управления Rich Edit, что пользователь предпринимает действие, которое изменит защищенный диапазон текста. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Структура [**енпротектед**](/windows/desktop/api/Richedit/ns-richedit-enprotected) , содержащая сведения о сообщении, вызвавшем код уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль, чтобы разрешить операцию.

Чтобы предотвратить операцию, возвращается ненулевое значение.

## <a name="remarks"></a>Комментарии

Если возвращается ноль и члены **MSG**, **wParam** и **lParam** структуры [**енпротектед**](/windows/desktop/api/Richedit/ns-richedit-enprotected) изменяются, элемент управления обрабатывает измененное сообщение, а не исходное сообщение.

Чтобы получить \_ коды уведомлений, защищенные с помощью короткого стандарта, укажите [**енм, \_ защищенный**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

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

[**енпротектед**](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[**\_уведомление WM**](wm-notify.md)
</dt> </dl>

 

 





