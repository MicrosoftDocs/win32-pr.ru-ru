---
title: Функция Аллмеморибарриер
description: Блокирует выполнение всех потоков в группе до тех пор, пока не завершится доступ к памяти.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- Функция Аллмеморибарриер HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3252389da64b74e07853069c71315b290a2ba6d5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411965"
---
# <a name="allmemorybarrier-function"></a><span data-ttu-id="feb0c-104">Функция Аллмеморибарриер</span><span class="sxs-lookup"><span data-stu-id="feb0c-104">AllMemoryBarrier function</span></span>

<span data-ttu-id="feb0c-105">Блокирует выполнение всех потоков в группе до тех пор, пока не завершится доступ к памяти.</span><span class="sxs-lookup"><span data-stu-id="feb0c-105">Blocks execution of all threads in a group until all memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb0c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="feb0c-106">Syntax</span></span>

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="feb0c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="feb0c-107">Parameters</span></span>

<span data-ttu-id="feb0c-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="feb0c-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="feb0c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="feb0c-109">Return value</span></span>

<span data-ttu-id="feb0c-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="feb0c-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="feb0c-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="feb0c-111">Remarks</span></span>

<span data-ttu-id="feb0c-112">Барьер памяти гарантирует завершение невыполненных операций с памятью.</span><span class="sxs-lookup"><span data-stu-id="feb0c-112">A memory barrier guarantees that outstanding memory operations have completed.</span></span> <span data-ttu-id="feb0c-113">Потоки синхронизируются с Граупсинк барьерами.</span><span class="sxs-lookup"><span data-stu-id="feb0c-113">Threads are synchronized at GroupSync barriers.</span></span> <span data-ttu-id="feb0c-114">Это может привести к остановке потока или потоков, если выполняются операции с памятью.</span><span class="sxs-lookup"><span data-stu-id="feb0c-114">This may stall a thread or threads if memory operations are in progress.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="feb0c-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="feb0c-115">Minimum Shader Model</span></span>

<span data-ttu-id="feb0c-116">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="feb0c-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="feb0c-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="feb0c-117">Shader Model</span></span>                                                                | <span data-ttu-id="feb0c-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="feb0c-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="feb0c-119">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="feb0c-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="feb0c-120">да</span><span class="sxs-lookup"><span data-stu-id="feb0c-120">yes</span></span>       |



 

<span data-ttu-id="feb0c-121">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="feb0c-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="feb0c-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="feb0c-122">Vertex</span></span> | <span data-ttu-id="feb0c-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="feb0c-123">Hull</span></span> | <span data-ttu-id="feb0c-124">Домен</span><span class="sxs-lookup"><span data-stu-id="feb0c-124">Domain</span></span> | <span data-ttu-id="feb0c-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="feb0c-125">Geometry</span></span> | <span data-ttu-id="feb0c-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="feb0c-126">Pixel</span></span> | <span data-ttu-id="feb0c-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="feb0c-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="feb0c-128">x</span><span class="sxs-lookup"><span data-stu-id="feb0c-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="feb0c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="feb0c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb0c-130">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="feb0c-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="feb0c-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="feb0c-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




