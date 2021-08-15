---
description: Используется в объекте сетки для указания материала, к которому относится этот объект. Элемент Нматериалс указывает, сколько материалов имеется, а материалы указывают, какой материал следует применить.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: мешматериаллист
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ef1d200e5f6a6913f996c186e121a8390de01e8f3347b6dcbaeac8eeefa708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798790"
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

 

 



