---
description: 'Метод ID3DXTextureShader:: Сетматрикстранспосе — задает перекладываемую матрицу.'
ms.assetid: 5339a9de-528f-4404-880b-73964192b766
title: 'Метод ID3DXTextureShader:: Сетматрикстранспосе (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91216b49dba7fabb25c128f3801d11bfa2fd95c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114302"
---
# <a name="id3dxtextureshadersetmatrixtranspose-method"></a><span data-ttu-id="b4601-103">Метод ID3DXTextureShader:: Сетматрикстранспосе</span><span class="sxs-lookup"><span data-stu-id="b4601-103">ID3DXTextureShader::SetMatrixTranspose method</span></span>

<span data-ttu-id="b4601-104">Задает трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="b4601-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4601-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4601-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="b4601-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4601-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4601-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4601-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4601-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b4601-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b4601-109">Уникальный идентификатор матрицы констант.</span><span class="sxs-lookup"><span data-stu-id="b4601-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="b4601-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="b4601-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4601-111">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4601-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4601-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b4601-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b4601-113">Указатель на переустановленную матрицу.</span><span class="sxs-lookup"><span data-stu-id="b4601-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="b4601-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="b4601-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4601-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4601-115">Return value</span></span>

<span data-ttu-id="b4601-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4601-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4601-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b4601-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b4601-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="b4601-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4601-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="b4601-119">Remarks</span></span>

<span data-ttu-id="b4601-120">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="b4601-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4601-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b4601-121">Requirements</span></span>



| <span data-ttu-id="b4601-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b4601-122">Requirement</span></span> | <span data-ttu-id="b4601-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b4601-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4601-124">Header</span><span class="sxs-lookup"><span data-stu-id="b4601-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b4601-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4601-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b4601-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4601-126">Library</span></span><br/> | <dl> <span data-ttu-id="b4601-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4601-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b4601-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b4601-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4601-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="b4601-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




