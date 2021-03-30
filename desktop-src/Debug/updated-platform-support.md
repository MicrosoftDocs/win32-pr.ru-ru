---
description: При необходимости библиотека DbgHelp была расширена для поддержки как 32, так и 64-разрядной версии Windows.
ms.assetid: 34ec8cd3-3260-441d-b55f-4ea21c736eb1
title: Поддержка платформы обновлена
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7b0b4f5e343c1dbfcbb0d9434a662553c93d67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538903"
---
# <a name="updated-platform-support"></a><span data-ttu-id="5b3af-103">Поддержка платформы обновлена</span><span class="sxs-lookup"><span data-stu-id="5b3af-103">Updated Platform Support</span></span>

<span data-ttu-id="5b3af-104">При необходимости библиотека DbgHelp была расширена для поддержки как 32, так и 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="5b3af-104">Where necessary, the DbgHelp library has been widened to support both 32- and 64-bit Windows.</span></span> <span data-ttu-id="5b3af-105">Исходные функции и определения структур по-прежнему находятся в DbgHelp. h, но существуют также обновленные версии этих определений, совместимые с 64-разрядными версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="5b3af-105">The original function and structure definitions are still in DbgHelp.h, but there are also updated versions of these definitions that are compatible with 64-bit Windows.</span></span> <span data-ttu-id="5b3af-106">Если вы используете в коде обновленные функции, они могут быть скомпилированы как для 32, так и для 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="5b3af-106">If you use the updated functions in your code, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="5b3af-107">Код также будет более эффективным, так как исходные функции просто вызывают обновленные функции для выполнения работы.</span><span class="sxs-lookup"><span data-stu-id="5b3af-107">Your code will also be more efficient, since the original functions simply call the updated functions to perform the work.</span></span>

<span data-ttu-id="5b3af-108">Например, DbgHelp. h содержит определения для **симунлоадмодуле** (исходная функция) и **SymUnloadModule64** (Обновленная функция).</span><span class="sxs-lookup"><span data-stu-id="5b3af-108">For example, DbgHelp.h contains definitions for **SymUnloadModule** (original function) and **SymUnloadModule64** (updated function).</span></span> <span data-ttu-id="5b3af-109">Эти определения практически идентичны, но используют разные типы для параметра *басеофдлл* .</span><span class="sxs-lookup"><span data-stu-id="5b3af-109">These definitions are nearly identical, but use different types for the *BaseOfDll* parameter.</span></span> <span data-ttu-id="5b3af-110">(**Симунлоадмодуле** использует тип **DWORD** , а **SymUnloadModule64** использует тип **DWORD64** .) Если вы написали код для использования **SymUnloadModule64**, он может быть скомпилирован как для 32, так и для 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="5b3af-110">(**SymUnloadModule** uses the **DWORD** type, while **SymUnloadModule64** uses the **DWORD64** type.) If you write your code to use **SymUnloadModule64**, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="5b3af-111">Код также более эффективен, чем если бы он вызывал **симунлоадмодуле**.</span><span class="sxs-lookup"><span data-stu-id="5b3af-111">The code is also more efficient than if it were to call **SymUnloadModule**.</span></span>

<span data-ttu-id="5b3af-112">Ниже приведен список обновленных функций.</span><span class="sxs-lookup"><span data-stu-id="5b3af-112">The following is a list of the updated functions:</span></span>

<dl>

[<span data-ttu-id="5b3af-113">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-113">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="5b3af-114">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-114">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="5b3af-115">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-115">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="5b3af-116">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-116">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="5b3af-117">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-117">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="5b3af-118">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-118">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="5b3af-119">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-119">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="5b3af-120">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-120">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="5b3af-121">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-121">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="5b3af-122">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-122">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="5b3af-123">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-123">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="5b3af-124">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-124">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="5b3af-125">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-125">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="5b3af-126">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-126">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="5b3af-127">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-127">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="5b3af-128">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-128">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="5b3af-129">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-129">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="5b3af-130">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-130">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="5b3af-131">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-131">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="5b3af-132">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-132">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

<span data-ttu-id="5b3af-133">Ниже приведен список обновленных структур.</span><span class="sxs-lookup"><span data-stu-id="5b3af-133">The following is a list of the updated structures:</span></span>

<dl>

[<span data-ttu-id="5b3af-134">**ADDRESS64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-134">**ADDRESS64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[<span data-ttu-id="5b3af-135">**IMAGEHLP \_ отложенный \_ символ \_ LOAD64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-135">**IMAGEHLP\_DEFERRED\_SYMBOL\_LOAD64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[<span data-ttu-id="5b3af-136">**IMAGEHLP \_ дубликат \_ SYMBOL64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-136">**IMAGEHLP\_DUPLICATE\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[<span data-ttu-id="5b3af-137">**IMAGEHLP \_ LINE64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-137">**IMAGEHLP\_LINE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[<span data-ttu-id="5b3af-138">**IMAGEHLP \_ MODULE64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-138">**IMAGEHLP\_MODULE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[<span data-ttu-id="5b3af-139">**IMAGEHLP \_ SYMBOL64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-139">**IMAGEHLP\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[<span data-ttu-id="5b3af-140">**KDHELP64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-140">**KDHELP64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[<span data-ttu-id="5b3af-141">**STACKFRAME64**</span><span class="sxs-lookup"><span data-stu-id="5b3af-141">**STACKFRAME64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



