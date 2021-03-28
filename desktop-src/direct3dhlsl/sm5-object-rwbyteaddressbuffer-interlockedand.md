---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккеданд'
description: And значение атомарным образом.
ms.assetid: c4024be0-3884-4af9-8075-76774c7c6178
keywords:
- Функция Интерлоккеданд HLSL
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a389da886b193815c7d4b2c1fe0a86db1f068fc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413143"
---
# <a name="interlockedand-function"></a><span data-ttu-id="d8668-104">Функция Интерлоккеданд</span><span class="sxs-lookup"><span data-stu-id="d8668-104">InterlockedAnd function</span></span>

<span data-ttu-id="d8668-105">And значение атомарным образом.</span><span class="sxs-lookup"><span data-stu-id="d8668-105">Ands the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8668-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8668-106">Syntax</span></span>

``` syntax
void InterlockedAnd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="d8668-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8668-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8668-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8668-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8668-109">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8668-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8668-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="d8668-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="d8668-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8668-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8668-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8668-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8668-113">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="d8668-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="d8668-114">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d8668-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8668-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8668-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8668-116">Исходное значение.</span><span class="sxs-lookup"><span data-stu-id="d8668-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8668-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8668-117">Return value</span></span>

<span data-ttu-id="d8668-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d8668-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8668-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="d8668-119">Remarks</span></span>

<span data-ttu-id="d8668-120">Эта операция может выполняться только с типизированными ресурсами типа int или uint и переменными общей памяти.</span><span class="sxs-lookup"><span data-stu-id="d8668-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="d8668-121">Существует три возможных способа использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="d8668-121">There are three possible uses for this function.</span></span> <span data-ttu-id="d8668-122">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="d8668-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="d8668-123">В этом случае функция выполняет атомарный параметр и для регистра общей памяти, на который ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="d8668-123">In this case, the function performs an atomic and of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="d8668-124">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="d8668-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="d8668-125">В этом сценарии функция выполняет атомарное значение и из для расположения ресурса, на которое ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="d8668-125">In this scenario, the function performs an atomic and of value to the resource location referenced by dest.</span></span> <span data-ttu-id="d8668-126">Наконец, третий сценарий происходит, когда R является локальным типом переменной.</span><span class="sxs-lookup"><span data-stu-id="d8668-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="d8668-127">В этом сценарии функция сокращается до и из значения dest и value, хранящегося в dest.</span><span class="sxs-lookup"><span data-stu-id="d8668-127">In this scenario, the function reduces to an and of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="d8668-128">Перегруженная функция имеет дополнительную выходную переменную, которой будет присвоено исходное значение dest.</span><span class="sxs-lookup"><span data-stu-id="d8668-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="d8668-129">Эта перегруженная операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d8668-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="d8668-130">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="d8668-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="d8668-131">VS</span><span class="sxs-lookup"><span data-stu-id="d8668-131">VS</span></span>  | <span data-ttu-id="d8668-132">HS</span><span class="sxs-lookup"><span data-stu-id="d8668-132">HS</span></span>  | <span data-ttu-id="d8668-133">DS</span><span class="sxs-lookup"><span data-stu-id="d8668-133">DS</span></span>  | <span data-ttu-id="d8668-134">GS</span><span class="sxs-lookup"><span data-stu-id="d8668-134">GS</span></span>  | <span data-ttu-id="d8668-135">PS</span><span class="sxs-lookup"><span data-stu-id="d8668-135">PS</span></span>  | <span data-ttu-id="d8668-136">CS</span><span class="sxs-lookup"><span data-stu-id="d8668-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="d8668-137">x</span><span class="sxs-lookup"><span data-stu-id="d8668-137">x</span></span>   | <span data-ttu-id="d8668-138">x</span><span class="sxs-lookup"><span data-stu-id="d8668-138">x</span></span>   |  <span data-ttu-id="d8668-139">x</span><span class="sxs-lookup"><span data-stu-id="d8668-139">x</span></span>  | <span data-ttu-id="d8668-140">x</span><span class="sxs-lookup"><span data-stu-id="d8668-140">x</span></span>   | <span data-ttu-id="d8668-141">x</span><span class="sxs-lookup"><span data-stu-id="d8668-141">x</span></span>   | <span data-ttu-id="d8668-142">x</span><span class="sxs-lookup"><span data-stu-id="d8668-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="d8668-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8668-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8668-144">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="d8668-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="d8668-145">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d8668-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 