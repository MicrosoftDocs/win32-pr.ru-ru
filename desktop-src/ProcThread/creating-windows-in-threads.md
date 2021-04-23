---
description: Любой поток может создать окно.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Создание окон в потоках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673769"
---
# <a name="creating-windows-in-threads"></a><span data-ttu-id="b7fbc-103">Создание окон в потоках</span><span class="sxs-lookup"><span data-stu-id="b7fbc-103">Creating Windows in Threads</span></span>

<span data-ttu-id="b7fbc-104">Любой поток может создать окно.</span><span class="sxs-lookup"><span data-stu-id="b7fbc-104">Any thread can create a window.</span></span> <span data-ttu-id="b7fbc-105">Поток, который создает окно, владеет окном и связанной с ним очередью сообщений.</span><span class="sxs-lookup"><span data-stu-id="b7fbc-105">The thread that creates the window owns the window and its associated message queue.</span></span> <span data-ttu-id="b7fbc-106">Таким образом, поток должен предоставить цикл обработки сообщений, чтобы обработать сообщения в очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="b7fbc-106">Therefore, the thread must provide a message loop to process the messages in its message queue.</span></span> <span data-ttu-id="b7fbc-107">Кроме того, необходимо использовать [**мсгваитформултиплеобжектс**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) или [**мсгваитформултиплеобжектсекс**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) в этом потоке, а не в других [функциях ожидания](/windows/desktop/Sync/wait-functions), чтобы она могла обрабатывать сообщения.</span><span class="sxs-lookup"><span data-stu-id="b7fbc-107">In addition, you must use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) or [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) in that thread, rather than the other [wait functions](/windows/desktop/Sync/wait-functions), so that it can process messages.</span></span> <span data-ttu-id="b7fbc-108">В противном случае система может быть заблокирована, когда поток отправляет сообщение в ожидании.</span><span class="sxs-lookup"><span data-stu-id="b7fbc-108">Otherwise, the system can become deadlocked when the thread is sent a message while it is waiting.</span></span>

<span data-ttu-id="b7fbc-109">Функцию [**аттачсреадинпут**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) можно использовать, чтобы разрешить набору потоков совместно использовать одно и то же состояние входа.</span><span class="sxs-lookup"><span data-stu-id="b7fbc-109">The [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) function can be used to allow a set of threads to share the same input state.</span></span> <span data-ttu-id="b7fbc-110">При совместном использовании входного состояния потоки совместно используют свою концепцию активного окна.</span><span class="sxs-lookup"><span data-stu-id="b7fbc-110">By sharing input state, the threads share their concept of the active window.</span></span> <span data-ttu-id="b7fbc-111">Таким образом, один поток всегда может активировать окно другого потока.</span><span class="sxs-lookup"><span data-stu-id="b7fbc-111">By doing this, one thread can always activate another thread's window.</span></span> <span data-ttu-id="b7fbc-112">Эта функция также полезна для совместного использования состояния фокуса, состояния захвата мыши, состояния клавиатуры и состояния окна Z-порядка в Windows, созданных различными потоками, для которых входное состояние является общим.</span><span class="sxs-lookup"><span data-stu-id="b7fbc-112">This function is also useful for sharing focus state, mouse capture state, keyboard state, and window Z-order state among windows created by different threads whose input state is shared.</span></span>

<span data-ttu-id="b7fbc-113">Сведения о создании окон см. в разделе [классы Windows](../winmsg/window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="b7fbc-113">For information about creating windows, see [Windows Classes](../winmsg/window-classes.md).</span></span>

 

 
