---
description: PatchMesh9 определяет сетку, определенную с помощью исправлений Безье, включая список вершин и исправлений для сетки путем индексирования в массив вершин.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404707"
---
# <a name="patchmesh9"></a>PatchMesh9

Определяет сетку, определенную с помощью исправлений Безье. Первый массив представляет собой список вершин, а второй массив определяет исправления для сетки путем индексирования в массиве вершин.

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

Где:

-   Тип сетки типа исправления: прямоугольник, треугольник или N-patch.
-   Градусы переменных в уравнении кривой.
-   Базовый тип поверхности исправления высокого порядка.
-   Нвертицес — число вершин.
-   вершины \[ нвертицес \] — массив вершин. См. раздел [**vector**](vector.md).
-   Нпатчес — число исправлений.
-   исправления \[ нпатчес \] — массив исправлений. См. [**исправление**](patch.md).
-   \[ ... \] -Здесь можно использовать любой шаблон файла. x. Это делает архитектуру расширяемой.

Исправления используют вершины в массиве вершин в качестве контрольных точек для каждого исправления.

## <a name="see-also"></a>См. также

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



