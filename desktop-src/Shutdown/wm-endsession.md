---
description: Сообщение WM \_ ENDSESSION отправляется в приложение после того, как система обработает результаты \_ сообщения WM куерендсессион. Сообщение WM \_ ENDSESSION информирует приложение о том, завершается ли сеанс.
ms.assetid: 9bf04f24-da1e-4680-a47b-28e9c500635e
title: Сообщение WM_ENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa62f356d881182dd6e6fd9e0558332bcc1b3fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662620"
---
# <a name="wm_endsession-message"></a><span data-ttu-id="49e5a-104">\_Сообщение ENDSESSION WM</span><span class="sxs-lookup"><span data-stu-id="49e5a-104">WM\_ENDSESSION message</span></span>

<span data-ttu-id="49e5a-105">Сообщение **WM \_ ENDSESSION** отправляется в приложение после того, как система обработает результаты сообщения [**WM \_ куерендсессион**](wm-queryendsession.md) .</span><span class="sxs-lookup"><span data-stu-id="49e5a-105">The **WM\_ENDSESSION** message is sent to an application after the system processes the results of the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message.</span></span> <span data-ttu-id="49e5a-106">Сообщение **WM \_ ENDSESSION** информирует приложение о том, завершается ли сеанс.</span><span class="sxs-lookup"><span data-stu-id="49e5a-106">The **WM\_ENDSESSION** message informs the application whether the session is ending.</span></span>

