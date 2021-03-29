---
description: Флаги возможностей координат текстуры в драйвере.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4973e045decd393be2f8a6d340f369761a411a44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990750"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="9c8d6-103">D3DTSS \_ тЦи</span><span class="sxs-lookup"><span data-stu-id="9c8d6-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="9c8d6-104">Флаги возможностей координат текстуры в драйвере.</span><span class="sxs-lookup"><span data-stu-id="9c8d6-104">Driver texture coordinate capability flags.</span></span>



|                                          |             |                                                                                                                                                                                                                      |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c8d6-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="9c8d6-105">\#define</span></span>                                 | <span data-ttu-id="9c8d6-106">Значение</span><span class="sxs-lookup"><span data-stu-id="9c8d6-106">Value</span></span>       | <span data-ttu-id="9c8d6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9c8d6-107">Description</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="9c8d6-108">D3DTSS \_ тЦи \_ пропускания</span><span class="sxs-lookup"><span data-stu-id="9c8d6-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="9c8d6-109">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c8d6-109">0x00000000L</span></span> | <span data-ttu-id="9c8d6-110">Используйте указанные координаты текстуры, содержащиеся в формате вершины.</span><span class="sxs-lookup"><span data-stu-id="9c8d6-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="9c8d6-111">Это значение разрешается в ноль.</span><span class="sxs-lookup"><span data-stu-id="9c8d6-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="9c8d6-112">D3DTSS \_ тЦи \_ камераспаценормал</span><span class="sxs-lookup"><span data-stu-id="9c8d6-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="9c8d6-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="9c8d6-113">0x00010000L</span></span> | <span data-ttu-id="9c8d6-114">Используйте нормальную вершину, преобразованную в пространство камеры, в качестве координат входной текстуры для преобразования текстур этого этапа.</span><span class="sxs-lookup"><span data-stu-id="9c8d6-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="9c8d6-115">D3DTSS \_ тЦи \_ камераспацепоситион</span><span class="sxs-lookup"><span data-stu-id="9c8d6-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="9c8d6-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="9c8d6-116">0x00020000L</span></span> | <span data-ttu-id="9c8d6-117">Используйте расположение вершины, преобразованное в область камеры, в качестве координат входной текстуры для преобразования текстур этого этапа.</span><span class="sxs-lookup"><span data-stu-id="9c8d6-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="9c8d6-118">D3DTSS \_ тЦи \_ камераспацерефлектионвектор</span><span class="sxs-lookup"><span data-stu-id="9c8d6-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="9c8d6-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="9c8d6-119">0x00030000L</span></span> | <span data-ttu-id="9c8d6-120">Используйте Вектор отражения, преобразованный в пространство камеры, как входную координату текстуры для преобразования текстур этого этапа.</span><span class="sxs-lookup"><span data-stu-id="9c8d6-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="9c8d6-121">Вектор отражения вычисляются на основе расположения входной вершины и обычного вектора.</span><span class="sxs-lookup"><span data-stu-id="9c8d6-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="9c8d6-122">D3DTSS \_ тЦи \_ сферемап</span><span class="sxs-lookup"><span data-stu-id="9c8d6-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="9c8d6-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="9c8d6-123">0x00040000L</span></span> | <span data-ttu-id="9c8d6-124">Используйте указанные координаты текстуры для сопоставления сфер.</span><span class="sxs-lookup"><span data-stu-id="9c8d6-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="9c8d6-125">Эти константы используются D3DTSS \_ текскурдиндекс.</span><span class="sxs-lookup"><span data-stu-id="9c8d6-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="9c8d6-126">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="9c8d6-126">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="9c8d6-127">Header</span><span class="sxs-lookup"><span data-stu-id="9c8d6-127">Header</span></span>                   | <span data-ttu-id="9c8d6-128">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="9c8d6-128">d3d9caps.h</span></span> |
| <span data-ttu-id="9c8d6-129">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="9c8d6-129">Minimum operating system</span></span> | <span data-ttu-id="9c8d6-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9c8d6-130">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9c8d6-131">См. также</span><span class="sxs-lookup"><span data-stu-id="9c8d6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c8d6-132">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="9c8d6-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



