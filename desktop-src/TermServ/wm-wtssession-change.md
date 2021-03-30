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
ms.openlocfilehash: db8f1dc421aa160824a194588711e84f961ea4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801277"
---
# <a name="wm_wtssession_change-message"></a><span data-ttu-id="564cd-104">\_ \_ Сообщение об изменении втссессион WM</span><span class="sxs-lookup"><span data-stu-id="564cd-104">WM\_WTSSESSION\_CHANGE message</span></span>

<span data-ttu-id="564cd-105">Уведомляет приложения об изменениях в состоянии сеанса.</span><span class="sxs-lookup"><span data-stu-id="564cd-105">Notifies applications of changes in session state.</span></span>

<span data-ttu-id="564cd-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="564cd-106">The window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a><span data-ttu-id="564cd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="564cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="564cd-108">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="564cd-108">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="564cd-109">Обработчик для окна.</span><span class="sxs-lookup"><span data-stu-id="564cd-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="564cd-110">*Сообщение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="564cd-110">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="564cd-111">Указывает сообщение (**изменение WM \_ втссессион \_**).</span><span class="sxs-lookup"><span data-stu-id="564cd-111">Specifies the message (**WM\_WTSSESSION\_CHANGE**).</span></span>

</dd> <dt>

<span data-ttu-id="564cd-112">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="564cd-112">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="564cd-113">Код состояния, описывающий причину отправки уведомления об изменении состояния сеанса.</span><span class="sxs-lookup"><span data-stu-id="564cd-113">Status code describing the reason the session state change notification was sent.</span></span> <span data-ttu-id="564cd-114">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="564cd-114">This parameter can be one of the following values.</span></span>

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span data-ttu-id="564cd-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**ВТС \_ \_Подключение к консоли** (0x1)</span><span class="sxs-lookup"><span data-stu-id="564cd-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS\_CONSOLE\_CONNECT** (0x1)</span></span>


</dt> <dd>

<span data-ttu-id="564cd-116">Сеанс, идентифицируемый *lParam* , был подключен к терминалу консоли или сеансу RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="564cd-116">The session identified by *lParam* was connected to the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span data-ttu-id="564cd-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**ВТС \_ \_Отключение консоли** (0x2)</span><span class="sxs-lookup"><span data-stu-id="564cd-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS\_CONSOLE\_DISCONNECT** (0x2)</span></span>


</dt> <dd>

<span data-ttu-id="564cd-118">Сеанс, идентифицируемый *lParam* , отключен от терминала консоли или сеанса RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="564cd-118">The session identified by *lParam* was disconnected from the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span data-ttu-id="564cd-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**ВТС \_ УДАЛЕНное \_ Подключение** (0x3)</span><span class="sxs-lookup"><span data-stu-id="564cd-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS\_REMOTE\_CONNECT** (0x3)</span></span>


</dt> <dd>

<span data-ttu-id="564cd-120">Сеанс, идентифицируемый *lParam* , был подключен к удаленному терминалу.</span><span class="sxs-lookup"><span data-stu-id="564cd-120">The session identified by *lParam* was connected to the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span data-ttu-id="564cd-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**ВТС \_ УДАЛЕНное \_ Отключение** (0x4)</span><span class="sxs-lookup"><span data-stu-id="564cd-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS\_REMOTE\_DISCONNECT** (0x4)</span></span>


</dt> <dd>

<span data-ttu-id="564cd-122">Сеанс, идентифицируемый *lParam* , был отключен от удаленного терминала.</span><span class="sxs-lookup"><span data-stu-id="564cd-122">The session identified by *lParam* was disconnected from the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span data-ttu-id="564cd-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**ВТС \_ \_Вход в сеанс** (0x5)</span><span class="sxs-lookup"><span data-stu-id="564cd-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS\_SESSION\_LOGON** (0x5)</span></span>


</dt> <dd>

<span data-ttu-id="564cd-124">Пользователь вошел в сеанс, определенный параметром *lParam*.</span><span class="sxs-lookup"><span data-stu-id="564cd-124">A user has logged on to the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span data-ttu-id="564cd-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**ВТС \_ \_Выход из сеанса** (0x6)</span><span class="sxs-lookup"><span data-stu-id="564cd-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS\_SESSION\_LOGOFF** (0x6)</span></span>


</dt> <dd>

<span data-ttu-id="564cd-126">Пользователь вышел из сеанса, определенного параметром *lParam*.</span><span class="sxs-lookup"><span data-stu-id="564cd-126">A user has logged off the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span data-ttu-id="564cd-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**ВТС \_ \_Блокировка сеанса** (0x7)</span><span class="sxs-lookup"><span data-stu-id="564cd-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS\_SESSION\_LOCK** (0x7)</span></span>


