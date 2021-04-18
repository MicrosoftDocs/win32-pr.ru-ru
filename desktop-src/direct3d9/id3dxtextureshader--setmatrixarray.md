---
description: Задает массив нестандартных матриц.
ms.assetid: 27f230bd-9aee-4673-aa70-5ecda541b1be
title: 'Метод ID3DXTextureShader:: Сетматриксаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b0545d48e16698f44cc48ad467f9454ac94db030
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713715"
---
# <a name="id3dxtextureshadersetmatrixarray-method"></a><span data-ttu-id="e8232-103">Метод ID3DXTextureShader:: Сетматриксаррай</span><span class="sxs-lookup"><span data-stu-id="e8232-103">ID3DXTextureShader::SetMatrixArray method</span></span>

<span data-ttu-id="e8232-104">Задает массив нестандартных матриц.</span><span class="sxs-lookup"><span data-stu-id="e8232-104">Sets an array of non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8232-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8232-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="e8232-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8232-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8232-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8232-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8232-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e8232-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e8232-109">Уникальный идентификатор массива константных матриц.</span><span class="sxs-lookup"><span data-stu-id="e8232-109">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="e8232-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="e8232-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8232-111">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8232-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8232-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8232-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e8232-113">Массив нестандартных матриц.</span><span class="sxs-lookup"><span data-stu-id="e8232-113">Array of non-transposed matrices.</span></span> <span data-ttu-id="e8232-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="e8232-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8232-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8232-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8232-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8232-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8232-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="e8232-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8232-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8232-118">Return value</span></span>

<span data-ttu-id="e8232-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8232-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8232-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e8232-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e8232-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e8232-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8232-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8232-122">Remarks</span></span>

<span data-ttu-id="e8232-123">Неперенесенная матрица содержит основные данные строки. то есть каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="e8232-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8232-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e8232-124">Requirements</span></span>



| <span data-ttu-id="e8232-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e8232-125">Requirement</span></span> | <span data-ttu-id="e8232-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e8232-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8232-127">Header</span><span class="sxs-lookup"><span data-stu-id="e8232-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e8232-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8232-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e8232-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e8232-129">Library</span></span><br/> | <dl> <span data-ttu-id="e8232-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8232-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e8232-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8232-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8232-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="e8232-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
