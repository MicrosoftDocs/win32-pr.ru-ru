---
title: Предустановленный макрос
description: Версия-кандидат не поддерживает предварительно определенные макросы ANSI C ( \_ \_ Дата \_ \_ , \_ \_ файл \_ \_ , \_ \_ строка \_ \_ , \_ \_ STDC \_ \_ , \_ \_ время \_ \_ , \_ \_ Метка времени \_ \_ ). Поэтому эти макросы нельзя включить в заголовочные файлы, которые будут включены в скрипт ресурсов.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 351674bc86ab56753bb49dba9e65edd97a7b1a04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132915"
---
# <a name="predefined-macros"></a><span data-ttu-id="63800-104">Предустановленный макрос</span><span class="sxs-lookup"><span data-stu-id="63800-104">Predefined Macros</span></span>

<span data-ttu-id="63800-105">Версия-кандидат не поддерживает предварительно определенные макросы ANSI C (**\_ \_ Дата \_ \_**, **\_ \_ файл \_ \_**, **\_ \_ строка \_ \_**, **\_ \_ STDC \_ \_**, **\_ \_ время \_ , метка \_** **\_ \_ времени). \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63800-105">RC does not support the ANSI C predefined macros (**\_\_DATE\_\_**, **\_\_FILE\_\_**, **\_\_LINE\_\_**, **\_\_STDC\_\_**, **\_\_TIME\_\_**, **\_\_TIMESTAMP\_\_**).</span></span> <span data-ttu-id="63800-106">Поэтому эти макросы нельзя включить в заголовочные файлы, которые будут включены в скрипт ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63800-106">Therefore, you cannot include these macros in header files that you will include in your resource script.</span></span>

<span data-ttu-id="63800-107">Версия-кандидат определяет \_ вызов RC, что позволяет условно компилировать части файлов заголовков в зависимости от того, является ли компилятор компилятором C или компилятором RC.</span><span class="sxs-lookup"><span data-stu-id="63800-107">RC does define RC\_INVOKED, which enables you conditionally compile portions of your header files, depending on whether the compiler is your C compiler or the RC compiler.</span></span> <span data-ttu-id="63800-108">Это важно, поскольку компилятор RC поддерживает только подмножество инструкций, поддерживаемых компилятором C.</span><span class="sxs-lookup"><span data-stu-id="63800-108">This is important because the RC compiler supports only a subset of the statements a C compiler would support.</span></span>

<span data-ttu-id="63800-109">Чтобы условно скомпилировать код с помощью компилятора RC, заключите код, который компилятор RC не может скомпилировать с помощью \# метода IFNDEF RC \_ Invoked и **\# endif**.</span><span class="sxs-lookup"><span data-stu-id="63800-109">To conditionally compile your code with the RC compiler, surround code that RC cannot compile with \#ifndef RC\_INVOKED and **\#endif**.</span></span>

<span data-ttu-id="63800-110">Следующий пример взят из примеров пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="63800-110">The following example is taken from the SDK samples.</span></span> <span data-ttu-id="63800-111">В нем показано, как создать файл заголовка, который может быть скомпилирован условно.</span><span class="sxs-lookup"><span data-stu-id="63800-111">It demonstrates how to create a header file that can be compiled conditionally.</span></span>

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




