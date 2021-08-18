---
description: Описывает объявление вершины.
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: деклдата
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5686e3344e4642483490c9bd2892cbc92ade290567107b702cc9c56ff351c71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803239"
---
# <a name="decldata"></a>деклдата

Описывает объявление вершины.

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

Где:

-   Нелементс — число элементов объявления вершины.
-   Elements \[ нелементс \] -Array элементов объявления вершины.
-   Ндвордс — число DWORD.
-   \[ндвордс данных \] — массив DWORD, который содержит данные в каждом элементе вершины.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



