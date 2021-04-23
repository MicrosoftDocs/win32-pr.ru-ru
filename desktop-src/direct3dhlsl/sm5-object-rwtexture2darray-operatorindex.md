---
title: 'Функция RWTexture2DArray:: operator'
description: 'Возвращает переменную ресурса. | Функция RWTexture2DArray:: operator'
ms.assetid: ae3d0697-ea0a-450d-bdfe-7bc5d8faf11a
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
ms.openlocfilehash: faf49c48fbf5042ce2765005cd8daea4d1227255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081757"
---
# <a name="rwtexture2darrayoperator--function"></a><span data-ttu-id="ae400-105">Функция RWTexture2DArray:: operator</span><span class="sxs-lookup"><span data-stu-id="ae400-105">RWTexture2DArray::Operator  function</span></span>

<span data-ttu-id="ae400-106">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae400-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae400-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae400-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="ae400-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae400-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae400-109">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ae400-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae400-110">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="ae400-110">Type: **uint3**</span></span>

<span data-ttu-id="ae400-111">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="ae400-111">The index position.</span></span> <span data-ttu-id="ae400-112">Первый и второй компоненты содержат координаты (x, y).</span><span class="sxs-lookup"><span data-stu-id="ae400-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="ae400-113">Третий компонент указывает нужный срез массива.</span><span class="sxs-lookup"><span data-stu-id="ae400-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae400-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae400-114">Return value</span></span>

<span data-ttu-id="ae400-115">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="ae400-115">Type: **R**</span></span>

<span data-ttu-id="ae400-116">Переменная ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae400-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae400-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae400-117">Remarks</span></span>

<span data-ttu-id="ae400-118">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ae400-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ae400-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="ae400-119">Vertex</span></span> | <span data-ttu-id="ae400-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ae400-120">Hull</span></span> | <span data-ttu-id="ae400-121">Домен</span><span class="sxs-lookup"><span data-stu-id="ae400-121">Domain</span></span> | <span data-ttu-id="ae400-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ae400-122">Geometry</span></span> | <span data-ttu-id="ae400-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ae400-123">Pixel</span></span> | <span data-ttu-id="ae400-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ae400-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ae400-125">x</span><span class="sxs-lookup"><span data-stu-id="ae400-125">x</span></span>     | <span data-ttu-id="ae400-126">x</span><span class="sxs-lookup"><span data-stu-id="ae400-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ae400-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae400-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae400-128">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="ae400-128">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="ae400-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ae400-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




