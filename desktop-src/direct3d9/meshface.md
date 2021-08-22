---
description: Используется шаблоном сетки для определения граней сетки. Каждый элемент массива Нфацевертексиндицес ссылается на вершину сетки, используемую для создания грани.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: мешфаце
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ea35d1db9e33644638455bc42cc2cbef320f748d96b086037dea6f10607dbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563534"
---
# <a name="meshface"></a>мешфаце

Используется шаблоном [**сетки**](mesh.md) для определения граней сетки. Каждый элемент массива Нфацевертексиндицес ссылается на вершину сетки, используемую для создания грани.

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

Где:

-   Нфацевертексиндицес — количество индексов.
-   Array DWORD Фацевертексиндицес \[ нфацевертексиндицес \] -массив индексов.

## <a name="see-also"></a>См. также

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



