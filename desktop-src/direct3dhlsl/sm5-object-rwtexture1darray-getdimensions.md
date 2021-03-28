---
title: 'Функция RWTexture1DArray:: Dimension'
description: 'Возвращает размеры ресурса. | Функция RWTexture1DArray:: Dimension'
ms.assetid: 64f2757e-c03c-4f72-b081-1c57656d6e95
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
ms.openlocfilehash: d31d04ccf62b42fede209589a5e4a6760a3091d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273538"
---
# <a name="rwtexture1darraygetdimensions-function"></a><span data-ttu-id="dfd2a-105">Функция RWTexture1DArray:: Dimension</span><span class="sxs-lookup"><span data-stu-id="dfd2a-105">RWTexture1DArray::GetDimensions function</span></span>

<span data-ttu-id="dfd2a-106">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="dfd2a-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd2a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfd2a-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="dfd2a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfd2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfd2a-109">*Ширина* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfd2a-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd2a-110">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dfd2a-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dfd2a-111">Ширина ресурса в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="dfd2a-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="dfd2a-112">*Элементы* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfd2a-112">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd2a-113">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dfd2a-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dfd2a-114">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="dfd2a-114">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfd2a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfd2a-115">Return value</span></span>

<span data-ttu-id="dfd2a-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dfd2a-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfd2a-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="dfd2a-117">Remarks</span></span>

<span data-ttu-id="dfd2a-118">Это список перегруженных версий этого метода.</span><span class="sxs-lookup"><span data-stu-id="dfd2a-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="dfd2a-119">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="dfd2a-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="dfd2a-120">Вершина</span><span class="sxs-lookup"><span data-stu-id="dfd2a-120">Vertex</span></span> | <span data-ttu-id="dfd2a-121">Поверхности</span><span class="sxs-lookup"><span data-stu-id="dfd2a-121">Hull</span></span> | <span data-ttu-id="dfd2a-122">Домен</span><span class="sxs-lookup"><span data-stu-id="dfd2a-122">Domain</span></span> | <span data-ttu-id="dfd2a-123">Геометрия</span><span class="sxs-lookup"><span data-stu-id="dfd2a-123">Geometry</span></span> | <span data-ttu-id="dfd2a-124">Пиксель</span><span class="sxs-lookup"><span data-stu-id="dfd2a-124">Pixel</span></span> | <span data-ttu-id="dfd2a-125">Вычисления</span><span class="sxs-lookup"><span data-stu-id="dfd2a-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="dfd2a-126">x</span><span class="sxs-lookup"><span data-stu-id="dfd2a-126">x</span></span>     | <span data-ttu-id="dfd2a-127">x</span><span class="sxs-lookup"><span data-stu-id="dfd2a-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dfd2a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfd2a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd2a-129">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="dfd2a-129">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="dfd2a-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="dfd2a-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
