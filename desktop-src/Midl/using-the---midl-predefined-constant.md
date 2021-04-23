---
title: Использование предопределенной константы __midl
description: Когда компилятор MIDL обрабатывает входные файлы IDL и ACF, \_ \_ MIDL определяется по умолчанию и используется для условной компиляции для достижения согласованности во всей сборке.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL компилятора MIDL с использованием предопределенной константы _midl
- _midl предопределенной константы MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068051"
---
# <a name="using-the-__midl-predefined-constant"></a><span data-ttu-id="bbfe6-105">Использование \_ \_ предопределенной константы MIDL</span><span class="sxs-lookup"><span data-stu-id="bbfe6-105">Using the \_\_midl Predefined Constant</span></span>

<span data-ttu-id="bbfe6-106">Когда компилятор MIDL обрабатывает входные файлы IDL и ACF, \_ \_ MIDL определяется по умолчанию и используется для условной компиляции для достижения согласованности во всей сборке.</span><span class="sxs-lookup"><span data-stu-id="bbfe6-106">When the MIDL compiler processes the input IDL and ACF files, \_\_midl is defined by default and is used for conditional compilation to attain consistency throughout the build.</span></span> <span data-ttu-id="bbfe6-107">Это поэтапное использование инструкций define в файлах заголовков, таких как **MIDL \_ Pass**, и их замена флагом «consistent».</span><span class="sxs-lookup"><span data-stu-id="bbfe6-107">This phases out the use of define statements in the header files, such as **MIDL\_PASS**, and replaces them with a consistent flag.</span></span> <span data-ttu-id="bbfe6-108">Значение \_ \_ константы MIDL обозначает версию компилятора *Major. Minor* в соответствии с формулой *основной* \* 100 + *дополнительный номер*, например MIDL ver.</span><span class="sxs-lookup"><span data-stu-id="bbfe6-108">The value of the \_\_midl constant indicates the compiler version *major.minor* according to the formula *major* \* 100 + *minor*; for example MIDL ver.</span></span> <span data-ttu-id="bbfe6-109">6.0. x имеет \_ \_ MIDL, определенный как 600.</span><span class="sxs-lookup"><span data-stu-id="bbfe6-109">6.0.x has the \_\_midl defined as 600.</span></span>

<span data-ttu-id="bbfe6-110">Если выбрать, можно переопределить это значение по умолчанию, указав в командной строке следующее: **/u \_ \_ MIDL**.</span><span class="sxs-lookup"><span data-stu-id="bbfe6-110">If you choose, you can override this default by specifying the following on the command line: **/U\_\_midl**.</span></span> <span data-ttu-id="bbfe6-111">Дополнительные сведения см. в разделе [**/u**](-u.md).</span><span class="sxs-lookup"><span data-stu-id="bbfe6-111">For more information, see [**/U**](-u.md).</span></span>

 

 




