---
description: Патчмеш определяет сетку, определенную с помощью исправлений Безье, включая список вершин и исправлений для сетки путем индексирования в массив вершин.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: патчмеш
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3bc3c243fb42014ba18aac134ea008d5818e249a601858be6724d5a0fd7310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746924"
---
# <a name="patchmesh"></a>патчмеш

Определяет сетку, определенную с помощью исправлений Безье. Первый массив представляет собой список вершин, а второй массив определяет исправления для сетки путем индексирования в массиве вершин.

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

Где:

-   Нвертицес — число вершин.
-   вершины \[ нвертицес \] — массив вершин. См. раздел [**vector**](vector.md).
-   Нпатчес — число исправлений.
-   исправления \[ нпатчес \] — массив исправлений. См. [**исправление**](patch.md).
-   \[ ... \] -Здесь можно использовать любой шаблон файла. x. Это делает архитектуру расширяемой.

Исправления используют вершины в массиве вершин в качестве контрольных точек для каждого исправления. Это устаревший шаблон. Последний шаблон сетки исправлений — [**PatchMesh9**](patchmesh9.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



