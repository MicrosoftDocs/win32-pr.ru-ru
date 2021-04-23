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
# <a name="mesh"></a><span data-ttu-id="c45b2-104">Сетка</span><span class="sxs-lookup"><span data-stu-id="c45b2-104">Mesh</span></span>

<span data-ttu-id="c45b2-105">Определяет простую сетку.</span><span class="sxs-lookup"><span data-stu-id="c45b2-105">Defines a simple mesh.</span></span> <span data-ttu-id="c45b2-106">Первый массив представляет собой список вершин, а второй массив определяет грани сетки путем индексации в массив вершин.</span><span class="sxs-lookup"><span data-stu-id="c45b2-106">The first array is a list of vertices, and the second array defines the faces of the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="c45b2-107">Где:</span><span class="sxs-lookup"><span data-stu-id="c45b2-107">Where:</span></span>

-   <span data-ttu-id="c45b2-108">Нвертицес — число вершин.</span><span class="sxs-lookup"><span data-stu-id="c45b2-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="c45b2-109">вершины вектора массива \[ нвертицес \] — массив вершин, каждый из которых имеет тип Vector.</span><span class="sxs-lookup"><span data-stu-id="c45b2-109">array Vector vertices\[nVertices\] - Array of vertices, each of type Vector.</span></span> <span data-ttu-id="c45b2-110">См. раздел [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="c45b2-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="c45b2-111">Нфацес — число граней.</span><span class="sxs-lookup"><span data-stu-id="c45b2-111">nFaces - Number of faces.</span></span>
-   <span data-ttu-id="c45b2-112">Array Мешфаце Face \[ нфацес \] — массив лиц, каждый из которых имеет тип мешфаце.</span><span class="sxs-lookup"><span data-stu-id="c45b2-112">array MeshFace faces\[nFaces\] - Array of faces, each of type MeshFace.</span></span> <span data-ttu-id="c45b2-113">См. [**мешфаце**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="c45b2-113">See [**MeshFace**](meshface.md).</span></span>
-   <span data-ttu-id="c45b2-114">\[ ... \] -Здесь можно использовать любой шаблон файла. x.</span><span class="sxs-lookup"><span data-stu-id="c45b2-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="c45b2-115">Это делает архитектуру расширяемой.</span><span class="sxs-lookup"><span data-stu-id="c45b2-115">This makes the architecture extensible.</span></span> <span data-ttu-id="c45b2-116">Обычно используются шаблоны [**Material**](material.md) и [**текстурефиленаме**](texturefilename.md) .</span><span class="sxs-lookup"><span data-stu-id="c45b2-116">[**Material**](material.md) and [**TextureFilename**](texturefilename.md) templates are typically used.</span></span>

## <a name="see-also"></a><span data-ttu-id="c45b2-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c45b2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c45b2-118">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="c45b2-118">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



