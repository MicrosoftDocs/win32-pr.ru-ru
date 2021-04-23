---
description: Следующий пример кода сборки x86 получает идентификатор сеанса служб терминалов, связанный с текущим процессом.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Получение идентификатора сеанса текущего процесса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76865bcfe9144e8b95d4642385804aaf1af8fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141398"
---
# <a name="getting-the-session-id-of-the-current-process"></a><span data-ttu-id="e1dde-103">Получение идентификатора сеанса текущего процесса</span><span class="sxs-lookup"><span data-stu-id="e1dde-103">Getting the Session ID of the Current Process</span></span>

<span data-ttu-id="e1dde-104">\[Адреса памяти, указанные в этом примере кода, могут измениться в будущих выпусках Windows.</span><span class="sxs-lookup"><span data-stu-id="e1dde-104">\[The memory addresses specified by this example code may change in future releases of Windows.</span></span> <span data-ttu-id="e1dde-105">Чтобы обеспечить правильную работу приложения в будущем, приложение должно вызвать [**жеткуррентпроцессид**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) , а затем [**процессидтосессионид**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) вместо следующего примера кода.\]</span><span class="sxs-lookup"><span data-stu-id="e1dde-105">To ensure that your application will continue to run correctly in the future, your application must call [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) and then [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) instead of the following sample code.\]</span></span>

<span data-ttu-id="e1dde-106">Следующий пример кода сборки x86 получает идентификатор сеанса служб терминалов, связанный с текущим процессом.</span><span class="sxs-lookup"><span data-stu-id="e1dde-106">The following example x86 assembly code gets the Terminal Services session ID associated with the current process.</span></span>

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
