---
description: Сочетание одного или нескольких флагов, управляющих поведением при создании устройства.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ee7e5d423169e561df28b5d69017c77a71e183
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998661"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="d4b9e-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="d4b9e-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="d4b9e-104">Сочетание одного или нескольких флагов, управляющих поведением при создании устройства.</span><span class="sxs-lookup"><span data-stu-id="d4b9e-104">A combination of one or more flags that control the device create behavior.</span></span>



| <span data-ttu-id="d4b9e-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="d4b9e-105">\#define</span></span>                                | <span data-ttu-id="d4b9e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d4b9e-106">Description</span></span>                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b9e-107">D3DVTXPCAPS \_ директионаллигхтс</span><span class="sxs-lookup"><span data-stu-id="d4b9e-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="d4b9e-108">Устройство может выполнять направленный свет.</span><span class="sxs-lookup"><span data-stu-id="d4b9e-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="d4b9e-109">D3DVTXPCAPS \_ локалвиевер</span><span class="sxs-lookup"><span data-stu-id="d4b9e-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="d4b9e-110">Устройство может выполнять локальное средство просмотра.</span><span class="sxs-lookup"><span data-stu-id="d4b9e-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="d4b9e-111">D3DVTXPCAPS \_ MATERIALSOURCE7</span><span class="sxs-lookup"><span data-stu-id="d4b9e-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="d4b9e-112">Если эта политика установлена, устройство поддерживает цветовые материальные состояния: D3DRS \_ амбиентматериалсаурце, D3DRS \_ ДИФФУСЕМАТЕРИАЛСАУРЦЕ, D3DRS \_ емиссивематериалсаурце и D3DRS \_ спекуларматериалсаурце.</span><span class="sxs-lookup"><span data-stu-id="d4b9e-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="d4b9e-113">D3DVTXPCAPS \_ No \_ тексжен \_ нонлокалвиевер</span><span class="sxs-lookup"><span data-stu-id="d4b9e-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="d4b9e-114">Устройство не поддерживает создание текстур в режиме нелокального просмотра.</span><span class="sxs-lookup"><span data-stu-id="d4b9e-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="d4b9e-115">D3DVTXPCAPS \_ поситионаллигхтс</span><span class="sxs-lookup"><span data-stu-id="d4b9e-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="d4b9e-116">Устройство может выполнять позиционированные источники света (включая точку и место).</span><span class="sxs-lookup"><span data-stu-id="d4b9e-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="d4b9e-117">D3DVTXPCAPS \_ тексжен</span><span class="sxs-lookup"><span data-stu-id="d4b9e-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="d4b9e-118">Устройство может выполнять тексжен.</span><span class="sxs-lookup"><span data-stu-id="d4b9e-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="d4b9e-119">D3DVTXPCAPS \_ тексжен \_ сферемап</span><span class="sxs-lookup"><span data-stu-id="d4b9e-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="d4b9e-120">Устройство поддерживает D3DTSS \_ тЦи \_ сферемап.</span><span class="sxs-lookup"><span data-stu-id="d4b9e-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="d4b9e-121">Tween — D3DVTXPCAPS \_</span><span class="sxs-lookup"><span data-stu-id="d4b9e-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="d4b9e-122">Устройство может выполнять анимацию вершин.</span><span class="sxs-lookup"><span data-stu-id="d4b9e-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="d4b9e-123">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="d4b9e-123">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="d4b9e-124">Header</span><span class="sxs-lookup"><span data-stu-id="d4b9e-124">Header</span></span>                   | <span data-ttu-id="d4b9e-125">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="d4b9e-125">d3d9caps.h</span></span> |
| <span data-ttu-id="d4b9e-126">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="d4b9e-126">Minimum operating system</span></span> | <span data-ttu-id="d4b9e-127">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d4b9e-127">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d4b9e-128">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d4b9e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4b9e-129">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="d4b9e-129">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



