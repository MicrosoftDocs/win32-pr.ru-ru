---
description: Научитесь использовать функцию CreateThread для создания нового потока для процесса. Отладчикам обычно требуется проверять или изменять содержимое регистров потока.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Функции потока для отладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff168d4840032a6199ef03e0cf2117c8ea87f4d6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403987"
---
# <a name="thread-functions-for-debugging"></a><span data-ttu-id="2aaa1-104">Функции потока для отладки</span><span class="sxs-lookup"><span data-stu-id="2aaa1-104">Thread Functions for Debugging</span></span>

<span data-ttu-id="2aaa1-105">Функция [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) создает новый поток для процесса.</span><span class="sxs-lookup"><span data-stu-id="2aaa1-105">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="2aaa1-106">Отладчикам обычно требуется проверять или изменять содержимое регистров потока.</span><span class="sxs-lookup"><span data-stu-id="2aaa1-106">Debuggers typically need to examine or change the contents of a thread's registers.</span></span> <span data-ttu-id="2aaa1-107">Для этого отладчик должен получить обработчик для потока с помощью функции [**дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) и указать соответствующий доступ к потоку ( \_ \_ контекст Get, контекст набора потоков \_ \_ или и то, и другое).</span><span class="sxs-lookup"><span data-stu-id="2aaa1-107">To accomplish this, a debugger must obtain a handle to the thread by using the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function and specifying the appropriate access to the thread (THREAD\_GET\_CONTEXT, THREAD\_SET\_CONTEXT, or both).</span></span> <span data-ttu-id="2aaa1-108">Функция [**опенсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) позволяет отладчику получить идентификатор существующего потока.</span><span class="sxs-lookup"><span data-stu-id="2aaa1-108">The [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function enables a debugger to obtain the identifier of an existing thread.</span></span>

<span data-ttu-id="2aaa1-109">Процесс с соответствующим доступом к потоку может проверить регистры потока с помощью функции [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) и установить содержимое регистров потока с помощью функции [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) .</span><span class="sxs-lookup"><span data-stu-id="2aaa1-109">A process with appropriate access to a thread can examine the thread's registers by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) function and set the contents of the thread's registers by using the [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) function.</span></span>

<span data-ttu-id="2aaa1-110">Процесс также может получить доступ к потоку \_ приостановки потока \_ .</span><span class="sxs-lookup"><span data-stu-id="2aaa1-110">A process can also obtain THREAD\_SUSPEND\_RESUME access to a thread.</span></span> <span data-ttu-id="2aaa1-111">Этот тип доступа позволяет отладчику управлять выполнением потока с помощью функций [**суспендсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) и [**ресумесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .</span><span class="sxs-lookup"><span data-stu-id="2aaa1-111">This type of access enables a debugger to control a thread's execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) and [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) functions.</span></span> <span data-ttu-id="2aaa1-112">Дополнительные сведения о потоках см. в разделе [процессы и потоки](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="2aaa1-112">For more information about threads, see [Processes and Threads](../procthread/processes-and-threads.md).</span></span>

 

 
