---
title: 'Функция Texture2D:: Dimension'
description: 'Возвращает размеры ресурса. | Функция Texture2D:: Dimension'
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998182"
---
# <a name="texture2dgetdimensions-function"></a><span data-ttu-id="3a898-105">Функция Texture2D:: Dimension</span><span class="sxs-lookup"><span data-stu-id="3a898-105">Texture2D::GetDimensions function</span></span>

<span data-ttu-id="3a898-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="3a898-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a898-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a898-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="3a898-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a898-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a898-109">*Миплевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a898-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a898-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3a898-110">Type: **uint**</span></span>

<span data-ttu-id="3a898-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="3a898-111">Optional.</span></span> <span data-ttu-id="3a898-112">Уровень mipmap (должен быть указан, если используется *нумберофлевелс* ).</span><span class="sxs-lookup"><span data-stu-id="3a898-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="3a898-113">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3a898-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a898-114">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3a898-114">Type: **uint**</span></span>

<span data-ttu-id="3a898-115">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="3a898-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="3a898-116">*Высота* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3a898-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a898-117">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3a898-117">Type: **uint**</span></span>

<span data-ttu-id="3a898-118">Высота ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="3a898-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="3a898-119">*Нумберофлевелс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3a898-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a898-120">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3a898-120">Type: **uint**</span></span>

<span data-ttu-id="3a898-121">Число уровней mipmap (требуется также *миплевел* ).</span><span class="sxs-lookup"><span data-stu-id="3a898-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a898-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a898-122">Return value</span></span>

<span data-ttu-id="3a898-123">Nothing</span><span class="sxs-lookup"><span data-stu-id="3a898-123">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="3a898-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="3a898-124">Remarks</span></span>

<span data-ttu-id="3a898-125">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="3a898-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="3a898-126">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="3a898-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3a898-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="3a898-127">Vertex</span></span> | <span data-ttu-id="3a898-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="3a898-128">Hull</span></span> | <span data-ttu-id="3a898-129">Домен</span><span class="sxs-lookup"><span data-stu-id="3a898-129">Domain</span></span> | <span data-ttu-id="3a898-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="3a898-130">Geometry</span></span> | <span data-ttu-id="3a898-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="3a898-131">Pixel</span></span> | <span data-ttu-id="3a898-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="3a898-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3a898-133">x</span><span class="sxs-lookup"><span data-stu-id="3a898-133">x</span></span>     | <span data-ttu-id="3a898-134">x</span><span class="sxs-lookup"><span data-stu-id="3a898-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3a898-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a898-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a898-136">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3a898-136">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="3a898-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="3a898-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




