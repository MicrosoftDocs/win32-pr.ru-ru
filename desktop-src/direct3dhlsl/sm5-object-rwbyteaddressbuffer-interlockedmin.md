---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккедмин'
description: Находит минимальное значение, атомарно.
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- Функция Интерлоккедмин HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b818a1fa0897d103e7d609a676212c6db428935f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070026"
---
# <a name="interlockedmin-function"></a><span data-ttu-id="2f118-104">Функция Интерлоккедмин</span><span class="sxs-lookup"><span data-stu-id="2f118-104">InterlockedMin function</span></span>

<span data-ttu-id="2f118-105">Находит минимальное значение, атомарно.</span><span class="sxs-lookup"><span data-stu-id="2f118-105">Finds the minimum value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f118-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f118-106">Syntax</span></span>

``` syntax
void InterlockedMin(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="2f118-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f118-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f118-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f118-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f118-109">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2f118-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2f118-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="2f118-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="2f118-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f118-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f118-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2f118-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2f118-113">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="2f118-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="2f118-114">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2f118-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f118-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2f118-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2f118-116">Исходное значение.</span><span class="sxs-lookup"><span data-stu-id="2f118-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f118-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f118-117">Return value</span></span>

<span data-ttu-id="2f118-118">Nothing</span><span class="sxs-lookup"><span data-stu-id="2f118-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="2f118-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f118-119">Remarks</span></span>

<span data-ttu-id="2f118-120">Эта операция может выполняться только с типизированными ресурсами int и uint и переменными общей памяти.</span><span class="sxs-lookup"><span data-stu-id="2f118-120">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="2f118-121">Существует три возможных способа использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="2f118-121">There are three possible uses for this function.</span></span> <span data-ttu-id="2f118-122">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="2f118-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="2f118-123">В этом случае функция выполняет атомарный минимум значения для регистра общей памяти, на который ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="2f118-123">In this case, the function performs an atomic minimum of the value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="2f118-124">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="2f118-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="2f118-125">В этом сценарии функция выполняет атомарное минимальное значение для расположения ресурса, на которое ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="2f118-125">In this scenario, the function performs an atomic minimum of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="2f118-126">Наконец, третий сценарий происходит, когда R является локальным типом переменной.</span><span class="sxs-lookup"><span data-stu-id="2f118-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="2f118-127">В этом сценарии функция сокращает до минимума значение dest и value, хранящееся в dest.</span><span class="sxs-lookup"><span data-stu-id="2f118-127">In this scenario, the function reduces to a minimum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="2f118-128">Перегруженная функция имеет дополнительную выходную переменную, которой будет присвоено исходное значение dest.</span><span class="sxs-lookup"><span data-stu-id="2f118-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="2f118-129">Эта перегруженная операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2f118-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="2f118-130">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="2f118-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2f118-131">VS</span><span class="sxs-lookup"><span data-stu-id="2f118-131">VS</span></span>  | <span data-ttu-id="2f118-132">HS</span><span class="sxs-lookup"><span data-stu-id="2f118-132">HS</span></span>  | <span data-ttu-id="2f118-133">DS</span><span class="sxs-lookup"><span data-stu-id="2f118-133">DS</span></span>  | <span data-ttu-id="2f118-134">GS</span><span class="sxs-lookup"><span data-stu-id="2f118-134">GS</span></span>  | <span data-ttu-id="2f118-135">PS</span><span class="sxs-lookup"><span data-stu-id="2f118-135">PS</span></span>  | <span data-ttu-id="2f118-136">CS</span><span class="sxs-lookup"><span data-stu-id="2f118-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="2f118-137">x</span><span class="sxs-lookup"><span data-stu-id="2f118-137">x</span></span>   |  <span data-ttu-id="2f118-138">x</span><span class="sxs-lookup"><span data-stu-id="2f118-138">x</span></span>  | <span data-ttu-id="2f118-139">x</span><span class="sxs-lookup"><span data-stu-id="2f118-139">x</span></span>   | <span data-ttu-id="2f118-140">x</span><span class="sxs-lookup"><span data-stu-id="2f118-140">x</span></span>   | <span data-ttu-id="2f118-141">x</span><span class="sxs-lookup"><span data-stu-id="2f118-141">x</span></span>   | <span data-ttu-id="2f118-142">x</span><span class="sxs-lookup"><span data-stu-id="2f118-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="2f118-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f118-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f118-144">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="2f118-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="2f118-145">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="2f118-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 