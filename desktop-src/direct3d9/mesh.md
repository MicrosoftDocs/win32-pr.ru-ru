---
description: Определяет простую сетку. Первый массив представляет собой список вершин, а второй массив определяет грани сетки путем индексации в массив вершин.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Сетка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ce4cf6fb6a3eee3417a7d0fe1594164c1e22df9d118f4f995955f8070fc015
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119240744"
---
# <a name="mesh"></a>Сетка

Определяет простую сетку. Первый массив представляет собой список вершин, а второй массив определяет грани сетки путем индексации в массив вершин.

``` syntax
template Mesh
{
    <3D82AB44-62DA-11CF-AB39-0020AF71E433>
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nFaces;
    array MeshFace faces[nFaces];
    [...]
}
```

Где:

-   Нвертицес — число вершин.
-   вершины вектора массива \[ нвертицес \] — массив вершин, каждый из которых имеет тип Vector. См. раздел [**vector**](vector.md).
-   Нфацес — число граней.
-   Array Мешфаце Face \[ нфацес \] — массив лиц, каждый из которых имеет тип мешфаце. См. [**мешфаце**](meshface.md).
-   \[ ... \] -Здесь можно использовать любой шаблон файла. x. Это делает архитектуру расширяемой. Обычно используются шаблоны [**Material**](material.md) и [**текстурефиленаме**](texturefilename.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



