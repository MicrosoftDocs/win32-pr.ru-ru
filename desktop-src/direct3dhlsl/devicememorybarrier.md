---
title: Функция Девицемеморибарриер
description: Блокирует выполнение всех потоков в группе до тех пор, пока не будут завершены все доступ к памяти устройства.
ms.assetid: 904ab8f6-4849-4b13-8fac-3967cf66574e
keywords:
- Функция Девицемеморибарриер HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875b780f528000d46ba31bb979072d6d462fa91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411501"
---
# <a name="devicememorybarrier-function"></a><span data-ttu-id="4bc95-104">Функция Девицемеморибарриер</span><span class="sxs-lookup"><span data-stu-id="4bc95-104">DeviceMemoryBarrier function</span></span>

<span data-ttu-id="4bc95-105">Блокирует выполнение всех потоков в группе до тех пор, пока не будут завершены все доступ к памяти устройства.</span><span class="sxs-lookup"><span data-stu-id="4bc95-105">Blocks execution of all threads in a group until all device memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc95-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bc95-106">Syntax</span></span>

``` syntax
void DeviceMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="4bc95-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bc95-107">Parameters</span></span>

<span data-ttu-id="4bc95-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="4bc95-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4bc95-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bc95-109">Return value</span></span>

<span data-ttu-id="4bc95-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4bc95-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bc95-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="4bc95-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="4bc95-112">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4bc95-112">Minimum Shader Model</span></span>

<span data-ttu-id="4bc95-113">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4bc95-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4bc95-114">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4bc95-114">Shader Model</span></span>                                                                | <span data-ttu-id="4bc95-115">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="4bc95-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4bc95-116">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="4bc95-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4bc95-117">да</span><span class="sxs-lookup"><span data-stu-id="4bc95-117">yes</span></span>       |



 

<span data-ttu-id="4bc95-118">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="4bc95-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4bc95-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="4bc95-119">Vertex</span></span> | <span data-ttu-id="4bc95-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="4bc95-120">Hull</span></span> | <span data-ttu-id="4bc95-121">Домен</span><span class="sxs-lookup"><span data-stu-id="4bc95-121">Domain</span></span> | <span data-ttu-id="4bc95-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="4bc95-122">Geometry</span></span> | <span data-ttu-id="4bc95-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="4bc95-123">Pixel</span></span> | <span data-ttu-id="4bc95-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="4bc95-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4bc95-125">x</span><span class="sxs-lookup"><span data-stu-id="4bc95-125">x</span></span>     | <span data-ttu-id="4bc95-126">x</span><span class="sxs-lookup"><span data-stu-id="4bc95-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4bc95-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bc95-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc95-128">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="4bc95-128">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="4bc95-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="4bc95-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




