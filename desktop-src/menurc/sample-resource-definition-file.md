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
# <a name="sample-resource-definition-file"></a>Пример файла Resource-Definition

В следующем примере показан файл скрипта, который определяет ресурсы для приложения с именем Shapes:

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

Оператор [**cursor**](cursor-resource.md) называет имя ресурса курсора приложения шапескурсор и указывает фигуры файла курсора. CUR, который содержит изображение для данного курсора.

В операторе [**Icon**](icon-resource.md) имя ресурса значка приложения шапесикон и указываются фигуры файла значка. ICO, который содержит изображение для этого значка.

Инструкция [**меню**](menu-resource.md) определяет меню приложения с именем **шапесмену**, всплывающее меню с пятью пунктами меню.

Текст определения меню, заключенный в фигурные скобки или ключевые слова **Begin** и **End** , задает каждый пункт меню и идентификатор меню, которые возвращаются, когда пользователь выбирает этот элемент. Например, первый элемент в меню **clear** возвращает идентификатор в меню, \_ когда пользователь выбирает его. Идентификаторы меню определяются в файле заголовка приложения SHAPEs. H.

 

 




