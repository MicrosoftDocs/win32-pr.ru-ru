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
ms.openlocfilehash: fc39a71bcbfb6f3719ecfc7d0abe463a1fd127e4
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827053"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="8eb1c-104">ОКП \_ домаинлокатион</span><span class="sxs-lookup"><span data-stu-id="8eb1c-104">SV\_DomainLocation</span></span>

<span data-ttu-id="8eb1c-105">Определяет расположение поверхности текущей доменной точки.</span><span class="sxs-lookup"><span data-stu-id="8eb1c-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="8eb1c-106">Тип</span><span class="sxs-lookup"><span data-stu-id="8eb1c-106">Type</span></span>



| <span data-ttu-id="8eb1c-107">Тип</span><span class="sxs-lookup"><span data-stu-id="8eb1c-107">Type</span></span>       | <span data-ttu-id="8eb1c-108">Топология ввода</span><span class="sxs-lookup"><span data-stu-id="8eb1c-108">Input topology</span></span>               |
|--------|----------------|
| <span data-ttu-id="8eb1c-109">float2</span><span class="sxs-lookup"><span data-stu-id="8eb1c-109">float2</span></span> | <span data-ttu-id="8eb1c-110">четыре исправления</span><span class="sxs-lookup"><span data-stu-id="8eb1c-110">quad patch</span></span>     |
| <span data-ttu-id="8eb1c-111">float3</span><span class="sxs-lookup"><span data-stu-id="8eb1c-111">float3</span></span> | <span data-ttu-id="8eb1c-112">три исправления</span><span class="sxs-lookup"><span data-stu-id="8eb1c-112">tri patch</span></span>      |
| <span data-ttu-id="8eb1c-113">float2</span><span class="sxs-lookup"><span data-stu-id="8eb1c-113">float2</span></span> | <span data-ttu-id="8eb1c-114">исолине</span><span class="sxs-lookup"><span data-stu-id="8eb1c-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="8eb1c-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="8eb1c-115">Remarks</span></span>

<span data-ttu-id="8eb1c-116">Это системное значение является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8eb1c-116">This system value is required.</span></span>

<span data-ttu-id="8eb1c-117">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8eb1c-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="8eb1c-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="8eb1c-118">Vertex</span></span> | <span data-ttu-id="8eb1c-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8eb1c-119">Hull</span></span> | <span data-ttu-id="8eb1c-120">Домен</span><span class="sxs-lookup"><span data-stu-id="8eb1c-120">Domain</span></span> | <span data-ttu-id="8eb1c-121">Geometry</span><span class="sxs-lookup"><span data-stu-id="8eb1c-121">Geometry</span></span> | <span data-ttu-id="8eb1c-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8eb1c-122">Pixel</span></span> | <span data-ttu-id="8eb1c-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8eb1c-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      | <span data-ttu-id="8eb1c-124">x</span><span class="sxs-lookup"><span data-stu-id="8eb1c-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="8eb1c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8eb1c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb1c-126">Семантика</span><span class="sxs-lookup"><span data-stu-id="8eb1c-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="8eb1c-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8eb1c-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




