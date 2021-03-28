---
title: 'Функция Рвбуффер:: operator'
description: 'Возвращает переменную ресурса. | Функция Рвбуффер:: operator'
ms.assetid: 59e5e4ec-ff0d-43aa-805a-04b79f5ab57f
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
ms.openlocfilehash: 40336c8ad6ee9e8008b82c172f1a5b863e967c0d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998022"
---
# <a name="rwbufferoperator--function"></a><span data-ttu-id="07875-105">Функция Рвбуффер:: operator</span><span class="sxs-lookup"><span data-stu-id="07875-105">RWBuffer::Operator  function</span></span>

<span data-ttu-id="07875-106">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="07875-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="07875-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07875-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="07875-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="07875-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07875-109">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07875-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07875-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="07875-110">Type: **uint**</span></span>

<span data-ttu-id="07875-111">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="07875-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07875-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07875-112">Return value</span></span>

<span data-ttu-id="07875-113">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="07875-113">Type: **R**</span></span>

<span data-ttu-id="07875-114">Переменная ресурса.</span><span class="sxs-lookup"><span data-stu-id="07875-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="07875-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="07875-115">Remarks</span></span>

<span data-ttu-id="07875-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="07875-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="07875-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="07875-117">Vertex</span></span> | <span data-ttu-id="07875-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="07875-118">Hull</span></span> | <span data-ttu-id="07875-119">Домен</span><span class="sxs-lookup"><span data-stu-id="07875-119">Domain</span></span> | <span data-ttu-id="07875-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="07875-120">Geometry</span></span> | <span data-ttu-id="07875-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="07875-121">Pixel</span></span> | <span data-ttu-id="07875-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="07875-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="07875-123">x</span><span class="sxs-lookup"><span data-stu-id="07875-123">x</span></span>      | <span data-ttu-id="07875-124">x</span><span class="sxs-lookup"><span data-stu-id="07875-124">x</span></span>    | <span data-ttu-id="07875-125">x</span><span class="sxs-lookup"><span data-stu-id="07875-125">x</span></span>      | <span data-ttu-id="07875-126">x</span><span class="sxs-lookup"><span data-stu-id="07875-126">x</span></span>        | <span data-ttu-id="07875-127">x</span><span class="sxs-lookup"><span data-stu-id="07875-127">x</span></span>     | <span data-ttu-id="07875-128">x</span><span class="sxs-lookup"><span data-stu-id="07875-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="07875-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07875-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07875-130">рвбуффер</span><span class="sxs-lookup"><span data-stu-id="07875-130">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="07875-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="07875-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




