---
description: Создает область прорисовки.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: Функция D3DXCreateRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fc64cbc65d30838db2105e0458d3553247f1ab1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713697"
---
# <a name="d3dxcreaterendertosurface-function"></a><span data-ttu-id="a7f28-103">Функция D3DXCreateRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="a7f28-103">D3DXCreateRenderToSurface function</span></span>

<span data-ttu-id="a7f28-104">Создает область прорисовки.</span><span class="sxs-lookup"><span data-stu-id="a7f28-104">Creates a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f28-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7f28-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## <a name="parameters"></a><span data-ttu-id="a7f28-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7f28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7f28-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7f28-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f28-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a7f28-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a7f28-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , устройство, которое должно быть связано с областью прорисовки.</span><span class="sxs-lookup"><span data-stu-id="a7f28-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="a7f28-110">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7f28-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f28-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7f28-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7f28-112">Ширина поверхности рендеринга в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a7f28-112">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a7f28-113">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7f28-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f28-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7f28-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7f28-115">Высота поверхности рендеринга (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="a7f28-115">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a7f28-116">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7f28-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f28-117">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="a7f28-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="a7f28-118">Элемент перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат пикселей поверхности рендеринга.</span><span class="sxs-lookup"><span data-stu-id="a7f28-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="a7f28-119">*ДепсстенЦил* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7f28-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f28-120">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7f28-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7f28-121">Если **значение — true**, поверхность рендеринга поддерживает поверхность набора элементов глубины.</span><span class="sxs-lookup"><span data-stu-id="a7f28-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="a7f28-122">В противном случае этому члену присваивается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a7f28-122">Otherwise, this member is set to **FALSE**.</span></span> <span data-ttu-id="a7f28-123">Эта функция создаст новый буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="a7f28-123">This function will create a new depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a7f28-124">*ДепсстенЦилформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7f28-124">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f28-125">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="a7f28-125">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="a7f28-126">Если *депсстенЦил* имеет значение **true**, этот параметр является членом перечислимого типа [D3DFORMAT](d3dformat.md) , описывающим формат трафарета глубины области рендеринга.</span><span class="sxs-lookup"><span data-stu-id="a7f28-126">If *DepthStencil* is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="a7f28-127">*ппрендертосурфаце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a7f28-127">*ppRenderToSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f28-128">Тип: **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7f28-128">Type: **[**LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span></span>

<span data-ttu-id="a7f28-129">Адрес указателя на интерфейс [**ID3DXRenderToSurface**](id3dxrendertosurface.md) , представляющий созданную область отрисовки.</span><span class="sxs-lookup"><span data-stu-id="a7f28-129">Address of a pointer to an [**ID3DXRenderToSurface**](id3dxrendertosurface.md) interface, representing the created render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7f28-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7f28-130">Return value</span></span>

<span data-ttu-id="a7f28-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7f28-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7f28-132">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a7f28-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a7f28-133">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a7f28-133">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f28-134">Требования</span><span class="sxs-lookup"><span data-stu-id="a7f28-134">Requirements</span></span>



| <span data-ttu-id="a7f28-135">Требование</span><span class="sxs-lookup"><span data-stu-id="a7f28-135">Requirement</span></span> | <span data-ttu-id="a7f28-136">Значение</span><span class="sxs-lookup"><span data-stu-id="a7f28-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f28-137">Header</span><span class="sxs-lookup"><span data-stu-id="a7f28-137">Header</span></span><br/>  | <dl> <span data-ttu-id="a7f28-138"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7f28-138"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a7f28-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7f28-139">Library</span></span><br/> | <dl> <span data-ttu-id="a7f28-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7f28-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a7f28-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7f28-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f28-142">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="a7f28-142">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
