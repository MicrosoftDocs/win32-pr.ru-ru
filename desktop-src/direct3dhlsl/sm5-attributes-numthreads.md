---
title: numthreads
description: Определяет число потоков, выполняемых в одной группе потоков при отправке шейдера вычислений (см. раздел Dispatch ссылку ID3D11DeviceContext).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413608"
---
# <a name="numthreads"></a><span data-ttu-id="fac53-103">numthreads</span><span class="sxs-lookup"><span data-stu-id="fac53-103">numthreads</span></span>

<span data-ttu-id="fac53-104">Определяет число потоков, выполняемых в одной группе потоков при отправке шейдера вычислений (см. раздел [**ссылку ID3D11DeviceContext::D Patch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span><span class="sxs-lookup"><span data-stu-id="fac53-104">Defines the number of threads to be executed in a single thread group when a compute shader is dispatched (see [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span></span>


```
numthreads(X, Y, Z)    
```



<span data-ttu-id="fac53-105">Значения X, Y и Z указывают размер группы потоков в определенном направлении, а суммарное значение X \* Y \* Z указывает число потоков в группе.</span><span class="sxs-lookup"><span data-stu-id="fac53-105">The X, Y and Z values indicate the size of the thread group in a particular direction and the total of X\*Y\*Z gives the number of threads in the group.</span></span> <span data-ttu-id="fac53-106">Возможность указывать размер группы потоков в трех измерениях позволяет осуществлять доступ к отдельным потокам способом, логически плоскими и трехмерными структурами данных.</span><span class="sxs-lookup"><span data-stu-id="fac53-106">The ability to specify the size of the thread group across three dimensions allows individual threads to be accessed in a manner that logically 2D and 3D data structures.</span></span>

<span data-ttu-id="fac53-107">Например, если в качестве шейдера вычислений выполняется добавление матрицы 4x4, то numthreads может иметь значение numthreads (4, 4, 1), а индексирование в отдельных потоках будет автоматически сопоставлять записи матрицы.</span><span class="sxs-lookup"><span data-stu-id="fac53-107">For example, if a compute shader is doing 4x4 matrix addition then numthreads could be set to numthreads(4,4,1) and the indexing in the individual threads would automatically match the matrix entries.</span></span> <span data-ttu-id="fac53-108">Шейдер вычислений также может объявить группу потоков с тем же числом потоков (16) с помощью numthreads (16, 1, 1), однако после этого потребуется вычислить текущую запись матрицы на основе текущего номера потока.</span><span class="sxs-lookup"><span data-stu-id="fac53-108">The compute shader could also declare a thread group with the same number of threads (16) using numthreads(16,1,1), however it would then have to calculate the current matrix entry based on the current thread number.</span></span>

<span data-ttu-id="fac53-109">Допустимые значения параметров для **numthreads** зависят от версии COMPUTE Shader.</span><span class="sxs-lookup"><span data-stu-id="fac53-109">The allowable parameter values for **numthreads** depends on the compute shader version.</span></span>



| <span data-ttu-id="fac53-110">Вычисление шейдера</span><span class="sxs-lookup"><span data-stu-id="fac53-110">Compute Shader</span></span> | <span data-ttu-id="fac53-111">Максимальное значение Z</span><span class="sxs-lookup"><span data-stu-id="fac53-111">Maximum Z</span></span> | <span data-ttu-id="fac53-112">Максимальное число потоков (X \* Y \* )</span><span class="sxs-lookup"><span data-stu-id="fac53-112">Maximum Threads (X\*Y\*Z)</span></span> |
|----------------|-----------|---------------------------|
| <span data-ttu-id="fac53-113">CS \_ 4 \_ x</span><span class="sxs-lookup"><span data-stu-id="fac53-113">cs\_4\_x</span></span>       | <span data-ttu-id="fac53-114">1</span><span class="sxs-lookup"><span data-stu-id="fac53-114">1</span></span>         | <span data-ttu-id="fac53-115">768</span><span class="sxs-lookup"><span data-stu-id="fac53-115">768</span></span>                       |
| <span data-ttu-id="fac53-116">CS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fac53-116">cs\_5\_0</span></span>       | <span data-ttu-id="fac53-117">64</span><span class="sxs-lookup"><span data-stu-id="fac53-117">64</span></span>        | <span data-ttu-id="fac53-118">1024</span><span class="sxs-lookup"><span data-stu-id="fac53-118">1024</span></span>                      |



 

<span data-ttu-id="fac53-119">На следующем рисунке показана связь между параметрами, передаваемыми в [**ссылку ID3D11DeviceContext::D диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), диспетчеризации (5, 3, 2), значениями, указанными в атрибуте numthreads, numthreads (10, 8, 3) и значениями, которые будут переданы в шейдер вычислений для системных значений, связанных с потоком ([ОКП \_ граупиндекс](sv-groupindex.md),[SV \_ диспатчсреадид](sv-dispatchthreadid.md),[ОКП \_ граупсреадид](sv-groupthreadid.md),[SV \_ groupId](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="fac53-119">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the numthreads attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![Иллюстрация связи между диспетчеризация, группами потоков и потоками](images/threadgroupids.png)

<span data-ttu-id="fac53-121">Этот атрибут поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="fac53-121">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="fac53-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="fac53-122">Vertex</span></span> | <span data-ttu-id="fac53-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="fac53-123">Hull</span></span> | <span data-ttu-id="fac53-124">Домен</span><span class="sxs-lookup"><span data-stu-id="fac53-124">Domain</span></span> | <span data-ttu-id="fac53-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="fac53-125">Geometry</span></span> | <span data-ttu-id="fac53-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="fac53-126">Pixel</span></span> | <span data-ttu-id="fac53-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="fac53-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="fac53-128">x</span><span class="sxs-lookup"><span data-stu-id="fac53-128">x</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="fac53-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fac53-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fac53-130">Атрибуты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="fac53-130">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="fac53-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="fac53-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 