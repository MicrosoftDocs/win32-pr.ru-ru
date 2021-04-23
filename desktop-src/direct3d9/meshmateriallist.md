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
# <a name="meshmateriallist"></a><span data-ttu-id="53cab-104">мешматериаллист</span><span class="sxs-lookup"><span data-stu-id="53cab-104">MeshMaterialList</span></span>

<span data-ttu-id="53cab-105">Используется в объекте сетки для указания материала, к которому относится этот объект.</span><span class="sxs-lookup"><span data-stu-id="53cab-105">Used in a mesh object to specify which material applies to which faces.</span></span> <span data-ttu-id="53cab-106">Элемент Нматериалс указывает, сколько материалов имеется, а материалы указывают, какой материал следует применить.</span><span class="sxs-lookup"><span data-stu-id="53cab-106">The nMaterials member specifies how many materials are present, and materials specify which material to apply.</span></span>

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

<span data-ttu-id="53cab-107">Где:</span><span class="sxs-lookup"><span data-stu-id="53cab-107">Where:</span></span>

-   <span data-ttu-id="53cab-108">Нматериалс — DWORD.</span><span class="sxs-lookup"><span data-stu-id="53cab-108">nMaterials - A DWORD.</span></span> <span data-ttu-id="53cab-109">Количество материалов.</span><span class="sxs-lookup"><span data-stu-id="53cab-109">The number of materials.</span></span>
-   <span data-ttu-id="53cab-110">Нфацеиндексес — DWORD.</span><span class="sxs-lookup"><span data-stu-id="53cab-110">nFaceIndexes - A DWORD.</span></span> <span data-ttu-id="53cab-111">Количество индексов.</span><span class="sxs-lookup"><span data-stu-id="53cab-111">The number of indices.</span></span>
-   <span data-ttu-id="53cab-112">Фацеиндексес \[ нфацеиндексес \] — массив DWORD, содержащий индексы граней.</span><span class="sxs-lookup"><span data-stu-id="53cab-112">faceIndexes\[nFaceIndexes\] - An array of DWORDs containing the face indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="53cab-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53cab-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53cab-114">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="53cab-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



