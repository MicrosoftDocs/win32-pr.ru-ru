---
description: Следующее определение Винтернл. h является статическим адресом памяти активного сеанса консоли служб терминалов. Идентификатор сеанса активной консоли не определен в версиях операционной системы Microsoft Windows, предшествующих Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Получение идентификатора активного сеанса консоли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936db3f8038348864fc90fc55eeb4287a67c45d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895765"
---
# <a name="getting-the-active-console-session-id"></a><span data-ttu-id="44db2-104">Получение идентификатора активного сеанса консоли</span><span class="sxs-lookup"><span data-stu-id="44db2-104">Getting the Active Console Session ID</span></span>

<span data-ttu-id="44db2-105">Следующее определение Винтернл. h является статическим адресом памяти активного сеанса консоли служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="44db2-105">The following Winternl.h definition is the static memory address of the active Terminal Services console session ID.</span></span> <span data-ttu-id="44db2-106">Идентификатор сеанса активной консоли не определен в версиях операционной системы Microsoft Windows, предшествующих Windows XP.</span><span class="sxs-lookup"><span data-stu-id="44db2-106">This active console session ID is not defined in versions of the Microsoft Windows operating system earlier than Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="44db2-107">Это определение может измениться в будущих выпусках Windows.</span><span class="sxs-lookup"><span data-stu-id="44db2-107">This definition may change in future releases of Windows.</span></span> <span data-ttu-id="44db2-108">Чтобы обеспечить правильную работу приложения в будущем, приложение должно вызвать [**втсжетактивеконсолесессионид**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span><span class="sxs-lookup"><span data-stu-id="44db2-108">To ensure that your application will continue to run correctly in the future, your application must call [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span></span>

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
