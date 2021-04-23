---
description: Задает логическое значение.
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
ms.openlocfilehash: 49fbc2d2841957e75a8bc3adaf40ce0fdf5e2a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821357"
---
# <a name="id3dxtextureshadersetbool-method"></a><span data-ttu-id="5b34b-103">Метод ID3DXTextureShader:: Сетбул</span><span class="sxs-lookup"><span data-stu-id="5b34b-103">ID3DXTextureShader::SetBool method</span></span>

<span data-ttu-id="5b34b-104">Задает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="5b34b-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b34b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b34b-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="5b34b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b34b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b34b-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b34b-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b34b-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5b34b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5b34b-109">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="5b34b-109">Unique identifier to the constant.</span></span> <span data-ttu-id="5b34b-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="5b34b-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b34b-111">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="5b34b-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b34b-112">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b34b-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b34b-113">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="5b34b-113">BOOL value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b34b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b34b-114">Return value</span></span>

<span data-ttu-id="5b34b-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b34b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b34b-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5b34b-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5b34b-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="5b34b-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b34b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5b34b-118">Requirements</span></span>



| <span data-ttu-id="5b34b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5b34b-119">Requirement</span></span> | <span data-ttu-id="5b34b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5b34b-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b34b-121">Header</span><span class="sxs-lookup"><span data-stu-id="5b34b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5b34b-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b34b-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5b34b-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5b34b-123">Library</span></span><br/> | <dl> <span data-ttu-id="5b34b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b34b-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5b34b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b34b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b34b-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="5b34b-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
