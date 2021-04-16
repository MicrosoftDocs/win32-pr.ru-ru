---
description: Задает массив указателей на перекладываемые матрицы.
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
ms.openlocfilehash: cd7c81dcb0fd9b9354c2536a91abaebfe8e4315b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664979"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="488ed-103">Метод ID3DXTextureShader:: Сетматрикстранспосепоинтераррай</span><span class="sxs-lookup"><span data-stu-id="488ed-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="488ed-104">Задает массив указателей на перекладываемые матрицы.</span><span class="sxs-lookup"><span data-stu-id="488ed-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="488ed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="488ed-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="488ed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="488ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="488ed-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="488ed-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="488ed-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="488ed-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="488ed-109">Уникальный идентификатор массива констант матрицы.</span><span class="sxs-lookup"><span data-stu-id="488ed-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="488ed-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="488ed-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="488ed-111">*ппматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="488ed-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="488ed-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="488ed-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="488ed-113">Массив указателей на переликвидированные матрицы.</span><span class="sxs-lookup"><span data-stu-id="488ed-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="488ed-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="488ed-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="488ed-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="488ed-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="488ed-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="488ed-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="488ed-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="488ed-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="488ed-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="488ed-118">Return value</span></span>

<span data-ttu-id="488ed-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="488ed-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="488ed-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="488ed-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="488ed-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="488ed-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="488ed-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="488ed-122">Remarks</span></span>

<span data-ttu-id="488ed-123">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="488ed-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="488ed-124">Требования</span><span class="sxs-lookup"><span data-stu-id="488ed-124">Requirements</span></span>



| <span data-ttu-id="488ed-125">Требование</span><span class="sxs-lookup"><span data-stu-id="488ed-125">Requirement</span></span> | <span data-ttu-id="488ed-126">Значение</span><span class="sxs-lookup"><span data-stu-id="488ed-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="488ed-127">Header</span><span class="sxs-lookup"><span data-stu-id="488ed-127">Header</span></span><br/>  | <dl> <span data-ttu-id="488ed-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="488ed-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="488ed-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="488ed-129">Library</span></span><br/> | <dl> <span data-ttu-id="488ed-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="488ed-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="488ed-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="488ed-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="488ed-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="488ed-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
