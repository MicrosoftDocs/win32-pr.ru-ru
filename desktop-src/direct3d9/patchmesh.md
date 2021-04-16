---
description: Определяет сетку, определенную с помощью исправлений Безье. Первый массив представляет собой список вершин, а второй массив определяет исправления для сетки путем индексирования в массиве вершин.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: патчмеш
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536821"
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

 

 



