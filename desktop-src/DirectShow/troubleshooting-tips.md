---
description: Советы по устранению неполадок
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Советы по устранению неполадок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663544"
---
# <a name="troubleshooting-tips"></a><span data-ttu-id="6d0a9-103">Советы по устранению неполадок</span><span class="sxs-lookup"><span data-stu-id="6d0a9-103">Troubleshooting Tips</span></span>

<span data-ttu-id="6d0a9-104">Следующие советы помогут избежать взаимоблокировок и сбоев в приложении DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-104">This following tips will help you to avoid deadlocks or crashes in your DirectShow application.</span></span>

<span data-ttu-id="6d0a9-105">**Глобальные объекты**</span><span class="sxs-lookup"><span data-stu-id="6d0a9-105">**Global Objects**</span></span>

<span data-ttu-id="6d0a9-106">Глобальный объект C++ не должен создавать объекты DirectShow в своем методе-конструкторе или освобождать их в методе деструктора.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-106">A global C++ object should not create DirectShow objects in its constructor method or release them in its destructor method.</span></span> <span data-ttu-id="6d0a9-107">Это может привести к неограниченному блокированию приложения по следующей причине:</span><span class="sxs-lookup"><span data-stu-id="6d0a9-107">Doing so can cause the application to block indefinitely, for the following reason:</span></span>

<span data-ttu-id="6d0a9-108">Потоки не могут выйти из функции точки входа в DLL.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-108">Threads cannot exit while inside a DLL's entry-point function.</span></span> <span data-ttu-id="6d0a9-109">Ядро 32 содержит блокировку глобального процесса во время функции точки входа, а блокировка предотвращает выход из потока.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-109">Kernel 32 holds a global process lock during the entry-point function, and the lock prevents the thread from exiting.</span></span> <span data-ttu-id="6d0a9-110">Так как некоторые объекты DirectShow являются собственными потоками, они могут блокироваться при их освобождении из функции точки входа в DLL.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-110">Because some DirectShow objects own threads, they can block if released from inside a DLL entry-point function.</span></span> <span data-ttu-id="6d0a9-111">Если приложение имеет глобальный объект C++, Библиотека DLL среды выполнения C вызывает деструктор объекта при выгрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-111">If an application has a global C++ object, the C runtime DLL calls the object's destructor when the DLL is unloaded.</span></span> <span data-ttu-id="6d0a9-112">Если деструктор освобождает объекты DirectShow, он может блокироваться в результате.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-112">If the destructor releases DirectShow objects, it can block as a result.</span></span>

<span data-ttu-id="6d0a9-113">По тем же причинам библиотека DLL не должна создавать или освобождать объекты DirectShow в своей подподпрограмме точки входа.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-113">For similar reasons, a DLL should not create or release DirectShow objects in its entry point routine.</span></span>

<span data-ttu-id="6d0a9-114">**Освобождение интерфейсов**</span><span class="sxs-lookup"><span data-stu-id="6d0a9-114">**Releasing Interfaces**</span></span>

<span data-ttu-id="6d0a9-115">Необходимо освободить все указатели интерфейса DirectShow, пока приложение все еще обрабатывает сообщения, до того, как оно завершит цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-115">You should release all DirectShow interface pointers while your application is still processing messages, before it exits the message loop.</span></span> <span data-ttu-id="6d0a9-116">В противном случае могут отображаться различные утверждения, так как некоторые объекты DirectShow отправляют сообщения во время выполнения подпрограмм очистки.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-116">Otherwise, you might see various asserts, because some DirectShow objects send messages during their clean-up routines.</span></span>

<span data-ttu-id="6d0a9-117">(Если вы используете класс ATL **квиндовимпл** , не следует ждать, пока **онфиналмессаже** освободит интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-117">(As a corollary, if you are using the ATL **CWindowImpl** class, do not wait until **OnFinalMessage** to free the interfaces.</span></span> <span data-ttu-id="6d0a9-118">Вместо этого Освободите их при обработке сообщения о \_ закрытии WM.)</span><span class="sxs-lookup"><span data-stu-id="6d0a9-118">Instead, free them when you handle the WM\_CLOSE message.)</span></span>

<span data-ttu-id="6d0a9-119">**Счетчики ссылок**</span><span class="sxs-lookup"><span data-stu-id="6d0a9-119">**Reference Counts**</span></span>

<span data-ttu-id="6d0a9-120">Когда отладочная версия Quartz.dll выгружается, она проверяет наличие у объектов DirectShow счетчиков ссылок, которые не были освобождены.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-120">When the debug version of Quartz.dll unloads, it checks whether any DirectShow objects have reference counts that were not released.</span></span> <span data-ttu-id="6d0a9-121">В этом случае создается утверждение:</span><span class="sxs-lookup"><span data-stu-id="6d0a9-121">If so, it throws an assertion:</span></span>


```C++
g_cFGObjects == 0 
```



<span data-ttu-id="6d0a9-122">Если это утверждение не выполняется, это означает, что приложение вызвало утечку счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-122">When this assertion fails, it means your application has leaked a reference count.</span></span> <span data-ttu-id="6d0a9-123">Проверьте код и убедитесь, что выпускают все указатели интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6d0a9-123">Review your code and make sure that you release all interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d0a9-124">См. также</span><span class="sxs-lookup"><span data-stu-id="6d0a9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d0a9-125">Отладка в DirectShow</span><span class="sxs-lookup"><span data-stu-id="6d0a9-125">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



