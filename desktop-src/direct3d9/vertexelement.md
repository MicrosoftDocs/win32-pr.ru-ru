---
description: Описывает отдельный элемент вершины в объявлении вершины.
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: вертекселемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2ecef6cfa8c522532599acef1b83343c64edd2b5eca93fe461d8bf8419ada8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518857"
---
# <a name="vertexelement"></a>вертекселемент

Описывает отдельный элемент вершины в объявлении вершины.

``` syntax
template VertexElement 
{ 
    < F752461C-1E23-48f6-B9F8-8350850F336F > 
    DWORD Type; 
    DWORD Method; 
    DWORD Usage; 
    DWORD UsageIndex; 
} 
```

Где:

-   Тип-вершинный тип данных. См. [**D3DDECLTYPE**](./d3ddecltype.md).
-   Метод обработки для тесселяции метода. См. [**D3DDECLMETHOD**](./d3ddeclmethod.md).
-   Использование данных вершин, предназначенное для использования. См. [**D3DDECLUSAGE**](./d3ddeclusage.md).
-   Усажеиндекс — изменяет данные об использовании. См. [**D3DDECLUSAGE**](./d3ddeclusage.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)
</dt> </dl>

 

 
