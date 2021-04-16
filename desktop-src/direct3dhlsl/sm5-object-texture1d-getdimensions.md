---
title: 'Функция Texture1D:: Dimension'
description: 'Возвращает размеры ресурса. | Функция Texture1D:: Dimension'
ms.assetid: eb8fc02f-01c8-44b9-9d7e-faf59660c287
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
ms.openlocfilehash: fdd9b79a1cc1fa2a5a8db3e0db7a7163878b066b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547634"
---
# <a name="texture1dgetdimensions-function"></a><span data-ttu-id="e2335-105">Функция Texture1D:: Dimension</span><span class="sxs-lookup"><span data-stu-id="e2335-105">Texture1D::GetDimensions function</span></span>

<span data-ttu-id="e2335-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="e2335-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2335-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2335-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="e2335-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2335-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2335-109">*Миплевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2335-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2335-110">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2335-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e2335-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e2335-111">Optional.</span></span> <span data-ttu-id="e2335-112">Уровень mipmap (должен быть указан, если используется *нумберофлевелс* ).</span><span class="sxs-lookup"><span data-stu-id="e2335-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="e2335-113">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e2335-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2335-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2335-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e2335-115">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="e2335-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e2335-116">*Нумберофлевелс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e2335-116">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2335-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2335-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e2335-118">Число уровней mipmap (требуется также *миплевел* ).</span><span class="sxs-lookup"><span data-stu-id="e2335-118">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2335-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2335-119">Return value</span></span>

<span data-ttu-id="e2335-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e2335-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2335-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2335-121">Remarks</span></span>

<span data-ttu-id="e2335-122">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="e2335-122">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float NumberOfLevels);

void GetDimensions(out float Width);
```



<span data-ttu-id="e2335-123">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="e2335-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e2335-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="e2335-124">Vertex</span></span> | <span data-ttu-id="e2335-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e2335-125">Hull</span></span> | <span data-ttu-id="e2335-126">Домен</span><span class="sxs-lookup"><span data-stu-id="e2335-126">Domain</span></span> | <span data-ttu-id="e2335-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e2335-127">Geometry</span></span> | <span data-ttu-id="e2335-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e2335-128">Pixel</span></span> | <span data-ttu-id="e2335-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="e2335-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e2335-130">x</span><span class="sxs-lookup"><span data-stu-id="e2335-130">x</span></span>     | <span data-ttu-id="e2335-131">x</span><span class="sxs-lookup"><span data-stu-id="e2335-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e2335-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2335-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2335-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e2335-133">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="e2335-134">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e2335-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
