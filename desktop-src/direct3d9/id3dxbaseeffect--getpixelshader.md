---
description: Возвращает шейдер пикселей.
ms.assetid: 173a20a5-dda0-493f-a161-2dc2881e71f2
title: 'Метод ID3DXBaseEffect:: Жетпикселшадер (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e555bac2e20ebab1cb0aec3d313cab8ad05e833e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713991"
---
# <a name="id3dxbaseeffectgetpixelshader-method"></a><span data-ttu-id="f1f20-103">Метод ID3DXBaseEffect:: Жетпикселшадер</span><span class="sxs-lookup"><span data-stu-id="f1f20-103">ID3DXBaseEffect::GetPixelShader method</span></span>

<span data-ttu-id="f1f20-104">Возвращает шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="f1f20-104">Gets a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f20-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1f20-105">Syntax</span></span>


```C++
HRESULT GetPixelShader(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DPIXELSHADER9 *ppPShader
);
```



## <a name="parameters"></a><span data-ttu-id="f1f20-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1f20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1f20-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1f20-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f20-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f1f20-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f1f20-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="f1f20-109">Unique identifier.</span></span> <span data-ttu-id="f1f20-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f1f20-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1f20-111">*пппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1f20-111">*ppPShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f20-112">Тип: **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***</span><span class="sxs-lookup"><span data-stu-id="f1f20-112">Type: **[**LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***</span></span>

<span data-ttu-id="f1f20-113">Возвращает объект шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="f1f20-113">Returns a pixel shader object.</span></span> <span data-ttu-id="f1f20-114">См. раздел объект [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9) .</span><span class="sxs-lookup"><span data-stu-id="f1f20-114">See [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1f20-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1f20-115">Return value</span></span>

<span data-ttu-id="f1f20-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1f20-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1f20-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f1f20-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f1f20-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="f1f20-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1f20-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f1f20-119">Requirements</span></span>



| <span data-ttu-id="f1f20-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f1f20-120">Requirement</span></span> | <span data-ttu-id="f1f20-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f1f20-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f20-122">Header</span><span class="sxs-lookup"><span data-stu-id="f1f20-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f1f20-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1f20-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f1f20-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f1f20-124">Library</span></span><br/> | <dl> <span data-ttu-id="f1f20-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1f20-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f1f20-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1f20-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f20-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f1f20-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
