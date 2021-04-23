---
title: 'Функция RWTexture2DArray:: Dimension'
description: 'Возвращает размеры ресурса. | Функция RWTexture2DArray:: Dimension'
ms.assetid: 473b3f41-854d-4881-a80b-2d2dd7e5d479
keywords:
- Функция Dimension HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6d95148cb6dc51c739ee4546bd64ce22666d5fd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273382"
---
# <a name="rwtexture2darraygetdimensions-function"></a><span data-ttu-id="d15ba-105">Функция RWTexture2DArray:: Dimension</span><span class="sxs-lookup"><span data-stu-id="d15ba-105">RWTexture2DArray::GetDimensions function</span></span>

<span data-ttu-id="d15ba-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="d15ba-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="d15ba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d15ba-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="d15ba-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d15ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d15ba-109">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d15ba-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d15ba-110">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d15ba-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d15ba-111">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="d15ba-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="d15ba-112">*Высота* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d15ba-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d15ba-113">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d15ba-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d15ba-114">Высота ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="d15ba-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="d15ba-115">*Элементы* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d15ba-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d15ba-116">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d15ba-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d15ba-117">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="d15ba-117">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d15ba-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d15ba-118">Return value</span></span>

<span data-ttu-id="d15ba-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d15ba-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d15ba-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="d15ba-120">Remarks</span></span>

<span data-ttu-id="d15ba-121">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="d15ba-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Elements);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="d15ba-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="d15ba-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d15ba-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="d15ba-123">Vertex</span></span> | <span data-ttu-id="d15ba-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="d15ba-124">Hull</span></span> | <span data-ttu-id="d15ba-125">Домен</span><span class="sxs-lookup"><span data-stu-id="d15ba-125">Domain</span></span> | <span data-ttu-id="d15ba-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="d15ba-126">Geometry</span></span> | <span data-ttu-id="d15ba-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="d15ba-127">Pixel</span></span> | <span data-ttu-id="d15ba-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="d15ba-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d15ba-129">x</span><span class="sxs-lookup"><span data-stu-id="d15ba-129">x</span></span>     | <span data-ttu-id="d15ba-130">x</span><span class="sxs-lookup"><span data-stu-id="d15ba-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d15ba-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d15ba-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d15ba-132">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="d15ba-132">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="d15ba-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d15ba-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
