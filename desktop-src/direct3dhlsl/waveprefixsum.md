---
title: 'Функция WavePrefixSum '
description: Возвращает сумму всех значений в активном желобе с меньшими индексами по сравнению с этим значением.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- Функция Вавепрефикссум HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2021
ms.locfileid: "104986152"
---
# <a name="waveprefixsum-function"></a><span data-ttu-id="2aaab-104">Функция WavePrefixSum </span><span class="sxs-lookup"><span data-stu-id="2aaab-104">WavePrefixSum function</span></span>

<span data-ttu-id="2aaab-105">Возвращает сумму всех значений в активном желобе с меньшими индексами по сравнению с этим значением.</span><span class="sxs-lookup"><span data-stu-id="2aaab-105">Returns the sum of all of the values in the active lanes with smaller indices than this one.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aaab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2aaab-106">Syntax</span></span>

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="2aaab-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2aaab-107">Parameters</span></span>

<span data-ttu-id="2aaab-108">*value*</span><span class="sxs-lookup"><span data-stu-id="2aaab-108">*value*</span></span> 

<span data-ttu-id="2aaab-109">Значение для суммирования.</span><span class="sxs-lookup"><span data-stu-id="2aaab-109">The value to sum up.</span></span>

## <a name="return-value"></a><span data-ttu-id="2aaab-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2aaab-110">Return value</span></span>

<span data-ttu-id="2aaab-111">Сумма значений.</span><span class="sxs-lookup"><span data-stu-id="2aaab-111">The sum of the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aaab-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="2aaab-112">Remarks</span></span>

<span data-ttu-id="2aaab-113">Порядок операций в этой подпрограммы не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="2aaab-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="2aaab-114">Таким образом, \[ точный флаг в \] нем игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2aaab-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="2aaab-115">Постфиксная сумма может быть вычислена путем добавления суммы префикса к значению текущей полосы.</span><span class="sxs-lookup"><span data-stu-id="2aaab-115">A postfix sum can be computed by adding the prefix sum to the current lane's value.</span></span>

<span data-ttu-id="2aaab-116">Обратите внимание, что активная полоса с наименьшим индексом всегда будет иметь значение 0 для своей суммы префикса.</span><span class="sxs-lookup"><span data-stu-id="2aaab-116">Note that the active lane with the lowest index will always receive a 0 for its prefix sum.</span></span>

<span data-ttu-id="2aaab-117">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="2aaab-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="2aaab-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="2aaab-118">Examples</span></span>

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

<span data-ttu-id="2aaab-119">На компьютере с размером волны 8 и всеми активными дорожками, кроме желобов 0 и 4, в Вавепрефикссум будут возвращены следующие значения.</span><span class="sxs-lookup"><span data-stu-id="2aaab-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixSum.</span></span>

| <span data-ttu-id="2aaab-120">Индекс полосы</span><span class="sxs-lookup"><span data-stu-id="2aaab-120">lane index</span></span> | <span data-ttu-id="2aaab-121">status</span><span class="sxs-lookup"><span data-stu-id="2aaab-121">status</span></span>   | <span data-ttu-id="2aaab-122">префикссум</span><span class="sxs-lookup"><span data-stu-id="2aaab-122">prefixSum</span></span>     | 
|------------|----------|---------------|
| <span data-ttu-id="2aaab-123">0</span><span class="sxs-lookup"><span data-stu-id="2aaab-123">0</span></span>          | <span data-ttu-id="2aaab-124">неактивно</span><span class="sxs-lookup"><span data-stu-id="2aaab-124">inactive</span></span> | <span data-ttu-id="2aaab-125">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2aaab-125">n/a</span></span>           |
| <span data-ttu-id="2aaab-126">1</span><span class="sxs-lookup"><span data-stu-id="2aaab-126">1</span></span>          | <span data-ttu-id="2aaab-127">active</span><span class="sxs-lookup"><span data-stu-id="2aaab-127">active</span></span>   | <span data-ttu-id="2aaab-128">= 0</span><span class="sxs-lookup"><span data-stu-id="2aaab-128">= 0</span></span>           |
| <span data-ttu-id="2aaab-129">2</span><span class="sxs-lookup"><span data-stu-id="2aaab-129">2</span></span>          | <span data-ttu-id="2aaab-130">active</span><span class="sxs-lookup"><span data-stu-id="2aaab-130">active</span></span>   | <span data-ttu-id="2aaab-131">= 0 + 2</span><span class="sxs-lookup"><span data-stu-id="2aaab-131">= 0+2</span></span>         |
| <span data-ttu-id="2aaab-132">3</span><span class="sxs-lookup"><span data-stu-id="2aaab-132">3</span></span>          | <span data-ttu-id="2aaab-133">active</span><span class="sxs-lookup"><span data-stu-id="2aaab-133">active</span></span>   | <span data-ttu-id="2aaab-134">= 0 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="2aaab-134">= 0+2+2</span></span>       |
| <span data-ttu-id="2aaab-135">4</span><span class="sxs-lookup"><span data-stu-id="2aaab-135">4</span></span>          | <span data-ttu-id="2aaab-136">неактивно</span><span class="sxs-lookup"><span data-stu-id="2aaab-136">inactive</span></span> | <span data-ttu-id="2aaab-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2aaab-137">n/a</span></span>           |
| <span data-ttu-id="2aaab-138">5</span><span class="sxs-lookup"><span data-stu-id="2aaab-138">5</span></span>          | <span data-ttu-id="2aaab-139">active</span><span class="sxs-lookup"><span data-stu-id="2aaab-139">active</span></span>   | <span data-ttu-id="2aaab-140">= 0 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="2aaab-140">= 0+2+2+2</span></span>     |
| <span data-ttu-id="2aaab-141">6</span><span class="sxs-lookup"><span data-stu-id="2aaab-141">6</span></span>          | <span data-ttu-id="2aaab-142">active</span><span class="sxs-lookup"><span data-stu-id="2aaab-142">active</span></span>   | <span data-ttu-id="2aaab-143">= 0 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="2aaab-143">= 0+2+2+2+2</span></span>   |
| <span data-ttu-id="2aaab-144">7</span><span class="sxs-lookup"><span data-stu-id="2aaab-144">7</span></span>          | <span data-ttu-id="2aaab-145">active</span><span class="sxs-lookup"><span data-stu-id="2aaab-145">active</span></span>   | <span data-ttu-id="2aaab-146">= 0 + 2 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="2aaab-146">= 0+2+2+2+2+2</span></span> |

## <a name="see-also"></a><span data-ttu-id="2aaab-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2aaab-147">See also</span></span>

[<span data-ttu-id="2aaab-148">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="2aaab-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="2aaab-149">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="2aaab-149">Shader Model 6</span></span>](shader-model-6-0.md)
