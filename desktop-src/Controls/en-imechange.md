---
title: Код уведомления EN_IMECHANGE (RichEdit. h)
description: Сообщает родителю элемента управления Rich Edit, что изменилось состояние преобразования редактора IME.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE кода уведомления элементы управления Windows
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
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071657"
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

## <a name="remarks"></a>Комментарии

Чтобы получить \_ коды уведомлений EN имечанже, укажите [**енм \_ имечанже**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

> [!Note]  
> Этот код уведомления поддерживается только в азиатской версии Rich Edit 1,0. Он не поддерживается в более поздних версиях. Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Другие ресурсы**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

