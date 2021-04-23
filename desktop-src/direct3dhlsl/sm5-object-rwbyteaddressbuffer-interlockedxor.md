---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккедксор'
description: Выполняет атомарное исключающее XOR для значения.
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
keywords:
- Функция Интерлоккедксор HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 920ae912c599b66a03a25d7bc8ecc9b199036b26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987531"
---
# <a name="interlockedxor-function"></a><span data-ttu-id="4db35-104">Функция Интерлоккедксор</span><span class="sxs-lookup"><span data-stu-id="4db35-104">InterlockedXor function</span></span>

<span data-ttu-id="4db35-105">Выполняет атомарное **исключающее XOR** для значения.</span><span class="sxs-lookup"><span data-stu-id="4db35-105">Performs an atomic **XOR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db35-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4db35-106">Syntax</span></span>

``` syntax
void InterlockedXor(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="4db35-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4db35-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4db35-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4db35-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db35-109">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4db35-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4db35-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="4db35-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="4db35-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4db35-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db35-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4db35-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4db35-113">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="4db35-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="4db35-114">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4db35-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4db35-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4db35-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4db35-116">Исходное значение.</span><span class="sxs-lookup"><span data-stu-id="4db35-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4db35-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4db35-117">Return value</span></span>

<span data-ttu-id="4db35-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4db35-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4db35-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="4db35-119">Remarks</span></span>

<span data-ttu-id="4db35-120">Эту операцию можно выполнить только для типизированных ресурсов **типа int** или **uint** и переменных общей памяти.</span><span class="sxs-lookup"><span data-stu-id="4db35-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="4db35-121">Существует три возможных способа использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="4db35-121">There are three possible uses for this function.</span></span> <span data-ttu-id="4db35-122">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="4db35-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="4db35-123">В этом случае функция выполняет атомарное **исключающее XOR** со значением регистра общей памяти, на который ссылается *dest*.</span><span class="sxs-lookup"><span data-stu-id="4db35-123">In this case, the function performs an atomic **XOR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="4db35-124">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="4db35-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="4db35-125">В этом сценарии функция выполняет атомарное **исключающее XOR** со значением расположения ресурса, на которое ссылается *dest*.</span><span class="sxs-lookup"><span data-stu-id="4db35-125">In this scenario, the function performs an atomic **XOR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="4db35-126">Наконец, третий сценарий происходит, когда R является локальным типом переменной.</span><span class="sxs-lookup"><span data-stu-id="4db35-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="4db35-127">В этом сценарии функция сокращается до **исключающего** со значениями *dest* и *value*.</span><span class="sxs-lookup"><span data-stu-id="4db35-127">In this scenario, the function reduces to an **XOR** of the values of *dest* and *value*.</span></span> <span data-ttu-id="4db35-128">Результат операции заменяет значение в *dest*.</span><span class="sxs-lookup"><span data-stu-id="4db35-128">The result of the operation replaces the value in *dest*.</span></span> <span data-ttu-id="4db35-129">Перегруженная функция имеет дополнительную выходную переменную, которой будет присвоено исходное значение *dest*.</span><span class="sxs-lookup"><span data-stu-id="4db35-129">The overloaded function has an additional output variable which will be set to the original value of *dest*.</span></span> <span data-ttu-id="4db35-130">Перегруженная операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4db35-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="4db35-131">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="4db35-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4db35-132">VS</span><span class="sxs-lookup"><span data-stu-id="4db35-132">VS</span></span>  | <span data-ttu-id="4db35-133">HS</span><span class="sxs-lookup"><span data-stu-id="4db35-133">HS</span></span>  | <span data-ttu-id="4db35-134">DS</span><span class="sxs-lookup"><span data-stu-id="4db35-134">DS</span></span>  | <span data-ttu-id="4db35-135">GS</span><span class="sxs-lookup"><span data-stu-id="4db35-135">GS</span></span>  | <span data-ttu-id="4db35-136">PS</span><span class="sxs-lookup"><span data-stu-id="4db35-136">PS</span></span>  | <span data-ttu-id="4db35-137">CS</span><span class="sxs-lookup"><span data-stu-id="4db35-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="4db35-138">x</span><span class="sxs-lookup"><span data-stu-id="4db35-138">x</span></span>   |  <span data-ttu-id="4db35-139">x</span><span class="sxs-lookup"><span data-stu-id="4db35-139">x</span></span>  | <span data-ttu-id="4db35-140">x</span><span class="sxs-lookup"><span data-stu-id="4db35-140">x</span></span>   | <span data-ttu-id="4db35-141">x</span><span class="sxs-lookup"><span data-stu-id="4db35-141">x</span></span>   | <span data-ttu-id="4db35-142">x</span><span class="sxs-lookup"><span data-stu-id="4db35-142">x</span></span>   | <span data-ttu-id="4db35-143">x</span><span class="sxs-lookup"><span data-stu-id="4db35-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="4db35-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4db35-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db35-145">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="4db35-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="4db35-146">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="4db35-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 