---
description: Преобразует карту высоты в обычную карту. Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: Функция D3DXComputeNormalMap (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e22418f5a023dbe70fee8ea0fba8a449abbcc8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713881"
---
# <a name="d3dxcomputenormalmap-function"></a><span data-ttu-id="65fed-104">Функция D3DXComputeNormalMap</span><span class="sxs-lookup"><span data-stu-id="65fed-104">D3DXComputeNormalMap function</span></span>

<span data-ttu-id="65fed-105">Преобразует карту высоты в обычную карту.</span><span class="sxs-lookup"><span data-stu-id="65fed-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="65fed-106">Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.</span><span class="sxs-lookup"><span data-stu-id="65fed-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="65fed-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65fed-107">Syntax</span></span>


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a><span data-ttu-id="65fed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="65fed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65fed-109">*птекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="65fed-109">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65fed-110">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="65fed-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="65fed-111">Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру назначения.</span><span class="sxs-lookup"><span data-stu-id="65fed-111">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="65fed-112">*псрктекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65fed-112">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65fed-113">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="65fed-113">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="65fed-114">Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру исходной карты с высотой.</span><span class="sxs-lookup"><span data-stu-id="65fed-114">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="65fed-115">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65fed-115">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65fed-116">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="65fed-116">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="65fed-117">Указатель на тип [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , который содержит исходную палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="65fed-117">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) type that contains the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="65fed-118">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65fed-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65fed-119">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65fed-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65fed-120">Один или несколько флагов [ \_ нормалмап D3DX](d3dx-normalmap.md) , управляющих созданием обычных карт.</span><span class="sxs-lookup"><span data-stu-id="65fed-120">One or more [D3DX\_NORMALMAP](d3dx-normalmap.md) flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="65fed-121">*Канал* \[ связи окне\]</span><span class="sxs-lookup"><span data-stu-id="65fed-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65fed-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65fed-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65fed-123">Один [флаг \_ канала D3DX](d3dx-channel.md) , указывающий источник сведений о высоте.</span><span class="sxs-lookup"><span data-stu-id="65fed-123">One [D3DX\_CHANNEL](d3dx-channel.md) flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="65fed-124">*Амплитуда* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65fed-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65fed-125">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65fed-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65fed-126">Коэффициент величины постоянного значения, увеличивающий (или уменьшающий) значения в нормальном сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="65fed-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="65fed-127">Более высокие значения обычно делают выпуклости более видимыми, а более низкие значения обычно делают невидимыми более выпуклости.</span><span class="sxs-lookup"><span data-stu-id="65fed-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65fed-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65fed-128">Return value</span></span>

<span data-ttu-id="65fed-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65fed-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65fed-130">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="65fed-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="65fed-131">Если функция завершается ошибкой, возвращаемое значение может иметь следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="65fed-131">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="65fed-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65fed-132">Remarks</span></span>

<span data-ttu-id="65fed-133">Этот метод рассчитывает нормальную работу, используя Центральное различие с размером ядра 3X3.</span><span class="sxs-lookup"><span data-stu-id="65fed-133">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="65fed-134">В качестве центрального знаменателя разницы используется 2,0.</span><span class="sxs-lookup"><span data-stu-id="65fed-134">The central differencing denominator used is 2.0.</span></span> <span data-ttu-id="65fed-135">Каналы RGB в назначении содержат смещенные компоненты (x, y, z) нормали.</span><span class="sxs-lookup"><span data-stu-id="65fed-135">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="65fed-136">Требования</span><span class="sxs-lookup"><span data-stu-id="65fed-136">Requirements</span></span>



| <span data-ttu-id="65fed-137">Требование</span><span class="sxs-lookup"><span data-stu-id="65fed-137">Requirement</span></span> | <span data-ttu-id="65fed-138">Значение</span><span class="sxs-lookup"><span data-stu-id="65fed-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65fed-139">Header</span><span class="sxs-lookup"><span data-stu-id="65fed-139">Header</span></span><br/>  | <dl> <span data-ttu-id="65fed-140"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="65fed-140"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="65fed-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="65fed-141">Library</span></span><br/> | <dl> <span data-ttu-id="65fed-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65fed-142"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="65fed-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65fed-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65fed-144">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="65fed-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
