---
description: Инициирует рисование каждой грани схемы среды.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'Метод ID3DXRenderToEnvMap:: Face (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 452933c0d85a7aad2987011796ff47eff41dc32b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821484"
---
# <a name="id3dxrendertoenvmapface-method"></a><span data-ttu-id="fde32-103">Метод ID3DXRenderToEnvMap:: Face</span><span class="sxs-lookup"><span data-stu-id="fde32-103">ID3DXRenderToEnvMap::Face method</span></span>

<span data-ttu-id="fde32-104">Инициирует рисование каждой грани схемы среды.</span><span class="sxs-lookup"><span data-stu-id="fde32-104">Initiate the drawing of each face of an environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde32-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fde32-105">Syntax</span></span>


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="fde32-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fde32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde32-107">*Лицо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fde32-107">*Face* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde32-108">Тип: **[ **D3DCUBEMAP \_ лиц**](./d3dcubemap-faces.md)**</span><span class="sxs-lookup"><span data-stu-id="fde32-108">Type: **[**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md)**</span></span>

<span data-ttu-id="fde32-109">Первое лицо из схемы куба среды.</span><span class="sxs-lookup"><span data-stu-id="fde32-109">The first face of the environmental cube map.</span></span> <span data-ttu-id="fde32-110">См [**. \_ раздел D3DCUBEMAP**](./d3dcubemap-faces.md)Face.</span><span class="sxs-lookup"><span data-stu-id="fde32-110">See [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md).</span></span>

</dd> <dt>

<span data-ttu-id="fde32-111">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fde32-111">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde32-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fde32-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fde32-113">Допустимое сочетание одного или нескольких флагов [ \_ фильтра D3DX](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="fde32-113">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde32-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fde32-114">Return value</span></span>

<span data-ttu-id="fde32-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fde32-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fde32-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fde32-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fde32-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="fde32-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fde32-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fde32-118">Remarks</span></span>

<span data-ttu-id="fde32-119">Этот метод должен вызываться один раз для каждого типа схемы среды.</span><span class="sxs-lookup"><span data-stu-id="fde32-119">This method must be called once for each type of environment map.</span></span> <span data-ttu-id="fde32-120">Единственным исключением является схема среды кубического типа, которая требует, чтобы этот метод вызывался шесть раз, один раз для каждого из граней в D3DCUBEMAP Face \_ .</span><span class="sxs-lookup"><span data-stu-id="fde32-120">The only exception is a cubic environment map which requires this method to be called six times, once for each face in D3DCUBEMAP\_FACES.</span></span> <span data-ttu-id="fde32-121">Дополнительные сведения см. в разделе [сопоставление среды (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="fde32-121">For more information, see [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fde32-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fde32-122">Requirements</span></span>



| <span data-ttu-id="fde32-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fde32-123">Requirement</span></span> | <span data-ttu-id="fde32-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fde32-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fde32-125">Header</span><span class="sxs-lookup"><span data-stu-id="fde32-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fde32-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde32-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="fde32-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fde32-127">Library</span></span><br/> | <dl> <span data-ttu-id="fde32-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fde32-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fde32-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fde32-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde32-130">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="fde32-130">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
