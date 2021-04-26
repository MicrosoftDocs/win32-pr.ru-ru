---
description: Флаги возможностей драйвера D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ef30540f19add130aaca6eb48655a5ac47b2b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999471"
---
# <a name="d3ddevcaps2"></a><span data-ttu-id="9e5ba-103">D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="9e5ba-103">D3DDEVCAPS2</span></span>

<span data-ttu-id="9e5ba-104">Флаги возможностей драйвера D3DDEVCAPS2.</span><span class="sxs-lookup"><span data-stu-id="9e5ba-104">D3DDEVCAPS2 driver capability flags.</span></span>



| <span data-ttu-id="9e5ba-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="9e5ba-105">\#define</span></span>                                        | <span data-ttu-id="9e5ba-106">Описание</span><span class="sxs-lookup"><span data-stu-id="9e5ba-106">Description</span></span>                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5ba-107">D3DDEVCAPS2 \_ адаптиветессртпатч</span><span class="sxs-lookup"><span data-stu-id="9e5ba-107">D3DDEVCAPS2\_ADAPTIVETESSRTPATCH</span></span>                | <span data-ttu-id="9e5ba-108">Устройство поддерживает адаптивную тесселяцию RT-патчей</span><span class="sxs-lookup"><span data-stu-id="9e5ba-108">Device supports adaptive tessellation of RT-patches</span></span>                                                                                                                                                                       |
| <span data-ttu-id="9e5ba-109">D3DDEVCAPS2 \_ адаптиветесснпатч</span><span class="sxs-lookup"><span data-stu-id="9e5ba-109">D3DDEVCAPS2\_ADAPTIVETESSNPATCH</span></span>                 | <span data-ttu-id="9e5ba-110">Устройство поддерживает адаптивную тесселяцию N-патчей.</span><span class="sxs-lookup"><span data-stu-id="9e5ba-110">Device supports adaptive tessellation of N-patches.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="9e5ba-111">D3DDEVCAPS2 \_ может \_ стретчрект \_ из \_ текстур</span><span class="sxs-lookup"><span data-stu-id="9e5ba-111">D3DDEVCAPS2\_CAN\_STRETCHRECT\_FROM\_TEXTURES</span></span>   | <span data-ttu-id="9e5ba-112">Устройство поддерживает [**стретчрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) , используя текстуру в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="9e5ba-112">Device supports [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) using a texture as the source.</span></span>                                                                                                                       |
| <span data-ttu-id="9e5ba-113">D3DDEVCAPS2 \_ дмапнпатч</span><span class="sxs-lookup"><span data-stu-id="9e5ba-113">D3DDEVCAPS2\_DMAPNPATCH</span></span>                         | <span data-ttu-id="9e5ba-114">Устройство поддерживает карты смещения для N-патчей.</span><span class="sxs-lookup"><span data-stu-id="9e5ba-114">Device supports displacement maps for N-patches.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="9e5ba-115">D3DDEVCAPS2 \_ пресампледдмапнпатч</span><span class="sxs-lookup"><span data-stu-id="9e5ba-115">D3DDEVCAPS2\_PRESAMPLEDDMAPNPATCH</span></span>               | <span data-ttu-id="9e5ba-116">Устройство поддерживает предварительно выбранные карты смещения для N-патчей.</span><span class="sxs-lookup"><span data-stu-id="9e5ba-116">Device supports presampled displacement maps for N-patches.</span></span> <span data-ttu-id="9e5ba-117">Дополнительные сведения о сопоставлении замещения см. в разделе [сопоставление смещения (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="9e5ba-117">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span>                                           |
| <span data-ttu-id="9e5ba-118">D3DDEVCAPS2 \_ стреамоффсет</span><span class="sxs-lookup"><span data-stu-id="9e5ba-118">D3DDEVCAPS2\_STREAMOFFSET</span></span>                       | <span data-ttu-id="9e5ba-119">Устройство поддерживает смещения потоков.</span><span class="sxs-lookup"><span data-stu-id="9e5ba-119">Device supports stream offsets.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="9e5ba-120">D3DDEVCAPS2 \_ вертекселементсканшарестреамоффсет</span><span class="sxs-lookup"><span data-stu-id="9e5ba-120">D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET</span></span> | <span data-ttu-id="9e5ba-121">Несколько элементов вершин могут совместно использовать одно и то же смещение в потоке, если D3DDEVCAPS2 \_ вертекселементсканшарестреамоффсет задано устройством, а объявление вершины не содержит элемент с D3DDECLUSAGE \_ POSITIONT0.</span><span class="sxs-lookup"><span data-stu-id="9e5ba-121">Multiple vertex elements can share the same offset in a stream if D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET is set by the device and the vertex declaration does not have an element with D3DDECLUSAGE\_POSITIONT0.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="9e5ba-122">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="9e5ba-122">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="9e5ba-123">Header</span><span class="sxs-lookup"><span data-stu-id="9e5ba-123">Header</span></span>                   | <span data-ttu-id="9e5ba-124">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="9e5ba-124">d3d9caps.h</span></span> |
| <span data-ttu-id="9e5ba-125">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="9e5ba-125">Minimum operating system</span></span> | <span data-ttu-id="9e5ba-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9e5ba-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9e5ba-127">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9e5ba-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e5ba-128">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="9e5ba-128">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
