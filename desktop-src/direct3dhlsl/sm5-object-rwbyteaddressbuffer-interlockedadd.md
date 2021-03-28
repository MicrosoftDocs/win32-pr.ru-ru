---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккедадд'
description: Добавляет значение атомарным образом.
ms.assetid: 27274aae-1e75-4626-9997-57c4e9393000
keywords:
- Функция Интерлоккедадд HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_location:
- winnt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d352ed97df15ce076c10950c6da94aaeaff0f2d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997074"
---
# <a name="interlockedadd-function"></a><span data-ttu-id="05b66-104">Функция Интерлоккедадд</span><span class="sxs-lookup"><span data-stu-id="05b66-104">InterlockedAdd function</span></span>

<span data-ttu-id="05b66-105">Добавляет значение атомарным образом.</span><span class="sxs-lookup"><span data-stu-id="05b66-105">Adds the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b66-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05b66-106">Syntax</span></span>

``` syntax
void InterlockedAdd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="05b66-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="05b66-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05b66-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05b66-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05b66-109">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="05b66-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="05b66-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="05b66-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="05b66-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05b66-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05b66-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="05b66-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="05b66-113">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="05b66-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="05b66-114">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="05b66-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05b66-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="05b66-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="05b66-116">Исходное значение.</span><span class="sxs-lookup"><span data-stu-id="05b66-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05b66-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05b66-117">Return value</span></span>

<span data-ttu-id="05b66-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="05b66-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05b66-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="05b66-119">Remarks</span></span>

<span data-ttu-id="05b66-120">Эту операцию можно выполнить только для типизированных ресурсов типа int или uint и переменных общей памяти.</span><span class="sxs-lookup"><span data-stu-id="05b66-120">This operation can be performed only on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="05b66-121">Существует три возможных способа использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="05b66-121">There are three possible uses for this function.</span></span> <span data-ttu-id="05b66-122">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="05b66-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="05b66-123">В этом случае функция выполняет атомарное Добавление значения в регистр общей памяти, на который ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="05b66-123">In this case, the function performs an atomic add of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="05b66-124">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="05b66-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="05b66-125">В этом сценарии функция выполняет атомарное Добавление значения в расположение ресурса, на которое ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="05b66-125">In this scenario, the function performs an atomic add of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="05b66-126">Наконец, третий сценарий происходит, когда R является локальным типом переменной.</span><span class="sxs-lookup"><span data-stu-id="05b66-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="05b66-127">В этом сценарии функция сокращается до суммы значений dest и value, сохраненных в dest.</span><span class="sxs-lookup"><span data-stu-id="05b66-127">In this scenario, the function reduces to a sum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="05b66-128">Перегруженная функция имеет дополнительную выходную переменную, которой будет присвоено исходное значение dest.</span><span class="sxs-lookup"><span data-stu-id="05b66-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="05b66-129">Эта перегруженная операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="05b66-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="05b66-130">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="05b66-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="05b66-131">VS</span><span class="sxs-lookup"><span data-stu-id="05b66-131">VS</span></span>  | <span data-ttu-id="05b66-132">HS</span><span class="sxs-lookup"><span data-stu-id="05b66-132">HS</span></span>  | <span data-ttu-id="05b66-133">DS</span><span class="sxs-lookup"><span data-stu-id="05b66-133">DS</span></span>  | <span data-ttu-id="05b66-134">GS</span><span class="sxs-lookup"><span data-stu-id="05b66-134">GS</span></span>  | <span data-ttu-id="05b66-135">PS</span><span class="sxs-lookup"><span data-stu-id="05b66-135">PS</span></span>  | <span data-ttu-id="05b66-136">CS</span><span class="sxs-lookup"><span data-stu-id="05b66-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="05b66-137">x</span><span class="sxs-lookup"><span data-stu-id="05b66-137">x</span></span>   | <span data-ttu-id="05b66-138">x</span><span class="sxs-lookup"><span data-stu-id="05b66-138">x</span></span>   | <span data-ttu-id="05b66-139">x</span><span class="sxs-lookup"><span data-stu-id="05b66-139">x</span></span>   | <span data-ttu-id="05b66-140">x</span><span class="sxs-lookup"><span data-stu-id="05b66-140">x</span></span>   | <span data-ttu-id="05b66-141">x</span><span class="sxs-lookup"><span data-stu-id="05b66-141">x</span></span>   | <span data-ttu-id="05b66-142">x</span><span class="sxs-lookup"><span data-stu-id="05b66-142">x</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="05b66-143">Требования</span><span class="sxs-lookup"><span data-stu-id="05b66-143">Requirements</span></span>




## <a name="see-also"></a><span data-ttu-id="05b66-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05b66-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05b66-145">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="05b66-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="05b66-146">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="05b66-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

