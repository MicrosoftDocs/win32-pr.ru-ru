---
title: 'Функция Texture2DMS:: Dimension'
description: 'Возвращает размеры ресурса. | Функция Texture2DMS:: Dimension'
ms.assetid: badf4127-2498-4c2e-acc7-20507488fc6b
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
ms.openlocfilehash: f720a10ac73f48ce1f27c5676d706a75178aa8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000143"
---
# <a name="texture2dmsgetdimensions-function"></a><span data-ttu-id="95964-105">Функция Texture2DMS:: Dimension</span><span class="sxs-lookup"><span data-stu-id="95964-105">Texture2DMS::GetDimensions function</span></span>

<span data-ttu-id="95964-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="95964-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="95964-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95964-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="95964-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="95964-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95964-109">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="95964-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95964-110">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95964-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="95964-111">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="95964-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="95964-112">*Высота* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="95964-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95964-113">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95964-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="95964-114">Высота ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="95964-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="95964-115">*Нумберофсамплес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="95964-115">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95964-116">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95964-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="95964-117">Число расположений выборки.</span><span class="sxs-lookup"><span data-stu-id="95964-117">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95964-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95964-118">Return value</span></span>

<span data-ttu-id="95964-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="95964-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95964-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="95964-120">Remarks</span></span>

<span data-ttu-id="95964-121">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="95964-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float NumberOfSamples);
```



<span data-ttu-id="95964-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="95964-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="95964-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="95964-123">Vertex</span></span> | <span data-ttu-id="95964-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="95964-124">Hull</span></span> | <span data-ttu-id="95964-125">Домен</span><span class="sxs-lookup"><span data-stu-id="95964-125">Domain</span></span> | <span data-ttu-id="95964-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="95964-126">Geometry</span></span> | <span data-ttu-id="95964-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="95964-127">Pixel</span></span> | <span data-ttu-id="95964-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="95964-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="95964-129">x</span><span class="sxs-lookup"><span data-stu-id="95964-129">x</span></span>     | <span data-ttu-id="95964-130">x</span><span class="sxs-lookup"><span data-stu-id="95964-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="95964-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95964-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95964-132">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="95964-132">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="95964-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="95964-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
