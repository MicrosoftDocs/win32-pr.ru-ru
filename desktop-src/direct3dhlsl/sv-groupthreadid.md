---
title: SV_GroupThreadID
description: Индексы, для которых выполняется отдельный поток в группе потоков, в которой работает шейдер вычислений.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d399008f1a9314ceb1fd4b1499b51340b499600b
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827033"
---
# <a name="sv_groupthreadid"></a><span data-ttu-id="59baf-104">ОКП \_ граупсреадид</span><span class="sxs-lookup"><span data-stu-id="59baf-104">SV\_GroupThreadID</span></span>

<span data-ttu-id="59baf-105">Индексы, для которых выполняется отдельный поток в группе потоков, в которой работает шейдер вычислений.</span><span class="sxs-lookup"><span data-stu-id="59baf-105">Indices for which an individual thread within a thread group a compute shader is executing in.</span></span> <span data-ttu-id="59baf-106">ОКП \_ граупсреадид варьируется в пределах диапазона, указанного для шейдера вычислений в атрибуте [numthreads](sm5-attributes-numthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="59baf-106">SV\_GroupThreadID varies across the range specified for the compute shader in the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span> <span data-ttu-id="59baf-107">Например, если задано значение numthreads (3, 2, 1), возможные значения для \_ входного значения SV граупсреадид имеют этот диапазон значений (0 – 2, 0 – 1, 0).</span><span class="sxs-lookup"><span data-stu-id="59baf-107">For example if numthreads(3,2,1) was specified possible values for the SV\_GroupThreadID input value have this range of values (0-2,0-1,0).</span></span>

## <a name="type"></a><span data-ttu-id="59baf-108">Тип</span><span class="sxs-lookup"><span data-stu-id="59baf-108">Type</span></span>



| <span data-ttu-id="59baf-109">Тип</span><span class="sxs-lookup"><span data-stu-id="59baf-109">Type</span></span>      |
|-------|
| <span data-ttu-id="59baf-110">uint3</span><span class="sxs-lookup"><span data-stu-id="59baf-110">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="59baf-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="59baf-111">Remarks</span></span>

<span data-ttu-id="59baf-112">Это системное значение является необязательным и всегда находится внутри границ значений, передаваемых в атрибут [numthreads](sm5-attributes-numthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="59baf-112">This system value is optional, and is always within the bounds of the values passed into the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span>

<span data-ttu-id="59baf-113">На следующем рисунке показана связь между параметрами, передаваемыми для [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), диспетчеризации (5, 3, 2), значениями, указанными в атрибуте [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3), и значениями, которые будут переданы в шейдер вычислений для системных значений, связанных с потоками ([ОКП \_ граупиндекс](sv-groupindex.md),[SV \_ диспатчсреадид](sv-dispatchthreadid.md), ОКП \_ граупсреадид,[SV \_ groupId](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="59baf-113">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),SV\_GroupThreadID,[SV\_GroupID](sv-groupid.md)).</span></span>

![Иллюстрация связи между диспетчеризация, группами потоков и потоками](images/threadgroupids.png)

<span data-ttu-id="59baf-115">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="59baf-115">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="59baf-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="59baf-116">Vertex</span></span> | <span data-ttu-id="59baf-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="59baf-117">Hull</span></span> | <span data-ttu-id="59baf-118">Домен</span><span class="sxs-lookup"><span data-stu-id="59baf-118">Domain</span></span> | <span data-ttu-id="59baf-119">Geometry</span><span class="sxs-lookup"><span data-stu-id="59baf-119">Geometry</span></span> | <span data-ttu-id="59baf-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="59baf-120">Pixel</span></span> | <span data-ttu-id="59baf-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="59baf-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="59baf-122">x</span><span class="sxs-lookup"><span data-stu-id="59baf-122">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="59baf-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59baf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59baf-124">Семантика</span><span class="sxs-lookup"><span data-stu-id="59baf-124">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="59baf-125">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="59baf-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
