---
title: 'Texture2DArray:: MIPS. Operator, функция'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Texture2DArray:: MIPS. Operator, функция'
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
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
ms.openlocfilehash: 17f24dd54768f3583f508527b7e03f72399bf98e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820789"
---
# <a name="texture2darraymipsoperator----function"></a><span data-ttu-id="86a89-105">Texture2DArray:: MIPS. Operator, функция</span><span class="sxs-lookup"><span data-stu-id="86a89-105">Texture2DArray::mips.Operator    function</span></span>

<span data-ttu-id="86a89-106">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="86a89-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="86a89-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86a89-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="86a89-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="86a89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86a89-109">*мипслице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86a89-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86a89-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="86a89-110">Type: **uint**</span></span>

<span data-ttu-id="86a89-111">Индекс среза MIP.</span><span class="sxs-lookup"><span data-stu-id="86a89-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="86a89-112">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86a89-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86a89-113">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="86a89-113">Type: **uint3**</span></span>

<span data-ttu-id="86a89-114">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="86a89-114">The index position.</span></span> <span data-ttu-id="86a89-115">Первый и второй компоненты содержат координаты (x, y).</span><span class="sxs-lookup"><span data-stu-id="86a89-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="86a89-116">Третий компонент указывает нужный срез массива.</span><span class="sxs-lookup"><span data-stu-id="86a89-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86a89-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86a89-117">Return value</span></span>

<span data-ttu-id="86a89-118">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="86a89-118">Type: **R**</span></span>

<span data-ttu-id="86a89-119">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="86a89-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="86a89-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="86a89-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="86a89-121">Пример использования</span><span class="sxs-lookup"><span data-stu-id="86a89-121">Usage Example</span></span>


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



<span data-ttu-id="86a89-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="86a89-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="86a89-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="86a89-123">Vertex</span></span> | <span data-ttu-id="86a89-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="86a89-124">Hull</span></span> | <span data-ttu-id="86a89-125">Домен</span><span class="sxs-lookup"><span data-stu-id="86a89-125">Domain</span></span> | <span data-ttu-id="86a89-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="86a89-126">Geometry</span></span> | <span data-ttu-id="86a89-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="86a89-127">Pixel</span></span> | <span data-ttu-id="86a89-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="86a89-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="86a89-129">x</span><span class="sxs-lookup"><span data-stu-id="86a89-129">x</span></span>      | <span data-ttu-id="86a89-130">x</span><span class="sxs-lookup"><span data-stu-id="86a89-130">x</span></span>    | <span data-ttu-id="86a89-131">x</span><span class="sxs-lookup"><span data-stu-id="86a89-131">x</span></span>      | <span data-ttu-id="86a89-132">x</span><span class="sxs-lookup"><span data-stu-id="86a89-132">x</span></span>        | <span data-ttu-id="86a89-133">x</span><span class="sxs-lookup"><span data-stu-id="86a89-133">x</span></span>     | <span data-ttu-id="86a89-134">x</span><span class="sxs-lookup"><span data-stu-id="86a89-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="86a89-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86a89-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86a89-136">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="86a89-136">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="86a89-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="86a89-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




