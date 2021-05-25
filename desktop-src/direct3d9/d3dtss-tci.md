---
description: Флаги возможностей координат текстуры в драйвере.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58746f17eb18b679a4dfe4957ac46236baeec35d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342979"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="6b464-103">D3DTSS \_ тЦи</span><span class="sxs-lookup"><span data-stu-id="6b464-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="6b464-104">Флаги возможностей координат текстуры в драйвере.</span><span class="sxs-lookup"><span data-stu-id="6b464-104">Driver texture coordinate capability flags.</span></span>



| <span data-ttu-id="6b464-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="6b464-105">\#define</span></span>                                 | <span data-ttu-id="6b464-106">Значение</span><span class="sxs-lookup"><span data-stu-id="6b464-106">Value</span></span>       | <span data-ttu-id="6b464-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6b464-107">Description</span></span>                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b464-108">D3DTSS \_ тЦи \_ пропускания</span><span class="sxs-lookup"><span data-stu-id="6b464-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="6b464-109">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b464-109">0x00000000L</span></span> | <span data-ttu-id="6b464-110">Используйте указанные координаты текстуры, содержащиеся в формате вершины.</span><span class="sxs-lookup"><span data-stu-id="6b464-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="6b464-111">Это значение разрешается в ноль.</span><span class="sxs-lookup"><span data-stu-id="6b464-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="6b464-112">D3DTSS \_ тЦи \_ камераспаценормал</span><span class="sxs-lookup"><span data-stu-id="6b464-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="6b464-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="6b464-113">0x00010000L</span></span> | <span data-ttu-id="6b464-114">Используйте нормальную вершину, преобразованную в пространство камеры, в качестве координат входной текстуры для преобразования текстур этого этапа.</span><span class="sxs-lookup"><span data-stu-id="6b464-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="6b464-115">D3DTSS \_ тЦи \_ камераспацепоситион</span><span class="sxs-lookup"><span data-stu-id="6b464-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="6b464-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="6b464-116">0x00020000L</span></span> | <span data-ttu-id="6b464-117">Используйте расположение вершины, преобразованное в область камеры, в качестве координат входной текстуры для преобразования текстур этого этапа.</span><span class="sxs-lookup"><span data-stu-id="6b464-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="6b464-118">D3DTSS \_ тЦи \_ камераспацерефлектионвектор</span><span class="sxs-lookup"><span data-stu-id="6b464-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="6b464-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="6b464-119">0x00030000L</span></span> | <span data-ttu-id="6b464-120">Используйте Вектор отражения, преобразованный в пространство камеры, как входную координату текстуры для преобразования текстур этого этапа.</span><span class="sxs-lookup"><span data-stu-id="6b464-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="6b464-121">Вектор отражения вычисляются на основе расположения входной вершины и обычного вектора.</span><span class="sxs-lookup"><span data-stu-id="6b464-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="6b464-122">D3DTSS \_ тЦи \_ сферемап</span><span class="sxs-lookup"><span data-stu-id="6b464-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="6b464-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="6b464-123">0x00040000L</span></span> | <span data-ttu-id="6b464-124">Используйте указанные координаты текстуры для сопоставления сфер.</span><span class="sxs-lookup"><span data-stu-id="6b464-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="6b464-125">Эти константы используются D3DTSS \_ текскурдиндекс.</span><span class="sxs-lookup"><span data-stu-id="6b464-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="6b464-126">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="6b464-126">Constant Information</span></span>



|  <span data-ttu-id="6b464-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6b464-127">Requirement</span></span>                        | <span data-ttu-id="6b464-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6b464-128">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="6b464-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6b464-129">Header</span></span>                   | <span data-ttu-id="6b464-130">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="6b464-130">d3d9caps.h</span></span> |
| <span data-ttu-id="6b464-131">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="6b464-131">Minimum operating system</span></span> | <span data-ttu-id="6b464-132">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6b464-132">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6b464-133">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="6b464-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b464-134">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="6b464-134">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



