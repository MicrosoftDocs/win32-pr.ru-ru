---
description: Задает текстуру.
ms.assetid: edf5bf61-508a-4417-bdf8-c36e6ba7ab30
title: 'Метод ID3DXBaseEffect:: Сеттекстуре (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 398dcc2f3d61ad32c08b67735a9ec7ed1a192acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720859"
---
# <a name="id3dxbaseeffectsettexture-method"></a><span data-ttu-id="cc7c7-103">Метод ID3DXBaseEffect:: Сеттекстуре</span><span class="sxs-lookup"><span data-stu-id="cc7c7-103">ID3DXBaseEffect::SetTexture method</span></span>

<span data-ttu-id="cc7c7-104">Задает текстуру.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-104">Sets a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc7c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc7c7-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] D3DXHANDLE             hParameter,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="cc7c7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc7c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc7c7-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc7c7-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc7c7-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="cc7c7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="cc7c7-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-109">Unique identifier.</span></span> <span data-ttu-id="cc7c7-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="cc7c7-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc7c7-111">*птекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc7c7-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc7c7-112">Тип: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="cc7c7-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="cc7c7-113">Объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-113">Texture object.</span></span> <span data-ttu-id="cc7c7-114">См. [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="cc7c7-114">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc7c7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc7c7-115">Return value</span></span>

<span data-ttu-id="cc7c7-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc7c7-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc7c7-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cc7c7-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="cc7c7-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc7c7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="cc7c7-119">Requirements</span></span>



| <span data-ttu-id="cc7c7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="cc7c7-120">Requirement</span></span> | <span data-ttu-id="cc7c7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="cc7c7-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc7c7-122">Header</span><span class="sxs-lookup"><span data-stu-id="cc7c7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cc7c7-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc7c7-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cc7c7-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc7c7-124">Library</span></span><br/> | <dl> <span data-ttu-id="cc7c7-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc7c7-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cc7c7-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc7c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc7c7-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="cc7c7-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="cc7c7-128">**Текстурирование**</span><span class="sxs-lookup"><span data-stu-id="cc7c7-128">**GetTexture**</span></span>](id3dxbaseeffect--gettexture.md)
</dt> </dl>

 

 
