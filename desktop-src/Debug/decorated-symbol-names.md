---
description: Декорированное имя символа содержит символы, которые определяют, как был объявлен открытый символ.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Декорированные имена символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791fe2220b24dfb73b314a91d1797edd739cb74f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495801"
---
# <a name="decorated-symbol-names"></a><span data-ttu-id="23a96-103">Декорированные имена символов</span><span class="sxs-lookup"><span data-stu-id="23a96-103">Decorated Symbol Names</span></span>

<span data-ttu-id="23a96-104">Декорированное имя символа содержит символы, которые определяют, как был объявлен открытый символ.</span><span class="sxs-lookup"><span data-stu-id="23a96-104">A decorated symbol name includes characters that distinguish how a public symbol has been declared.</span></span> <span data-ttu-id="23a96-105">Для \_ \_ функций STDCALL имена включают символ "@" и десятичное число, которое указывает число байтов в его параметрах функции.</span><span class="sxs-lookup"><span data-stu-id="23a96-105">For \_\_stdcall functions, names include the "@" character and a decimal number that specifies the number of bytes in its function parameters.</span></span> <span data-ttu-id="23a96-106">Например, декорированное имя функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) — LoadLibrary@4 .</span><span class="sxs-lookup"><span data-stu-id="23a96-106">For example, the decorated name of the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is LoadLibrary@4.</span></span> <span data-ttu-id="23a96-107">Для функций C++ декорирование имен является более сложным и отличается от компилятора к компилятору.</span><span class="sxs-lookup"><span data-stu-id="23a96-107">For C++ functions the name decoration is more complex and varies from compiler to compiler.</span></span>

<span data-ttu-id="23a96-108">Чтобы получить недекорированное имя символа, используйте функцию [**ундекоратесимболнаме**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) .</span><span class="sxs-lookup"><span data-stu-id="23a96-108">To retrieve the undecorated symbol name, use the [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) function.</span></span> <span data-ttu-id="23a96-109">Кроме того, можно вызвать функцию [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) , чтобы запросить, чтобы обработчик символов всегда присутствовал символы с недекорированными именами.</span><span class="sxs-lookup"><span data-stu-id="23a96-109">Alternatively, you can call the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to request that the symbol handler always present symbols with undecorated names.</span></span> <span data-ttu-id="23a96-110">Этот параметр необходимо задать перед загрузкой символов, поскольку обработчик символов создает таблицы имен символов во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="23a96-110">You must set this option before loading the symbols because the symbol handler creates the symbol name tables at load time.</span></span>

 

 
