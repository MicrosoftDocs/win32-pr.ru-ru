---
description: Инициация отрисовки схемы кубической среды.
ms.assetid: 0f02b2e2-8132-4994-ab07-c79a1b7821dd
title: 'Метод ID3DXRenderToEnvMap:: Бегинкубе (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginCube
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bff6c8f3bdc49dfe0c1b677c6805cb332c05007d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354573"
---
# <a name="id3dxrendertoenvmapbegincube-method"></a><span data-ttu-id="a8bcd-103">Метод ID3DXRenderToEnvMap:: Бегинкубе</span><span class="sxs-lookup"><span data-stu-id="a8bcd-103">ID3DXRenderToEnvMap::BeginCube method</span></span>

<span data-ttu-id="a8bcd-104">Инициация отрисовки схемы кубической среды.</span><span class="sxs-lookup"><span data-stu-id="a8bcd-104">Initiate the rendering of a cubic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8bcd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8bcd-105">Syntax</span></span>


```C++
HRESULT BeginCube(
  [in] LPDIRECT3DCUBETEXTURE9 pCubeTex
);
```



## <a name="parameters"></a><span data-ttu-id="a8bcd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8bcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8bcd-107">*пкубетекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8bcd-107">*pCubeTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bcd-108">Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="a8bcd-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="a8bcd-109">Указатель на интерфейс [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий текстуру Куба, для которой необходимо выполнить рендеринг.</span><span class="sxs-lookup"><span data-stu-id="a8bcd-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface that represents the cube texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8bcd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8bcd-110">Return value</span></span>

<span data-ttu-id="a8bcd-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8bcd-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8bcd-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a8bcd-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a8bcd-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="a8bcd-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8bcd-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8bcd-114">Remarks</span></span>

<span data-ttu-id="a8bcd-115">Рисование каждого из шести Сторон см. в разделе [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .</span><span class="sxs-lookup"><span data-stu-id="a8bcd-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw each of the 6 faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8bcd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a8bcd-116">Requirements</span></span>



| <span data-ttu-id="a8bcd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a8bcd-117">Requirement</span></span> | <span data-ttu-id="a8bcd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bcd-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bcd-119">Header</span><span class="sxs-lookup"><span data-stu-id="a8bcd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a8bcd-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8bcd-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a8bcd-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a8bcd-121">Library</span></span><br/> | <dl> <span data-ttu-id="a8bcd-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8bcd-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8bcd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8bcd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bcd-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="a8bcd-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="a8bcd-125">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="a8bcd-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
