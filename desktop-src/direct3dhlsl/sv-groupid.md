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
ms.openlocfilehash: a2588474a4c6f2cfc6d616cdb70940277389fd1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134022"
---
# <a name="sv_groupid"></a><span data-ttu-id="c1473-104">SV \_ groupId</span><span class="sxs-lookup"><span data-stu-id="c1473-104">SV\_GroupID</span></span>

<span data-ttu-id="c1473-105">Индексы для группы потоков, в которой выполняется шейдер вычислений.</span><span class="sxs-lookup"><span data-stu-id="c1473-105">Indices for which thread group a compute shader is executing in.</span></span> <span data-ttu-id="c1473-106">Индексы относятся ко всей группе, а не к отдельному потоку.</span><span class="sxs-lookup"><span data-stu-id="c1473-106">The indices are to the whole group and not an individual thread.</span></span> <span data-ttu-id="c1473-107">Возможные значения зависят от диапазона, передаваемого в качестве параметров для [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span><span class="sxs-lookup"><span data-stu-id="c1473-107">Possible values vary across the range passed as parameters to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span></span> <span data-ttu-id="c1473-108">Например, вызов диспетчеризации (2, 1, 1) приводит к получению возможных значений 0, 0, 0 и 1, 0, 0.</span><span class="sxs-lookup"><span data-stu-id="c1473-108">For example calling Dispatch(2,1,1) results in possible values of 0,0,0 and 1,0,0.</span></span>

<span data-ttu-id="c1473-109">Определяет смещение группы в вызове [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) для каждого измерения вызова диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="c1473-109">Defines the group offset within a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) call, per dimension of the dispatch call.</span></span>

## <a name="type"></a><span data-ttu-id="c1473-110">Тип</span><span class="sxs-lookup"><span data-stu-id="c1473-110">Type</span></span>



|       |
|-------|
| <span data-ttu-id="c1473-111">Тип</span><span class="sxs-lookup"><span data-stu-id="c1473-111">Type</span></span>  |
| <span data-ttu-id="c1473-112">uint3</span><span class="sxs-lookup"><span data-stu-id="c1473-112">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c1473-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="c1473-113">Remarks</span></span>

<span data-ttu-id="c1473-114">Это системное значение является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c1473-114">This system value is optional.</span></span>

<span data-ttu-id="c1473-115">На следующем рисунке показана связь между параметрами, передаваемыми для [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), диспетчеризации (5, 3, 2), значениями, указанными в атрибуте [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3), и значениями, которые будут переданы в шейдер вычислений для системных значений, связанных с потоками ([ОКП \_ граупиндекс](sv-groupindex.md),[SV \_ диспатчсреадид](sv-dispatchthreadid.md),[ОКП \_ граупсреадид](sv-groupthreadid.md), SV \_ GroupId).</span><span class="sxs-lookup"><span data-stu-id="c1473-115">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),SV\_GroupID).</span></span>

![Иллюстрация связи между диспетчеризация, группами потоков и потоками](images/threadgroupids.png)

<span data-ttu-id="c1473-117">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="c1473-117">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c1473-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="c1473-118">Vertex</span></span> | <span data-ttu-id="c1473-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="c1473-119">Hull</span></span> | <span data-ttu-id="c1473-120">Домен</span><span class="sxs-lookup"><span data-stu-id="c1473-120">Domain</span></span> | <span data-ttu-id="c1473-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="c1473-121">Geometry</span></span> | <span data-ttu-id="c1473-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="c1473-122">Pixel</span></span> | <span data-ttu-id="c1473-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="c1473-123">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="c1473-124">x</span><span class="sxs-lookup"><span data-stu-id="c1473-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c1473-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1473-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1473-126">Семантика</span><span class="sxs-lookup"><span data-stu-id="c1473-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="c1473-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c1473-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 