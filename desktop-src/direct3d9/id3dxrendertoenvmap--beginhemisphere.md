---
description: Инициация отрисовки схемы среды хемисферик.
ms.assetid: 1150aad9-dd8c-4943-afaf-90794faaaf70
title: 'Метод ID3DXRenderToEnvMap:: Бегинхемисфере (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginHemisphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96eb4bbf4cfc6cac952368337456b946f64cf711
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273749"
---
# <a name="id3dxrendertoenvmapbeginhemisphere-method"></a><span data-ttu-id="a7ca3-103">Метод ID3DXRenderToEnvMap:: Бегинхемисфере</span><span class="sxs-lookup"><span data-stu-id="a7ca3-103">ID3DXRenderToEnvMap::BeginHemisphere method</span></span>

<span data-ttu-id="a7ca3-104">Инициация отрисовки схемы среды хемисферик.</span><span class="sxs-lookup"><span data-stu-id="a7ca3-104">Initiate the rendering of a hemispheric environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7ca3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7ca3-105">Syntax</span></span>


```C++
HRESULT BeginHemisphere(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="a7ca3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7ca3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7ca3-107">*птексзпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7ca3-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ca3-108">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="a7ca3-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="a7ca3-109">Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий поверхность прорисовки положительной текстуры.</span><span class="sxs-lookup"><span data-stu-id="a7ca3-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive texture render surface.</span></span>

</dd> <dt>

<span data-ttu-id="a7ca3-110">*птексзнег* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7ca3-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ca3-111">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="a7ca3-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="a7ca3-112">Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий поверхность прорисовки отрицательной текстуры.</span><span class="sxs-lookup"><span data-stu-id="a7ca3-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative texture render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7ca3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7ca3-113">Return value</span></span>

<span data-ttu-id="a7ca3-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7ca3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7ca3-115">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a7ca3-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a7ca3-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл. \_Ошибка E</span><span class="sxs-lookup"><span data-stu-id="a7ca3-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="a7ca3-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7ca3-117">Remarks</span></span>

<span data-ttu-id="a7ca3-118">Чтобы нарисовать грань, см. раздел [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .</span><span class="sxs-lookup"><span data-stu-id="a7ca3-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7ca3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a7ca3-119">Requirements</span></span>



| <span data-ttu-id="a7ca3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a7ca3-120">Requirement</span></span> | <span data-ttu-id="a7ca3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a7ca3-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ca3-122">Header</span><span class="sxs-lookup"><span data-stu-id="a7ca3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a7ca3-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7ca3-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a7ca3-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7ca3-124">Library</span></span><br/> | <dl> <span data-ttu-id="a7ca3-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7ca3-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a7ca3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7ca3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ca3-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="a7ca3-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="a7ca3-128">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="a7ca3-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
