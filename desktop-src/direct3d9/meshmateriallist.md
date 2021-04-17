---
description: Используется в объекте сетки для указания материала, к которому относится этот объект. Элемент Нматериалс указывает, сколько материалов имеется, а материалы указывают, какой материал следует применить.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: мешматериаллист
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b746802dc3ef54a8feacc8ddfdaa0db1e45112b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710573"
---
# <a name="meshmateriallist"></a>мешматериаллист

Используется в объекте сетки для указания материала, к которому относится этот объект. Элемент Нматериалс указывает, сколько материалов имеется, а материалы указывают, какой материал следует применить.

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

Где:

-   Нматериалс — DWORD. Количество материалов.
-   Нфацеиндексес — DWORD. Количество индексов.
-   Фацеиндексес \[ нфацеиндексес \] — массив DWORD, содержащий индексы граней.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



