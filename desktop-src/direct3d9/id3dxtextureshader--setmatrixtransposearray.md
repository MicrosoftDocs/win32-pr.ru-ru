---
description: Задает массив переданных матриц.
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
ms.openlocfilehash: c9efd0c81cef8a72880a9755ca40e4dd8b4950ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000340"
---
# <a name="id3dxtextureshadersetmatrixtransposearray-method"></a><span data-ttu-id="70923-103">Метод ID3DXTextureShader:: Сетматрикстранспосеаррай</span><span class="sxs-lookup"><span data-stu-id="70923-103">ID3DXTextureShader::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="70923-104">Задает массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="70923-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="70923-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70923-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="70923-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="70923-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70923-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70923-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70923-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="70923-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="70923-109">Уникальный идентификатор массива констант матрицы.</span><span class="sxs-lookup"><span data-stu-id="70923-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="70923-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="70923-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="70923-111">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70923-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70923-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="70923-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="70923-113">Массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="70923-113">Array of transposed matrices.</span></span> <span data-ttu-id="70923-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="70923-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="70923-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70923-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70923-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70923-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70923-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="70923-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70923-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70923-118">Return value</span></span>

<span data-ttu-id="70923-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70923-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70923-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="70923-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="70923-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="70923-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="70923-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70923-122">Remarks</span></span>

<span data-ttu-id="70923-123">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="70923-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="70923-124">Требования</span><span class="sxs-lookup"><span data-stu-id="70923-124">Requirements</span></span>



| <span data-ttu-id="70923-125">Требование</span><span class="sxs-lookup"><span data-stu-id="70923-125">Requirement</span></span> | <span data-ttu-id="70923-126">Значение</span><span class="sxs-lookup"><span data-stu-id="70923-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="70923-127">Header</span><span class="sxs-lookup"><span data-stu-id="70923-127">Header</span></span><br/>  | <dl> <span data-ttu-id="70923-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="70923-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="70923-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="70923-129">Library</span></span><br/> | <dl> <span data-ttu-id="70923-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70923-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="70923-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70923-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70923-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="70923-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
