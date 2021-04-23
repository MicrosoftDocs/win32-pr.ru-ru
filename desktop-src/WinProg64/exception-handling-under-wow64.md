---
title: Обработка исключений в WOW64
description: WOW64 использует собственные исключения x64, ia64 или ARM64 в качестве транспорта для исключений x86. Поэтому в 32-разрядном приложении, работающем в эмуляторе WOW64, неперехваченные исключения ведут себя как собственные 64-разрядные исключения.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070484"
---
# <a name="exception-handling-under-wow64"></a><span data-ttu-id="2fbd8-104">Обработка исключений в WOW64</span><span class="sxs-lookup"><span data-stu-id="2fbd8-104">Exception Handling under WOW64</span></span>

<span data-ttu-id="2fbd8-105">WOW64 использует собственные исключения x64, ia64 или ARM64 в качестве транспорта для исключений x86.</span><span class="sxs-lookup"><span data-stu-id="2fbd8-105">WOW64 uses native x64, ia64, or ARM64 exceptions as a transport for x86 exceptions.</span></span> <span data-ttu-id="2fbd8-106">Поэтому в 32-разрядном приложении, работающем в эмуляторе WOW64, неперехваченные исключения ведут себя как собственные 64-разрядные исключения.</span><span class="sxs-lookup"><span data-stu-id="2fbd8-106">Therefore, in a 32-bit application running under WOW64, uncaught exceptions behave like native 64-bit exceptions.</span></span>

<span data-ttu-id="2fbd8-107">В приложении, работающем в 32-разрядной версии Windows, неперехваченные исключения передаются в обработчики исключений более высокого уровня приложения, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="2fbd8-107">In an application running on a 32-bit version of Windows, uncaught exceptions are passed on to higher-level exception handlers of the application, when available.</span></span> <span data-ttu-id="2fbd8-108">В одном и том же 32-разрядном приложении, работающем в эмуляторе WOW64, система может подавить неперехваченные исключения.</span><span class="sxs-lookup"><span data-stu-id="2fbd8-108">In the same 32-bit application running under WOW64, the system may suppress uncaught exceptions.</span></span>

<span data-ttu-id="2fbd8-109">Windows **Vista, Windows Server 2003 и Windows XP:** В одном и том же 32-разрядном приложении, работающем в эмуляторе WOW64, система вызывает фильтры исключений, но может подавить неперехваченные исключения без вызова связанных обработчиков.</span><span class="sxs-lookup"><span data-stu-id="2fbd8-109">**Windows Vista, Windows Server 2003 and Windows XP:** In the same 32-bit application running under WOW64, the system calls the exception filters but may suppress uncaught exceptions without invoking the associated handlers.</span></span> <span data-ttu-id="2fbd8-110">Это поведение изменилось, начиная с Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2fbd8-110">This behavior changed starting with Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="2fbd8-111">Дополнительные сведения о неперехваченных исключениях в оконных процедурах см. в описании функции [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2fbd8-111">For more information about uncaught exceptions in window procedures, see the [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

 

 