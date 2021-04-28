---
description: 'Метод ID3DXTextureShader:: Сетматрикстранспосепоинтераррай — задает массив указателей на перекладываемые матрицы.'
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: 'Метод ID3DXTextureShader:: Сетматрикстранспосепоинтераррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 46e04c8c86bd0cdf7acea44872d00ad19f620ee6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090152"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="442e9-103">Метод ID3DXTextureShader:: Сетматрикстранспосепоинтераррай</span><span class="sxs-lookup"><span data-stu-id="442e9-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="442e9-104">Задает массив указателей на перекладываемые матрицы.</span><span class="sxs-lookup"><span data-stu-id="442e9-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="442e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="442e9-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="442e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="442e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="442e9-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="442e9-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="442e9-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="442e9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="442e9-109">Уникальный идентификатор массива констант матрицы.</span><span class="sxs-lookup"><span data-stu-id="442e9-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="442e9-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="442e9-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="442e9-111">*ппматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="442e9-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="442e9-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="442e9-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="442e9-113">Массив указателей на переликвидированные матрицы.</span><span class="sxs-lookup"><span data-stu-id="442e9-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="442e9-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="442e9-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="442e9-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="442e9-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="442e9-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="442e9-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="442e9-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="442e9-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="442e9-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="442e9-118">Return value</span></span>

<span data-ttu-id="442e9-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="442e9-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="442e9-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="442e9-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="442e9-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="442e9-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="442e9-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="442e9-122">Remarks</span></span>

<span data-ttu-id="442e9-123">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="442e9-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="442e9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="442e9-124">Requirements</span></span>



| <span data-ttu-id="442e9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="442e9-125">Requirement</span></span> | <span data-ttu-id="442e9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="442e9-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="442e9-127">Header</span><span class="sxs-lookup"><span data-stu-id="442e9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="442e9-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="442e9-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="442e9-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="442e9-129">Library</span></span><br/> | <dl> <span data-ttu-id="442e9-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="442e9-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="442e9-131">См. также</span><span class="sxs-lookup"><span data-stu-id="442e9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="442e9-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="442e9-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
