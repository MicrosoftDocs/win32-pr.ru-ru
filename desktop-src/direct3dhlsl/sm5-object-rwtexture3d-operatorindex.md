---
title: 'Функция RWTexture3D:: operator'
description: Возвращает переменную ресурса RWTexture3D.
ms.assetid: 0b4ea895-ac34-49e5-80e6-74229c33bfe9
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
ms.openlocfilehash: e41ff4db387c4d0926083419082fd589005d96a6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104984128"
---
# <a name="rwtexture3doperator--function"></a><span data-ttu-id="b0130-104">Функция RWTexture3D:: operator</span><span class="sxs-lookup"><span data-stu-id="b0130-104">RWTexture3D::Operator  function</span></span>

<span data-ttu-id="b0130-105">Возвращает переменную ресурса [**RWTexture3D**](sm5-object-rwtexture3d.md).</span><span class="sxs-lookup"><span data-stu-id="b0130-105">Returns a resource variable of a [**RWTexture3D**](sm5-object-rwtexture3d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0130-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0130-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="b0130-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0130-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0130-108">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0130-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0130-109">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="b0130-109">Type: **uint3**</span></span>

<span data-ttu-id="b0130-110">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="b0130-110">The index position.</span></span> <span data-ttu-id="b0130-111">Содержит координаты (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="b0130-111">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0130-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0130-112">Return value</span></span>

<span data-ttu-id="b0130-113">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="b0130-113">Type: **R**</span></span>

<span data-ttu-id="b0130-114">Переменная ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0130-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0130-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0130-115">Remarks</span></span>

<span data-ttu-id="b0130-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="b0130-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b0130-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="b0130-117">Vertex</span></span> | <span data-ttu-id="b0130-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="b0130-118">Hull</span></span> | <span data-ttu-id="b0130-119">Домен</span><span class="sxs-lookup"><span data-stu-id="b0130-119">Domain</span></span> | <span data-ttu-id="b0130-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="b0130-120">Geometry</span></span> | <span data-ttu-id="b0130-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="b0130-121">Pixel</span></span> | <span data-ttu-id="b0130-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="b0130-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b0130-123">x</span><span class="sxs-lookup"><span data-stu-id="b0130-123">x</span></span>     | <span data-ttu-id="b0130-124">x</span><span class="sxs-lookup"><span data-stu-id="b0130-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b0130-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0130-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0130-126">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="b0130-126">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="b0130-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b0130-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




