---
title: 'Buffer:: оператор, функция'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Buffer:: оператор, функция'
ms.assetid: 6a9e1176-439b-4565-9c7e-957d7c4045f0
keywords:
- Оператор прямой записи функции оператора
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b811dd2409a00bb07f0b2441f6d57d4bd122f50
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424174"
---
# <a name="bufferoperator--function"></a><span data-ttu-id="56a32-105">Buffer:: оператор, функция</span><span class="sxs-lookup"><span data-stu-id="56a32-105">Buffer::Operator  function</span></span>

<span data-ttu-id="56a32-106">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="56a32-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a32-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56a32-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="56a32-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="56a32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56a32-109">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="56a32-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56a32-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="56a32-110">Type: **uint**</span></span>

<span data-ttu-id="56a32-111">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="56a32-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56a32-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56a32-112">Return value</span></span>

<span data-ttu-id="56a32-113">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="56a32-113">Type: **R**</span></span>

<span data-ttu-id="56a32-114">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="56a32-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="56a32-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="56a32-115">Remarks</span></span>

<span data-ttu-id="56a32-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="56a32-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="56a32-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="56a32-117">Vertex</span></span> | <span data-ttu-id="56a32-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="56a32-118">Hull</span></span> | <span data-ttu-id="56a32-119">Домен</span><span class="sxs-lookup"><span data-stu-id="56a32-119">Domain</span></span> | <span data-ttu-id="56a32-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="56a32-120">Geometry</span></span> | <span data-ttu-id="56a32-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="56a32-121">Pixel</span></span> | <span data-ttu-id="56a32-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="56a32-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="56a32-123">x</span><span class="sxs-lookup"><span data-stu-id="56a32-123">x</span></span>     | <span data-ttu-id="56a32-124">x</span><span class="sxs-lookup"><span data-stu-id="56a32-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="56a32-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56a32-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a32-126">Буфер</span><span class="sxs-lookup"><span data-stu-id="56a32-126">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="56a32-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="56a32-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




