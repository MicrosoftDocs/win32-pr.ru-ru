---
description: 'Метод ID3DXTextureShader:: сетматрикс — задает трансобъектную матрицу.'
ms.assetid: 891441ea-09d5-43b6-a080-578d7f8e4586
title: 'Метод ID3DXTextureShader:: Сетматрикс (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15ba6b289ad106a8fad4a932b9c5d01e0a52dc18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090222"
---
# <a name="id3dxtextureshadersetmatrix-method"></a><span data-ttu-id="31a3a-103">Метод ID3DXTextureShader:: Сетматрикс</span><span class="sxs-lookup"><span data-stu-id="31a3a-103">ID3DXTextureShader::SetMatrix method</span></span>

<span data-ttu-id="31a3a-104">Задает трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="31a3a-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a3a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31a3a-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="31a3a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31a3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31a3a-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31a3a-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a3a-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="31a3a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="31a3a-109">Уникальный идентификатор матрицы констант.</span><span class="sxs-lookup"><span data-stu-id="31a3a-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="31a3a-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="31a3a-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="31a3a-111">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31a3a-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a3a-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="31a3a-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="31a3a-113">Указатель на трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="31a3a-113">Pointer to a non-transposed matrix.</span></span> <span data-ttu-id="31a3a-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="31a3a-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31a3a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31a3a-115">Return value</span></span>

<span data-ttu-id="31a3a-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31a3a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31a3a-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="31a3a-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="31a3a-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="31a3a-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="31a3a-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="31a3a-119">Remarks</span></span>

<span data-ttu-id="31a3a-120">Неперенесенная матрица содержит основные данные строки. то есть каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="31a3a-120">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="31a3a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="31a3a-121">Requirements</span></span>



| <span data-ttu-id="31a3a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="31a3a-122">Requirement</span></span> | <span data-ttu-id="31a3a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="31a3a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="31a3a-124">Header</span><span class="sxs-lookup"><span data-stu-id="31a3a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="31a3a-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="31a3a-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="31a3a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31a3a-126">Library</span></span><br/> | <dl> <span data-ttu-id="31a3a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31a3a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="31a3a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="31a3a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a3a-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="31a3a-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




