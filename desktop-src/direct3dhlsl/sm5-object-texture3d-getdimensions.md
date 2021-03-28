---
title: 'Функция Texture3D:: Dimension'
description: 'Возвращает размеры ресурса. | Функция Texture3D:: Dimension'
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
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
ms.openlocfilehash: 7a700e0ff065e5f4758241ee0c8252965209a21f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998267"
---
# <a name="texture3dgetdimensions-function"></a><span data-ttu-id="22dd2-105">Функция Texture3D:: Dimension</span><span class="sxs-lookup"><span data-stu-id="22dd2-105">Texture3D::GetDimensions function</span></span>

<span data-ttu-id="22dd2-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="22dd2-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="22dd2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22dd2-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="22dd2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="22dd2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22dd2-109">*Миплевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22dd2-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22dd2-110">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="22dd2-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="22dd2-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="22dd2-111">Optional.</span></span> <span data-ttu-id="22dd2-112">Уровень mipmap (должен быть указан, если используется *нумберофлевелс* ).</span><span class="sxs-lookup"><span data-stu-id="22dd2-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="22dd2-113">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="22dd2-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22dd2-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="22dd2-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="22dd2-115">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="22dd2-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="22dd2-116">*Высота* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="22dd2-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22dd2-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="22dd2-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="22dd2-118">Высота ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="22dd2-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="22dd2-119">*Глубина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="22dd2-119">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22dd2-120">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="22dd2-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="22dd2-121">Глубина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="22dd2-121">The resource depth, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="22dd2-122">*Нумберофлевелс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="22dd2-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22dd2-123">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="22dd2-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="22dd2-124">Число уровней mipmap (требуется также *миплевел* ).</span><span class="sxs-lookup"><span data-stu-id="22dd2-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22dd2-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22dd2-125">Return value</span></span>

<span data-ttu-id="22dd2-126">Nothing</span><span class="sxs-lookup"><span data-stu-id="22dd2-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="22dd2-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="22dd2-127">Remarks</span></span>

<span data-ttu-id="22dd2-128">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="22dd2-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="22dd2-129">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="22dd2-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="22dd2-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="22dd2-130">Vertex</span></span> | <span data-ttu-id="22dd2-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="22dd2-131">Hull</span></span> | <span data-ttu-id="22dd2-132">Домен</span><span class="sxs-lookup"><span data-stu-id="22dd2-132">Domain</span></span> | <span data-ttu-id="22dd2-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="22dd2-133">Geometry</span></span> | <span data-ttu-id="22dd2-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="22dd2-134">Pixel</span></span> | <span data-ttu-id="22dd2-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="22dd2-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="22dd2-136">x</span><span class="sxs-lookup"><span data-stu-id="22dd2-136">x</span></span>     | <span data-ttu-id="22dd2-137">x</span><span class="sxs-lookup"><span data-stu-id="22dd2-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="22dd2-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22dd2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22dd2-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="22dd2-139">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="22dd2-140">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="22dd2-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
