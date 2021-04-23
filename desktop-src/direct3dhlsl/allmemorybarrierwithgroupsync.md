---
title: Функция Аллмеморибарриервисграупсинк
description: Блокирует выполнение всех потоков в группе до тех пор, пока не будут завершены все доступ к памяти и все потоки в группе достигли этого вызова.
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- Функция Аллмеморибарриервисграупсинк HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fc005545485b7f894729ab6c7d7975acfd5b6d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069154"
---
# <a name="allmemorybarrierwithgroupsync-function"></a><span data-ttu-id="9f739-104">Функция Аллмеморибарриервисграупсинк</span><span class="sxs-lookup"><span data-stu-id="9f739-104">AllMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="9f739-105">Блокирует выполнение всех потоков в группе до тех пор, пока не будут завершены все доступ к памяти и все потоки в группе достигли этого вызова.</span><span class="sxs-lookup"><span data-stu-id="9f739-105">Blocks execution of all threads in a group until all memory accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f739-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f739-106">Syntax</span></span>

``` syntax
void AllMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="9f739-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f739-107">Parameters</span></span>

<span data-ttu-id="9f739-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="9f739-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f739-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f739-109">Return value</span></span>

<span data-ttu-id="9f739-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9f739-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f739-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="9f739-111">Remarks</span></span>

<span data-ttu-id="9f739-112">Барьер памяти гарантирует завершение невыполненных операций с памятью.</span><span class="sxs-lookup"><span data-stu-id="9f739-112">A memory barrier guarantees that outstanding memory operations have completed.</span></span> <span data-ttu-id="9f739-113">Потоки синхронизируются с Граупсинк барьерами.</span><span class="sxs-lookup"><span data-stu-id="9f739-113">Threads are synchronized at GroupSync barriers.</span></span> <span data-ttu-id="9f739-114">Это может привести к остановке потока или потоков, если выполняются операции с памятью.</span><span class="sxs-lookup"><span data-stu-id="9f739-114">This may stall a thread or threads if memory operations are in progress.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="9f739-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9f739-115">Minimum Shader Model</span></span>

<span data-ttu-id="9f739-116">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="9f739-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9f739-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9f739-117">Shader Model</span></span>                                                                | <span data-ttu-id="9f739-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9f739-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9f739-119">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="9f739-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9f739-120">да</span><span class="sxs-lookup"><span data-stu-id="9f739-120">yes</span></span>       |



 

<span data-ttu-id="9f739-121">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9f739-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="9f739-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="9f739-122">Vertex</span></span> | <span data-ttu-id="9f739-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9f739-123">Hull</span></span> | <span data-ttu-id="9f739-124">Домен</span><span class="sxs-lookup"><span data-stu-id="9f739-124">Domain</span></span> | <span data-ttu-id="9f739-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9f739-125">Geometry</span></span> | <span data-ttu-id="9f739-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9f739-126">Pixel</span></span> | <span data-ttu-id="9f739-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9f739-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="9f739-128">x</span><span class="sxs-lookup"><span data-stu-id="9f739-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9f739-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f739-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f739-130">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="9f739-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="9f739-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9f739-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