</dt> <dd>

<span data-ttu-id="564cd-128">Сеанс, указанный параметром *lParam* , заблокирован.</span><span class="sxs-lookup"><span data-stu-id="564cd-128">The session identified by *lParam* has been locked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span data-ttu-id="564cd-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**ВТС \_ \_Разблокировка сеанса** (0x8)</span><span class="sxs-lookup"><span data-stu-id="564cd-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS\_SESSION\_UNLOCK** (0x8)</span></span>


</dt> <dd>

<span data-ttu-id="564cd-130">Сеанс, определенный параметром *lParam* , разблокирован.</span><span class="sxs-lookup"><span data-stu-id="564cd-130">The session identified by *lParam* has been unlocked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span data-ttu-id="564cd-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**ВТС \_ \_Удаленное \_ Управление сеансом** (0x9)</span><span class="sxs-lookup"><span data-stu-id="564cd-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS\_SESSION\_REMOTE\_CONTROL** (0x9)</span></span>


</dt> <dd>

<span data-ttu-id="564cd-132">Сеанс, идентифицируемый *lParam* , изменил состояние удаленного управления.</span><span class="sxs-lookup"><span data-stu-id="564cd-132">The session identified by *lParam* has changed its remote controlled status.</span></span> <span data-ttu-id="564cd-133">Чтобы определить состояние, вызовите [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) и проверьте метрику **SM \_ ремотеконтрол** .</span><span class="sxs-lookup"><span data-stu-id="564cd-133">To determine the status, call [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) and check the **SM\_REMOTECONTROL** metric.</span></span>

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span data-ttu-id="564cd-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**ВТС \_ \_Создание сеанса** (0xA)</span><span class="sxs-lookup"><span data-stu-id="564cd-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS\_SESSION\_CREATE** (0xA)</span></span>


</dt> <dd>

<span data-ttu-id="564cd-135">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="564cd-135">Reserved for future use.</span></span>

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span data-ttu-id="564cd-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**ВТС \_ \_Завершение сеанса** (0xB)</span><span class="sxs-lookup"><span data-stu-id="564cd-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS\_SESSION\_TERMINATE** (0xB)</span></span>


</dt> <dd>

<span data-ttu-id="564cd-137">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="564cd-137">Reserved for future use.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="564cd-138">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="564cd-138">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="564cd-139">Идентификатор сеанса.</span><span class="sxs-lookup"><span data-stu-id="564cd-139">The identifier of the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="564cd-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="564cd-140">Return value</span></span>

<span data-ttu-id="564cd-141">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="564cd-141">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="564cd-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="564cd-142">Remarks</span></span>

<span data-ttu-id="564cd-143">Это сообщение отправляется только приложениям, зарегистрированным для получения этого сообщения путем вызова [**втсрегистерсессионнотификатион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span><span class="sxs-lookup"><span data-stu-id="564cd-143">This message is sent only to applications that have registered to receive this message by calling [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span></span>

<span data-ttu-id="564cd-144">Примеры того, как приложения могут реагировать на это сообщение, включают освобождение или получение ресурсов, связанных с консолью, определение способа рисования экрана или запуск эффектов анимации консоли.</span><span class="sxs-lookup"><span data-stu-id="564cd-144">Examples of how applications can respond to this message include releasing or acquiring console-specific resources, determining how a screen is to be painted, or triggering console animation effects.</span></span>

## <a name="requirements"></a><span data-ttu-id="564cd-145">Требования</span><span class="sxs-lookup"><span data-stu-id="564cd-145">Requirements</span></span>



| <span data-ttu-id="564cd-146">Требование</span><span class="sxs-lookup"><span data-stu-id="564cd-146">Requirement</span></span> | <span data-ttu-id="564cd-147">Значение</span><span class="sxs-lookup"><span data-stu-id="564cd-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="564cd-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="564cd-148">Minimum supported client</span></span><br/> | <span data-ttu-id="564cd-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="564cd-149">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="564cd-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="564cd-150">Minimum supported server</span></span><br/> | <span data-ttu-id="564cd-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="564cd-151">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="564cd-152">Header</span><span class="sxs-lookup"><span data-stu-id="564cd-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="564cd-153"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="564cd-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="564cd-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="564cd-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="564cd-155">**втсрегистерсессионнотификатион**</span><span class="sxs-lookup"><span data-stu-id="564cd-155">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[<span data-ttu-id="564cd-156">**втсунрегистерсессионнотификатион**</span><span class="sxs-lookup"><span data-stu-id="564cd-156">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

