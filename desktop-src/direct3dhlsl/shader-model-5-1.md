---
title: Модель шейдера 5,1
description: В этом разделе содержатся справочные страницы для модели шейдеров HLSL 5,1, которая появилась в D3D12.
ms.assetid: 814FAC95-7FD5-450F-964B-18E687DBCC56
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5fd2f2a2f4ebe86a090ebade8ebf8a033a7c612
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996891"
---
# <a name="shader-model-51"></a><span data-ttu-id="b305e-103">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="b305e-103">Shader Model 5.1</span></span>

<span data-ttu-id="b305e-104">В этом разделе содержатся справочные страницы для модели шейдеров HLSL 5,1, которая появилась в D3D12.</span><span class="sxs-lookup"><span data-stu-id="b305e-104">This section contains the reference pages for HLSL Shader Model 5.1, introduced with D3D12.</span></span>

<span data-ttu-id="b305e-105">Модель шейдеров 5,1 функционально похожа на [модель шейдера 5](d3d11-graphics-reference-sm5.md). Основное изменение является большей гибкостью выбора ресурсов за счет возможности индексации массивов дескрипторов из шейдера.</span><span class="sxs-lookup"><span data-stu-id="b305e-105">Shader Model 5.1 is functionally very similar to [Shader Model 5](d3d11-graphics-reference-sm5.md), the main change is more flexibility in resource selection by allowing indexing of arrays of descriptors from within a shader.</span></span>



| <span data-ttu-id="b305e-106">Компонент</span><span class="sxs-lookup"><span data-stu-id="b305e-106">Feature</span></span>                   | <span data-ttu-id="b305e-107">Возможностями.</span><span class="sxs-lookup"><span data-stu-id="b305e-107">Capability</span></span>                                                                |
|---------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b305e-108">Набор инструкций</span><span class="sxs-lookup"><span data-stu-id="b305e-108">Instruction Set</span></span>           | [<span data-ttu-id="b305e-109">**Встроенные функции HLSL**</span><span class="sxs-lookup"><span data-stu-id="b305e-109">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)  |
| <span data-ttu-id="b305e-110">Максимум вершинного шейдера</span><span class="sxs-lookup"><span data-stu-id="b305e-110">Vertex Shader Max</span></span>         | <span data-ttu-id="b305e-111">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="b305e-111">No restriction</span></span>                                                            |
| <span data-ttu-id="b305e-112">Максимальный размер шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="b305e-112">Pixel Shader Max</span></span>          | <span data-ttu-id="b305e-113">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="b305e-113">No restriction</span></span>                                                            |
| <span data-ttu-id="b305e-114">Добавлены новые профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="b305e-114">New Shader Profiles Added</span></span> | <span data-ttu-id="b305e-115">CS \_ 5 \_ 1, DS \_ 5 \_ 1, GS \_ 5 \_ 1, HS \_ 5 \_ 1, PS \_ 5 \_ 1, VS \_ 5 \_ 1, рутсиг \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b305e-115">cs\_5\_1, ds\_5\_1, gs\_5\_1, hs\_5\_1, ps\_5\_1, vs\_5\_1, rootsig\_1\_0</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="b305e-116">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b305e-116">In this section</span></span>



| <span data-ttu-id="b305e-117">Раздел</span><span class="sxs-lookup"><span data-stu-id="b305e-117">Topic</span></span>                                                                           | <span data-ttu-id="b305e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="b305e-118">Description</span></span>                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b305e-119">Объекты модели шейдеров 5,1</span><span class="sxs-lookup"><span data-stu-id="b305e-119">Shader Model 5.1 Objects</span></span>](shader-model-5-1-objects.md)<br/>             | <span data-ttu-id="b305e-120">В модель шейдера 5,1 добавлены следующие объекты.</span><span class="sxs-lookup"><span data-stu-id="b305e-120">The following objects have been added to shader model 5.1.</span></span><br/> |
| [<span data-ttu-id="b305e-121">Системные значения модели шейдеров 5,1</span><span class="sxs-lookup"><span data-stu-id="b305e-121">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)<br/> | <span data-ttu-id="b305e-122">В модели шейдеров 5,1 добавлены следующие новые системные значения.</span><span class="sxs-lookup"><span data-stu-id="b305e-122">Shader Model 5.1 adds the following new system values.</span></span><br/>     |



 

## <a name="related-topics"></a><span data-ttu-id="b305e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b305e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b305e-124">Модели шейдеров и профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="b305e-124">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> <dt>

[<span data-ttu-id="b305e-125">Функции HLSL Shader Model 5,1 для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b305e-125">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 





