---
description: Определяет простую сетку. Первый массив представляет собой список вершин, а второй массив определяет грани сетки путем индексации в массив вершин.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Сетка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced60785a5f013db7fc26e4d203119a160953b65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494277"
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

 

 



