---
description: Задает массив указателей на перекладываемые матрицы.
ms.assetid: 11a21077-eeee-4d52-ac16-41444e3eca4f
title: 'Метод ID3DXBaseEffect:: Сетматрикстранспосепоинтераррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1152deccdcadebe9f421fac6d7d5ce53c8d3e5f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720937"
---
# <a name="id3dxbaseeffectsetmatrixtransposepointerarray-method"></a><span data-ttu-id="dcb26-103">Метод ID3DXBaseEffect:: Сетматрикстранспосепоинтераррай</span><span class="sxs-lookup"><span data-stu-id="dcb26-103">ID3DXBaseEffect::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="dcb26-104">Задает массив указателей на перекладываемые матрицы.</span><span class="sxs-lookup"><span data-stu-id="dcb26-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcb26-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcb26-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="dcb26-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcb26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcb26-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcb26-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcb26-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="dcb26-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="dcb26-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="dcb26-109">Unique identifier.</span></span> <span data-ttu-id="dcb26-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="dcb26-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcb26-111">*ппматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcb26-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcb26-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="dcb26-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="dcb26-113">Массив указателей на переликвидированные матрицы.</span><span class="sxs-lookup"><span data-stu-id="dcb26-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="dcb26-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="dcb26-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcb26-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcb26-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcb26-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcb26-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcb26-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="dcb26-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcb26-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcb26-118">Return value</span></span>

<span data-ttu-id="dcb26-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dcb26-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dcb26-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="dcb26-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dcb26-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="dcb26-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcb26-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcb26-122">Remarks</span></span>

<span data-ttu-id="dcb26-123">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="dcb26-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="dcb26-124">Если целевые матрицы меньше исходных матриц, то дополнительные компоненты исходных матриц будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="dcb26-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcb26-125">Требования</span><span class="sxs-lookup"><span data-stu-id="dcb26-125">Requirements</span></span>



| <span data-ttu-id="dcb26-126">Требование</span><span class="sxs-lookup"><span data-stu-id="dcb26-126">Requirement</span></span> | <span data-ttu-id="dcb26-127">Значение</span><span class="sxs-lookup"><span data-stu-id="dcb26-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb26-128">Header</span><span class="sxs-lookup"><span data-stu-id="dcb26-128">Header</span></span><br/>  | <dl> <span data-ttu-id="dcb26-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcb26-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="dcb26-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dcb26-130">Library</span></span><br/> | <dl> <span data-ttu-id="dcb26-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcb26-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dcb26-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcb26-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb26-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="dcb26-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="dcb26-134">**жетматрикстранспосеаррай**</span><span class="sxs-lookup"><span data-stu-id="dcb26-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
