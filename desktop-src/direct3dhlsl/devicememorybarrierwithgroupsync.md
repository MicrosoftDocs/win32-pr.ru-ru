---
title: Функция Девицемеморибарриервисграупсинк
description: Блокирует выполнение всех потоков в группе до тех пор, пока не будут завершены все доступ к памяти устройства и все потоки в группе достигли этого вызова.
ms.assetid: 77c54064-a996-4c51-84b5-7da60e884c4f
keywords:
- Функция Девицемеморибарриервисграупсинк HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a7a4a27b3256fb78c7b60b960fc5383cfd5b5d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334403"
---
# <a name="devicememorybarrierwithgroupsync-function"></a><span data-ttu-id="db4d4-104">Функция Девицемеморибарриервисграупсинк</span><span class="sxs-lookup"><span data-stu-id="db4d4-104">DeviceMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="db4d4-105">Блокирует выполнение всех потоков в группе до тех пор, пока не будут завершены все доступ к памяти устройства и все потоки в группе достигли этого вызова.</span><span class="sxs-lookup"><span data-stu-id="db4d4-105">Blocks execution of all threads in a group until all device memory accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="db4d4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db4d4-106">Syntax</span></span>

``` syntax
void DeviceMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="db4d4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="db4d4-107">Parameters</span></span>

<span data-ttu-id="db4d4-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="db4d4-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db4d4-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db4d4-109">Return value</span></span>

<span data-ttu-id="db4d4-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="db4d4-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db4d4-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="db4d4-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="db4d4-112">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="db4d4-112">Minimum Shader Model</span></span>

<span data-ttu-id="db4d4-113">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="db4d4-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="db4d4-114">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="db4d4-114">Shader Model</span></span>                                                                | <span data-ttu-id="db4d4-115">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="db4d4-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="db4d4-116">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="db4d4-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="db4d4-117">да</span><span class="sxs-lookup"><span data-stu-id="db4d4-117">yes</span></span>       |



 

<span data-ttu-id="db4d4-118">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="db4d4-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="db4d4-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="db4d4-119">Vertex</span></span> | <span data-ttu-id="db4d4-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="db4d4-120">Hull</span></span> | <span data-ttu-id="db4d4-121">Домен</span><span class="sxs-lookup"><span data-stu-id="db4d4-121">Domain</span></span> | <span data-ttu-id="db4d4-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="db4d4-122">Geometry</span></span> | <span data-ttu-id="db4d4-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="db4d4-123">Pixel</span></span> | <span data-ttu-id="db4d4-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="db4d4-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="db4d4-125">x</span><span class="sxs-lookup"><span data-stu-id="db4d4-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="db4d4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db4d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4d4-127">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="db4d4-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="db4d4-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="db4d4-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




