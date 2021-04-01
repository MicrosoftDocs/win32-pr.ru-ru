---
description: Определяет нормали для сетки.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: мешнормалс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65b9e0ffc89af5a0a55ef7bd1fa2575a4943137e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262408"
---
# <a name="meshnormals"></a><span data-ttu-id="f9f83-103">мешнормалс</span><span class="sxs-lookup"><span data-stu-id="f9f83-103">MeshNormals</span></span>

<span data-ttu-id="f9f83-104">Определяет нормали для сетки.</span><span class="sxs-lookup"><span data-stu-id="f9f83-104">Defines normals for a mesh.</span></span> <span data-ttu-id="f9f83-105">Первый массив векторов — это обычные векторы, а второй массив — это массив индексов, указывающий, какие нормали должны применяться к данной грани.</span><span class="sxs-lookup"><span data-stu-id="f9f83-105">The first array of vectors is the normal vectors themselves, and the second array is an array of indexes specifying which normals should be applied to a given face.</span></span> <span data-ttu-id="f9f83-106">Значение элемента Нфаценормалс должно быть равно числу граней в сети.</span><span class="sxs-lookup"><span data-stu-id="f9f83-106">The value of the nFaceNormals member should be equal to the number of faces in a mesh.</span></span>

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

<span data-ttu-id="f9f83-107">Где:</span><span class="sxs-lookup"><span data-stu-id="f9f83-107">Where:</span></span>

-   <span data-ttu-id="f9f83-108">Ннормалс — число нормалей.</span><span class="sxs-lookup"><span data-stu-id="f9f83-108">nNormals - Number of normals.</span></span>
-   <span data-ttu-id="f9f83-109">Векторы массивов нормали \[ ннормалс \] -Array нормалей.</span><span class="sxs-lookup"><span data-stu-id="f9f83-109">array Vector normals\[nNormals\] - Array of normals.</span></span> <span data-ttu-id="f9f83-110">См. раздел [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="f9f83-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="f9f83-111">Нфаценормалс — число нормальных граней.</span><span class="sxs-lookup"><span data-stu-id="f9f83-111">nFaceNormals - Number of face normals.</span></span>
-   <span data-ttu-id="f9f83-112">Array Мешфаце Фаценормалс \[ нфаценормалс \] -массив нормалей граней.</span><span class="sxs-lookup"><span data-stu-id="f9f83-112">array MeshFace faceNormals\[nFaceNormals\] - Array of mesh face normals.</span></span> <span data-ttu-id="f9f83-113">См. [**мешфаце**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="f9f83-113">See [**MeshFace**](meshface.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f9f83-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9f83-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f83-115">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="f9f83-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



