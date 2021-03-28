---
title: 'Функция Рвструктуредбуффер:: operator'
description: 'Возвращает переменную ресурса. | Функция Рвструктуредбуффер:: operator'
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
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
ms.openlocfilehash: e915d7862f7994d3b438bf3255ee836ede4b3d7d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547535"
---
# <a name="rwstructuredbufferoperator--function"></a><span data-ttu-id="7cf69-105">Функция Рвструктуредбуффер:: operator</span><span class="sxs-lookup"><span data-stu-id="7cf69-105">RWStructuredBuffer::Operator  function</span></span>

<span data-ttu-id="7cf69-106">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="7cf69-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf69-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cf69-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="7cf69-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cf69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cf69-109">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cf69-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf69-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="7cf69-110">Type: **uint**</span></span>

<span data-ttu-id="7cf69-111">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="7cf69-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cf69-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cf69-112">Return value</span></span>

<span data-ttu-id="7cf69-113">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="7cf69-113">Type: **R**</span></span>

<span data-ttu-id="7cf69-114">Переменная ресурса.</span><span class="sxs-lookup"><span data-stu-id="7cf69-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cf69-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="7cf69-115">Remarks</span></span>

<span data-ttu-id="7cf69-116">Структурированный ресурс можно дополнительно индексировать на основе имен компонентов структур.</span><span class="sxs-lookup"><span data-stu-id="7cf69-116">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="7cf69-117">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="7cf69-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7cf69-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="7cf69-118">Vertex</span></span> | <span data-ttu-id="7cf69-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="7cf69-119">Hull</span></span> | <span data-ttu-id="7cf69-120">Домен</span><span class="sxs-lookup"><span data-stu-id="7cf69-120">Domain</span></span> | <span data-ttu-id="7cf69-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="7cf69-121">Geometry</span></span> | <span data-ttu-id="7cf69-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="7cf69-122">Pixel</span></span> | <span data-ttu-id="7cf69-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="7cf69-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7cf69-124">x</span><span class="sxs-lookup"><span data-stu-id="7cf69-124">x</span></span>     | <span data-ttu-id="7cf69-125">x</span><span class="sxs-lookup"><span data-stu-id="7cf69-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7cf69-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cf69-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf69-127">рвструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="7cf69-127">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="7cf69-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="7cf69-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




