---
description: Начинает сцену.
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: 'Метод ID3DXRenderToSurface:: Бегинсцене (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5aa2229e88123cc1d52f65f1edf032c46f819229
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647885"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a><span data-ttu-id="d7ae9-103">Метод ID3DXRenderToSurface:: Бегинсцене</span><span class="sxs-lookup"><span data-stu-id="d7ae9-103">ID3DXRenderToSurface::BeginScene method</span></span>

<span data-ttu-id="d7ae9-104">Начинает сцену.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-104">Begins a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ae9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7ae9-105">Syntax</span></span>


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a><span data-ttu-id="d7ae9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7ae9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ae9-107">*псурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7ae9-107">*pSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ae9-108">Тип: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="d7ae9-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="d7ae9-109">Указатель на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , представляющий поверхность рендеринга.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="d7ae9-110">*пвиевпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7ae9-110">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ae9-111">Тип: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="d7ae9-111">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="d7ae9-112">Указатель на структуру [**D3DVIEWPORT9**](d3dviewport9.md) , описывающий окно просмотра для сцены.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-112">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, describing the viewport for the scene.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ae9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7ae9-113">Return value</span></span>

<span data-ttu-id="d7ae9-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d7ae9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d7ae9-115">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d7ae9-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл. D3DERR \_ АУТОФВИДЕОМЕМОРИ D3DXERR \_ INVALIDDATA E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d7ae9-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.D3DERR\_OUTOFVIDEOMEMORY D3DXERR\_INVALIDDATA E\_OUTOFMEMORY</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ae9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d7ae9-117">Requirements</span></span>



| <span data-ttu-id="d7ae9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d7ae9-118">Requirement</span></span> | <span data-ttu-id="d7ae9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d7ae9-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ae9-120">Header</span><span class="sxs-lookup"><span data-stu-id="d7ae9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d7ae9-121"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ae9-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d7ae9-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d7ae9-122">Library</span></span><br/> | <dl> <span data-ttu-id="d7ae9-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7ae9-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d7ae9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7ae9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ae9-125">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="d7ae9-125">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="d7ae9-126">**ID3DXRenderToSurface:: Ендсцене**</span><span class="sxs-lookup"><span data-stu-id="d7ae9-126">**ID3DXRenderToSurface::EndScene**</span></span>](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 
