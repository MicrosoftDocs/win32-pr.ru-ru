---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккедкомпаресторе'
description: Ккомпарес входные данные для значения сравнения атомарно.
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
keywords:
- Функция Интерлоккедкомпаресторе HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abaa390ba74657e42b54a5147a7bc4006564a5fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890909"
---
# <a name="interlockedcomparestore-function"></a><span data-ttu-id="f8ac7-104">Функция Интерлоккедкомпаресторе</span><span class="sxs-lookup"><span data-stu-id="f8ac7-104">InterlockedCompareStore function</span></span>

<span data-ttu-id="f8ac7-105">Ккомпарес входные данные для значения сравнения атомарно.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-105">Ccompares the input to the comparison value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ac7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8ac7-106">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a><span data-ttu-id="f8ac7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8ac7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ac7-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8ac7-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ac7-109">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8ac7-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8ac7-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="f8ac7-111">*сравнить \_ значение* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f8ac7-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ac7-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8ac7-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8ac7-113">Значение сравнения.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="f8ac7-114">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8ac7-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ac7-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8ac7-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8ac7-116">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-116">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ac7-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8ac7-117">Return value</span></span>

<span data-ttu-id="f8ac7-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ac7-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8ac7-119">Remarks</span></span>

<span data-ttu-id="f8ac7-120">Эта операция может выполняться только с типизированными ресурсами типа int или uint и переменными общей памяти.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="f8ac7-121">Существует три возможных способа использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-121">There are three possible uses for this function.</span></span> <span data-ttu-id="f8ac7-122">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="f8ac7-123">В этом случае функция выполняет операцию с регистром общей памяти, на который ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="f8ac7-124">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="f8ac7-125">В этом сценарии функция выполняет операцию с расположением ресурса, на которое ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="f8ac7-126">Наконец, третий сценарий происходит, когда R является локальным типом переменной.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="f8ac7-127">В этом сценарии функция сокращается до операции, выполняемой с помощью локальных операций.</span><span class="sxs-lookup"><span data-stu-id="f8ac7-127">In this scenario, the function reduces to the operation performed using local operations.</span></span>

<span data-ttu-id="f8ac7-128">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="f8ac7-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f8ac7-129">VS</span><span class="sxs-lookup"><span data-stu-id="f8ac7-129">VS</span></span>  | <span data-ttu-id="f8ac7-130">HS</span><span class="sxs-lookup"><span data-stu-id="f8ac7-130">HS</span></span>  | <span data-ttu-id="f8ac7-131">DS</span><span class="sxs-lookup"><span data-stu-id="f8ac7-131">DS</span></span>  | <span data-ttu-id="f8ac7-132">GS</span><span class="sxs-lookup"><span data-stu-id="f8ac7-132">GS</span></span>  | <span data-ttu-id="f8ac7-133">PS</span><span class="sxs-lookup"><span data-stu-id="f8ac7-133">PS</span></span>  | <span data-ttu-id="f8ac7-134">CS</span><span class="sxs-lookup"><span data-stu-id="f8ac7-134">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="f8ac7-135">x</span><span class="sxs-lookup"><span data-stu-id="f8ac7-135">x</span></span>   | <span data-ttu-id="f8ac7-136">x</span><span class="sxs-lookup"><span data-stu-id="f8ac7-136">x</span></span>   | <span data-ttu-id="f8ac7-137">x</span><span class="sxs-lookup"><span data-stu-id="f8ac7-137">x</span></span>   | <span data-ttu-id="f8ac7-138">x</span><span class="sxs-lookup"><span data-stu-id="f8ac7-138">x</span></span>   | <span data-ttu-id="f8ac7-139">x</span><span class="sxs-lookup"><span data-stu-id="f8ac7-139">x</span></span>   | <span data-ttu-id="f8ac7-140">x</span><span class="sxs-lookup"><span data-stu-id="f8ac7-140">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="f8ac7-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8ac7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ac7-142">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="f8ac7-142">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="f8ac7-143">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="f8ac7-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 