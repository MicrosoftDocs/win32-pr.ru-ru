---
title: 'Функция Texture2DMSArray:: Dimension'
description: 'Возвращает размеры ресурса. | Функция Texture2DMSArray:: Dimension'
ms.assetid: 86d54e0d-f168-479f-b2af-f021b8994741
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
ms.openlocfilehash: e22a225178c2fa965ea842b8c86692d09b87168f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353722"
---
# <a name="texture2dmsarraygetdimensions-function"></a><span data-ttu-id="c3be4-105">Функция Texture2DMSArray:: Dimension</span><span class="sxs-lookup"><span data-stu-id="c3be4-105">Texture2DMSArray::GetDimensions function</span></span>

<span data-ttu-id="c3be4-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="c3be4-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3be4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3be4-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="c3be4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3be4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3be4-109">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c3be4-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3be4-110">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3be4-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3be4-111">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="c3be4-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="c3be4-112">*Высота* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c3be4-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3be4-113">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3be4-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3be4-114">Высота ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="c3be4-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="c3be4-115">*Элементы* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c3be4-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3be4-116">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3be4-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3be4-117">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="c3be4-117">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="c3be4-118">*Нумберофсамплес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c3be4-118">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3be4-119">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3be4-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3be4-120">Число расположений выборки.</span><span class="sxs-lookup"><span data-stu-id="c3be4-120">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3be4-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3be4-121">Return value</span></span>

<span data-ttu-id="c3be4-122">Nothing</span><span class="sxs-lookup"><span data-stu-id="c3be4-122">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="c3be4-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3be4-123">Remarks</span></span>

<span data-ttu-id="c3be4-124">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="c3be4-124">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float Elements,
  out float NumberOfSamples);
```



<span data-ttu-id="c3be4-125">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="c3be4-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c3be4-126">Вершина</span><span class="sxs-lookup"><span data-stu-id="c3be4-126">Vertex</span></span> | <span data-ttu-id="c3be4-127">Поверхности</span><span class="sxs-lookup"><span data-stu-id="c3be4-127">Hull</span></span> | <span data-ttu-id="c3be4-128">Домен</span><span class="sxs-lookup"><span data-stu-id="c3be4-128">Domain</span></span> | <span data-ttu-id="c3be4-129">Геометрия</span><span class="sxs-lookup"><span data-stu-id="c3be4-129">Geometry</span></span> | <span data-ttu-id="c3be4-130">Пиксель</span><span class="sxs-lookup"><span data-stu-id="c3be4-130">Pixel</span></span> | <span data-ttu-id="c3be4-131">Вычисления</span><span class="sxs-lookup"><span data-stu-id="c3be4-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c3be4-132">x</span><span class="sxs-lookup"><span data-stu-id="c3be4-132">x</span></span>     | <span data-ttu-id="c3be4-133">x</span><span class="sxs-lookup"><span data-stu-id="c3be4-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c3be4-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3be4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3be4-135">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c3be4-135">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="c3be4-136">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c3be4-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
