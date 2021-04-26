---
title: SV_DispatchThreadID
description: Индексы, для которых в объединенном потоке и группе потоков выполняется шейдер вычислений.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9653d98ebbfef6dd25bb137af3358a14d177f3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996521"
---
# <a name="sv_dispatchthreadid"></a><span data-ttu-id="a6f3a-104">ОКП \_ диспатчсреадид</span><span class="sxs-lookup"><span data-stu-id="a6f3a-104">SV\_DispatchThreadID</span></span>

<span data-ttu-id="a6f3a-105">Индексы, для которых в объединенном потоке и группе потоков выполняется шейдер вычислений.</span><span class="sxs-lookup"><span data-stu-id="a6f3a-105">Indices for which combined thread and thread group a compute shader is executing in.</span></span> <span data-ttu-id="a6f3a-106">ОКП \_ диспатчсреадид — это сумма значений ОКП \_ groupId \* numthreads и граупсреадид.</span><span class="sxs-lookup"><span data-stu-id="a6f3a-106">SV\_DispatchThreadID is the sum of SV\_GroupID \* numthreads and GroupThreadID.</span></span> <span data-ttu-id="a6f3a-107">Он зависит от диапазона, указанного в поле [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md).</span><span class="sxs-lookup"><span data-stu-id="a6f3a-107">It varies across the range specified in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md).</span></span> <span data-ttu-id="a6f3a-108">Например, если метод Dispatch (2, 2, 2) вызывается для Compute Shader с numthreads (3, 3, 3) ОКП \_ диспатчсреадид будет иметь диапазон 0.. 5 для каждого измерения.</span><span class="sxs-lookup"><span data-stu-id="a6f3a-108">For example if Dispatch(2,2,2) is called on a compute shader with numthreads(3,3,3) SV\_DispatchThreadID will have a range of 0..5 for each dimension.</span></span>

## <a name="type"></a><span data-ttu-id="a6f3a-109">Тип</span><span class="sxs-lookup"><span data-stu-id="a6f3a-109">Type</span></span>



|       |
|-------|
| <span data-ttu-id="a6f3a-110">Тип</span><span class="sxs-lookup"><span data-stu-id="a6f3a-110">Type</span></span>  |
| <span data-ttu-id="a6f3a-111">uint3</span><span class="sxs-lookup"><span data-stu-id="a6f3a-111">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a6f3a-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6f3a-112">Remarks</span></span>

<span data-ttu-id="a6f3a-113">Это системное значение является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a6f3a-113">This system value is optional.</span></span>

<span data-ttu-id="a6f3a-114">На следующем рисунке показана связь между параметрами, передаваемыми для [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), диспетчеризации (5, 3, 2), значениями, указанными в атрибуте [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3), и значениями, которые будут переданы в шейдер вычислений для системных значений, связанных с потоками ([ОКП \_ граупиндекс](sv-groupindex.md), SV \_ диспатчсреадид,[ОКП \_ граупсреадид](sv-groupthreadid.md),[SV \_ groupId](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="a6f3a-114">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),SV\_DispatchThreadID,[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![Иллюстрация связи между диспетчеризация, группами потоков и потоками](images/threadgroupids.png)

<span data-ttu-id="a6f3a-116">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="a6f3a-116">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="a6f3a-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="a6f3a-117">Vertex</span></span> | <span data-ttu-id="a6f3a-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="a6f3a-118">Hull</span></span> | <span data-ttu-id="a6f3a-119">Домен</span><span class="sxs-lookup"><span data-stu-id="a6f3a-119">Domain</span></span> | <span data-ttu-id="a6f3a-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="a6f3a-120">Geometry</span></span> | <span data-ttu-id="a6f3a-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="a6f3a-121">Pixel</span></span> | <span data-ttu-id="a6f3a-122">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="a6f3a-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="a6f3a-123">x</span><span class="sxs-lookup"><span data-stu-id="a6f3a-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a6f3a-124">См. также</span><span class="sxs-lookup"><span data-stu-id="a6f3a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f3a-125">Семантика</span><span class="sxs-lookup"><span data-stu-id="a6f3a-125">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="a6f3a-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="a6f3a-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
