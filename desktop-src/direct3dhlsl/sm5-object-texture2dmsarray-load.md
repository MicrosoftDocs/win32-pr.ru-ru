---
title: 'Функция Texture2DMSArray:: Load (int, int)'
description: 'Возвращает одно значение. | Функция Texture2DMSArray:: Load (int, int)'
ms.assetid: 955135cf-1bac-4d0c-9870-2b6d59d9dd88
keywords:
- Загрузить функцию HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83da1a2af6ffc7e990ba1fd4c7f220387304c770
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000257"
---
# <a name="texture2dmsarrayloadintint-function"></a><span data-ttu-id="dc666-105">Функция Texture2DMSArray:: Load (int, int)</span><span class="sxs-lookup"><span data-stu-id="dc666-105">Texture2DMSArray::Load(int,int) function</span></span>

<span data-ttu-id="dc666-106">Возвращает одно значение.</span><span class="sxs-lookup"><span data-stu-id="dc666-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc666-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc666-107">Syntax</span></span>

``` syntax
T Load(
  in int3 coord,
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="dc666-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc666-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc666-109">*курд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc666-109">*coord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc666-110">Тип: " **корпус** "</span><span class="sxs-lookup"><span data-stu-id="dc666-110">Type: **int3**</span></span>

<span data-ttu-id="dc666-111">Входное расположение.</span><span class="sxs-lookup"><span data-stu-id="dc666-111">The input location.</span></span>

</dd> <dt>

<span data-ttu-id="dc666-112">*sampleindex* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc666-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc666-113">Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc666-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dc666-114">Пример индекса.</span><span class="sxs-lookup"><span data-stu-id="dc666-114">The sample index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc666-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc666-115">Return value</span></span>

<span data-ttu-id="dc666-116">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="dc666-116">Type: **T**</span></span>

<span data-ttu-id="dc666-117">Одно значение, тип которого соответствует типу шаблона текстуры.</span><span class="sxs-lookup"><span data-stu-id="dc666-117">One value, whose type matches the texture template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc666-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="dc666-118">Remarks</span></span>

<span data-ttu-id="dc666-119">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="dc666-119">This is a list of the overloaded versions of this method.</span></span>


```
void Load(in int3 coord,
  in int sampleindex,
  in int2 offset);
```



<span data-ttu-id="dc666-120">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="dc666-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="dc666-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="dc666-121">Vertex</span></span> | <span data-ttu-id="dc666-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="dc666-122">Hull</span></span> | <span data-ttu-id="dc666-123">Домен</span><span class="sxs-lookup"><span data-stu-id="dc666-123">Domain</span></span> | <span data-ttu-id="dc666-124">Геометрия</span><span class="sxs-lookup"><span data-stu-id="dc666-124">Geometry</span></span> | <span data-ttu-id="dc666-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="dc666-125">Pixel</span></span> | <span data-ttu-id="dc666-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="dc666-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="dc666-127">x</span><span class="sxs-lookup"><span data-stu-id="dc666-127">x</span></span>     | <span data-ttu-id="dc666-128">x</span><span class="sxs-lookup"><span data-stu-id="dc666-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dc666-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc666-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc666-130">Методы Load</span><span class="sxs-lookup"><span data-stu-id="dc666-130">Load methods</span></span>](texture2dmsarray-load.md)
</dt> <dt>

[<span data-ttu-id="dc666-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="dc666-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
