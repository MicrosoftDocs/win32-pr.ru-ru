---
title: SV_GroupIndex
description: '\ 0034; плоская \ 0034; Индекс вычисленного потока шейдера в группе потоков, который превращает многомерное ОКП \_ граупсреадид в значение 1d. ОКП \_ граупиндекс меняется от 0 до (нумсреадскс \ нумсреадси \ нумсреадсз) \ 8211; одного.'
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792283"
---
# <a name="sv_groupindex"></a><span data-ttu-id="3ba2d-105">ОКП \_ граупиндекс</span><span class="sxs-lookup"><span data-stu-id="3ba2d-105">SV\_GroupIndex</span></span>

<span data-ttu-id="3ba2d-106">"Плоский" индекс потока вычислений для шейдера в группе потоков, который превращает многомерное ОКП \_ граупсреадид в значение 1d.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-106">The "flattened" index of a compute shader thread within a thread group, which turns the multi-dimensional SV\_GroupThreadID into a 1D value.</span></span> <span data-ttu-id="3ba2d-107">ОКП \_ граупиндекс варьируется от 0 до (нумсреадскс \* нумсреадси \* нумсреадсз) – 1.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-107">SV\_GroupIndex varies from 0 to (numthreadsX \* numthreadsY \* numThreadsZ) – 1.</span></span>

## <a name="type"></a><span data-ttu-id="3ba2d-108">Тип</span><span class="sxs-lookup"><span data-stu-id="3ba2d-108">Type</span></span>



| <span data-ttu-id="3ba2d-109">Тип</span><span class="sxs-lookup"><span data-stu-id="3ba2d-109">Type</span></span> |
|------|
| <span data-ttu-id="3ba2d-110">uint</span><span class="sxs-lookup"><span data-stu-id="3ba2d-110">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3ba2d-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="3ba2d-111">Remarks</span></span>


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



<span data-ttu-id="3ba2d-112">где димкс и Дими — это измерения, указанные в атрибуте [numthreads](sm5-attributes-numthreads.md) для точки входа.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-112">where dimx and dimy are the dimensions specified in the [numthreads](sm5-attributes-numthreads.md) attribute for the entry point.</span></span>

<span data-ttu-id="3ba2d-113">Это системное значение является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-113">This system value is optional.</span></span> <span data-ttu-id="3ba2d-114">Однако его использование гарантирует, что поток записывается только в назначенную ему область памяти в переменной граупшаред.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-114">However, its use ensures that a thread only writes to its assigned region of memory in the groupshared variable.</span></span>

<span data-ttu-id="3ba2d-115">На следующем рисунке показана связь между параметрами, передаваемыми в [**ссылку ID3D11DeviceContext::D диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), диспетчеризации (5, 3, 2), значениями, указанными в атрибуте [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) и значениями, которые будут переданы в шейдер вычислений для системных значений, связанных с потоками (ОКП \_ граупиндекс,[SV \_ диспатчсреадид](sv-dispatchthreadid.md),[ОКП \_ граупсреадид](sv-groupthreadid.md),[SV \_ groupId](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="3ba2d-115">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values (SV\_GroupIndex,[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![Иллюстрация связи между диспетчеризация, группами потоков и потоками](images/threadgroupids.png)

<span data-ttu-id="3ba2d-117">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="3ba2d-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3ba2d-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="3ba2d-118">Vertex</span></span> | <span data-ttu-id="3ba2d-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="3ba2d-119">Hull</span></span> | <span data-ttu-id="3ba2d-120">Домен</span><span class="sxs-lookup"><span data-stu-id="3ba2d-120">Domain</span></span> | <span data-ttu-id="3ba2d-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="3ba2d-121">Geometry</span></span> | <span data-ttu-id="3ba2d-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="3ba2d-122">Pixel</span></span> | <span data-ttu-id="3ba2d-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="3ba2d-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="3ba2d-124">x</span><span class="sxs-lookup"><span data-stu-id="3ba2d-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3ba2d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ba2d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba2d-126">Семантика</span><span class="sxs-lookup"><span data-stu-id="3ba2d-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="3ba2d-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="3ba2d-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 