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
# <a name="comments-menus-and-other-resources"></a>Комментарии (меню и другие ресурсы)

Версия-кандидат поддерживает синтаксис в стиле C для однострочных комментариев и блочных комментариев. Однострочные комментарии начинаются с двух косых черт (//) и выполняются до конца строки. Ниже приведен пример инструкции Resource, за которой следует однострочный комментарий.

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

Комментарии блока начинаются с открывающего разделителя (/ \* ) и выполняются в закрывающем разделителе ( \* /). Комментарии не предусматривают вложения. Ниже приведен пример блочного комментария в начале RC-файла.

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




