---
title: 'Рвбитеаддрессбуффер:: функция взаимоблокировки'
description: Выполняет атомарное или для значения.
ms.assetid: 3a05619b-db97-4cf1-af3c-12c376e605a6
keywords:
- HLSL функция взаимоблокировки
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14b902f70919c79ed3e313671ede709f284a1490
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987532"
---
# <a name="interlockedor-function"></a><span data-ttu-id="5c2c1-104">Функция взаимоблокировки</span><span class="sxs-lookup"><span data-stu-id="5c2c1-104">InterlockedOr function</span></span>

<span data-ttu-id="5c2c1-105">Выполняет атомарное **или** для значения.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-105">Performs an atomic **OR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2c1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c2c1-106">Syntax</span></span>

``` syntax
void InterlockedOr(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="5c2c1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c2c1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c2c1-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c2c1-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c2c1-109">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c2c1-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5c2c1-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="5c2c1-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c2c1-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c2c1-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c2c1-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5c2c1-113">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="5c2c1-114">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c2c1-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c2c1-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c2c1-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5c2c1-116">Исходное значение.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c2c1-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c2c1-117">Return value</span></span>

<span data-ttu-id="5c2c1-118">Nothing</span><span class="sxs-lookup"><span data-stu-id="5c2c1-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="5c2c1-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c2c1-119">Remarks</span></span>

<span data-ttu-id="5c2c1-120">Эту операцию можно выполнить только для типизированных ресурсов **типа int** или **uint** и переменных общей памяти.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="5c2c1-121">Существует три возможных способа использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-121">There are three possible uses for this function.</span></span> <span data-ttu-id="5c2c1-122">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="5c2c1-123">В этом случае функция выполняет атомарную операцию **или** со значением регистра общей памяти, на который ссылается *dest*.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-123">In this case, the function performs an atomic **OR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="5c2c1-124">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="5c2c1-125">В этом сценарии функция выполняет атомарную операцию **или** со значением расположения ресурса, на которое ссылается *dest*.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-125">In this scenario, the function performs an atomic **OR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="5c2c1-126">Наконец, третий сценарий происходит, когда R является локальным типом переменной.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="5c2c1-127">В этом сценарии функция сокращается до **или** со значениями *dest* и *value*.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-127">In this scenario, the function reduces to an **OR** with the values of *dest* and *value*.</span></span> <span data-ttu-id="5c2c1-128">Результат операции заменяет значение *dest*.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-128">The result of the operation replaces the value of *dest*.</span></span> <span data-ttu-id="5c2c1-129">Перегруженная функция имеет дополнительную выходную переменную, которой будет присвоено исходное значение *dest*.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-129">The overloaded function has an additional output variable, which will be set to the original value of *dest*.</span></span> <span data-ttu-id="5c2c1-130">Перегруженная операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5c2c1-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="5c2c1-131">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="5c2c1-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="5c2c1-132">VS</span><span class="sxs-lookup"><span data-stu-id="5c2c1-132">VS</span></span>  | <span data-ttu-id="5c2c1-133">HS</span><span class="sxs-lookup"><span data-stu-id="5c2c1-133">HS</span></span>  | <span data-ttu-id="5c2c1-134">DS</span><span class="sxs-lookup"><span data-stu-id="5c2c1-134">DS</span></span>  | <span data-ttu-id="5c2c1-135">GS</span><span class="sxs-lookup"><span data-stu-id="5c2c1-135">GS</span></span>  | <span data-ttu-id="5c2c1-136">PS</span><span class="sxs-lookup"><span data-stu-id="5c2c1-136">PS</span></span>  | <span data-ttu-id="5c2c1-137">CS</span><span class="sxs-lookup"><span data-stu-id="5c2c1-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="5c2c1-138">x</span><span class="sxs-lookup"><span data-stu-id="5c2c1-138">x</span></span>   |  <span data-ttu-id="5c2c1-139">x</span><span class="sxs-lookup"><span data-stu-id="5c2c1-139">x</span></span>  | <span data-ttu-id="5c2c1-140">x</span><span class="sxs-lookup"><span data-stu-id="5c2c1-140">x</span></span>   | <span data-ttu-id="5c2c1-141">x</span><span class="sxs-lookup"><span data-stu-id="5c2c1-141">x</span></span>   | <span data-ttu-id="5c2c1-142">x</span><span class="sxs-lookup"><span data-stu-id="5c2c1-142">x</span></span>   | <span data-ttu-id="5c2c1-143">x</span><span class="sxs-lookup"><span data-stu-id="5c2c1-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="5c2c1-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c2c1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2c1-145">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="5c2c1-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="5c2c1-146">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="5c2c1-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 