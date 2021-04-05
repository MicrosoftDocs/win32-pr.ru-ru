---
description: Возвращает массив указателей на нонтранспосед матрицы.
ms.assetid: ee9f752d-a06a-43a3-b4ce-d1d585ba8c08
title: 'Метод ID3DXBaseEffect:: Жетматрикспоинтераррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a841c321e641b74841a76432eab8b016f396f61a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000515"
---
# <a name="id3dxbaseeffectgetmatrixpointerarray-method"></a><span data-ttu-id="3939d-103">Метод ID3DXBaseEffect:: Жетматрикспоинтераррай</span><span class="sxs-lookup"><span data-stu-id="3939d-103">ID3DXBaseEffect::GetMatrixPointerArray method</span></span>

<span data-ttu-id="3939d-104">Возвращает массив указателей на нонтранспосед матрицы.</span><span class="sxs-lookup"><span data-stu-id="3939d-104">Gets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="3939d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3939d-105">Syntax</span></span>


```C++
HRESULT GetMatrixPointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="3939d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3939d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3939d-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3939d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3939d-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3939d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3939d-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3939d-109">Unique identifier.</span></span> <span data-ttu-id="3939d-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="3939d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="3939d-111">*ппматрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3939d-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3939d-112">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3939d-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="3939d-113">Массив указателей на матрицы нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="3939d-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="3939d-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="3939d-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="3939d-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3939d-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3939d-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3939d-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3939d-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="3939d-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3939d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3939d-118">Return value</span></span>

<span data-ttu-id="3939d-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3939d-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3939d-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3939d-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3939d-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="3939d-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3939d-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3939d-122">Remarks</span></span>

<span data-ttu-id="3939d-123">Матрица нонтранспосед содержит основные данные строки. то есть каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="3939d-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="3939d-124">Если целевые матрицы больше, чем исходные матрицы, будут заполнены только верхние левые компоненты каждой целевой матрицы, а остальные компоненты матрицы назначения будут иметь нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3939d-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3939d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3939d-125">Requirements</span></span>



| <span data-ttu-id="3939d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3939d-126">Requirement</span></span> | <span data-ttu-id="3939d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3939d-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3939d-128">Header</span><span class="sxs-lookup"><span data-stu-id="3939d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3939d-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3939d-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3939d-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3939d-130">Library</span></span><br/> | <dl> <span data-ttu-id="3939d-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3939d-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3939d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3939d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3939d-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="3939d-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="3939d-134">**жетматриксаррай**</span><span class="sxs-lookup"><span data-stu-id="3939d-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
