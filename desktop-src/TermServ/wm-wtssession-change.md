---
title: Сообщение WM_WTSSESSION_CHANGE (Winuser. h)
description: Уведомляет приложения об изменениях в состоянии сеанса.
ms.assetid: 758a130c-b75a-40fd-8530-3766aa86c5ba
ms.tgt_platform: multiple
keywords:
- Сообщение WM_WTSSESSION_CHANGE службы удаленных рабочих столов
topic_type:
- apiref
api_name:
- WM_WTSSESSION_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f29bef7eb7778602a256f80cb04e47eae905a245783906c3388b576aecedee18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419844"
---
# <a name="wm_wtssession_change-message"></a>\_ \_ Сообщение об изменении втссессион WM

Уведомляет приложения об изменениях в состоянии сеанса.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* \[ окне\]
</dt> <dd>

Дескриптор для окна.

</dd> <dt>

*Сообщение* \[ окне\]
</dt> <dd>

Указывает сообщение (**изменение WM \_ втссессион \_**).

</dd> <dt>

*wParam* \[ окне\]
</dt> <dd>

Код состояния, описывающий причину отправки уведомления об изменении состояния сеанса. Этот параметр может принимать одно из указанных ниже значений.

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ \_Подключение к консоли** (0x1)


</dt> <dd>

сеанс, определенный параметром *lParam* , был подключен к терминалу консоли или сеансу RemoteFX.

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ \_Отключение консоли** (0x2)


</dt> <dd>

сеанс, определенный параметром *lParam* , был отключен от терминала консоли или сеанса RemoteFX.

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ УДАЛЕНное \_ Подключение** (0x3)


</dt> <dd>

Сеанс, идентифицируемый *lParam* , был подключен к удаленному терминалу.

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ УДАЛЕНное \_ Отключение** (0x4)


</dt> <dd>

Сеанс, идентифицируемый *lParam* , был отключен от удаленного терминала.

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ \_Вход в сеанс** (0x5)


</dt> <dd>

Пользователь вошел в сеанс, определенный параметром *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_Выход из сеанса** (0x6)


</dt> <dd>

Пользователь вышел из сеанса, определенного параметром *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ \_Блокировка сеанса** (0x7)


</dt> <dd>

Сеанс, указанный параметром *lParam* , заблокирован.

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ \_Разблокировка сеанса** (0x8)


</dt> <dd>

Сеанс, определенный параметром *lParam* , разблокирован.

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ \_Удаленное \_ Управление сеансом** (0x9)


</dt> <dd>

Сеанс, идентифицируемый *lParam* , изменил состояние удаленного управления. Чтобы определить состояние, вызовите [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) и проверьте метрику **SM \_ ремотеконтрол** .

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ \_Создание сеанса** (0xA)


</dt> <dd>

Зарезервировано для последующего использования.

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ \_Завершение сеанса** (0xB)


</dt> <dd>

Зарезервировано для последующего использования.

</dd> </dl> </dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Идентификатор сеанса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="remarks"></a>Remarks

Это сообщение отправляется только приложениям, зарегистрированным для получения этого сообщения путем вызова [**втсрегистерсессионнотификатион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).

Примеры того, как приложения могут реагировать на это сообщение, включают освобождение или получение ресурсов, связанных с консолью, определение способа рисования экрана или запуск эффектов анимации консоли.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                           |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**втсрегистерсессионнотификатион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[**втсунрегистерсессионнотификатион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

