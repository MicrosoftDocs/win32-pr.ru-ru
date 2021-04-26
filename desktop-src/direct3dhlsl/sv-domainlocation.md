---
title: SV_DomainLocation
description: Определяет расположение поверхности текущей доменной точки.
ms.assetid: 907f568c-7c45-41e5-96c4-6e6b816a4a53
keywords:
- SV_DomainLocation HLSL
topic_type:
- apiref
api_name:
- SV_DomainLocation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb9265734663881981f1626db6e23c6b7dd9415a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996511"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="674c0-104">ОКП \_ домаинлокатион</span><span class="sxs-lookup"><span data-stu-id="674c0-104">SV\_DomainLocation</span></span>

<span data-ttu-id="674c0-105">Определяет расположение поверхности текущей доменной точки.</span><span class="sxs-lookup"><span data-stu-id="674c0-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="674c0-106">Тип</span><span class="sxs-lookup"><span data-stu-id="674c0-106">Type</span></span>



|        |                |
|--------|----------------|
| <span data-ttu-id="674c0-107">Тип</span><span class="sxs-lookup"><span data-stu-id="674c0-107">Type</span></span>   | <span data-ttu-id="674c0-108">Топология ввода</span><span class="sxs-lookup"><span data-stu-id="674c0-108">Input Topology</span></span> |
| <span data-ttu-id="674c0-109">float2</span><span class="sxs-lookup"><span data-stu-id="674c0-109">float2</span></span> | <span data-ttu-id="674c0-110">четыре исправления</span><span class="sxs-lookup"><span data-stu-id="674c0-110">quad patch</span></span>     |
| <span data-ttu-id="674c0-111">float3</span><span class="sxs-lookup"><span data-stu-id="674c0-111">float3</span></span> | <span data-ttu-id="674c0-112">три исправления</span><span class="sxs-lookup"><span data-stu-id="674c0-112">tri patch</span></span>      |
| <span data-ttu-id="674c0-113">float2</span><span class="sxs-lookup"><span data-stu-id="674c0-113">float2</span></span> | <span data-ttu-id="674c0-114">исолине</span><span class="sxs-lookup"><span data-stu-id="674c0-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="674c0-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="674c0-115">Remarks</span></span>

<span data-ttu-id="674c0-116">Это системное значение является обязательным.</span><span class="sxs-lookup"><span data-stu-id="674c0-116">This system value is required.</span></span>

<span data-ttu-id="674c0-117">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="674c0-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="674c0-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="674c0-118">Vertex</span></span> | <span data-ttu-id="674c0-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="674c0-119">Hull</span></span> | <span data-ttu-id="674c0-120">Домен</span><span class="sxs-lookup"><span data-stu-id="674c0-120">Domain</span></span> | <span data-ttu-id="674c0-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="674c0-121">Geometry</span></span> | <span data-ttu-id="674c0-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="674c0-122">Pixel</span></span> | <span data-ttu-id="674c0-123">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="674c0-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      | <span data-ttu-id="674c0-124">x</span><span class="sxs-lookup"><span data-stu-id="674c0-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="674c0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="674c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="674c0-126">Семантика</span><span class="sxs-lookup"><span data-stu-id="674c0-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="674c0-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="674c0-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




