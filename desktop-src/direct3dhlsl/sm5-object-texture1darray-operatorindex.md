---
title: 'Функция Texture1DArray:: operator'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Функция Texture1DArray:: operator'
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
keywords:
- Оператор Function HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 578d778cd1e0e064c435c19fb094feb66f651e05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986476"
---
# <a name="texture1darrayoperator--function"></a><span data-ttu-id="d41a8-105">Функция Texture1DArray:: operator</span><span class="sxs-lookup"><span data-stu-id="d41a8-105">Texture1DArray::Operator  function</span></span>

<span data-ttu-id="d41a8-106">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d41a8-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d41a8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d41a8-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="d41a8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d41a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d41a8-109">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d41a8-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d41a8-110">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="d41a8-110">Type: **uint2**</span></span>

<span data-ttu-id="d41a8-111">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="d41a8-111">The index position.</span></span> <span data-ttu-id="d41a8-112">Первый компонент содержит координату x.</span><span class="sxs-lookup"><span data-stu-id="d41a8-112">The first component contains the x-coordinate.</span></span> <span data-ttu-id="d41a8-113">Второй компонент указывает нужный срез массива.</span><span class="sxs-lookup"><span data-stu-id="d41a8-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d41a8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d41a8-114">Return value</span></span>

<span data-ttu-id="d41a8-115">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="d41a8-115">Type: **R**</span></span>

<span data-ttu-id="d41a8-116">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d41a8-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="d41a8-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="d41a8-117">Remarks</span></span>

<span data-ttu-id="d41a8-118">Этот метод всегда обращается к первому MIP уровню.</span><span class="sxs-lookup"><span data-stu-id="d41a8-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="d41a8-119">Чтобы указать другие уровни MIP, используйте вместо него метод [**MIP \[ \] \[ \] . operator**](sm5-object-texture1darray-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="d41a8-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="d41a8-120">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="d41a8-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d41a8-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="d41a8-121">Vertex</span></span> | <span data-ttu-id="d41a8-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="d41a8-122">Hull</span></span> | <span data-ttu-id="d41a8-123">Домен</span><span class="sxs-lookup"><span data-stu-id="d41a8-123">Domain</span></span> | <span data-ttu-id="d41a8-124">Геометрия</span><span class="sxs-lookup"><span data-stu-id="d41a8-124">Geometry</span></span> | <span data-ttu-id="d41a8-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="d41a8-125">Pixel</span></span> | <span data-ttu-id="d41a8-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="d41a8-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d41a8-127">x</span><span class="sxs-lookup"><span data-stu-id="d41a8-127">x</span></span>      | <span data-ttu-id="d41a8-128">x</span><span class="sxs-lookup"><span data-stu-id="d41a8-128">x</span></span>    | <span data-ttu-id="d41a8-129">x</span><span class="sxs-lookup"><span data-stu-id="d41a8-129">x</span></span>      | <span data-ttu-id="d41a8-130">x</span><span class="sxs-lookup"><span data-stu-id="d41a8-130">x</span></span>        | <span data-ttu-id="d41a8-131">x</span><span class="sxs-lookup"><span data-stu-id="d41a8-131">x</span></span>     | <span data-ttu-id="d41a8-132">x</span><span class="sxs-lookup"><span data-stu-id="d41a8-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d41a8-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d41a8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d41a8-134">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d41a8-134">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="d41a8-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d41a8-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




