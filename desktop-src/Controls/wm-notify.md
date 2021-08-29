---
title: Сообщение WM_NOTIFY (Winuser. h)
description: Посылается обычным элементом управления в его родительское окно, когда произошло событие или для элемента управления требуются некоторые сведения.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- элементы управления Windows сообщений WM_NOTIFY
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9139f2dab6410eeb2bacbde93b5e163c0591f350626046861426ddc53beab389
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539714"
---
# <a name="wm_notify-message"></a>\_Уведомить сообщение WM

Посылается обычным элементом управления в его родительское окно, когда произошло событие или для элемента управления требуются некоторые сведения.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор общего элемента управления, отправляющего сообщение. Этот идентификатор не обязательно должен быть уникальным. Для обнаружения элемента управления приложение должно использовать элемент **хвндфром** или **идфром** структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) (переданный как параметр *lParam* ).

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую код уведомления и дополнительные сведения. Для некоторых сообщений с уведомлениями этот параметр указывает на большую структуру, в которой структура **NMHDR** является первым элементом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется, за исключением сообщений уведомления, в которых указано иное.

## <a name="remarks"></a>Remarks

Место назначения сообщения должно быть **HWND** родительского элемента управления. Это значение можно получить с помощью функции- [**родителя**](/windows/desktop/api/winuser/nf-winuser-getparent), как показано в следующем примере, где *m \_ контролхвнд* — это **HWND** самого элемента управления.


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



Приложения обрабатывают сообщение в процедуре окна родительского окна, как показано в следующем примере, который обрабатывает сообщение уведомления, отправленное пользовательским элементом управления в предыдущем примере.


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



Некоторые уведомления, которые находятся в API в течение длительного времени, отправляются в виде [**\_ командных сообщений WM**](/windows/desktop/menurc/wm-command) . Дополнительные сведения см. в разделе [Управление сообщениями](control-messages.md).

Если обработчик сообщений находится в процедуре диалогового окна, необходимо использовать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) с DWL \_ мсгресулт, чтобы задать возвращаемое значение.

для Windows Vista и более поздних систем сообщение **WM \_ NOTIFY** не может быть отправлено между процессами.

Многие уведомления доступны в форматах ANSI и Юникод. Окно, отправляющее сообщение **WM \_ Notify** , использует сообщение [**WM \_ нотифиформат**](wm-notifyformat.md) для определения формата, который следует использовать. Дополнительные сведения см. в разделе **WM \_ нотифиформат** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**WM \_ нотифиформат**](wm-notifyformat.md)
</dt> </dl>

 

