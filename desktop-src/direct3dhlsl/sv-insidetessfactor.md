---
title: SV_InsideTessFactor
description: Определяет объем тесселяции в области исправления.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90d31aa6a11ce8e2bdd75ff1171705cc9b3de437
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826618"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="9cf7b-104">ОКП \_ инсидетессфактор</span><span class="sxs-lookup"><span data-stu-id="9cf7b-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="9cf7b-105">Определяет объем тесселяции в области исправления.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="9cf7b-106">Тип</span><span class="sxs-lookup"><span data-stu-id="9cf7b-106">Type</span></span>



|  <span data-ttu-id="9cf7b-107">Тип</span><span class="sxs-lookup"><span data-stu-id="9cf7b-107">Type</span></span>          | <span data-ttu-id="9cf7b-108">Топология ввода</span><span class="sxs-lookup"><span data-stu-id="9cf7b-108">Input topology</span></span>               |
|------------|----------------|
| <span data-ttu-id="9cf7b-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="9cf7b-109">float\[2\]</span></span> | <span data-ttu-id="9cf7b-110">четыре исправления</span><span class="sxs-lookup"><span data-stu-id="9cf7b-110">quad patch</span></span>     |
| <span data-ttu-id="9cf7b-111">FLOAT</span><span class="sxs-lookup"><span data-stu-id="9cf7b-111">float</span></span>      | <span data-ttu-id="9cf7b-112">три исправления</span><span class="sxs-lookup"><span data-stu-id="9cf7b-112">tri patch</span></span>      |
| <span data-ttu-id="9cf7b-113">unused</span><span class="sxs-lookup"><span data-stu-id="9cf7b-113">unused</span></span>     | <span data-ttu-id="9cf7b-114">исолине</span><span class="sxs-lookup"><span data-stu-id="9cf7b-114">isoline</span></span>        |



 

<span data-ttu-id="9cf7b-115">Факторы тесселяции должны быть объявлены как массив. они не могут быть упакованы в один вектор.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cf7b-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="9cf7b-116">Remarks</span></span>

<span data-ttu-id="9cf7b-117">Это значение должно быть определено во время функции Constant исправления шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="9cf7b-118">Обязательное выходное значение для шейдера поверхности при использовании исправлений с четырьмя или тремя обновлениями.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="9cf7b-119">Это значение является обязательным входом для шейдера домена, чтобы оборудование соответствовало сигнатурам через тесселяцию.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="9cf7b-120">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9cf7b-120">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="9cf7b-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="9cf7b-121">Vertex</span></span> | <span data-ttu-id="9cf7b-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9cf7b-122">Hull</span></span> | <span data-ttu-id="9cf7b-123">Домен</span><span class="sxs-lookup"><span data-stu-id="9cf7b-123">Domain</span></span> | <span data-ttu-id="9cf7b-124">Geometry</span><span class="sxs-lookup"><span data-stu-id="9cf7b-124">Geometry</span></span> | <span data-ttu-id="9cf7b-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9cf7b-125">Pixel</span></span> | <span data-ttu-id="9cf7b-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9cf7b-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="9cf7b-127">x</span><span class="sxs-lookup"><span data-stu-id="9cf7b-127">x</span></span>    | <span data-ttu-id="9cf7b-128">x</span><span class="sxs-lookup"><span data-stu-id="9cf7b-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="9cf7b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cf7b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cf7b-130">Семантика</span><span class="sxs-lookup"><span data-stu-id="9cf7b-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="9cf7b-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9cf7b-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




