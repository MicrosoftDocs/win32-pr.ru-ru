---
description: Создает карту среды отрисовки.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: Функция D3DXCreateRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081864"
---
# <a name="d3dxcreaterendertoenvmap-function"></a><span data-ttu-id="ad7c1-103">Функция D3DXCreateRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="ad7c1-103">D3DXCreateRenderToEnvMap function</span></span>

<span data-ttu-id="ad7c1-104">Создает карту среды отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ad7c1-104">Creates a render environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad7c1-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a><span data-ttu-id="ad7c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad7c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad7c1-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad7c1-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7c1-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ad7c1-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ad7c1-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , который является устройством, связываемым с областью прорисовки.</span><span class="sxs-lookup"><span data-stu-id="ad7c1-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, which is the device to associate with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="ad7c1-110">*Размер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad7c1-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7c1-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad7c1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad7c1-112">Размер области прорисовки.</span><span class="sxs-lookup"><span data-stu-id="ad7c1-112">Size of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="ad7c1-113">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad7c1-113">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7c1-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad7c1-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad7c1-115">Число уровней mipmap.</span><span class="sxs-lookup"><span data-stu-id="ad7c1-115">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="ad7c1-116">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad7c1-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7c1-117">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ad7c1-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ad7c1-118">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат пикселей для схемы среды.</span><span class="sxs-lookup"><span data-stu-id="ad7c1-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the pixel format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="ad7c1-119">*ДепсстенЦил* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad7c1-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7c1-120">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad7c1-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad7c1-121">Если **значение — true**, поверхность рендеринга поддерживает поверхность набора элементов глубины.</span><span class="sxs-lookup"><span data-stu-id="ad7c1-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="ad7c1-122">В противном случае этому члену присваивается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ad7c1-122">Otherwise, this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ad7c1-123">*ДепсстенЦилформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad7c1-123">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7c1-124">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ad7c1-124">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ad7c1-125">Если ДепсстенЦил имеет значение **true**, этот параметр является членом перечислимого типа [D3DFORMAT](d3dformat.md) , который описывает формат шаблона глубины для схемы среды.</span><span class="sxs-lookup"><span data-stu-id="ad7c1-125">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the depth-stencil format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="ad7c1-126">*ппрендертоенвмап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ad7c1-126">*ppRenderToEnvMap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7c1-127">Тип: **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad7c1-127">Type: **[**LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span></span>

<span data-ttu-id="ad7c1-128">Адрес указателя на интерфейс [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) , представляющий созданную карту среды отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ad7c1-128">Address of a pointer to an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) interface that represents the created render environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad7c1-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad7c1-129">Return value</span></span>

<span data-ttu-id="ad7c1-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad7c1-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad7c1-131">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ad7c1-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ad7c1-132">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ad7c1-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad7c1-133">Требования</span><span class="sxs-lookup"><span data-stu-id="ad7c1-133">Requirements</span></span>



| <span data-ttu-id="ad7c1-134">Требование</span><span class="sxs-lookup"><span data-stu-id="ad7c1-134">Requirement</span></span> | <span data-ttu-id="ad7c1-135">Значение</span><span class="sxs-lookup"><span data-stu-id="ad7c1-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7c1-136">Header</span><span class="sxs-lookup"><span data-stu-id="ad7c1-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ad7c1-137"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad7c1-137"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ad7c1-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ad7c1-138">Library</span></span><br/> | <dl> <span data-ttu-id="ad7c1-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad7c1-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad7c1-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad7c1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7c1-141">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="ad7c1-141">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
