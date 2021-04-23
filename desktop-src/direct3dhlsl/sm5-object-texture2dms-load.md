---
title: 'Функция Texture2DMS:: Load (int, int)'
description: 'Возвращает одно значение. | Функция Texture2DMS:: Load (int, int)'
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Загрузить функцию DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d9c86bea7d914dd5975105a00a64789864a1fbd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986456"
---
# <a name="texture2dmsloadintint-function"></a><span data-ttu-id="be0a2-105">Функция Texture2DMS:: Load (int, int)</span><span class="sxs-lookup"><span data-stu-id="be0a2-105">Texture2DMS::Load(int,int) function</span></span>

<span data-ttu-id="be0a2-106">Возвращает одно значение.</span><span class="sxs-lookup"><span data-stu-id="be0a2-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="be0a2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be0a2-107">Syntax</span></span>

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="be0a2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="be0a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be0a2-109">*курд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be0a2-109">*coord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be0a2-110">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="be0a2-110">Type: **int2**</span></span>

<span data-ttu-id="be0a2-111">Входное расположение.</span><span class="sxs-lookup"><span data-stu-id="be0a2-111">The input location.</span></span>

</dd> <dt>

<span data-ttu-id="be0a2-112">*sampleindex* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be0a2-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be0a2-113">Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="be0a2-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="be0a2-114">Пример индекса.</span><span class="sxs-lookup"><span data-stu-id="be0a2-114">The sample index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be0a2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be0a2-115">Return value</span></span>

<span data-ttu-id="be0a2-116">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="be0a2-116">Type: **T**</span></span>

<span data-ttu-id="be0a2-117">Одно значение, тип которого соответствует типу шаблона текстуры.</span><span class="sxs-lookup"><span data-stu-id="be0a2-117">One value, whose type matches the texture template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="be0a2-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="be0a2-118">Remarks</span></span>

<span data-ttu-id="be0a2-119">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="be0a2-119">This is a list of the overloaded versions of this method.</span></span>


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



<span data-ttu-id="be0a2-120">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="be0a2-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="be0a2-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="be0a2-121">Vertex</span></span> | <span data-ttu-id="be0a2-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="be0a2-122">Hull</span></span> | <span data-ttu-id="be0a2-123">Домен</span><span class="sxs-lookup"><span data-stu-id="be0a2-123">Domain</span></span> | <span data-ttu-id="be0a2-124">Геометрия</span><span class="sxs-lookup"><span data-stu-id="be0a2-124">Geometry</span></span> | <span data-ttu-id="be0a2-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="be0a2-125">Pixel</span></span> | <span data-ttu-id="be0a2-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="be0a2-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="be0a2-127">x</span><span class="sxs-lookup"><span data-stu-id="be0a2-127">x</span></span>     | <span data-ttu-id="be0a2-128">x</span><span class="sxs-lookup"><span data-stu-id="be0a2-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="be0a2-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be0a2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be0a2-130">Методы Load</span><span class="sxs-lookup"><span data-stu-id="be0a2-130">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="be0a2-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="be0a2-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
