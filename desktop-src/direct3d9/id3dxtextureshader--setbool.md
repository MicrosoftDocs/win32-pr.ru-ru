---
description: 'Метод ID3DXTextureShader:: Сетбул — задает логическое значение.'
ms.assetid: 0d3c1f3a-f497-4e92-81e9-8647006910e1
title: 'Метод ID3DXTextureShader:: Сетбул (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 512daf7e770c72fe038622877d1756a5fd3532bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117632"
---
# <a name="id3dxtextureshadersetbool-method"></a><span data-ttu-id="c5bb4-103">Метод ID3DXTextureShader:: Сетбул</span><span class="sxs-lookup"><span data-stu-id="c5bb4-103">ID3DXTextureShader::SetBool method</span></span>

<span data-ttu-id="c5bb4-104">Задает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="c5bb4-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5bb4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5bb4-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="c5bb4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5bb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5bb4-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5bb4-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5bb4-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c5bb4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c5bb4-109">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="c5bb4-109">Unique identifier to the constant.</span></span> <span data-ttu-id="c5bb4-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="c5bb4-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5bb4-111">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c5bb4-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5bb4-112">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5bb4-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5bb4-113">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="c5bb4-113">BOOL value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5bb4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5bb4-114">Return value</span></span>

<span data-ttu-id="c5bb4-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5bb4-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5bb4-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c5bb4-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c5bb4-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c5bb4-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5bb4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c5bb4-118">Requirements</span></span>



| <span data-ttu-id="c5bb4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c5bb4-119">Requirement</span></span> | <span data-ttu-id="c5bb4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c5bb4-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5bb4-121">Header</span><span class="sxs-lookup"><span data-stu-id="c5bb4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c5bb4-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5bb4-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c5bb4-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c5bb4-123">Library</span></span><br/> | <dl> <span data-ttu-id="c5bb4-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5bb4-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c5bb4-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c5bb4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5bb4-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c5bb4-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
