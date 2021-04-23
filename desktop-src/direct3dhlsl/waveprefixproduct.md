---
title: 'Функция WavePrefixProduct '
description: Возвращает произведение всех значений в активных желобах в этой волновой области с индексами, меньшими, чем эта полоса.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- Функция Вавепрефикспродукт HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414153"
---
# <a name="waveprefixproduct-function"></a><span data-ttu-id="4c4d9-104">Функция WavePrefixProduct </span><span class="sxs-lookup"><span data-stu-id="4c4d9-104">WavePrefixProduct function</span></span>

<span data-ttu-id="4c4d9-105">Возвращает произведение всех значений в активных желобах в этой волновой области с индексами, меньшими, чем эта полоса.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-105">Returns the product of all of the values in the active lanes in this wave with indices less than this lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c4d9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c4d9-106">Syntax</span></span>

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="4c4d9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c4d9-107">Parameters</span></span>

<span data-ttu-id="4c4d9-108">*value*</span><span class="sxs-lookup"><span data-stu-id="4c4d9-108">*value*</span></span> 

<span data-ttu-id="4c4d9-109">Значение для умножения.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-109">The value to multiply.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c4d9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c4d9-110">Return value</span></span>

<span data-ttu-id="4c4d9-111">Произведение всех значений.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-111">The product of all the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c4d9-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="4c4d9-112">Remarks</span></span>

<span data-ttu-id="4c4d9-113">Порядок операций в этой подпрограммы не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="4c4d9-114">Таким образом, \[ точный флаг в \] нем игнорируется.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="4c4d9-115">Постфиксный продукт может быть вычислен путем умножения префиксного продукта на значение текущей полосы.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-115">A postfix product can be computed by multiplying the prefix product by the current lane's value.</span></span>

<span data-ttu-id="4c4d9-116">Обратите внимание, что активная полоса с наименьшим индексом всегда будет иметь значение 1 для своего префиксного продукта.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-116">Note that the active lane with the lowest index will always receive a 1 for its prefix product.</span></span>

<span data-ttu-id="4c4d9-117">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="4c4d9-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="4c4d9-118">Examples</span></span>

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

<span data-ttu-id="4c4d9-119">На компьютере с размером волны 8 и всеми активными дорожками, кроме желобов 0 и 4, в Вавепрефикспродукт будут возвращены следующие значения.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixProduct.</span></span>

| <span data-ttu-id="4c4d9-120">Индекс полосы</span><span class="sxs-lookup"><span data-stu-id="4c4d9-120">lane index</span></span> | <span data-ttu-id="4c4d9-121">status</span><span class="sxs-lookup"><span data-stu-id="4c4d9-121">status</span></span>   | <span data-ttu-id="4c4d9-122">префикспродукт</span><span class="sxs-lookup"><span data-stu-id="4c4d9-122">prefixProduct</span></span> | 
|------------|----------|---------------|
| <span data-ttu-id="4c4d9-123">0</span><span class="sxs-lookup"><span data-stu-id="4c4d9-123">0</span></span>          | <span data-ttu-id="4c4d9-124">неактивно</span><span class="sxs-lookup"><span data-stu-id="4c4d9-124">inactive</span></span> | <span data-ttu-id="4c4d9-125">Недоступно</span><span class="sxs-lookup"><span data-stu-id="4c4d9-125">n/a</span></span>           |
| <span data-ttu-id="4c4d9-126">1</span><span class="sxs-lookup"><span data-stu-id="4c4d9-126">1</span></span>          | <span data-ttu-id="4c4d9-127">active</span><span class="sxs-lookup"><span data-stu-id="4c4d9-127">active</span></span>   | <span data-ttu-id="4c4d9-128">= 1</span><span class="sxs-lookup"><span data-stu-id="4c4d9-128">= 1</span></span>           |
| <span data-ttu-id="4c4d9-129">2</span><span class="sxs-lookup"><span data-stu-id="4c4d9-129">2</span></span>          | <span data-ttu-id="4c4d9-130">active</span><span class="sxs-lookup"><span data-stu-id="4c4d9-130">active</span></span>   | <span data-ttu-id="4c4d9-131">= 1 \* 2</span><span class="sxs-lookup"><span data-stu-id="4c4d9-131">= 1\*2</span></span>        |
| <span data-ttu-id="4c4d9-132">3</span><span class="sxs-lookup"><span data-stu-id="4c4d9-132">3</span></span>          | <span data-ttu-id="4c4d9-133">active</span><span class="sxs-lookup"><span data-stu-id="4c4d9-133">active</span></span>   | <span data-ttu-id="4c4d9-134">= 1 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="4c4d9-134">= 1\*2\*2</span></span>     |
| <span data-ttu-id="4c4d9-135">4</span><span class="sxs-lookup"><span data-stu-id="4c4d9-135">4</span></span>          | <span data-ttu-id="4c4d9-136">неактивно</span><span class="sxs-lookup"><span data-stu-id="4c4d9-136">inactive</span></span> | <span data-ttu-id="4c4d9-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="4c4d9-137">n/a</span></span>           |
| <span data-ttu-id="4c4d9-138">5</span><span class="sxs-lookup"><span data-stu-id="4c4d9-138">5</span></span>          | <span data-ttu-id="4c4d9-139">active</span><span class="sxs-lookup"><span data-stu-id="4c4d9-139">active</span></span>   | <span data-ttu-id="4c4d9-140">= 1 \* 2 \* 2 2 \*</span><span class="sxs-lookup"><span data-stu-id="4c4d9-140">= 1\*2\*2\*2</span></span>       |
| <span data-ttu-id="4c4d9-141">6</span><span class="sxs-lookup"><span data-stu-id="4c4d9-141">6</span></span>          | <span data-ttu-id="4c4d9-142">active</span><span class="sxs-lookup"><span data-stu-id="4c4d9-142">active</span></span>   | <span data-ttu-id="4c4d9-143">= 1 \* 2 \* 2 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="4c4d9-143">= 1\*2\*2\*2\*2</span></span>    |
| <span data-ttu-id="4c4d9-144">7</span><span class="sxs-lookup"><span data-stu-id="4c4d9-144">7</span></span>          | <span data-ttu-id="4c4d9-145">active</span><span class="sxs-lookup"><span data-stu-id="4c4d9-145">active</span></span>   | <span data-ttu-id="4c4d9-146">= 1 \* 2 \* 2 \* 2 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="4c4d9-146">= 1\*2\*2\*2\*2\*2</span></span> |

## <a name="see-also"></a><span data-ttu-id="4c4d9-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c4d9-147">See also</span></span>

[<span data-ttu-id="4c4d9-148">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="4c4d9-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="4c4d9-149">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="4c4d9-149">Shader Model 6</span></span>](shader-model-6-0.md)
