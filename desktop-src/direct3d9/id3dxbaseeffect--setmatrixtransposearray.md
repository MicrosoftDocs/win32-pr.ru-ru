---
description: Задает массив переданных матриц.
ms.assetid: 5dc65424-b0cd-490d-900e-60b9f7536ace
title: 'Метод ID3DXBaseEffect:: Сетматрикстранспосеаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e646761435f75688fe652683281297ca2b8de99e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713811"
---
# <a name="id3dxbaseeffectsetmatrixtransposearray-method"></a><span data-ttu-id="fe743-103">Метод ID3DXBaseEffect:: Сетматрикстранспосеаррай</span><span class="sxs-lookup"><span data-stu-id="fe743-103">ID3DXBaseEffect::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="fe743-104">Задает массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="fe743-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe743-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe743-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="fe743-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe743-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe743-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe743-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe743-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fe743-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fe743-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="fe743-109">Unique identifier.</span></span> <span data-ttu-id="fe743-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fe743-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe743-111">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe743-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe743-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe743-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fe743-113">Массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="fe743-113">Array of transposed matrices.</span></span> <span data-ttu-id="fe743-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="fe743-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe743-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe743-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe743-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe743-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe743-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="fe743-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe743-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe743-118">Return value</span></span>

<span data-ttu-id="fe743-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe743-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe743-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fe743-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fe743-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="fe743-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe743-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe743-122">Remarks</span></span>

<span data-ttu-id="fe743-123">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="fe743-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="fe743-124">Если целевые матрицы меньше исходных матриц, то дополнительные компоненты исходных матриц будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="fe743-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe743-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fe743-125">Requirements</span></span>



| <span data-ttu-id="fe743-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fe743-126">Requirement</span></span> | <span data-ttu-id="fe743-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fe743-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe743-128">Header</span><span class="sxs-lookup"><span data-stu-id="fe743-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fe743-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe743-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fe743-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe743-130">Library</span></span><br/> | <dl> <span data-ttu-id="fe743-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe743-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fe743-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe743-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe743-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fe743-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="fe743-134">**жетматрикстранспосеаррай**</span><span class="sxs-lookup"><span data-stu-id="fe743-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
