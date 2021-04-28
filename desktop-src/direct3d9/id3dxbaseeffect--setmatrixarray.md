---
description: 'Метод ID3DXBaseEffect:: Сетматриксаррай — задает массив матриц нонтранспосед.'
ms.assetid: 008de62c-3a36-4499-8a0b-9075756395e9
title: 'Метод ID3DXBaseEffect:: Сетматриксаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ae603708be4b34c9aa12722fe282df470c85d476
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107432"
---
# <a name="id3dxbaseeffectsetmatrixarray-method"></a><span data-ttu-id="79c8c-103">Метод ID3DXBaseEffect:: Сетматриксаррай</span><span class="sxs-lookup"><span data-stu-id="79c8c-103">ID3DXBaseEffect::SetMatrixArray method</span></span>

<span data-ttu-id="79c8c-104">Задает массив матриц нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="79c8c-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c8c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79c8c-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="79c8c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="79c8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79c8c-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79c8c-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79c8c-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="79c8c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="79c8c-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="79c8c-109">Unique identifier.</span></span> <span data-ttu-id="79c8c-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="79c8c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="79c8c-111">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79c8c-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79c8c-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="79c8c-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="79c8c-113">Массив матриц нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="79c8c-113">Array of nontransposed matrices.</span></span> <span data-ttu-id="79c8c-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="79c8c-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="79c8c-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79c8c-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79c8c-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79c8c-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79c8c-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="79c8c-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79c8c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79c8c-118">Return value</span></span>

<span data-ttu-id="79c8c-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79c8c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79c8c-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="79c8c-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="79c8c-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="79c8c-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="79c8c-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="79c8c-122">Remarks</span></span>

<span data-ttu-id="79c8c-123">Матрица нонтранспосед содержит основные данные строки. то есть каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="79c8c-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="79c8c-124">Если целевые матрицы меньше исходных матриц, то дополнительные компоненты исходных матриц будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="79c8c-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="79c8c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="79c8c-125">Requirements</span></span>



| <span data-ttu-id="79c8c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="79c8c-126">Requirement</span></span> | <span data-ttu-id="79c8c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="79c8c-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c8c-128">Header</span><span class="sxs-lookup"><span data-stu-id="79c8c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="79c8c-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="79c8c-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="79c8c-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="79c8c-130">Library</span></span><br/> | <dl> <span data-ttu-id="79c8c-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79c8c-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="79c8c-132">См. также</span><span class="sxs-lookup"><span data-stu-id="79c8c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c8c-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="79c8c-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="79c8c-134">**жетматриксаррай**</span><span class="sxs-lookup"><span data-stu-id="79c8c-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
