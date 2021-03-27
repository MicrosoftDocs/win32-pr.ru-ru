---
title: 'Функция Рвструктуредбуффер:: Инкременткаунтер (Хттпсерв. h)'
description: Увеличивает значение скрытого счетчика объекта.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- Функция Инкременткаунтер HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355493"
---
# <a name="incrementcounter-function"></a><span data-ttu-id="c73d2-104">Функция Инкременткаунтер</span><span class="sxs-lookup"><span data-stu-id="c73d2-104">IncrementCounter function</span></span>

<span data-ttu-id="c73d2-105">Увеличивает значение скрытого счетчика объекта.</span><span class="sxs-lookup"><span data-stu-id="c73d2-105">Increments the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c73d2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c73d2-106">Syntax</span></span>

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="c73d2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c73d2-107">Parameters</span></span>

<span data-ttu-id="c73d2-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="c73d2-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c73d2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c73d2-109">Return value</span></span>

<span data-ttu-id="c73d2-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="c73d2-110">Type: **uint**</span></span>

<span data-ttu-id="c73d2-111">Предварительно увеличенное значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="c73d2-111">The pre-incremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c73d2-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="c73d2-112">Remarks</span></span>

<span data-ttu-id="c73d2-113">Чтобы этот метод работал, в связанном представлении неупорядоченного доступа должен быть задан [**\_ \_ \_ \_ Счетчик флагов UAV buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) .</span><span class="sxs-lookup"><span data-stu-id="c73d2-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creation for this method to work.</span></span>

<span data-ttu-id="c73d2-114">Структурированный ресурс можно дополнительно индексировать на основе имен компонентов структур.</span><span class="sxs-lookup"><span data-stu-id="c73d2-114">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="c73d2-115">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="c73d2-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c73d2-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="c73d2-116">Vertex</span></span> | <span data-ttu-id="c73d2-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="c73d2-117">Hull</span></span> | <span data-ttu-id="c73d2-118">Домен</span><span class="sxs-lookup"><span data-stu-id="c73d2-118">Domain</span></span> | <span data-ttu-id="c73d2-119">Геометрия</span><span class="sxs-lookup"><span data-stu-id="c73d2-119">Geometry</span></span> | <span data-ttu-id="c73d2-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="c73d2-120">Pixel</span></span> | <span data-ttu-id="c73d2-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="c73d2-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c73d2-122">x</span><span class="sxs-lookup"><span data-stu-id="c73d2-122">x</span></span>     | <span data-ttu-id="c73d2-123">x</span><span class="sxs-lookup"><span data-stu-id="c73d2-123">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="c73d2-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c73d2-124">Requirements</span></span>



| <span data-ttu-id="c73d2-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c73d2-125">Requirement</span></span> | <span data-ttu-id="c73d2-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c73d2-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c73d2-127">Header</span><span class="sxs-lookup"><span data-stu-id="c73d2-127">Header</span></span><br/> | <dl> <span data-ttu-id="c73d2-128"><dt>Хттпсерв. h</dt></span><span class="sxs-lookup"><span data-stu-id="c73d2-128"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c73d2-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c73d2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c73d2-130">рвструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="c73d2-130">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="c73d2-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c73d2-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

