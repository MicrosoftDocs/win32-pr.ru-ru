---
title: SV_GroupID
description: Индексы для группы потоков, в которой выполняется шейдер вычислений.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf96e1db7dbb93c88ec741e309413dea3df2b01d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997001"
---
# <a name="sv_groupid"></a><span data-ttu-id="dabc9-104">SV \_ groupId</span><span class="sxs-lookup"><span data-stu-id="dabc9-104">SV\_GroupID</span></span>

<span data-ttu-id="dabc9-105">Индексы для группы потоков, в которой выполняется шейдер вычислений.</span><span class="sxs-lookup"><span data-stu-id="dabc9-105">Indices for which thread group a compute shader is executing in.</span></span> <span data-ttu-id="dabc9-106">Индексы относятся ко всей группе, а не к отдельному потоку.</span><span class="sxs-lookup"><span data-stu-id="dabc9-106">The indices are to the whole group and not an individual thread.</span></span> <span data-ttu-id="dabc9-107">Возможные значения зависят от диапазона, передаваемого в качестве параметров для [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span><span class="sxs-lookup"><span data-stu-id="dabc9-107">Possible values vary across the range passed as parameters to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span></span> <span data-ttu-id="dabc9-108">Например, вызов диспетчеризации (2, 1, 1) приводит к получению возможных значений 0, 0, 0 и 1, 0, 0.</span><span class="sxs-lookup"><span data-stu-id="dabc9-108">For example calling Dispatch(2,1,1) results in possible values of 0,0,0 and 1,0,0.</span></span>

<span data-ttu-id="dabc9-109">Определяет смещение группы в вызове [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) для каждого измерения вызова диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="dabc9-109">Defines the group offset within a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) call, per dimension of the dispatch call.</span></span>

## <a name="type"></a><span data-ttu-id="dabc9-110">Тип</span><span class="sxs-lookup"><span data-stu-id="dabc9-110">Type</span></span>



|       |
|-------|
| <span data-ttu-id="dabc9-111">Тип</span><span class="sxs-lookup"><span data-stu-id="dabc9-111">Type</span></span>  |
| <span data-ttu-id="dabc9-112">uint3</span><span class="sxs-lookup"><span data-stu-id="dabc9-112">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="dabc9-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="dabc9-113">Remarks</span></span>

<span data-ttu-id="dabc9-114">Это системное значение является необязательным.</span><span class="sxs-lookup"><span data-stu-id="dabc9-114">This system value is optional.</span></span>

<span data-ttu-id="dabc9-115">На следующем рисунке показана связь между параметрами, передаваемыми для [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), диспетчеризации (5, 3, 2), значениями, указанными в атрибуте [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3), и значениями, которые будут переданы в шейдер вычислений для системных значений, связанных с потоками ([ОКП \_ граупиндекс](sv-groupindex.md),[SV \_ диспатчсреадид](sv-dispatchthreadid.md),[ОКП \_ граупсреадид](sv-groupthreadid.md), SV \_ GroupId).</span><span class="sxs-lookup"><span data-stu-id="dabc9-115">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),SV\_GroupID).</span></span>

![Иллюстрация связи между диспетчеризация, группами потоков и потоками](images/threadgroupids.png)

<span data-ttu-id="dabc9-117">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="dabc9-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="dabc9-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="dabc9-118">Vertex</span></span> | <span data-ttu-id="dabc9-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="dabc9-119">Hull</span></span> | <span data-ttu-id="dabc9-120">Домен</span><span class="sxs-lookup"><span data-stu-id="dabc9-120">Domain</span></span> | <span data-ttu-id="dabc9-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="dabc9-121">Geometry</span></span> | <span data-ttu-id="dabc9-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="dabc9-122">Pixel</span></span> | <span data-ttu-id="dabc9-123">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="dabc9-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="dabc9-124">x</span><span class="sxs-lookup"><span data-stu-id="dabc9-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dabc9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="dabc9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dabc9-126">Семантика</span><span class="sxs-lookup"><span data-stu-id="dabc9-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="dabc9-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="dabc9-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
