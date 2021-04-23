---
title: 'Функция Texture2DMS:: operator'
description: Извлекает значение из ресурса в расположении, указанном в примере индекса 0.
ms.assetid: 80380D3F-1E71-4C43-A17B-F94F6E5215B1
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
ms.openlocfilehash: 6ae7976e6871dc2547ed5c372e1551e5bf0ca148
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104984140"
---
# <a name="texture2dmsoperator--function"></a><span data-ttu-id="ee648-104">Функция Texture2DMS:: operator</span><span class="sxs-lookup"><span data-stu-id="ee648-104">Texture2DMS::Operator  function</span></span>

<span data-ttu-id="ee648-105">Извлекает значение из ресурса в расположении, указанном в примере индекса 0.</span><span class="sxs-lookup"><span data-stu-id="ee648-105">Retrieves a value from the resource at the location provided at sample index 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee648-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee648-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="ee648-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee648-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee648-108">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee648-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee648-109">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="ee648-109">Type: **uint2**</span></span>

<span data-ttu-id="ee648-110">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="ee648-110">The index position.</span></span> <span data-ttu-id="ee648-111">Содержит координаты (x, y).</span><span class="sxs-lookup"><span data-stu-id="ee648-111">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee648-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee648-112">Return value</span></span>

<span data-ttu-id="ee648-113">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="ee648-113">Type: **R**</span></span>

<span data-ttu-id="ee648-114">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ee648-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee648-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee648-115">Remarks</span></span>

<span data-ttu-id="ee648-116">Чтобы выбрать конкретный пример, см [**. пример. \[Оператор \] . \[ \]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="ee648-116">To select a particular sample, refer to [**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md).</span></span>

<span data-ttu-id="ee648-117">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ee648-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ee648-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="ee648-118">Vertex</span></span> | <span data-ttu-id="ee648-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ee648-119">Hull</span></span> | <span data-ttu-id="ee648-120">Домен</span><span class="sxs-lookup"><span data-stu-id="ee648-120">Domain</span></span> | <span data-ttu-id="ee648-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ee648-121">Geometry</span></span> | <span data-ttu-id="ee648-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ee648-122">Pixel</span></span> | <span data-ttu-id="ee648-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ee648-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ee648-124">x</span><span class="sxs-lookup"><span data-stu-id="ee648-124">x</span></span>      | <span data-ttu-id="ee648-125">x</span><span class="sxs-lookup"><span data-stu-id="ee648-125">x</span></span>    | <span data-ttu-id="ee648-126">x</span><span class="sxs-lookup"><span data-stu-id="ee648-126">x</span></span>      | <span data-ttu-id="ee648-127">x</span><span class="sxs-lookup"><span data-stu-id="ee648-127">x</span></span>        | <span data-ttu-id="ee648-128">x</span><span class="sxs-lookup"><span data-stu-id="ee648-128">x</span></span>     | <span data-ttu-id="ee648-129">x</span><span class="sxs-lookup"><span data-stu-id="ee648-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ee648-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee648-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee648-131">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="ee648-131">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="ee648-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ee648-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




