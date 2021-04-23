---
description: Задает значение албедо для каждого шаг текселя, перезаписывая предыдущие значения албедо.
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: 'Метод ID3DXPRTEngine:: Сетпертекселалбедо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce977a1ab28477ab8e40d59d18cfbcc55f558f88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424434"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a><span data-ttu-id="beb5c-103">Метод ID3DXPRTEngine:: Сетпертекселалбедо</span><span class="sxs-lookup"><span data-stu-id="beb5c-103">ID3DXPRTEngine::SetPerTexelAlbedo method</span></span>

<span data-ttu-id="beb5c-104">Задает значение албедо для каждого шаг текселя, перезаписывая предыдущие значения албедо.</span><span class="sxs-lookup"><span data-stu-id="beb5c-104">Sets an albedo value for each texel, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb5c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="beb5c-105">Syntax</span></span>


```C++
HRESULT SetPerTexelAlbedo(
  [in] LPDIRECT3DTEXTURE9        pAlbedoTexture,
  [in] UINT                      NumChannels,
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="beb5c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="beb5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb5c-107">*палбедотекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="beb5c-107">*pAlbedoTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb5c-108">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="beb5c-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="beb5c-109">Указатель на объект текстуры [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , в котором хранятся значения албедо.</span><span class="sxs-lookup"><span data-stu-id="beb5c-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object in which to store albedo values.</span></span>

</dd> <dt>

<span data-ttu-id="beb5c-110">*Нумчаннелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="beb5c-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb5c-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="beb5c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="beb5c-112">Число устанавливаемых цветовых каналов.</span><span class="sxs-lookup"><span data-stu-id="beb5c-112">Number of color channels to set.</span></span> <span data-ttu-id="beb5c-113">Задайте значение 1, чтобы указать серые материалы (R = G = B), или 3, чтобы включить эффекты цвета суперсовременные.</span><span class="sxs-lookup"><span data-stu-id="beb5c-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="beb5c-114">*ПГХ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="beb5c-114">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb5c-115">Тип: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="beb5c-115">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="beb5c-116">Необязательный указатель на объект [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="beb5c-116">Optional pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object.</span></span> <span data-ttu-id="beb5c-117">Если не указано, вспомогательный объект переплета текстуры создается и уничтожается внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="beb5c-117">If not provided, a texture gutter helper object is created and destroyed internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb5c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="beb5c-118">Return value</span></span>

<span data-ttu-id="beb5c-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="beb5c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="beb5c-120">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="beb5c-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="beb5c-121">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLED3DERR \_ аутофвидеомемори, D3DERR \_ васстиллдравинг, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="beb5c-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLED3DERR\_OUTOFVIDEOMEMORY, D3DERR\_WASSTILLDRAWING, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="beb5c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="beb5c-122">Requirements</span></span>



| <span data-ttu-id="beb5c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="beb5c-123">Requirement</span></span> | <span data-ttu-id="beb5c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="beb5c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="beb5c-125">Header</span><span class="sxs-lookup"><span data-stu-id="beb5c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="beb5c-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb5c-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="beb5c-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="beb5c-127">Library</span></span><br/> | <dl> <span data-ttu-id="beb5c-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="beb5c-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="beb5c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="beb5c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb5c-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="beb5c-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
