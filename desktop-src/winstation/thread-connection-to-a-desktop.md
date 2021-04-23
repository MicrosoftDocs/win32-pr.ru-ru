---
title: Подключение потока к рабочему столу
description: Когда процесс подключается к Windows-станции, система назначает рабочий стол потоку, выполняющему подключение.
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260906"
---
# <a name="thread-connection-to-a-desktop"></a><span data-ttu-id="50077-103">Подключение потока к рабочему столу</span><span class="sxs-lookup"><span data-stu-id="50077-103">Thread Connection to a Desktop</span></span>

<span data-ttu-id="50077-104">Когда процесс подключается к Windows-станции, система назначает рабочий стол потоку, выполняющему подключение.</span><span class="sxs-lookup"><span data-stu-id="50077-104">After a process connects to a window station, the system assigns a desktop to the thread making the connection.</span></span> <span data-ttu-id="50077-105">Система определяет рабочий стол для назначения потоку согласно следующим правилам.</span><span class="sxs-lookup"><span data-stu-id="50077-105">The system determines the desktop to assign to the thread according to the following rules:</span></span>

1.  <span data-ttu-id="50077-106">Если поток вызвал функцию [**сетсреаддесктоп**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) , он подключается к указанному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="50077-106">If the thread has called the [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) function, it connects to the specified desktop.</span></span>
2.  <span data-ttu-id="50077-107">Если поток не вызывал [**сетсреаддесктоп**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), он подключается к рабочему столу, унаследованному от родительского процесса.</span><span class="sxs-lookup"><span data-stu-id="50077-107">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), it connects to the desktop inherited from the parent process.</span></span>
3.  <span data-ttu-id="50077-108">Если поток не вызывал [**сетсреаддесктоп**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) и не наследовал класс Desktop, система пытается открыть для максимального \_ разрешенного доступа и подключиться к рабочему столу следующим образом:</span><span class="sxs-lookup"><span data-stu-id="50077-108">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) and did not inherit a desktop, the system attempts to open for MAXIMUM\_ALLOWED access and connect to a desktop as follows:</span></span>
    -   <span data-ttu-id="50077-109">Если имя рабочего стола было указано в элементе **лпдесктоп** структуры [**стартупинфо**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) , которая использовалась при создании процесса, поток подключается к указанному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="50077-109">If a desktop name was specified in the **lpDesktop** member of the [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure that was used when the process was created, the thread connects to the specified desktop.</span></span>
    -   <span data-ttu-id="50077-110">В противном случае поток подключается к рабочему столу по умолчанию рабочей станции Windows, к которой подключен процесс.</span><span class="sxs-lookup"><span data-stu-id="50077-110">Otherwise, the thread connects to the default desktop of the window station to which the process connected.</span></span>

<span data-ttu-id="50077-111">Рабочий стол, назначенный во время этого процесса подключения, не может быть закрыт путем вызова функции [**клоседесктоп**](/windows/win32/api/winuser/nf-winuser-closedesktop) .</span><span class="sxs-lookup"><span data-stu-id="50077-111">The desktop assigned during this connection process cannot be closed by calling the [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) function.</span></span>

<span data-ttu-id="50077-112">Когда процесс подключается к рабочему столу, система выполняет поиск унаследованных дескрипторов в таблице дескрипторов процесса.</span><span class="sxs-lookup"><span data-stu-id="50077-112">When a process is connecting to a desktop, the system searches the process's handle table for inherited handles.</span></span> <span data-ttu-id="50077-113">Система использует первый найденный обработчик рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="50077-113">The system uses the first desktop handle it finds.</span></span> <span data-ttu-id="50077-114">Если требуется, чтобы дочерний процесс подключаться к определенному настольному рабочему столу, необходимо убедиться, что только нужный маркер помечен как наследуемый.</span><span class="sxs-lookup"><span data-stu-id="50077-114">If you want a child process to connect to a particular inherited desktop, you must ensure that the only the desired handle is marked inheritable.</span></span> <span data-ttu-id="50077-115">Если дочерний процесс наследует несколько дескрипторов рабочего стола, то результаты подключения к рабочему столу не будут определены.</span><span class="sxs-lookup"><span data-stu-id="50077-115">If a child process inherits multiple desktop handles, the results of the desktop connection are undefined.</span></span>

<span data-ttu-id="50077-116">Дескрипторы рабочего стола, которые открывает система при подключении процесса к рабочему столу, не наследуются.</span><span class="sxs-lookup"><span data-stu-id="50077-116">Handles to a desktop that the system opens while connecting a process to a desktop are not inheritable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50077-117">См. также</span><span class="sxs-lookup"><span data-stu-id="50077-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50077-118">Обработка подключения к оконной станции</span><span class="sxs-lookup"><span data-stu-id="50077-118">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
</dt> </dl>

 

 