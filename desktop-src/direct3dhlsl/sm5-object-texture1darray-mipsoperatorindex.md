---
title: 'Texture1DArray:: MIPS. Operator, функция'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Texture1DArray:: MIPS. Operator, функция'
ms.assetid: b8f2ef78-4b50-4051-a00f-5b81cd77d1e0
keywords:
- MIPS. Оператор Function HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbe2d1116839cede8dda69f1b0b8cf9a049595e9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081794"
---
# <a name="texture1darraymipsoperator----function"></a><span data-ttu-id="42461-105">Texture1DArray:: MIPS. Operator, функция</span><span class="sxs-lookup"><span data-stu-id="42461-105">Texture1DArray::mips.Operator    function</span></span>

<span data-ttu-id="42461-106">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="42461-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="42461-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42461-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="42461-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="42461-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42461-109">*мипслице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42461-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42461-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="42461-110">Type: **uint**</span></span>

<span data-ttu-id="42461-111">Индекс среза MIP.</span><span class="sxs-lookup"><span data-stu-id="42461-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="42461-112">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42461-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42461-113">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="42461-113">Type: **uint2**</span></span>

<span data-ttu-id="42461-114">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="42461-114">The index position.</span></span> <span data-ttu-id="42461-115">Первый компонент содержит координату x.</span><span class="sxs-lookup"><span data-stu-id="42461-115">The first component contains the x-coordinate.</span></span> <span data-ttu-id="42461-116">Второй компонент указывает нужный срез массива.</span><span class="sxs-lookup"><span data-stu-id="42461-116">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42461-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42461-117">Return value</span></span>

<span data-ttu-id="42461-118">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="42461-118">Type: **R**</span></span>

<span data-ttu-id="42461-119">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="42461-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="42461-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="42461-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="42461-121">Пример использования</span><span class="sxs-lookup"><span data-stu-id="42461-121">Usage Example</span></span>


```
Texture1DArray<float4> tex;
uint mip = 2;
uint2 pos_x_and_array = {1234, 3};
float4 f = tex.mips[mip][pos_x_and_array];        
        
```



<span data-ttu-id="42461-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="42461-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="42461-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="42461-123">Vertex</span></span> | <span data-ttu-id="42461-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="42461-124">Hull</span></span> | <span data-ttu-id="42461-125">Домен</span><span class="sxs-lookup"><span data-stu-id="42461-125">Domain</span></span> | <span data-ttu-id="42461-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="42461-126">Geometry</span></span> | <span data-ttu-id="42461-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="42461-127">Pixel</span></span> | <span data-ttu-id="42461-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="42461-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="42461-129">x</span><span class="sxs-lookup"><span data-stu-id="42461-129">x</span></span>      | <span data-ttu-id="42461-130">x</span><span class="sxs-lookup"><span data-stu-id="42461-130">x</span></span>    | <span data-ttu-id="42461-131">x</span><span class="sxs-lookup"><span data-stu-id="42461-131">x</span></span>      | <span data-ttu-id="42461-132">x</span><span class="sxs-lookup"><span data-stu-id="42461-132">x</span></span>        | <span data-ttu-id="42461-133">x</span><span class="sxs-lookup"><span data-stu-id="42461-133">x</span></span>     | <span data-ttu-id="42461-134">x</span><span class="sxs-lookup"><span data-stu-id="42461-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="42461-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42461-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42461-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="42461-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="42461-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="42461-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




