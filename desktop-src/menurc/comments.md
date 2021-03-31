---
title: Комментарии (меню и другие ресурсы)
description: Версия-кандидат поддерживает синтаксис в стиле C для однострочных комментариев и блочных комментариев. Однострочные комментарии начинаются с двух косых черт (//) и выполняются до конца строки. Ниже приведен пример инструкции Resource, за которой следует однострочный комментарий.
ms.assetid: 045268fb-2d6e-446c-8b95-90e42baeb282
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fda05690df9b7e7fff6974d75d8275a2842b68
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800869"
---
# <a name="comments-menus-and-other-resources"></a><span data-ttu-id="a4ead-105">Комментарии (меню и другие ресурсы)</span><span class="sxs-lookup"><span data-stu-id="a4ead-105">Comments (Menus and Other Resources)</span></span>

<span data-ttu-id="a4ead-106">Версия-кандидат поддерживает синтаксис в стиле C для однострочных комментариев и блочных комментариев.</span><span class="sxs-lookup"><span data-stu-id="a4ead-106">RC supports C-style syntax for both single-line comments and block comments.</span></span> <span data-ttu-id="a4ead-107">Однострочные комментарии начинаются с двух косых черт (//) и выполняются до конца строки.</span><span class="sxs-lookup"><span data-stu-id="a4ead-107">Single-line comments begin with two forward slashes (//) and run to the end of the line.</span></span> <span data-ttu-id="a4ead-108">Ниже приведен пример инструкции Resource, за которой следует однострочный комментарий.</span><span class="sxs-lookup"><span data-stu-id="a4ead-108">The following is an example of a resource statement followed by a single-line comment.</span></span>

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

<span data-ttu-id="a4ead-109">Комментарии блока начинаются с открывающего разделителя (/ \* ) и выполняются в закрывающем разделителе ( \* /).</span><span class="sxs-lookup"><span data-stu-id="a4ead-109">Block comments begin with an opening delimiter (/\*) and run to a closing delimiter (\*/).</span></span> <span data-ttu-id="a4ead-110">Комментарии не предусматривают вложения.</span><span class="sxs-lookup"><span data-stu-id="a4ead-110">Comments do not nest.</span></span> <span data-ttu-id="a4ead-111">Ниже приведен пример блочного комментария в начале RC-файла.</span><span class="sxs-lookup"><span data-stu-id="a4ead-111">The following is an example of a block comment at the beginning of a .rc file.</span></span>

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




