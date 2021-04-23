---
title: 'Консуместруктуредбуффер:: использование функции'
description: Удаляет значение из конца буфера.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Использование функции HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104069247"
---
# <a name="consume-function"></a><span data-ttu-id="ad05c-104">Использование функции</span><span class="sxs-lookup"><span data-stu-id="ad05c-104">Consume function</span></span>

<span data-ttu-id="ad05c-105">Удаляет значение из конца буфера.</span><span class="sxs-lookup"><span data-stu-id="ad05c-105">Removes a value from the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad05c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad05c-106">Syntax</span></span>

``` syntax
T Consume(void);
```

## <a name="parameters"></a><span data-ttu-id="ad05c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad05c-107">Parameters</span></span>

<span data-ttu-id="ad05c-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="ad05c-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad05c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad05c-109">Return value</span></span>

<span data-ttu-id="ad05c-110">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="ad05c-110">Type: **T**</span></span>

<span data-ttu-id="ad05c-111">Значение удалено (может быть структурой).</span><span class="sxs-lookup"><span data-stu-id="ad05c-111">The value removed (can be a structure).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad05c-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad05c-112">Remarks</span></span>

<span data-ttu-id="ad05c-113">T может быть любым типом данных, включая структуру.</span><span class="sxs-lookup"><span data-stu-id="ad05c-113">T can be any data type including a structure.</span></span>

<span data-ttu-id="ad05c-114">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ad05c-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ad05c-115">Вершина</span><span class="sxs-lookup"><span data-stu-id="ad05c-115">Vertex</span></span> | <span data-ttu-id="ad05c-116">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ad05c-116">Hull</span></span> | <span data-ttu-id="ad05c-117">Домен</span><span class="sxs-lookup"><span data-stu-id="ad05c-117">Domain</span></span> | <span data-ttu-id="ad05c-118">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ad05c-118">Geometry</span></span> | <span data-ttu-id="ad05c-119">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ad05c-119">Pixel</span></span> | <span data-ttu-id="ad05c-120">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ad05c-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ad05c-121">x</span><span class="sxs-lookup"><span data-stu-id="ad05c-121">x</span></span>      | <span data-ttu-id="ad05c-122">x</span><span class="sxs-lookup"><span data-stu-id="ad05c-122">x</span></span>    | <span data-ttu-id="ad05c-123">x</span><span class="sxs-lookup"><span data-stu-id="ad05c-123">x</span></span>      | <span data-ttu-id="ad05c-124">x</span><span class="sxs-lookup"><span data-stu-id="ad05c-124">x</span></span>        | <span data-ttu-id="ad05c-125">x</span><span class="sxs-lookup"><span data-stu-id="ad05c-125">x</span></span>     | <span data-ttu-id="ad05c-126">x</span><span class="sxs-lookup"><span data-stu-id="ad05c-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ad05c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad05c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad05c-128">консуместруктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="ad05c-128">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="ad05c-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ad05c-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




