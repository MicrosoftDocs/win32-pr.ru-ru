---
title: 'Texture1D:: MIPS. Operator, функция'
description: Возвращает переменную ресурса, доступную только для чтения, или Texture1D.
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
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
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340230"
---
# <a name="texture1dmipsoperator----function"></a><span data-ttu-id="cefdc-104">Texture1D:: MIPS. Operator, функция</span><span class="sxs-lookup"><span data-stu-id="cefdc-104">Texture1D::mips.Operator    function</span></span>

<span data-ttu-id="cefdc-105">Возвращает переменную ресурса, доступную только для чтения, или [**Texture1D**](sm5-object-texture1d.md).</span><span class="sxs-lookup"><span data-stu-id="cefdc-105">Returns a read-only resource variable or a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cefdc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cefdc-106">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="cefdc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cefdc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cefdc-108">*мипслице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cefdc-108">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cefdc-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="cefdc-109">Type: **uint**</span></span>

<span data-ttu-id="cefdc-110">Индекс среза MIP.</span><span class="sxs-lookup"><span data-stu-id="cefdc-110">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="cefdc-111">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cefdc-111">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cefdc-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="cefdc-112">Type: **uint**</span></span>

<span data-ttu-id="cefdc-113">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="cefdc-113">The index position.</span></span> <span data-ttu-id="cefdc-114">Содержит координату x.</span><span class="sxs-lookup"><span data-stu-id="cefdc-114">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cefdc-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cefdc-115">Return value</span></span>

<span data-ttu-id="cefdc-116">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="cefdc-116">Type: **R**</span></span>

<span data-ttu-id="cefdc-117">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cefdc-117">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="cefdc-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="cefdc-118">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="cefdc-119">Пример использования</span><span class="sxs-lookup"><span data-stu-id="cefdc-119">Usage Example</span></span>


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



<span data-ttu-id="cefdc-120">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="cefdc-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cefdc-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="cefdc-121">Vertex</span></span> | <span data-ttu-id="cefdc-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="cefdc-122">Hull</span></span> | <span data-ttu-id="cefdc-123">Домен</span><span class="sxs-lookup"><span data-stu-id="cefdc-123">Domain</span></span> | <span data-ttu-id="cefdc-124">Геометрия</span><span class="sxs-lookup"><span data-stu-id="cefdc-124">Geometry</span></span> | <span data-ttu-id="cefdc-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="cefdc-125">Pixel</span></span> | <span data-ttu-id="cefdc-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="cefdc-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cefdc-127">x</span><span class="sxs-lookup"><span data-stu-id="cefdc-127">x</span></span>      | <span data-ttu-id="cefdc-128">x</span><span class="sxs-lookup"><span data-stu-id="cefdc-128">x</span></span>    | <span data-ttu-id="cefdc-129">x</span><span class="sxs-lookup"><span data-stu-id="cefdc-129">x</span></span>      | <span data-ttu-id="cefdc-130">x</span><span class="sxs-lookup"><span data-stu-id="cefdc-130">x</span></span>        | <span data-ttu-id="cefdc-131">x</span><span class="sxs-lookup"><span data-stu-id="cefdc-131">x</span></span>     | <span data-ttu-id="cefdc-132">x</span><span class="sxs-lookup"><span data-stu-id="cefdc-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cefdc-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cefdc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cefdc-134">Texture1D</span><span class="sxs-lookup"><span data-stu-id="cefdc-134">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="cefdc-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="cefdc-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




