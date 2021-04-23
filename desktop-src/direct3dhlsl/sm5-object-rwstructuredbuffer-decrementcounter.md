---
title: 'Рвструктуредбуффер: функция Екременткаунтер:D (Хттпсерв. h)'
description: Уменьшает значение скрытого счетчика объекта.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- Функция Декременткаунтер HLSL
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987062"
---
# <a name="decrementcounter-function"></a><span data-ttu-id="06a22-104">Функция Декременткаунтер</span><span class="sxs-lookup"><span data-stu-id="06a22-104">DecrementCounter function</span></span>

<span data-ttu-id="06a22-105">Уменьшает значение скрытого счетчика объекта.</span><span class="sxs-lookup"><span data-stu-id="06a22-105">Decrements the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a22-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06a22-106">Syntax</span></span>

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="06a22-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="06a22-107">Parameters</span></span>

<span data-ttu-id="06a22-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="06a22-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06a22-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06a22-109">Return value</span></span>

<span data-ttu-id="06a22-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="06a22-110">Type: **uint**</span></span>

<span data-ttu-id="06a22-111">Значение счетчика после уменьшения.</span><span class="sxs-lookup"><span data-stu-id="06a22-111">The post-decremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a22-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="06a22-112">Remarks</span></span>

<span data-ttu-id="06a22-113">Для связанного представления неупорядоченного доступа должен быть [**установлен \_ \_ \_ \_ Счетчик флагов UAV buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) во время работы креатионфор этого метода.</span><span class="sxs-lookup"><span data-stu-id="06a22-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creationfor this method to work.</span></span>

<span data-ttu-id="06a22-114">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="06a22-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="06a22-115">Вершина</span><span class="sxs-lookup"><span data-stu-id="06a22-115">Vertex</span></span> | <span data-ttu-id="06a22-116">Поверхности</span><span class="sxs-lookup"><span data-stu-id="06a22-116">Hull</span></span> | <span data-ttu-id="06a22-117">Домен</span><span class="sxs-lookup"><span data-stu-id="06a22-117">Domain</span></span> | <span data-ttu-id="06a22-118">Геометрия</span><span class="sxs-lookup"><span data-stu-id="06a22-118">Geometry</span></span> | <span data-ttu-id="06a22-119">Пиксель</span><span class="sxs-lookup"><span data-stu-id="06a22-119">Pixel</span></span> | <span data-ttu-id="06a22-120">Вычисления</span><span class="sxs-lookup"><span data-stu-id="06a22-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="06a22-121">x</span><span class="sxs-lookup"><span data-stu-id="06a22-121">x</span></span>     | <span data-ttu-id="06a22-122">x</span><span class="sxs-lookup"><span data-stu-id="06a22-122">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="06a22-123">Требования</span><span class="sxs-lookup"><span data-stu-id="06a22-123">Requirements</span></span>



| <span data-ttu-id="06a22-124">Требование</span><span class="sxs-lookup"><span data-stu-id="06a22-124">Requirement</span></span> | <span data-ttu-id="06a22-125">Значение</span><span class="sxs-lookup"><span data-stu-id="06a22-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06a22-126">Header</span><span class="sxs-lookup"><span data-stu-id="06a22-126">Header</span></span><br/> | <dl> <span data-ttu-id="06a22-127"><dt>Хттпсерв. h</dt></span><span class="sxs-lookup"><span data-stu-id="06a22-127"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06a22-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06a22-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a22-129">рвструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="06a22-129">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="06a22-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="06a22-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

