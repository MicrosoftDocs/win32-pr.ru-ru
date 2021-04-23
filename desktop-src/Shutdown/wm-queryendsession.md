---
description: Сообщение WM \_ куерендсессион отправляется, когда пользователь выбирает завершение сеанса или когда приложение вызывает одну из функций завершения работы системы.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: Сообщение WM_QUERYENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2e2f82388b229523f371c680d6ccc7c4b1e27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664521"
---
# <a name="wm_queryendsession-message"></a><span data-ttu-id="a2383-103">\_Сообщение КУЕРЕНДСЕССИОН WM</span><span class="sxs-lookup"><span data-stu-id="a2383-103">WM\_QUERYENDSESSION message</span></span>

<span data-ttu-id="a2383-104">Сообщение **WM \_ куерендсессион** отправляется, когда пользователь выбирает завершение сеанса или когда приложение вызывает одну из функций завершения работы системы.</span><span class="sxs-lookup"><span data-stu-id="a2383-104">The **WM\_QUERYENDSESSION** message is sent when the user chooses to end the session or when an application calls one of the system shutdown functions.</span></span> <span data-ttu-id="a2383-105">Если какое-либо приложение возвращает ноль, сеанс не завершается.</span><span class="sxs-lookup"><span data-stu-id="a2383-105">If any application returns zero, the session is not ended.</span></span> <span data-ttu-id="a2383-106">Система перестает отправлять сообщения **WM \_ куерендсессион** , как только одно приложение возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="a2383-106">The system stops sending **WM\_QUERYENDSESSION** messages as soon as one application returns zero.</span></span>

<span data-ttu-id="a2383-107">После обработки этого сообщения система отправляет сообщение [**WM \_ ENDSESSION**](wm-endsession.md) с параметром *wParam* , равным результатам сообщения **\_ куерендсессион WM** .</span><span class="sxs-lookup"><span data-stu-id="a2383-107">After processing this message, the system sends the [**WM\_ENDSESSION**](wm-endsession.md) message with the *wParam* parameter set to the results of the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="a2383-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a2383-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="a2383-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2383-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2383-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a2383-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a2383-111">Маркер окна.</span><span class="sxs-lookup"><span data-stu-id="a2383-111">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="a2383-112">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="a2383-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="a2383-113">Идентификатор **WM \_ куерендсессион** .</span><span class="sxs-lookup"><span data-stu-id="a2383-113">The **WM\_QUERYENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a2383-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2383-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2383-115">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="a2383-115">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a2383-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2383-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2383-117">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a2383-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="a2383-118">Если этот параметр равен 0, система завершает работу или перезапускается (невозможно определить, какое событие происходит).</span><span class="sxs-lookup"><span data-stu-id="a2383-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="a2383-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a2383-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="a2383-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a2383-120">Meaning</span></span>                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="a2383-121"><dt>**ENDSESSION \_ КЛОСЕАПП**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a2383-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="a2383-122">Приложение использует файл, который должен быть заменен, система обслуживается, или исчерпаны системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a2383-122">The application is using a file that must be replaced, the system is being serviced, or system resources are exhausted.</span></span> <span data-ttu-id="a2383-123">Дополнительные сведения см. в разделе [рекомендации для приложений](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="a2383-123">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="a2383-124"><dt>**ENDSESSION \_ КРИТическая**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="a2383-124"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="a2383-125">Приложение принудительно завершает работу.</span><span class="sxs-lookup"><span data-stu-id="a2383-125">The application is forced to shut down.</span></span><br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="a2383-126"><dt>**ENDSESSION \_ Выход из системы**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="a2383-126"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="a2383-127">Пользователь записывается в систему.</span><span class="sxs-lookup"><span data-stu-id="a2383-127">The user is logging off.</span></span> <span data-ttu-id="a2383-128">Дополнительные сведения см. в разделе выход [из системы](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="a2383-128">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                   |



 

<span data-ttu-id="a2383-129">Обратите внимание, что этот параметр является битовой маской.</span><span class="sxs-lookup"><span data-stu-id="a2383-129">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="a2383-130">Чтобы проверить это значение, используйте операцию побитового выполнения. не проверяйте на равенство.</span><span class="sxs-lookup"><span data-stu-id="a2383-130">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2383-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2383-131">Return value</span></span>

<span data-ttu-id="a2383-132">Приложения должны учитывать намерения пользователя и возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a2383-132">Applications should respect the user's intentions and return **TRUE**.</span></span> <span data-ttu-id="a2383-133">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает **значение true** для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="a2383-133">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE** for this message.</span></span>

<span data-ttu-id="a2383-134">Если завершение работы приведет к повреждению записываемой системы или носителя, приложение может вернуть **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a2383-134">If shutting down would corrupt the system or media that is being burned, the application can return **FALSE**.</span></span> <span data-ttu-id="a2383-135">Однако рекомендуется учитывать действия пользователя.</span><span class="sxs-lookup"><span data-stu-id="a2383-135">However, it is good practice to respect the user's actions.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2383-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2383-136">Remarks</span></span>

