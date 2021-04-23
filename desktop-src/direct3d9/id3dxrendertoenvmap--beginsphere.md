---
description: Инициация отрисовки сферической схемы среды.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'Метод ID3DXRenderToEnvMap:: Бегинсфере (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 872aa06734ae818ef248b03fbc14dcd1c33fe815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354570"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a><span data-ttu-id="fc6a9-103">Метод ID3DXRenderToEnvMap:: Бегинсфере</span><span class="sxs-lookup"><span data-stu-id="fc6a9-103">ID3DXRenderToEnvMap::BeginSphere method</span></span>

<span data-ttu-id="fc6a9-104">Инициация отрисовки сферической схемы среды.</span><span class="sxs-lookup"><span data-stu-id="fc6a9-104">Initiate the rendering of a spherical environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc6a9-105">Syntax</span></span>


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a><span data-ttu-id="fc6a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc6a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc6a9-107">*птекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc6a9-107">*pTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc6a9-108">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="fc6a9-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="fc6a9-109">Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру, для которой необходимо выполнить рендеринг.</span><span class="sxs-lookup"><span data-stu-id="fc6a9-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc6a9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc6a9-110">Return value</span></span>

<span data-ttu-id="fc6a9-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc6a9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc6a9-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fc6a9-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fc6a9-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл. \_Ошибка E</span><span class="sxs-lookup"><span data-stu-id="fc6a9-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="fc6a9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc6a9-114">Remarks</span></span>

<span data-ttu-id="fc6a9-115">Чтобы нарисовать грань, см. раздел [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .</span><span class="sxs-lookup"><span data-stu-id="fc6a9-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc6a9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fc6a9-116">Requirements</span></span>



| <span data-ttu-id="fc6a9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fc6a9-117">Requirement</span></span> | <span data-ttu-id="fc6a9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fc6a9-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc6a9-119">Header</span><span class="sxs-lookup"><span data-stu-id="fc6a9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fc6a9-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc6a9-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="fc6a9-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fc6a9-121">Library</span></span><br/> | <dl> <span data-ttu-id="fc6a9-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc6a9-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc6a9-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc6a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc6a9-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="fc6a9-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="fc6a9-125">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="fc6a9-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
