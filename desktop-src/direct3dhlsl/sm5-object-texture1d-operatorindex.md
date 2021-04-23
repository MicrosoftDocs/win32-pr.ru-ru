---
title: 'Функция Texture1D:: operator'
description: Возвращает переменную ресурса, доступную только для чтения, для Texture1D.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: 44e5b502c7ae8b766363956920d7922858b4d771
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134950"
---
# <a name="texture1doperator--function"></a><span data-ttu-id="57b21-104">Функция Texture1D:: operator</span><span class="sxs-lookup"><span data-stu-id="57b21-104">Texture1D::Operator  function</span></span>

<span data-ttu-id="57b21-105">Возвращает переменную ресурса, доступную только для чтения, для [**Texture1D**](sm5-object-texture1d.md).</span><span class="sxs-lookup"><span data-stu-id="57b21-105">Returns a read-only resource variable for a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="57b21-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57b21-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="57b21-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="57b21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b21-108">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57b21-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57b21-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="57b21-109">Type: **uint**</span></span>

<span data-ttu-id="57b21-110">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="57b21-110">The index position.</span></span> <span data-ttu-id="57b21-111">Содержит координату x.</span><span class="sxs-lookup"><span data-stu-id="57b21-111">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b21-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57b21-112">Return value</span></span>

<span data-ttu-id="57b21-113">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="57b21-113">Type: **R**</span></span>

<span data-ttu-id="57b21-114">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="57b21-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="57b21-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="57b21-115">Remarks</span></span>

<span data-ttu-id="57b21-116">Этот метод всегда обращается к первому MIP уровню.</span><span class="sxs-lookup"><span data-stu-id="57b21-116">This method always accesses the first mip level.</span></span> <span data-ttu-id="57b21-117">Чтобы указать другие уровни MIP, используйте вместо него [**\[ \] \[ \] оператор MIP.**](sm5-object-texture1d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="57b21-117">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="57b21-118">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="57b21-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="57b21-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="57b21-119">Vertex</span></span> | <span data-ttu-id="57b21-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="57b21-120">Hull</span></span> | <span data-ttu-id="57b21-121">Домен</span><span class="sxs-lookup"><span data-stu-id="57b21-121">Domain</span></span> | <span data-ttu-id="57b21-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="57b21-122">Geometry</span></span> | <span data-ttu-id="57b21-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="57b21-123">Pixel</span></span> | <span data-ttu-id="57b21-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="57b21-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="57b21-125">x</span><span class="sxs-lookup"><span data-stu-id="57b21-125">x</span></span>      | <span data-ttu-id="57b21-126">x</span><span class="sxs-lookup"><span data-stu-id="57b21-126">x</span></span>    | <span data-ttu-id="57b21-127">x</span><span class="sxs-lookup"><span data-stu-id="57b21-127">x</span></span>      | <span data-ttu-id="57b21-128">x</span><span class="sxs-lookup"><span data-stu-id="57b21-128">x</span></span>        | <span data-ttu-id="57b21-129">x</span><span class="sxs-lookup"><span data-stu-id="57b21-129">x</span></span>     | <span data-ttu-id="57b21-130">x</span><span class="sxs-lookup"><span data-stu-id="57b21-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="57b21-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57b21-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b21-132">Texture1D</span><span class="sxs-lookup"><span data-stu-id="57b21-132">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="57b21-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="57b21-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




