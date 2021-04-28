---
description: 'Метод ID3DXTextureShader:: SetInt — задает целочисленное значение.'
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
ms.openlocfilehash: 23c347c35b8accd60bdb81c931ebc3d35b48f957
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117608"
---
# <a name="id3dxtextureshadersetint-method"></a><span data-ttu-id="a5c53-103">Метод ID3DXTextureShader:: SetInt</span><span class="sxs-lookup"><span data-stu-id="a5c53-103">ID3DXTextureShader::SetInt method</span></span>

<span data-ttu-id="a5c53-104">Задает целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="a5c53-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5c53-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hConstant,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="a5c53-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5c53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5c53-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5c53-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c53-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a5c53-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a5c53-109">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="a5c53-109">Unique identifier to the constant.</span></span> <span data-ttu-id="a5c53-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a5c53-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5c53-111">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a5c53-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c53-112">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5c53-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5c53-113">Целое значение.</span><span class="sxs-lookup"><span data-stu-id="a5c53-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5c53-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5c53-114">Return value</span></span>

<span data-ttu-id="a5c53-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5c53-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5c53-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a5c53-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a5c53-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="a5c53-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c53-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a5c53-118">Requirements</span></span>



| <span data-ttu-id="a5c53-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a5c53-119">Requirement</span></span> | <span data-ttu-id="a5c53-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a5c53-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c53-121">Header</span><span class="sxs-lookup"><span data-stu-id="a5c53-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a5c53-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5c53-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a5c53-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a5c53-123">Library</span></span><br/> | <dl> <span data-ttu-id="a5c53-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5c53-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a5c53-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a5c53-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c53-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="a5c53-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
