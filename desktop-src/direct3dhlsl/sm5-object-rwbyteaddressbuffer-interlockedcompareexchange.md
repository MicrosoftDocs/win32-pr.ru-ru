---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккедкомпариксчанже'
description: Сравнивает входные данные со значением сравнения и обменивает результат атомарным образом.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
keywords:
- Функция Интерлоккедкомпариксчанже HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793008"
---
# <a name="interlockedcompareexchange-function"></a><span data-ttu-id="b0f1d-104">Функция Интерлоккедкомпариксчанже</span><span class="sxs-lookup"><span data-stu-id="b0f1d-104">InterlockedCompareExchange function</span></span>

<span data-ttu-id="b0f1d-105">Сравнивает входные данные со значением сравнения и обменивает результат атомарным образом.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-105">Compares the input to the comparison value and exchanges the result, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f1d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0f1d-106">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="b0f1d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0f1d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f1d-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0f1d-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f1d-109">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b0f1d-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b0f1d-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="b0f1d-111">*сравнить \_ значение* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="b0f1d-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f1d-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b0f1d-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b0f1d-113">Значение сравнения.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="b0f1d-114">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0f1d-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f1d-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b0f1d-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b0f1d-116">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-116">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="b0f1d-117">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b0f1d-117">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f1d-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b0f1d-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b0f1d-119">Исходное значение.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-119">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0f1d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0f1d-120">Return value</span></span>

<span data-ttu-id="b0f1d-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0f1d-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0f1d-122">Remarks</span></span>

<span data-ttu-id="b0f1d-123">Атомарно сравнивает значение в *dest* для сравнения со *\_ значением*, сохраняет значение в *dest* , если значения совпадают, и возвращает исходное значение *dest* в *исходном \_ значении*.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-123">Atomically compares the value in *dest* to *compare\_value*, stores value in *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="b0f1d-124">Эта операция может выполняться только с типизированными ресурсами **типа int** или *uint* и переменными общей памяти.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-124">This operation can only be performed on **int** or *uint* typed resources and shared memory variables.</span></span> <span data-ttu-id="b0f1d-125">Существует три возможных способа использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-125">There are three possible uses for this function.</span></span> <span data-ttu-id="b0f1d-126">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-126">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="b0f1d-127">В этом случае функция выполняет операцию с регистром общей памяти, на который ссылается *dest*.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-127">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="b0f1d-128">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-128">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="b0f1d-129">В этом сценарии функция выполняет операцию с расположением ресурса, на которое ссылается *dest*.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-129">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="b0f1d-130">Наконец, третий сценарий происходит, когда R является локальным типом переменной.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-130">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="b0f1d-131">В этом сценарии функция сокращается до операции, выполняемой с помощью локальных операций.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-131">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="b0f1d-132">Эта операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-132">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="b0f1d-133">Если вы вызываете **интерлоккедкомпариксчанже** в цикле [**for**](dx-graphics-hlsl-for.md) или [**while**](dx-graphics-hlsl-while.md) COMPUTE, для правильной компиляции необходимо использовать атрибут **\[ allow \_ UAV \_ Condition \]** в этом цикле.</span><span class="sxs-lookup"><span data-stu-id="b0f1d-133">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

<span data-ttu-id="b0f1d-134">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="b0f1d-134">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="b0f1d-135">VS</span><span class="sxs-lookup"><span data-stu-id="b0f1d-135">VS</span></span>  | <span data-ttu-id="b0f1d-136">HS</span><span class="sxs-lookup"><span data-stu-id="b0f1d-136">HS</span></span>  | <span data-ttu-id="b0f1d-137">DS</span><span class="sxs-lookup"><span data-stu-id="b0f1d-137">DS</span></span>  | <span data-ttu-id="b0f1d-138">GS</span><span class="sxs-lookup"><span data-stu-id="b0f1d-138">GS</span></span>  | <span data-ttu-id="b0f1d-139">PS</span><span class="sxs-lookup"><span data-stu-id="b0f1d-139">PS</span></span>  | <span data-ttu-id="b0f1d-140">CS</span><span class="sxs-lookup"><span data-stu-id="b0f1d-140">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="b0f1d-141">x</span><span class="sxs-lookup"><span data-stu-id="b0f1d-141">x</span></span>   | <span data-ttu-id="b0f1d-142">x</span><span class="sxs-lookup"><span data-stu-id="b0f1d-142">x</span></span>   | <span data-ttu-id="b0f1d-143">x</span><span class="sxs-lookup"><span data-stu-id="b0f1d-143">x</span></span>   | <span data-ttu-id="b0f1d-144">x</span><span class="sxs-lookup"><span data-stu-id="b0f1d-144">x</span></span>   | <span data-ttu-id="b0f1d-145">x</span><span class="sxs-lookup"><span data-stu-id="b0f1d-145">x</span></span>   | <span data-ttu-id="b0f1d-146">x</span><span class="sxs-lookup"><span data-stu-id="b0f1d-146">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="b0f1d-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0f1d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f1d-148">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="b0f1d-148">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="b0f1d-149">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b0f1d-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 