---
title: 'Функция Texture2DArray:: Dimension'
description: 'Возвращает размеры ресурса. | Функция Texture2DArray:: Dimension'
ms.assetid: 0f6d88b3-195d-4f8c-ac31-ac90129a233e
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
ms.openlocfilehash: b3a78bd12f6924c85d4d395c3cdf73443ae51478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986196"
---
# <a name="texture2darraygetdimensions-function"></a><span data-ttu-id="7863e-105">Функция Texture2DArray:: Dimension</span><span class="sxs-lookup"><span data-stu-id="7863e-105">Texture2DArray::GetDimensions function</span></span>

<span data-ttu-id="7863e-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="7863e-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="7863e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7863e-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="7863e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7863e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7863e-109">*Миплевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7863e-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7863e-110">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7863e-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7863e-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="7863e-111">Optional.</span></span> <span data-ttu-id="7863e-112">Уровень mipmap (должен быть указан, если используется *нумберофлевелс* ).</span><span class="sxs-lookup"><span data-stu-id="7863e-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="7863e-113">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7863e-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7863e-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7863e-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7863e-115">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="7863e-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="7863e-116">*Высота* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7863e-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7863e-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7863e-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7863e-118">Высота ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="7863e-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="7863e-119">*Элементы* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7863e-119">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7863e-120">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7863e-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7863e-121">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="7863e-121">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="7863e-122">*Нумберофлевелс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7863e-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7863e-123">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7863e-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7863e-124">Число уровней mipmap (требуется также *миплевел* ).</span><span class="sxs-lookup"><span data-stu-id="7863e-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7863e-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7863e-125">Return value</span></span>

<span data-ttu-id="7863e-126">Nothing</span><span class="sxs-lookup"><span data-stu-id="7863e-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="7863e-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="7863e-127">Remarks</span></span>

<span data-ttu-id="7863e-128">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="7863e-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out float Height,
  out float Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="7863e-129">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="7863e-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7863e-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="7863e-130">Vertex</span></span> | <span data-ttu-id="7863e-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="7863e-131">Hull</span></span> | <span data-ttu-id="7863e-132">Домен</span><span class="sxs-lookup"><span data-stu-id="7863e-132">Domain</span></span> | <span data-ttu-id="7863e-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="7863e-133">Geometry</span></span> | <span data-ttu-id="7863e-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="7863e-134">Pixel</span></span> | <span data-ttu-id="7863e-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="7863e-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7863e-136">x</span><span class="sxs-lookup"><span data-stu-id="7863e-136">x</span></span>     | <span data-ttu-id="7863e-137">x</span><span class="sxs-lookup"><span data-stu-id="7863e-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7863e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7863e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7863e-139">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="7863e-139">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="7863e-140">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="7863e-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
