---
title: C/C++-рекомендации по компиляторам
description: Компилятор MIDL должен взаимодействовать с препроцессором C компилятора и C.
ms.assetid: 3d91d0e4-3a47-4aa2-82d6-c3af11df3a78
keywords:
- MIDL компилятора MIDL, C-Compiler
- C — компилятор MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf6968951bbcbb423896f5609092054dfa65f4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068371"
---
# <a name="cc-compiler-considerations"></a><span data-ttu-id="f8bea-105">C/C++-рекомендации по компиляторам</span><span class="sxs-lookup"><span data-stu-id="f8bea-105">C/C++-Compiler Considerations</span></span>

<span data-ttu-id="f8bea-106">Компилятор MIDL должен взаимодействовать с препроцессором C компилятора и C.</span><span class="sxs-lookup"><span data-stu-id="f8bea-106">The MIDL compiler must interoperate with the C compiler and C preprocessor.</span></span> <span data-ttu-id="f8bea-107">MIDL не принимает синтаксис C++ для входных данных.</span><span class="sxs-lookup"><span data-stu-id="f8bea-107">MIDL does not accept C++ syntax on input.</span></span> <span data-ttu-id="f8bea-108">Созданный h-файл содержит определения в стиле C и C++ для интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="f8bea-108">The generated .h file has both C-style and C++-style definitions for interfaces.</span></span> <span data-ttu-id="f8bea-109">В следующих разделах описываются требования для компилятора C.</span><span class="sxs-lookup"><span data-stu-id="f8bea-109">The following topics describe the requirements for the C compiler.</span></span>

-   [<span data-ttu-id="f8bea-110">Вопросы упаковки C-компилятора</span><span class="sxs-lookup"><span data-stu-id="f8bea-110">C-Compiler Packing Issues</span></span>](c-compiler-packing-issues.md)
-   [<span data-ttu-id="f8bea-111">Определения для прокси-сервера и заглушек C-компилятора</span><span class="sxs-lookup"><span data-stu-id="f8bea-111">C-Compiler Definitions for Proxy/Stubs</span></span>](c-compiler-definitions-for-proxy-stubs.md)

 

 




