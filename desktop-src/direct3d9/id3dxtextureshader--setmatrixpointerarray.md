---
description: Задает массив указателей на нестандартные матрицы.
ms.assetid: 5ad83abd-1895-4838-85b5-c437c23a3d91
title: 'Метод ID3DXTextureShader:: Сетматрикспоинтераррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1bde5250ae8ceeab7522b9df15c99070e9471608
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354493"
---
# <a name="id3dxtextureshadersetmatrixpointerarray-method"></a><span data-ttu-id="b0f29-103">Метод ID3DXTextureShader:: Сетматрикспоинтераррай</span><span class="sxs-lookup"><span data-stu-id="b0f29-103">ID3DXTextureShader::SetMatrixPointerArray method</span></span>

<span data-ttu-id="b0f29-104">Задает массив указателей на нестандартные матрицы.</span><span class="sxs-lookup"><span data-stu-id="b0f29-104">Sets an array of pointers to non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f29-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0f29-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="b0f29-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0f29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f29-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0f29-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f29-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b0f29-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b0f29-109">Уникальный идентификатор массива константных матриц.</span><span class="sxs-lookup"><span data-stu-id="b0f29-109">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="b0f29-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="b0f29-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0f29-111">*ппматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0f29-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f29-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="b0f29-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="b0f29-113">Массив указателей на нестандартные матрицы.</span><span class="sxs-lookup"><span data-stu-id="b0f29-113">Array of pointers to non-transposed matrices.</span></span> <span data-ttu-id="b0f29-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="b0f29-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0f29-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0f29-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f29-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0f29-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0f29-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="b0f29-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0f29-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0f29-118">Return value</span></span>

<span data-ttu-id="b0f29-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0f29-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0f29-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b0f29-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b0f29-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="b0f29-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0f29-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0f29-122">Remarks</span></span>

<span data-ttu-id="b0f29-123">Неперенесенная матрица содержит основные данные строки. то есть каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="b0f29-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f29-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b0f29-124">Requirements</span></span>



| <span data-ttu-id="b0f29-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b0f29-125">Requirement</span></span> | <span data-ttu-id="b0f29-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b0f29-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f29-127">Header</span><span class="sxs-lookup"><span data-stu-id="b0f29-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b0f29-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0f29-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b0f29-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b0f29-129">Library</span></span><br/> | <dl> <span data-ttu-id="b0f29-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0f29-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b0f29-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0f29-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f29-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="b0f29-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