<span data-ttu-id="49e5a-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="49e5a-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="49e5a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="49e5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49e5a-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="49e5a-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="49e5a-110">Маркер окна.</span><span class="sxs-lookup"><span data-stu-id="49e5a-110">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="49e5a-111">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="49e5a-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="49e5a-112">Идентификатор **WM \_ ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="49e5a-112">The **WM\_ENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="49e5a-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49e5a-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49e5a-114">Если сеанс завершается, этот параметр имеет **значение true**. сеанс может завершиться в любое время после того, как все приложения возвращали это сообщение.</span><span class="sxs-lookup"><span data-stu-id="49e5a-114">If the session is being ended, this parameter is **TRUE**; the session can end any time after all applications have returned from processing this message.</span></span> <span data-ttu-id="49e5a-115">В противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="49e5a-115">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="49e5a-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49e5a-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49e5a-117">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="49e5a-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="49e5a-118">Если этот параметр равен 0, система завершает работу или перезапускается (невозможно определить, какое событие происходит).</span><span class="sxs-lookup"><span data-stu-id="49e5a-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="49e5a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="49e5a-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="49e5a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="49e5a-120">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="49e5a-121"><dt>**ENDSESSION \_ КЛОСЕАПП**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="49e5a-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x1</dt></span></span> </dl>        | <span data-ttu-id="49e5a-122">Если параметр *wParam* имеет **значение true**, приложение должно завершить работу.</span><span class="sxs-lookup"><span data-stu-id="49e5a-122">If *wParam* is **TRUE**, the application must shut down.</span></span> <span data-ttu-id="49e5a-123">Любые данные должны сохраняться автоматически без запроса пользователя (Дополнительные сведения см. в разделе Примечания).</span><span class="sxs-lookup"><span data-stu-id="49e5a-123">Any data should be saved automatically without prompting the user (for more information, see Remarks).</span></span> <span data-ttu-id="49e5a-124">Диспетчер перезапуска отправляет это сообщение, когда приложение использует файл, который необходимо заменить, когда он должен обслуживать систему или когда ресурсы системы исчерпаны.</span><span class="sxs-lookup"><span data-stu-id="49e5a-124">The Restart Manager sends this message when the application is using a file that needs to be replaced, when it must service the system, or when system resources are exhausted.</span></span> <span data-ttu-id="49e5a-125">Приложение будет перезапущено, если оно было зарегистрировано для перезапуска с помощью функции [**регистераппликатионрестарт**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) .</span><span class="sxs-lookup"><span data-stu-id="49e5a-125">The application will be restarted if it has registered for restart using the [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) function.</span></span> <span data-ttu-id="49e5a-126">Дополнительные сведения см. в разделе [рекомендации для приложений](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="49e5a-126">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span> <br/> <span data-ttu-id="49e5a-127">Если параметр *wParam* имеет **значение false**, приложение не должно завершать работу.</span><span class="sxs-lookup"><span data-stu-id="49e5a-127">If *wParam* is **FALSE**, the application should not shut down.</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="49e5a-128"><dt>**ENDSESSION \_ КРИТическая**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="49e5a-128"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="49e5a-129">Приложение принудительно завершает работу.</span><span class="sxs-lookup"><span data-stu-id="49e5a-129">The application is forced to shut down.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="49e5a-130"><dt>**ENDSESSION \_ Выход из системы**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="49e5a-130"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="49e5a-131">Пользователь записывается в систему.</span><span class="sxs-lookup"><span data-stu-id="49e5a-131">The user is logging off.</span></span> <span data-ttu-id="49e5a-132">Дополнительные сведения см. в разделе выход [из системы](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="49e5a-132">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="49e5a-133">Обратите внимание, что этот параметр является битовой маской.</span><span class="sxs-lookup"><span data-stu-id="49e5a-133">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="49e5a-134">Чтобы проверить это значение, используйте операцию побитового выполнения. не проверяйте на равенство.</span><span class="sxs-lookup"><span data-stu-id="49e5a-134">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49e5a-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49e5a-135">Return value</span></span>

<span data-ttu-id="49e5a-136">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="49e5a-136">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="49e5a-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49e5a-137">Remarks</span></span>

<span data-ttu-id="49e5a-138">Приложения с несохраненными данными могут сохранить данные во временном расположении и восстановить их при следующем запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="49e5a-138">Applications that have unsaved data could save the data to a temporary location and restore it the next time the application starts.</span></span> <span data-ttu-id="49e5a-139">Рекомендуется часто сохранять данные и состояние приложений. Например, автоматическое сохранение данных между операциями сохранения, инициированными пользователем, для уменьшения объема данных, сохраняемых при завершении работы.</span><span class="sxs-lookup"><span data-stu-id="49e5a-139">It is recommended that applications save their data and state frequently; for example, automatically save data between save operations initiated by the user to reduce the amount of data to be saved at shutdown.</span></span>

<span data-ttu-id="49e5a-140">При завершении сеанса приложению не требуется вызывать функцию [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) или [**посткуитмессаже**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .</span><span class="sxs-lookup"><span data-stu-id="49e5a-140">The application need not call the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) or [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function when the session is ending.</span></span>

## <a name="requirements"></a><span data-ttu-id="49e5a-141">Требования</span><span class="sxs-lookup"><span data-stu-id="49e5a-141">Requirements</span></span>



| <span data-ttu-id="49e5a-142">Требование</span><span class="sxs-lookup"><span data-stu-id="49e5a-142">Requirement</span></span> | <span data-ttu-id="49e5a-143">Значение</span><span class="sxs-lookup"><span data-stu-id="49e5a-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49e5a-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49e5a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="49e5a-145">\[Приложения UWP для классических приложений Windows XP \|\]</span><span class="sxs-lookup"><span data-stu-id="49e5a-145">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="49e5a-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49e5a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="49e5a-147">\[Приложения UWP для классических приложений Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="49e5a-147">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="49e5a-148">Header</span><span class="sxs-lookup"><span data-stu-id="49e5a-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="49e5a-149"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49e5a-149"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49e5a-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49e5a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e5a-151">Выход из системы</span><span class="sxs-lookup"><span data-stu-id="49e5a-151">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="49e5a-152">Завершение работы</span><span class="sxs-lookup"><span data-stu-id="49e5a-152">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="49e5a-153">**дестройвиндов**</span><span class="sxs-lookup"><span data-stu-id="49e5a-153">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="49e5a-154">**посткуитмессаже**</span><span class="sxs-lookup"><span data-stu-id="49e5a-154">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="49e5a-155">**сетпроцессшутдовнпараметерс**</span><span class="sxs-lookup"><span data-stu-id="49e5a-155">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="49e5a-156">**WM \_ куерендсессион**</span><span class="sxs-lookup"><span data-stu-id="49e5a-156">**WM\_QUERYENDSESSION**</span></span>](wm-queryendsession.md)
</dt> </dl>

 

 
