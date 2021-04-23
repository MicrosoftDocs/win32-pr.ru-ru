---
title: Функция Граупмеморибарриервисграупсинк
description: Блокирует выполнение всех потоков в группе до тех пор, пока все общие группы доступа не будут завершены и все потоки в группе достигли этого вызова.
ms.assetid: 64dd78e1-c597-4bd0-8a9b-592123178de5
keywords:
- Функция Граупмеморибарриервисграупсинк HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07798bb8ad6bd9c4cdfa14bfa57d97818dbd6962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104983753"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a><span data-ttu-id="1df68-104">Функция Граупмеморибарриервисграупсинк</span><span class="sxs-lookup"><span data-stu-id="1df68-104">GroupMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="1df68-105">Блокирует выполнение всех потоков в группе до тех пор, пока все общие группы доступа не будут завершены и все потоки в группе достигли этого вызова.</span><span class="sxs-lookup"><span data-stu-id="1df68-105">Blocks execution of all threads in a group until all group shared accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df68-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1df68-106">Syntax</span></span>

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="1df68-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1df68-107">Parameters</span></span>

<span data-ttu-id="1df68-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="1df68-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1df68-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1df68-109">Return value</span></span>

<span data-ttu-id="1df68-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1df68-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1df68-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="1df68-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="1df68-112">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1df68-112">Minimum Shader Model</span></span>

<span data-ttu-id="1df68-113">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="1df68-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1df68-114">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1df68-114">Shader Model</span></span>                                                                | <span data-ttu-id="1df68-115">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1df68-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1df68-116">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="1df68-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="1df68-117">да</span><span class="sxs-lookup"><span data-stu-id="1df68-117">yes</span></span>       |



 

<span data-ttu-id="1df68-118">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1df68-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="1df68-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="1df68-119">Vertex</span></span> | <span data-ttu-id="1df68-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1df68-120">Hull</span></span> | <span data-ttu-id="1df68-121">Домен</span><span class="sxs-lookup"><span data-stu-id="1df68-121">Domain</span></span> | <span data-ttu-id="1df68-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1df68-122">Geometry</span></span> | <span data-ttu-id="1df68-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1df68-123">Pixel</span></span> | <span data-ttu-id="1df68-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1df68-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="1df68-125">x</span><span class="sxs-lookup"><span data-stu-id="1df68-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1df68-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1df68-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df68-127">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="1df68-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="1df68-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1df68-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




