---
title: 'Функция Структуредбуффер:: operator'
description: Возвращает переменную ресурса Структуредбуффер, доступную только для чтения.
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
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
ms.openlocfilehash: 1f0d75bdfbcd3bfc560e896416f241f1291120d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134951"
---
# <a name="structuredbufferoperator--function"></a><span data-ttu-id="40ca0-104">Функция Структуредбуффер:: operator</span><span class="sxs-lookup"><span data-stu-id="40ca0-104">StructuredBuffer::Operator  function</span></span>

<span data-ttu-id="40ca0-105">Возвращает переменную ресурса [**структуредбуффер**](sm5-object-structuredbuffer.md), доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="40ca0-105">Returns a read-only resource variable of a [**StructuredBuffer**](sm5-object-structuredbuffer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="40ca0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40ca0-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="40ca0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="40ca0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40ca0-108">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="40ca0-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ca0-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="40ca0-109">Type: **uint**</span></span>

<span data-ttu-id="40ca0-110">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="40ca0-110">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40ca0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40ca0-111">Return value</span></span>

<span data-ttu-id="40ca0-112">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="40ca0-112">Type: **R**</span></span>

<span data-ttu-id="40ca0-113">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="40ca0-113">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="40ca0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="40ca0-114">Remarks</span></span>

<span data-ttu-id="40ca0-115">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="40ca0-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="40ca0-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="40ca0-116">Vertex</span></span> | <span data-ttu-id="40ca0-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="40ca0-117">Hull</span></span> | <span data-ttu-id="40ca0-118">Домен</span><span class="sxs-lookup"><span data-stu-id="40ca0-118">Domain</span></span> | <span data-ttu-id="40ca0-119">Геометрия</span><span class="sxs-lookup"><span data-stu-id="40ca0-119">Geometry</span></span> | <span data-ttu-id="40ca0-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="40ca0-120">Pixel</span></span> | <span data-ttu-id="40ca0-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="40ca0-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="40ca0-122">x</span><span class="sxs-lookup"><span data-stu-id="40ca0-122">x</span></span>      | <span data-ttu-id="40ca0-123">x</span><span class="sxs-lookup"><span data-stu-id="40ca0-123">x</span></span>    | <span data-ttu-id="40ca0-124">x</span><span class="sxs-lookup"><span data-stu-id="40ca0-124">x</span></span>      | <span data-ttu-id="40ca0-125">x</span><span class="sxs-lookup"><span data-stu-id="40ca0-125">x</span></span>        | <span data-ttu-id="40ca0-126">x</span><span class="sxs-lookup"><span data-stu-id="40ca0-126">x</span></span>     | <span data-ttu-id="40ca0-127">x</span><span class="sxs-lookup"><span data-stu-id="40ca0-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="40ca0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40ca0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ca0-129">структуредбуффер</span><span class="sxs-lookup"><span data-stu-id="40ca0-129">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="40ca0-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="40ca0-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