<span data-ttu-id="a2383-137">Когда приложение возвращает **значение true** для этого сообщения, оно получает сообщение [**WM \_ ENDSESSION**](wm-endsession.md) , независимо от того, как другие приложения реагируют на сообщение **\_ куерендсессион WM** .</span><span class="sxs-lookup"><span data-stu-id="a2383-137">When an application returns **TRUE** for this message, it receives the [**WM\_ENDSESSION**](wm-endsession.md) message, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span> <span data-ttu-id="a2383-138">Каждое приложение должно возвращать **значение true** или **false** сразу после получения этого сообщения и откладывать все операции очистки до получения сообщения **WM \_ ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="a2383-138">Each application should return **TRUE** or **FALSE** immediately upon receiving this message, and defer any cleanup operations until it receives the **WM\_ENDSESSION** message.</span></span>

<span data-ttu-id="a2383-139">Приложения могут отображать пользовательский интерфейс, предлагающий пользователю получить сведения при завершении работы, но не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a2383-139">Applications can display a user interface prompting the user for information at shutdown, however it is not recommended.</span></span> <span data-ttu-id="a2383-140">Через пять секунд система отображает сведения о приложениях, препятствующих завершению работы, и позволяет пользователю их завершить.</span><span class="sxs-lookup"><span data-stu-id="a2383-140">After five seconds, the system displays information about the applications that are preventing shutdown and allows the user to terminate them.</span></span> <span data-ttu-id="a2383-141">Например, в Windows XP отображается диалоговое окно, а в Windows Vista отображается полный экран с дополнительной информацией о приложениях, блокирующих завершение работы.</span><span class="sxs-lookup"><span data-stu-id="a2383-141">For example, Windows XP displays a dialog box, while Windows Vista displays a full screen with additional information about the applications blocking shutdown.</span></span> <span data-ttu-id="a2383-142">Если приложение должно блокировать или откладывать завершение работы системы, используйте функцию [**шутдовнблоккреасонкреате**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .</span><span class="sxs-lookup"><span data-stu-id="a2383-142">If your application must block or postpone system shutdown, use the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span> <span data-ttu-id="a2383-143">Дополнительные сведения см. в разделе [изменение завершения работы Windows Vista](shutdown-changes-for-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="a2383-143">For more information, see [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).</span></span>

<span data-ttu-id="a2383-144">Консольные приложения могут использовать функцию [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) для получения уведомлений о завершении работы.</span><span class="sxs-lookup"><span data-stu-id="a2383-144">Console applications can use the [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) function to receive shutdown notification.</span></span>

<span data-ttu-id="a2383-145">Приложения служб могут использовать функцию [**регистерсервицектрлхандлерекс**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) для получения уведомлений о завершении работы в подпрограмме обработчика.</span><span class="sxs-lookup"><span data-stu-id="a2383-145">Service applications can use the [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function to receive shutdown notifications in a handler routine.</span></span>

## <a name="examples"></a><span data-ttu-id="a2383-146">Примеры</span><span class="sxs-lookup"><span data-stu-id="a2383-146">Examples</span></span>

<span data-ttu-id="a2383-147">Пример см. в разделе [выход из системы](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="a2383-147">For an example, see [Logging Off](logging-off.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2383-148">Требования</span><span class="sxs-lookup"><span data-stu-id="a2383-148">Requirements</span></span>



| <span data-ttu-id="a2383-149">Требование</span><span class="sxs-lookup"><span data-stu-id="a2383-149">Requirement</span></span> | <span data-ttu-id="a2383-150">Значение</span><span class="sxs-lookup"><span data-stu-id="a2383-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2383-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2383-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a2383-152">\[Приложения UWP для классических приложений Windows XP \|\]</span><span class="sxs-lookup"><span data-stu-id="a2383-152">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="a2383-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2383-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a2383-154">\[Приложения UWP для классических приложений Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="a2383-154">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="a2383-155">Header</span><span class="sxs-lookup"><span data-stu-id="a2383-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2383-156"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2383-156"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2383-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2383-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2383-158">Выход из системы</span><span class="sxs-lookup"><span data-stu-id="a2383-158">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="a2383-159">Завершение работы</span><span class="sxs-lookup"><span data-stu-id="a2383-159">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="a2383-160">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="a2383-160">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="a2383-161">**екситвиндовс**</span><span class="sxs-lookup"><span data-stu-id="a2383-161">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[<span data-ttu-id="a2383-162">**сетпроцессшутдовнпараметерс**</span><span class="sxs-lookup"><span data-stu-id="a2383-162">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="a2383-163">**WM \_ ENDSESSION**</span><span class="sxs-lookup"><span data-stu-id="a2383-163">**WM\_ENDSESSION**</span></span>](wm-endsession.md)
</dt> </dl>

 

 
