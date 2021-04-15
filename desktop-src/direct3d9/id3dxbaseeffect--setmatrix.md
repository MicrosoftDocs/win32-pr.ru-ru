---
description: Задает трансобъектную матрицу.
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: 'Метод ID3DXBaseEffect:: Сетматрикс (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 39a5aed1d6321cf0599d212222fd967ee512e20e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547823"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="4cbe0-103">Метод ID3DXBaseEffect:: Сетматрикс</span><span class="sxs-lookup"><span data-stu-id="4cbe0-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="4cbe0-104">Задает трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="4cbe0-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cbe0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cbe0-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="4cbe0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cbe0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cbe0-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4cbe0-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cbe0-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4cbe0-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4cbe0-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="4cbe0-109">Unique identifier.</span></span> <span data-ttu-id="4cbe0-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="4cbe0-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="4cbe0-111">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4cbe0-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cbe0-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cbe0-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4cbe0-113">Указатель на матрицу нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="4cbe0-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="4cbe0-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="4cbe0-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cbe0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cbe0-115">Return value</span></span>

<span data-ttu-id="4cbe0-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4cbe0-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4cbe0-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4cbe0-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4cbe0-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="4cbe0-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cbe0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cbe0-119">Remarks</span></span>

<span data-ttu-id="4cbe0-120">Неперенесенная матрица содержит основные данные строки.</span><span class="sxs-lookup"><span data-stu-id="4cbe0-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="4cbe0-121">Иными словами, каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="4cbe0-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="4cbe0-122">Если целевая матрица меньше, чем исходная матрица, дополнительные компоненты исходной матрицы будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="4cbe0-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cbe0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4cbe0-123">Requirements</span></span>



| <span data-ttu-id="4cbe0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4cbe0-124">Requirement</span></span> | <span data-ttu-id="4cbe0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4cbe0-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cbe0-126">Header</span><span class="sxs-lookup"><span data-stu-id="4cbe0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4cbe0-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cbe0-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4cbe0-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4cbe0-128">Library</span></span><br/> | <dl> <span data-ttu-id="4cbe0-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cbe0-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4cbe0-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cbe0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cbe0-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="4cbe0-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="4cbe0-132">**Матрица**</span><span class="sxs-lookup"><span data-stu-id="4cbe0-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




