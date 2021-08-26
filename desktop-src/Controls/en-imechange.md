---
title: Код уведомления EN_IMECHANGE (RichEdit. h)
description: Сообщает родителю элемента управления Rich Edit, что изменилось состояние преобразования редактора IME.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4974c4126606b8ed95ffa645778469b6fc897488533b81498347de1c1995e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047684"
---
# <a name="en_imechange-notification-code"></a>\_Код уведомления EN имечанже

Сообщает родителю элемента управления Rich Edit, что изменилось состояние преобразования редактора IME. Этот код уведомления доступен *только* для азиатских языковых версий операционной системы. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в [**виде \_ командного сообщения WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления Rich Edit. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.

</dd> <dt>

*lParam* 
</dt> <dd>

Обработчик для элемента управления Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот код уведомления возвращает ноль.

## <a name="remarks"></a>Remarks

Чтобы получить \_ коды уведомлений EN имечанже, укажите [**енм \_ имечанже**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

> [!Note]  
> Этот код уведомления поддерживается только в азиатской версии Rich Edit 1,0. Он не поддерживается в более поздних версиях. Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Другие ресурсы**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

