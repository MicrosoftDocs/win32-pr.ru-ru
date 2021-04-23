---
title: 'Функция RWTexture3D:: Dimension'
description: 'Возвращает размеры ресурса. | Функция RWTexture3D:: Dimension'
ms.assetid: ba70b955-1e80-4f27-84f1-fc9d26a1f1ab
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
ms.openlocfilehash: 499ab493851257030921e9d55f4873eef8726915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352965"
---
# <a name="rwtexture3dgetdimensions-function"></a><span data-ttu-id="87e33-105">Функция RWTexture3D:: Dimension</span><span class="sxs-lookup"><span data-stu-id="87e33-105">RWTexture3D::GetDimensions function</span></span>

<span data-ttu-id="87e33-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="87e33-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e33-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87e33-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Depth
);
```

## <a name="parameters"></a><span data-ttu-id="87e33-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="87e33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e33-109">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="87e33-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87e33-110">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="87e33-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="87e33-111">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="87e33-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="87e33-112">*Высота* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="87e33-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87e33-113">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="87e33-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="87e33-114">Высота ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="87e33-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="87e33-115">*Глубина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="87e33-115">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87e33-116">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="87e33-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="87e33-117">Глубина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="87e33-117">The resource depth, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87e33-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87e33-118">Return value</span></span>

<span data-ttu-id="87e33-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="87e33-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87e33-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="87e33-120">Remarks</span></span>

<span data-ttu-id="87e33-121">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="87e33-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="87e33-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="87e33-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="87e33-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="87e33-123">Vertex</span></span> | <span data-ttu-id="87e33-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="87e33-124">Hull</span></span> | <span data-ttu-id="87e33-125">Домен</span><span class="sxs-lookup"><span data-stu-id="87e33-125">Domain</span></span> | <span data-ttu-id="87e33-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="87e33-126">Geometry</span></span> | <span data-ttu-id="87e33-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="87e33-127">Pixel</span></span> | <span data-ttu-id="87e33-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="87e33-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="87e33-129">x</span><span class="sxs-lookup"><span data-stu-id="87e33-129">x</span></span>     | <span data-ttu-id="87e33-130">x</span><span class="sxs-lookup"><span data-stu-id="87e33-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="87e33-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87e33-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e33-132">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="87e33-132">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="87e33-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="87e33-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
