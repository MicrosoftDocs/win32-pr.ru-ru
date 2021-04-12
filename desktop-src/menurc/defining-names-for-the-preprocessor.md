---
title: Определение имен для препроцессора
description: Условную компиляцию можно указать в скрипте, в зависимости от того, определено ли имя в командной строке RC с параметром/d или в файле или включаемом файле с директивой \ define.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64b339959ace5a70d83fa8ee8beb615f1bc5ce4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328771"
---
# <a name="defining-names-for-the-preprocessor"></a><span data-ttu-id="64ccc-103">Определение имен для препроцессора</span><span class="sxs-lookup"><span data-stu-id="64ccc-103">Defining Names for the Preprocessor</span></span>

<span data-ttu-id="64ccc-104">Условную компиляцию можно указать в скрипте, в зависимости от того, определено ли имя в командной строке RC с параметром **/d** или в файле или включаемом файле с директивой [**\# define**](-define.md) .</span><span class="sxs-lookup"><span data-stu-id="64ccc-104">You can specify conditional compilation in a script, based on whether a name is defined on the RC command line with the **/d** option, or in the file or an include file with the [**\#define**](-define.md) directive.</span></span>

<span data-ttu-id="64ccc-105">Например, предположим, что в приложении есть всплывающее меню, которое должно отображаться только с отладочными версиями приложения.</span><span class="sxs-lookup"><span data-stu-id="64ccc-105">For example, suppose your application has a pop-up menu that should appear only with debugging versions of the application.</span></span> <span data-ttu-id="64ccc-106">При компиляции приложения для обычного использования меню не включается.</span><span class="sxs-lookup"><span data-stu-id="64ccc-106">When you compile the application for normal use, the menu is not included.</span></span> <span data-ttu-id="64ccc-107">В следующем примере показаны инструкции, которые можно добавить в файл определения ресурса для определения меню отладки:</span><span class="sxs-lookup"><span data-stu-id="64ccc-107">The following example shows the statements that can be added to the resource-definition file to define a Debug menu:</span></span>

``` syntax
#include <windows.h>

MainMenu MENU
{
    //. . .
#ifdef DEBUG
    POPUP "&Debug"
    {
        MENUITEM "&Memory usage", ID_MEMORY
        MENUITEM "&Walk data heap", ID_WALK_HEAP
    }
#endif
}
```

<span data-ttu-id="64ccc-108">При компиляции ресурсов для отладочной версии приложения можно включить меню отладку с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="64ccc-108">When compiling resources for a debugging version of the application, you could include the Debug menu by using the following command:</span></span>

<span data-ttu-id="64ccc-109">**Версия-d ОТЛАДКа MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="64ccc-109">**rc -d DEBUG myapp.rc**</span></span>

<span data-ttu-id="64ccc-110">Для компиляции ресурсов для обычной версии приложения? одна из которых не включает меню "Отладка"? можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="64ccc-110">To compile resources for a normal version of the application?one that does not include the Debug menu?you could use the following command:</span></span>

<span data-ttu-id="64ccc-111">**Версия-кандидат MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="64ccc-111">**rc myapp.rc**</span></span>

 

 




