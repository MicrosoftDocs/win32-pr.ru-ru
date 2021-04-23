---
title: 'Функция RWTexture2D:: Dimension'
description: 'Возвращает размеры ресурса. | Функция RWTexture2D:: Dimension'
ms.assetid: bc55622d-fbff-4aeb-aceb-4eb2cfc7ac28
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
ms.openlocfilehash: 19a6711e8f04afdb2f5ec66ff33c8aaf1d59b40c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104157110"
---
# <a name="rwtexture2dgetdimensions-function"></a><span data-ttu-id="a35c7-105">Функция RWTexture2D:: Dimension</span><span class="sxs-lookup"><span data-stu-id="a35c7-105">RWTexture2D::GetDimensions function</span></span>

<span data-ttu-id="a35c7-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="a35c7-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35c7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a35c7-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height
);
```

## <a name="parameters"></a><span data-ttu-id="a35c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a35c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a35c7-109">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a35c7-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a35c7-110">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a35c7-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a35c7-111">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="a35c7-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="a35c7-112">*Высота* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a35c7-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a35c7-113">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a35c7-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a35c7-114">Высота ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="a35c7-114">The resource height, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a35c7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a35c7-115">Return value</span></span>

<span data-ttu-id="a35c7-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a35c7-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a35c7-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="a35c7-117">Remarks</span></span>

<span data-ttu-id="a35c7-118">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="a35c7-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="a35c7-119">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="a35c7-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a35c7-120">Вершина</span><span class="sxs-lookup"><span data-stu-id="a35c7-120">Vertex</span></span> | <span data-ttu-id="a35c7-121">Поверхности</span><span class="sxs-lookup"><span data-stu-id="a35c7-121">Hull</span></span> | <span data-ttu-id="a35c7-122">Домен</span><span class="sxs-lookup"><span data-stu-id="a35c7-122">Domain</span></span> | <span data-ttu-id="a35c7-123">Геометрия</span><span class="sxs-lookup"><span data-stu-id="a35c7-123">Geometry</span></span> | <span data-ttu-id="a35c7-124">Пиксель</span><span class="sxs-lookup"><span data-stu-id="a35c7-124">Pixel</span></span> | <span data-ttu-id="a35c7-125">Вычисления</span><span class="sxs-lookup"><span data-stu-id="a35c7-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a35c7-126">x</span><span class="sxs-lookup"><span data-stu-id="a35c7-126">x</span></span>     | <span data-ttu-id="a35c7-127">x</span><span class="sxs-lookup"><span data-stu-id="a35c7-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a35c7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a35c7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35c7-129">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="a35c7-129">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="a35c7-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="a35c7-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
