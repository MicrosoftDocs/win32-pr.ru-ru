---
description: Структурированные механизмы обработки исключений и обработки прерываний являются неотъемлемой частью системы. они обеспечивают надежность системы. Эти механизмы можно использовать для создания согласованных надежных и надежных приложений.
ms.assetid: ab5bc1bd-107f-4ed2-b471-a229a76637fe
title: Сведения об структурированной обработке исключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161e60725f137f379b7d734485fae7cad39ae1be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262552"
---
# <a name="about-structured-exception-handling"></a><span data-ttu-id="65a93-104">Сведения об структурированной обработке исключений</span><span class="sxs-lookup"><span data-stu-id="65a93-104">About Structured Exception Handling</span></span>

<span data-ttu-id="65a93-105">Структурированные механизмы обработки исключений и обработки прерываний являются неотъемлемой частью системы. они обеспечивают надежность системы.</span><span class="sxs-lookup"><span data-stu-id="65a93-105">The structured exception handling and termination handling mechanisms are integral parts of the system; they enable the system to be robust.</span></span> <span data-ttu-id="65a93-106">Эти механизмы можно использовать для создания согласованных надежных и надежных приложений.</span><span class="sxs-lookup"><span data-stu-id="65a93-106">You can use these mechanisms to create consistently robust and reliable applications.</span></span>

<span data-ttu-id="65a93-107">Структурированная обработка исключений предоставляется в основном через поддержку компилятора.</span><span class="sxs-lookup"><span data-stu-id="65a93-107">Structured exception handling is made available primarily through compiler support.</span></span> <span data-ttu-id="65a93-108">Например, оптимизирующий компилятор Microsoft C/C++ поддерживает ключевое слово **\_ \_ try** , определяющее защищенный текст кода, ключевое слово **\_ \_ except** , идентифицирующее обработчик исключений, и ключевое слово **\_ \_ finally** , идентифицирующее обработчик завершения.</span><span class="sxs-lookup"><span data-stu-id="65a93-108">For example, the Microsoft C/C++ Optimizing Compiler supports the **\_\_try** keyword that identifies a guarded body of code, the **\_\_except** keyword that identifies an exception handler, and the **\_\_finally** keyword that identifies a termination handler.</span></span> <span data-ttu-id="65a93-109">Хотя в этом обзоре используются примеры, характерные для компилятора Microsoft C/C++, эта поддержка также предоставляется и другими компиляторами.</span><span class="sxs-lookup"><span data-stu-id="65a93-109">Although this overview uses examples specific to the Microsoft C/C++ compiler, other compilers provide this support as well.</span></span>

-   [<span data-ttu-id="65a93-110">Обработка исключений</span><span class="sxs-lookup"><span data-stu-id="65a93-110">Exception Handling</span></span>](exception-handling.md)
-   [<span data-ttu-id="65a93-111">Обработка исключений на основе кадров</span><span class="sxs-lookup"><span data-stu-id="65a93-111">Frame-based Exception Handling</span></span>](frame-based-exception-handling.md)
-   [<span data-ttu-id="65a93-112">Обработка векторных исключений</span><span class="sxs-lookup"><span data-stu-id="65a93-112">Vectored Exception Handling</span></span>](vectored-exception-handling.md)
-   [<span data-ttu-id="65a93-113">Обработка завершения</span><span class="sxs-lookup"><span data-stu-id="65a93-113">Termination Handling</span></span>](termination-handling.md)
-   [<span data-ttu-id="65a93-114">Синтаксис обработчика</span><span class="sxs-lookup"><span data-stu-id="65a93-114">Handler Syntax</span></span>](handler-syntax.md)

 

 



