---
description: Возвращает массив указателей на перелагаемые матрицы.
ms.assetid: b859ff2f-cf62-4619-b8be-b940fa0513b3
title: 'Метод ID3DXBaseEffect:: Жетматрикстранспосепоинтераррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e69c01395582691e6fdd0a695991ff1f726a362b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273959"
---
# <a name="id3dxbaseeffectgetmatrixtransposepointerarray-method"></a><span data-ttu-id="18724-103">Метод ID3DXBaseEffect:: Жетматрикстранспосепоинтераррай</span><span class="sxs-lookup"><span data-stu-id="18724-103">ID3DXBaseEffect::GetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="18724-104">Возвращает массив указателей на перелагаемые матрицы.</span><span class="sxs-lookup"><span data-stu-id="18724-104">Gets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="18724-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18724-105">Syntax</span></span>


```C++
HRESULT GetMatrixTransposePointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="18724-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="18724-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18724-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18724-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18724-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="18724-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="18724-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="18724-109">Unique identifier.</span></span> <span data-ttu-id="18724-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="18724-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="18724-111">*ппматрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="18724-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18724-112">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="18724-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="18724-113">Массив указателей на переликвидированные матрицы.</span><span class="sxs-lookup"><span data-stu-id="18724-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="18724-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="18724-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="18724-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18724-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18724-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18724-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18724-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="18724-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18724-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18724-118">Return value</span></span>

<span data-ttu-id="18724-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="18724-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="18724-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="18724-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="18724-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="18724-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="18724-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18724-122">Remarks</span></span>

<span data-ttu-id="18724-123">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="18724-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="18724-124">Если целевые матрицы больше, чем исходные матрицы, будут заполнены только верхние левые компоненты каждой целевой матрицы, а остальные компоненты матрицы назначения будут иметь нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="18724-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="18724-125">Требования</span><span class="sxs-lookup"><span data-stu-id="18724-125">Requirements</span></span>



| <span data-ttu-id="18724-126">Требование</span><span class="sxs-lookup"><span data-stu-id="18724-126">Requirement</span></span> | <span data-ttu-id="18724-127">Значение</span><span class="sxs-lookup"><span data-stu-id="18724-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18724-128">Header</span><span class="sxs-lookup"><span data-stu-id="18724-128">Header</span></span><br/>  | <dl> <span data-ttu-id="18724-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="18724-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="18724-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="18724-130">Library</span></span><br/> | <dl> <span data-ttu-id="18724-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18724-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="18724-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18724-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18724-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="18724-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="18724-134">**жетматрикстранспосеаррай**</span><span class="sxs-lookup"><span data-stu-id="18724-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
