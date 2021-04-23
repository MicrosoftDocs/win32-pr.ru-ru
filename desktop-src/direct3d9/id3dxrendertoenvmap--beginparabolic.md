---
description: Инициация отрисовки схемы среды параболическим.
ms.assetid: 80456084-f5f5-4dfe-805a-7eaaf7f7cb2a
title: 'Метод ID3DXRenderToEnvMap:: Бегинпараболик (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginParabolic
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a818abb424fa55bc01eca7ce9f64bc5629a7d50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081852"
---
# <a name="id3dxrendertoenvmapbeginparabolic-method"></a><span data-ttu-id="54a25-103">Метод ID3DXRenderToEnvMap:: Бегинпараболик</span><span class="sxs-lookup"><span data-stu-id="54a25-103">ID3DXRenderToEnvMap::BeginParabolic method</span></span>

<span data-ttu-id="54a25-104">Инициация отрисовки схемы среды параболическим.</span><span class="sxs-lookup"><span data-stu-id="54a25-104">Initiate the rendering of a parabolic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="54a25-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54a25-105">Syntax</span></span>


```C++
HRESULT BeginParabolic(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="54a25-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="54a25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54a25-107">*птексзпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54a25-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a25-108">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="54a25-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="54a25-109">Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий положительную текстуру рендеринга.</span><span class="sxs-lookup"><span data-stu-id="54a25-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive render texture.</span></span>

</dd> <dt>

<span data-ttu-id="54a25-110">*птексзнег* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54a25-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a25-111">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="54a25-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="54a25-112">Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру с отрицательным рендерингом.</span><span class="sxs-lookup"><span data-stu-id="54a25-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative render texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54a25-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54a25-113">Return value</span></span>

<span data-ttu-id="54a25-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54a25-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54a25-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="54a25-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="54a25-116">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл. \_Ошибка E</span><span class="sxs-lookup"><span data-stu-id="54a25-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="54a25-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54a25-117">Remarks</span></span>

<span data-ttu-id="54a25-118">Рисование граней см. в разделе [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .</span><span class="sxs-lookup"><span data-stu-id="54a25-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="54a25-119">Требования</span><span class="sxs-lookup"><span data-stu-id="54a25-119">Requirements</span></span>



| <span data-ttu-id="54a25-120">Требование</span><span class="sxs-lookup"><span data-stu-id="54a25-120">Requirement</span></span> | <span data-ttu-id="54a25-121">Значение</span><span class="sxs-lookup"><span data-stu-id="54a25-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54a25-122">Header</span><span class="sxs-lookup"><span data-stu-id="54a25-122">Header</span></span><br/>  | <dl> <span data-ttu-id="54a25-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="54a25-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="54a25-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="54a25-124">Library</span></span><br/> | <dl> <span data-ttu-id="54a25-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54a25-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54a25-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54a25-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a25-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="54a25-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="54a25-128">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="54a25-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
