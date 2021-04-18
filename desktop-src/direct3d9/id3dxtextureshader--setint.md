---
description: Задает целочисленное значение.
ms.assetid: e7dcf3f4-1d0c-432a-85fc-0473c49956ff
title: 'Метод ID3DXTextureShader:: SetInt (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetInt
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b440811123935f279b0c4c1661c2a39aa86669f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713919"
---
# <a name="id3dxtextureshadersetint-method"></a><span data-ttu-id="2bd4d-103">Метод ID3DXTextureShader:: SetInt</span><span class="sxs-lookup"><span data-stu-id="2bd4d-103">ID3DXTextureShader::SetInt method</span></span>

<span data-ttu-id="2bd4d-104">Задает целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="2bd4d-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bd4d-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hConstant,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="2bd4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bd4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bd4d-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2bd4d-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd4d-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2bd4d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2bd4d-109">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="2bd4d-109">Unique identifier to the constant.</span></span> <span data-ttu-id="2bd4d-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="2bd4d-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd4d-111">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2bd4d-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd4d-112">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bd4d-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2bd4d-113">Целое значение.</span><span class="sxs-lookup"><span data-stu-id="2bd4d-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bd4d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bd4d-114">Return value</span></span>

<span data-ttu-id="2bd4d-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2bd4d-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2bd4d-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2bd4d-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2bd4d-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="2bd4d-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd4d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2bd4d-118">Requirements</span></span>



| <span data-ttu-id="2bd4d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2bd4d-119">Requirement</span></span> | <span data-ttu-id="2bd4d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2bd4d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd4d-121">Header</span><span class="sxs-lookup"><span data-stu-id="2bd4d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2bd4d-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bd4d-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2bd4d-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2bd4d-123">Library</span></span><br/> | <dl> <span data-ttu-id="2bd4d-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bd4d-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2bd4d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bd4d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd4d-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="2bd4d-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
