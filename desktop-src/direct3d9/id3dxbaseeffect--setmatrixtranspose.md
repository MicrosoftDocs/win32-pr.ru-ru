---
description: Задает трансобъектную матрицу.
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: 'Метод ID3DXBaseEffect:: Сетматрикстранспосе (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f62847f7b15899389cbd5f207ce810b0ed0dd119
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720863"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a><span data-ttu-id="74205-103">Метод ID3DXBaseEffect:: Сетматрикстранспосе</span><span class="sxs-lookup"><span data-stu-id="74205-103">ID3DXBaseEffect::SetMatrixTranspose method</span></span>

<span data-ttu-id="74205-104">Задает трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="74205-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="74205-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74205-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="74205-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74205-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74205-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74205-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74205-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="74205-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="74205-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="74205-109">Unique identifier.</span></span> <span data-ttu-id="74205-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="74205-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="74205-111">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74205-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74205-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="74205-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="74205-113">Указатель на переустановленную матрицу.</span><span class="sxs-lookup"><span data-stu-id="74205-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="74205-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="74205-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74205-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74205-115">Return value</span></span>

<span data-ttu-id="74205-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74205-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74205-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="74205-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="74205-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="74205-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="74205-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74205-119">Remarks</span></span>

<span data-ttu-id="74205-120">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="74205-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="74205-121">Если целевая матрица меньше, чем исходная матрица, дополнительные компоненты исходной матрицы будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="74205-121">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="74205-122">Требования</span><span class="sxs-lookup"><span data-stu-id="74205-122">Requirements</span></span>



| <span data-ttu-id="74205-123">Требование</span><span class="sxs-lookup"><span data-stu-id="74205-123">Requirement</span></span> | <span data-ttu-id="74205-124">Значение</span><span class="sxs-lookup"><span data-stu-id="74205-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="74205-125">Header</span><span class="sxs-lookup"><span data-stu-id="74205-125">Header</span></span><br/>  | <dl> <span data-ttu-id="74205-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="74205-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="74205-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="74205-127">Library</span></span><br/> | <dl> <span data-ttu-id="74205-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74205-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="74205-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74205-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74205-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="74205-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="74205-131">**жетматрикстранспосе**</span><span class="sxs-lookup"><span data-stu-id="74205-131">**GetMatrixTranspose**</span></span>](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




