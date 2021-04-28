---
description: 'Метод ID3DXTextureShader:: Сетматрикстранспосеаррай — задает массив переданных матриц.'
ms.assetid: 100288f2-44f0-4e75-bffb-78732c50a55c
title: 'Метод ID3DXTextureShader:: Сетматрикстранспосеаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 663f49f600c000ff37974c8ecd4da56ba59630d1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090212"
---
# <a name="id3dxtextureshadersetmatrixtransposearray-method"></a><span data-ttu-id="ebf74-103">Метод ID3DXTextureShader:: Сетматрикстранспосеаррай</span><span class="sxs-lookup"><span data-stu-id="ebf74-103">ID3DXTextureShader::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="ebf74-104">Задает массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="ebf74-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf74-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebf74-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="ebf74-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebf74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf74-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebf74-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf74-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ebf74-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ebf74-109">Уникальный идентификатор массива констант матрицы.</span><span class="sxs-lookup"><span data-stu-id="ebf74-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="ebf74-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="ebf74-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebf74-111">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebf74-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf74-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ebf74-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ebf74-113">Массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="ebf74-113">Array of transposed matrices.</span></span> <span data-ttu-id="ebf74-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="ebf74-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebf74-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebf74-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf74-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ebf74-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ebf74-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="ebf74-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebf74-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebf74-118">Return value</span></span>

<span data-ttu-id="ebf74-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ebf74-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ebf74-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ebf74-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ebf74-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ebf74-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf74-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="ebf74-122">Remarks</span></span>

<span data-ttu-id="ebf74-123">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="ebf74-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf74-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ebf74-124">Requirements</span></span>



| <span data-ttu-id="ebf74-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ebf74-125">Requirement</span></span> | <span data-ttu-id="ebf74-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ebf74-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf74-127">Header</span><span class="sxs-lookup"><span data-stu-id="ebf74-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ebf74-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebf74-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ebf74-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ebf74-129">Library</span></span><br/> | <dl> <span data-ttu-id="ebf74-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebf74-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ebf74-131">См. также</span><span class="sxs-lookup"><span data-stu-id="ebf74-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf74-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="ebf74-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
