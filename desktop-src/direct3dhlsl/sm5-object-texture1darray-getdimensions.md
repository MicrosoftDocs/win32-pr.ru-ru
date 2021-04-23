---
title: 'Функция Texture1DArray:: Dimension'
description: 'Возвращает размеры ресурса. | Функция Texture1DArray:: Dimension'
ms.assetid: a15f1808-296d-43ac-80c0-5cbec0bcb801
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
ms.openlocfilehash: 46cc7e93fc01e14ff34091da4549308730d7cd7c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820708"
---
# <a name="texture1darraygetdimensions-function"></a><span data-ttu-id="a626e-105">Функция Texture1DArray:: Dimension</span><span class="sxs-lookup"><span data-stu-id="a626e-105">Texture1DArray::GetDimensions function</span></span>

<span data-ttu-id="a626e-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="a626e-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a626e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a626e-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="a626e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a626e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a626e-109">*Миплевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a626e-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a626e-110">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a626e-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a626e-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="a626e-111">Optional.</span></span> <span data-ttu-id="a626e-112">Уровень mipmap (должен быть указан, если используется *нумберофлевелс* ).</span><span class="sxs-lookup"><span data-stu-id="a626e-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="a626e-113">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a626e-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a626e-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a626e-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a626e-115">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="a626e-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="a626e-116">*Элементы* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a626e-116">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a626e-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a626e-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a626e-118">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="a626e-118">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="a626e-119">*Нумберофлевелс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a626e-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a626e-120">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a626e-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a626e-121">Число уровней mipmap (требуется также *миплевел* ).</span><span class="sxs-lookup"><span data-stu-id="a626e-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a626e-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a626e-122">Return value</span></span>

<span data-ttu-id="a626e-123">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a626e-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a626e-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a626e-124">Remarks</span></span>

<span data-ttu-id="a626e-125">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="a626e-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out UINT Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="a626e-126">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="a626e-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a626e-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="a626e-127">Vertex</span></span> | <span data-ttu-id="a626e-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="a626e-128">Hull</span></span> | <span data-ttu-id="a626e-129">Домен</span><span class="sxs-lookup"><span data-stu-id="a626e-129">Domain</span></span> | <span data-ttu-id="a626e-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="a626e-130">Geometry</span></span> | <span data-ttu-id="a626e-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="a626e-131">Pixel</span></span> | <span data-ttu-id="a626e-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="a626e-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a626e-133">x</span><span class="sxs-lookup"><span data-stu-id="a626e-133">x</span></span>     | <span data-ttu-id="a626e-134">x</span><span class="sxs-lookup"><span data-stu-id="a626e-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a626e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a626e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a626e-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a626e-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="a626e-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="a626e-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
