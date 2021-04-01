---
description: Функция Екситвиндовс выходит из системы текущего пользователя. Также можно вызвать функцию ExitWindowsEx с \_ флагом выхода из ЕКСВ.
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Выход из системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0571c0522c494acd763d57dcae8d200125cd53d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913851"
---
# <a name="logging-off"></a><span data-ttu-id="d826a-104">Выход из системы</span><span class="sxs-lookup"><span data-stu-id="d826a-104">Logging Off</span></span>

<span data-ttu-id="d826a-105">Функция [**екситвиндовс**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) выходит из системы текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="d826a-105">The [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function logs off the current user.</span></span> <span data-ttu-id="d826a-106">Также можно вызвать функцию [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) с \_ флагом выхода из ЕКСВ.</span><span class="sxs-lookup"><span data-stu-id="d826a-106">You can also call the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function with the EXW\_LOGOFF flag.</span></span>

<span data-ttu-id="d826a-107">По умолчанию, когда приложение использует [**екситвиндовс**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) или [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) для выхода из системы, система отправляет сообщение [**WM \_ куерендсессион**](wm-queryendsession.md) в каждое окно.</span><span class="sxs-lookup"><span data-stu-id="d826a-107">By default, when an application uses [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) to log off, the system sends the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message to each window.</span></span> <span data-ttu-id="d826a-108">Приложения договариваются о завершении, возвращая **значение true** , когда они получили это сообщение.</span><span class="sxs-lookup"><span data-stu-id="d826a-108">Applications agree to terminate by returning **TRUE** when they receive this message.</span></span> <span data-ttu-id="d826a-109">Если какое-либо приложение возвращает **значение false** при обработке этого сообщения, операция выхода из системы отменяется.</span><span class="sxs-lookup"><span data-stu-id="d826a-109">If any application returns **FALSE** when processing this message, the log-off operation is canceled.</span></span> <span data-ttu-id="d826a-110">Если приложение обрабатывает сообщение **WM \_ куерендсессион** , можно разрешить пользователю отменить операцию выхода, даже если другое приложение или система поступили к порождению запроса на завершение сеанса.</span><span class="sxs-lookup"><span data-stu-id="d826a-110">If your application handles the **WM\_QUERYENDSESSION** message, you can allow the user to cancel the log-off operation, even if another application or the system originated the end-session request.</span></span> <span data-ttu-id="d826a-111">Пример см. в разделе выход [из текущего пользователя](how-to-log-off-the-current-user.md).</span><span class="sxs-lookup"><span data-stu-id="d826a-111">For an example, see [How to Log Off the Current User](how-to-log-off-the-current-user.md).</span></span>

<span data-ttu-id="d826a-112">Когда приложение возвращает **true** для [**WM \_ куерендсессион**](wm-queryendsession.md), оно получает сообщение [**WM \_ ENDSESSION**](wm-endsession.md) и завершается, независимо от того, как другие приложения реагируют на сообщение **WM \_ куерендсессион** .</span><span class="sxs-lookup"><span data-stu-id="d826a-112">When an application returns **TRUE** for [**WM\_QUERYENDSESSION**](wm-queryendsession.md), it receives the [**WM\_ENDSESSION**](wm-endsession.md) message and it is terminated, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="d826a-113">Чтобы принудительно завершить все приложения, используйте функцию [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)и укажите \_ флаг force ЕКСВ.</span><span class="sxs-lookup"><span data-stu-id="d826a-113">To force all applications to terminate, use [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex), and specify the EXW\_FORCE flag.</span></span> <span data-ttu-id="d826a-114">Это предотвращает отправку сообщений [**\_ куерендсессион WM**](wm-queryendsession.md) .</span><span class="sxs-lookup"><span data-stu-id="d826a-114">This prevents the system from sending [**WM\_QUERYENDSESSION**](wm-queryendsession.md) messages.</span></span>

<span data-ttu-id="d826a-115">Система также отправляет \_ \_ сигнал управления событиями нажатия клавиши CTRL для каждого процесса во время операции выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="d826a-115">The system also sends the CTRL\_LOGOFF\_EVENT control signal to every process during a log-off operation.</span></span> <span data-ttu-id="d826a-116">Консольное приложение может зарегистрировать [**хандлерраутине**](/windows/console/handlerroutine) для обработки этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="d826a-116">A console application can register a [**HandlerRoutine**](/windows/console/handlerroutine) to process these messages.</span></span>

<span data-ttu-id="d826a-117">Если процесс, который вызвал функцию [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) , выполняется в сеансе входа интерактивного пользователя, все процессы в сеансе входа будут прерваны.</span><span class="sxs-lookup"><span data-stu-id="d826a-117">If the process that called [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) is running in the logon session of the interactive user, all processes in the logon session are terminated.</span></span> <span data-ttu-id="d826a-118">Если процесс, вызывающий функцию **ExitWindowsEx** , находится в другом сеансе входа, выполняются только уведомления. процессы не прерываются.</span><span class="sxs-lookup"><span data-stu-id="d826a-118">If the process calling **ExitWindowsEx** is in some other logon session, only the notifications are made; no processes are terminated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d826a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d826a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d826a-120">Выход из системы текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="d826a-120">How to Log Off the Current User</span></span>](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
