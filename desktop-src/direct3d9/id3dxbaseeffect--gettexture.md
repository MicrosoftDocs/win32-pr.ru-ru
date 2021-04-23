---
description: Возвращает текстуру.
ms.assetid: e009ccc2-4491-4976-9460-7478b2bd34c2
title: 'Метод ID3DXBaseEffect:: метода текстурирования (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 25ef71df1f9dcd84bbe6726fd3a13f9ec09eff17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820948"
---
# <a name="id3dxbaseeffectgettexture-method"></a><span data-ttu-id="98e44-103">Метод ID3DXBaseEffect:: метода текстурирования</span><span class="sxs-lookup"><span data-stu-id="98e44-103">ID3DXBaseEffect::GetTexture method</span></span>

<span data-ttu-id="98e44-104">Возвращает текстуру.</span><span class="sxs-lookup"><span data-stu-id="98e44-104">Gets a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e44-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98e44-105">Syntax</span></span>


```C++
HRESULT GetTexture(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DBASETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="98e44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="98e44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e44-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="98e44-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98e44-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="98e44-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="98e44-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="98e44-109">Unique identifier.</span></span> <span data-ttu-id="98e44-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="98e44-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e44-111">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="98e44-111">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98e44-112">Тип: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="98e44-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span></span>

<span data-ttu-id="98e44-113">Возвращает объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="98e44-113">Returns a texture object.</span></span> <span data-ttu-id="98e44-114">См. [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="98e44-114">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e44-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98e44-115">Return value</span></span>

<span data-ttu-id="98e44-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="98e44-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="98e44-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="98e44-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="98e44-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="98e44-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e44-119">Требования</span><span class="sxs-lookup"><span data-stu-id="98e44-119">Requirements</span></span>



| <span data-ttu-id="98e44-120">Требование</span><span class="sxs-lookup"><span data-stu-id="98e44-120">Requirement</span></span> | <span data-ttu-id="98e44-121">Значение</span><span class="sxs-lookup"><span data-stu-id="98e44-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e44-122">Header</span><span class="sxs-lookup"><span data-stu-id="98e44-122">Header</span></span><br/>  | <dl> <span data-ttu-id="98e44-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="98e44-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="98e44-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="98e44-124">Library</span></span><br/> | <dl> <span data-ttu-id="98e44-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98e44-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="98e44-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98e44-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e44-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="98e44-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="98e44-128">**сеттекстуре**</span><span class="sxs-lookup"><span data-stu-id="98e44-128">**SetTexture**</span></span>](id3dxbaseeffect--settexture.md)
</dt> </dl>

 

 
