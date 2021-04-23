---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккедексчанже'
description: Обменивает значение атомарным образом.
ms.assetid: a50f4cba-a7a2-44b0-9de7-003b4c7a947f
keywords:
- Функция Интерлоккедексчанже HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47c51374b7dcd62ac208e0aa8811a8d693ce0ac6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997043"
---
# <a name="interlockedexchange-function"></a><span data-ttu-id="c8b3c-104">Функция Интерлоккедексчанже</span><span class="sxs-lookup"><span data-stu-id="c8b3c-104">InterlockedExchange function</span></span>

<span data-ttu-id="c8b3c-105">Обменивает значение атомарным образом.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-105">Exchanges a value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b3c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8b3c-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="c8b3c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8b3c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8b3c-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8b3c-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b3c-109">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c8b3c-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c8b3c-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="c8b3c-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8b3c-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b3c-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c8b3c-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c8b3c-113">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="c8b3c-114">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8b3c-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b3c-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c8b3c-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c8b3c-116">Исходное значение.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8b3c-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8b3c-117">Return value</span></span>

<span data-ttu-id="c8b3c-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8b3c-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="c8b3c-119">Remarks</span></span>

<span data-ttu-id="c8b3c-120">Эта операция может выполняться только с скалярными ресурсами и переменными общей памяти.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="c8b3c-121">Существует три возможных способа использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-121">There are three possible uses for this function.</span></span> <span data-ttu-id="c8b3c-122">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="c8b3c-123">В этом случае функция выполняет операцию с регистром общей памяти, на который ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="c8b3c-124">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="c8b3c-125">В этом сценарии функция выполняет операцию с расположением ресурса, на которое ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="c8b3c-126">Наконец, третий сценарий происходит, когда R является локальным типом переменной.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="c8b3c-127">В этом сценарии функция сокращается до операции, выполняемой с помощью локальных операций.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-127">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="c8b3c-128">Эта операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c8b3c-128">This operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="c8b3c-129">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="c8b3c-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c8b3c-130">VS</span><span class="sxs-lookup"><span data-stu-id="c8b3c-130">VS</span></span>  | <span data-ttu-id="c8b3c-131">HS</span><span class="sxs-lookup"><span data-stu-id="c8b3c-131">HS</span></span>  | <span data-ttu-id="c8b3c-132">DS</span><span class="sxs-lookup"><span data-stu-id="c8b3c-132">DS</span></span>  | <span data-ttu-id="c8b3c-133">GS</span><span class="sxs-lookup"><span data-stu-id="c8b3c-133">GS</span></span>  | <span data-ttu-id="c8b3c-134">PS</span><span class="sxs-lookup"><span data-stu-id="c8b3c-134">PS</span></span>  | <span data-ttu-id="c8b3c-135">CS</span><span class="sxs-lookup"><span data-stu-id="c8b3c-135">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
|  <span data-ttu-id="c8b3c-136">x</span><span class="sxs-lookup"><span data-stu-id="c8b3c-136">x</span></span>  |  <span data-ttu-id="c8b3c-137">x</span><span class="sxs-lookup"><span data-stu-id="c8b3c-137">x</span></span>  |  <span data-ttu-id="c8b3c-138">x</span><span class="sxs-lookup"><span data-stu-id="c8b3c-138">x</span></span>  |  <span data-ttu-id="c8b3c-139">x</span><span class="sxs-lookup"><span data-stu-id="c8b3c-139">x</span></span>  | <span data-ttu-id="c8b3c-140">x</span><span class="sxs-lookup"><span data-stu-id="c8b3c-140">x</span></span>   | <span data-ttu-id="c8b3c-141">x</span><span class="sxs-lookup"><span data-stu-id="c8b3c-141">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="c8b3c-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8b3c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b3c-143">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="c8b3c-143">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="c8b3c-144">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c8b3c-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 