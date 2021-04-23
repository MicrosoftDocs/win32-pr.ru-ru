---
description: Задает свойства материала сетки в трехмерной сцене. Используйте этот метод, чтобы указать параметры геоточечной подповерхности.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'Метод ID3DXPRTEngine:: Сетмешматериалс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355683"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a><span data-ttu-id="41a11-104">Метод ID3DXPRTEngine:: Сетмешматериалс</span><span class="sxs-lookup"><span data-stu-id="41a11-104">ID3DXPRTEngine::SetMeshMaterials method</span></span>

<span data-ttu-id="41a11-105">Задает свойства материала сетки в трехмерной сцене.</span><span class="sxs-lookup"><span data-stu-id="41a11-105">Sets mesh material properties in the 3D scene.</span></span> <span data-ttu-id="41a11-106">Используйте этот метод, чтобы указать параметры геоточечной подповерхности.</span><span class="sxs-lookup"><span data-stu-id="41a11-106">Use this method to specify subsurface scattering parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="41a11-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41a11-107">Syntax</span></span>


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a><span data-ttu-id="41a11-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="41a11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41a11-109">*ппматериалс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41a11-109">*ppMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41a11-110">Тип: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="41a11-110">Type: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md)\*\***</span></span>

<span data-ttu-id="41a11-111">Адрес указателя на требуемые свойства материала сетки.</span><span class="sxs-lookup"><span data-stu-id="41a11-111">Address of a pointer to desired mesh material properties.</span></span> <span data-ttu-id="41a11-112">См. [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span><span class="sxs-lookup"><span data-stu-id="41a11-112">See [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="41a11-113">*Нуммешес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41a11-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41a11-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41a11-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41a11-115">Индекс сетки, для которой задаются свойства материала.</span><span class="sxs-lookup"><span data-stu-id="41a11-115">Index of the mesh on which to set material properties.</span></span>

</dd> <dt>

<span data-ttu-id="41a11-116">*Нумчаннелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41a11-116">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41a11-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41a11-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41a11-118">Число цветовых каналов, устанавливаемых в сетке.</span><span class="sxs-lookup"><span data-stu-id="41a11-118">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="41a11-119">Задайте значение 1, чтобы указать серые материалы (R = G = B), или 3, чтобы включить эффекты цвета суперсовременные.</span><span class="sxs-lookup"><span data-stu-id="41a11-119">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span> <span data-ttu-id="41a11-120">Если вы собираетесь изменить этот параметр, сначала установите албедо с помощью другого метода, такого как [**ID3DXPRTEngine:: сетпертекселалбедо**](id3dxprtengine--setpertexelalbedo.md) или [**ID3DXPRTEngine:: сетпервертексалбедо**](id3dxprtengine--setpervertexalbedo.md).</span><span class="sxs-lookup"><span data-stu-id="41a11-120">If you intend to change this parameter, first set the albedo using another method such as [**ID3DXPRTEngine::SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) or [**ID3DXPRTEngine::SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).</span></span>

</dd> <dt>

<span data-ttu-id="41a11-121">*бсеталбедо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41a11-121">*bSetAlbedo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41a11-122">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41a11-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41a11-123">Если **значение — true**, задает для албедо сетки значение ппматериалс, перезаписывая все существующие значения шаг текселя и вершин албедо.</span><span class="sxs-lookup"><span data-stu-id="41a11-123">If **TRUE**, sets the albedo of the mesh to ppMaterials, overwriting all existing texel and vertex albedo values.</span></span> <span data-ttu-id="41a11-124">Если **значение равно false**, сохраняет все существующие значения шаг текселя и вершин албедо, заданные другими методами. Нумчаннелс должен соответствовать параметру Нумчаннелс, используемому для создания буфера в [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) или [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span><span class="sxs-lookup"><span data-stu-id="41a11-124">If **FALSE**, preserves all existing texel and vertex albedo values set by other methods; NumChannels must match the NumChannels parameter used to create the buffer in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span></span>

</dd> <dt>

<span data-ttu-id="41a11-125">*фленгсскале* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41a11-125">*fLengthScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41a11-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41a11-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41a11-127">Масштаб трехмерной сцены относительно Куба 1 мм.</span><span class="sxs-lookup"><span data-stu-id="41a11-127">Scale of the 3D scene relative to a 1-mm cube.</span></span> <span data-ttu-id="41a11-128">Используется для вычислений с разбросами подповерхности.</span><span class="sxs-lookup"><span data-stu-id="41a11-128">Used for subsurface scattering computations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41a11-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41a11-129">Return value</span></span>

<span data-ttu-id="41a11-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41a11-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41a11-131">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="41a11-131">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="41a11-132">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="41a11-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="41a11-133">Требования</span><span class="sxs-lookup"><span data-stu-id="41a11-133">Requirements</span></span>



| <span data-ttu-id="41a11-134">Требование</span><span class="sxs-lookup"><span data-stu-id="41a11-134">Requirement</span></span> | <span data-ttu-id="41a11-135">Значение</span><span class="sxs-lookup"><span data-stu-id="41a11-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41a11-136">Header</span><span class="sxs-lookup"><span data-stu-id="41a11-136">Header</span></span><br/>  | <dl> <span data-ttu-id="41a11-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="41a11-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="41a11-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="41a11-138">Library</span></span><br/> | <dl> <span data-ttu-id="41a11-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41a11-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41a11-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41a11-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a11-141">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="41a11-141">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
