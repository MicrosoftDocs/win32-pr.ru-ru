---
description: Используется шаблоном сетки для определения граней сетки. Каждый элемент массива Нфацевертексиндицес ссылается на вершину сетки, используемую для создания грани.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: мешфаце
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9e8b73efb214f7a767d986830cccc83ee6cbc1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139282"
---
# <a name="meshface"></a><span data-ttu-id="f8ac8-104">мешфаце</span><span class="sxs-lookup"><span data-stu-id="f8ac8-104">MeshFace</span></span>

<span data-ttu-id="f8ac8-105">Используется шаблоном [**сетки**](mesh.md) для определения граней сетки.</span><span class="sxs-lookup"><span data-stu-id="f8ac8-105">Used by the [**Mesh**](mesh.md) template to define a mesh's faces.</span></span> <span data-ttu-id="f8ac8-106">Каждый элемент массива Нфацевертексиндицес ссылается на вершину сетки, используемую для создания грани.</span><span class="sxs-lookup"><span data-stu-id="f8ac8-106">Each element of the nFaceVertexIndices array references a mesh vertex used to build the face.</span></span>

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

<span data-ttu-id="f8ac8-107">Где:</span><span class="sxs-lookup"><span data-stu-id="f8ac8-107">Where:</span></span>

-   <span data-ttu-id="f8ac8-108">Нфацевертексиндицес — количество индексов.</span><span class="sxs-lookup"><span data-stu-id="f8ac8-108">nFaceVertexIndices - Number of indices.</span></span>
-   <span data-ttu-id="f8ac8-109">Array DWORD Фацевертексиндицес \[ нфацевертексиндицес \] -массив индексов.</span><span class="sxs-lookup"><span data-stu-id="f8ac8-109">array DWORD faceVertexIndices\[nFaceVertexIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8ac8-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8ac8-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ac8-111">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="f8ac8-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



