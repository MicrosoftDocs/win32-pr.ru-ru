---
title: 'Функция RWTexture1D:: Dimension'
description: 'Возвращает размеры ресурса. | Функция RWTexture1D:: Dimension'
ms.assetid: 1bbd53ed-9396-4e8e-b2f3-3bd85f6e1a90
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
ms.openlocfilehash: b65f0113ecf2c91786e45c35f5e8e832744bc952
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986200"
---
# <a name="rwtexture1dgetdimensions-function"></a><span data-ttu-id="52f24-105">Функция RWTexture1D:: Dimension</span><span class="sxs-lookup"><span data-stu-id="52f24-105">RWTexture1D::GetDimensions function</span></span>

<span data-ttu-id="52f24-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="52f24-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="52f24-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52f24-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width
);
```

## <a name="parameters"></a><span data-ttu-id="52f24-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="52f24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52f24-109">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="52f24-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52f24-110">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="52f24-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="52f24-111">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="52f24-111">The resource width, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52f24-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52f24-112">Return value</span></span>

<span data-ttu-id="52f24-113">Nothing</span><span class="sxs-lookup"><span data-stu-id="52f24-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="52f24-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="52f24-114">Remarks</span></span>

<span data-ttu-id="52f24-115">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="52f24-115">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width);

void GetDimensions(out float Width);
```



<span data-ttu-id="52f24-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="52f24-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="52f24-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="52f24-117">Vertex</span></span> | <span data-ttu-id="52f24-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="52f24-118">Hull</span></span> | <span data-ttu-id="52f24-119">Домен</span><span class="sxs-lookup"><span data-stu-id="52f24-119">Domain</span></span> | <span data-ttu-id="52f24-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="52f24-120">Geometry</span></span> | <span data-ttu-id="52f24-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="52f24-121">Pixel</span></span> | <span data-ttu-id="52f24-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="52f24-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="52f24-123">x</span><span class="sxs-lookup"><span data-stu-id="52f24-123">x</span></span>     | <span data-ttu-id="52f24-124">x</span><span class="sxs-lookup"><span data-stu-id="52f24-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="52f24-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52f24-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f24-126">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="52f24-126">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="52f24-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="52f24-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
