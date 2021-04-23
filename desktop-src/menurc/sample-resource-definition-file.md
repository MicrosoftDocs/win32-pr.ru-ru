---
title: Пример файла Resource-Definition
description: Пример файла скрипта, который определяет ресурсы для приложения с именем Shapes.
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e6a870b4b63b0e88e5ddcd069e8318e4bdb750
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068315"
---
# <a name="sample-resource-definition-file"></a><span data-ttu-id="f5db8-103">Пример файла Resource-Definition</span><span class="sxs-lookup"><span data-stu-id="f5db8-103">Sample Resource-Definition File</span></span>

<span data-ttu-id="f5db8-104">В следующем примере показан файл скрипта, который определяет ресурсы для приложения с именем Shapes:</span><span class="sxs-lookup"><span data-stu-id="f5db8-104">The following example shows a script file that defines the resources for an application named Shapes:</span></span>

``` syntax
#include "shapes.h"

ShapesCursor  CURSOR  SHAPES.CUR
ShapesIcon    ICON    SHAPES.ICO

ShapesMenu MENU
{
    POPUP "&Shape"
    {
        MENUITEM "&Clear", ID_CLEAR
        MENUITEM "&Rectangle", ID_RECT
        MENUITEM "&Triangle", ID_TRIANGLE
        MENUITEM "&Star", ID_STAR
        MENUITEM "&Ellipse", ID_ELLIPSE
    }
}
```

<span data-ttu-id="f5db8-105">Оператор [**cursor**](cursor-resource.md) называет имя ресурса курсора приложения шапескурсор и указывает фигуры файла курсора. CUR, который содержит изображение для данного курсора.</span><span class="sxs-lookup"><span data-stu-id="f5db8-105">The [**CURSOR**](cursor-resource.md) statement names the application's cursor resource ShapesCursor and specifies the cursor file SHAPES.CUR, which contains the image for that cursor.</span></span>

<span data-ttu-id="f5db8-106">В операторе [**Icon**](icon-resource.md) имя ресурса значка приложения шапесикон и указываются фигуры файла значка. ICO, который содержит изображение для этого значка.</span><span class="sxs-lookup"><span data-stu-id="f5db8-106">The [**ICON**](icon-resource.md) statement names the application's icon resource ShapesIcon and specifies the icon file SHAPES.ICO, which contains the image for that icon.</span></span>

<span data-ttu-id="f5db8-107">Инструкция [**меню**](menu-resource.md) определяет меню приложения с именем **шапесмену**, всплывающее меню с пятью пунктами меню.</span><span class="sxs-lookup"><span data-stu-id="f5db8-107">The [**MENU**](menu-resource.md) statement defines an application menu named **ShapesMenu**, a pop-up menu with five menu items.</span></span>

<span data-ttu-id="f5db8-108">Текст определения меню, заключенный в фигурные скобки или ключевые слова **Begin** и **End** , задает каждый пункт меню и идентификатор меню, которые возвращаются, когда пользователь выбирает этот элемент.</span><span class="sxs-lookup"><span data-stu-id="f5db8-108">The body of the menu definition, enclosed by the curly braces, or the **BEGIN** and **END** keywords, specifies each menu item and the menu identifier that is returned when the user selects that item.</span></span> <span data-ttu-id="f5db8-109">Например, первый элемент в меню **clear** возвращает идентификатор в меню, \_ когда пользователь выбирает его.</span><span class="sxs-lookup"><span data-stu-id="f5db8-109">For example, the first item on the menu, **Clear**, returns the menu identifier ID\_CLEAR when the user selects it.</span></span> <span data-ttu-id="f5db8-110">Идентификаторы меню определяются в файле заголовка приложения SHAPEs. H.</span><span class="sxs-lookup"><span data-stu-id="f5db8-110">The menu identifiers are defined in the application header file, SHAPES.H.</span></span>

 

 




