---
title: 'Функция Texture2DArray:: operator'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Функция Texture2DArray:: operator'
ms.assetid: eb6ff496-c46f-405f-a172-ab747415a2f9
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
ms.openlocfilehash: 1b86aad839fbf28a4fc666b3a5fe5c5788b7b3ae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081756"
---
# <a name="texture2darrayoperator--function"></a><span data-ttu-id="ca52c-105">Функция Texture2DArray:: operator</span><span class="sxs-lookup"><span data-stu-id="ca52c-105">Texture2DArray::Operator  function</span></span>

<span data-ttu-id="ca52c-106">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ca52c-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca52c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca52c-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="ca52c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca52c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca52c-109">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca52c-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca52c-110">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="ca52c-110">Type: **uint3**</span></span>

<span data-ttu-id="ca52c-111">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="ca52c-111">The index position.</span></span> <span data-ttu-id="ca52c-112">Первый и второй компоненты содержат координаты (x, y).</span><span class="sxs-lookup"><span data-stu-id="ca52c-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="ca52c-113">Третий компонент указывает нужный срез массива.</span><span class="sxs-lookup"><span data-stu-id="ca52c-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca52c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca52c-114">Return value</span></span>

<span data-ttu-id="ca52c-115">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="ca52c-115">Type: **R**</span></span>

<span data-ttu-id="ca52c-116">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ca52c-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca52c-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca52c-117">Remarks</span></span>

<span data-ttu-id="ca52c-118">Этот метод всегда обращается к первому MIP уровню.</span><span class="sxs-lookup"><span data-stu-id="ca52c-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="ca52c-119">Чтобы указать другие уровни MIP, используйте вместо него метод [**MIP \[ \] \[ \] . operator**](sm5-object-texture2darray-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="ca52c-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="ca52c-120">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="ca52c-120">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ca52c-121">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ca52c-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ca52c-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="ca52c-122">Vertex</span></span> | <span data-ttu-id="ca52c-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ca52c-123">Hull</span></span> | <span data-ttu-id="ca52c-124">Домен</span><span class="sxs-lookup"><span data-stu-id="ca52c-124">Domain</span></span> | <span data-ttu-id="ca52c-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ca52c-125">Geometry</span></span> | <span data-ttu-id="ca52c-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ca52c-126">Pixel</span></span> | <span data-ttu-id="ca52c-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ca52c-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ca52c-128">x</span><span class="sxs-lookup"><span data-stu-id="ca52c-128">x</span></span>      | <span data-ttu-id="ca52c-129">x</span><span class="sxs-lookup"><span data-stu-id="ca52c-129">x</span></span>    | <span data-ttu-id="ca52c-130">x</span><span class="sxs-lookup"><span data-stu-id="ca52c-130">x</span></span>      | <span data-ttu-id="ca52c-131">x</span><span class="sxs-lookup"><span data-stu-id="ca52c-131">x</span></span>        | <span data-ttu-id="ca52c-132">x</span><span class="sxs-lookup"><span data-stu-id="ca52c-132">x</span></span>     | <span data-ttu-id="ca52c-133">x</span><span class="sxs-lookup"><span data-stu-id="ca52c-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ca52c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca52c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca52c-135">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ca52c-135">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="ca52c-136">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ca52c-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




