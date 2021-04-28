---
description: Функция D3DXComputeNormalMap — преобразует карту высоты в обычную карту. Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.
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
ms.openlocfilehash: 920ad763f478a2e6bcb9fbe98cc7e2a677ebe783
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105232"
---
# <a name="d3dxcomputenormalmap-function"></a><span data-ttu-id="b98cb-104">Функция D3DXComputeNormalMap</span><span class="sxs-lookup"><span data-stu-id="b98cb-104">D3DXComputeNormalMap function</span></span>

<span data-ttu-id="b98cb-105">Преобразует карту высоты в обычную карту.</span><span class="sxs-lookup"><span data-stu-id="b98cb-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="b98cb-106">Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.</span><span class="sxs-lookup"><span data-stu-id="b98cb-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b98cb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b98cb-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b98cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b98cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b98cb-109">*птекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b98cb-109">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b98cb-110">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="b98cb-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="b98cb-111">Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру назначения.</span><span class="sxs-lookup"><span data-stu-id="b98cb-111">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="b98cb-112">*псрктекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b98cb-112">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b98cb-113">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="b98cb-113">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="b98cb-114">Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру исходной карты с высотой.</span><span class="sxs-lookup"><span data-stu-id="b98cb-114">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="b98cb-115">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b98cb-115">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b98cb-116">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="b98cb-116">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="b98cb-117">Указатель на тип [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , который содержит исходную палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b98cb-117">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) type that contains the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b98cb-118">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b98cb-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b98cb-119">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b98cb-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b98cb-120">Один или несколько флагов [ \_ нормалмап D3DX](d3dx-normalmap.md) , управляющих созданием обычных карт.</span><span class="sxs-lookup"><span data-stu-id="b98cb-120">One or more [D3DX\_NORMALMAP](d3dx-normalmap.md) flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="b98cb-121">*Канал* \[ связи окне\]</span><span class="sxs-lookup"><span data-stu-id="b98cb-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b98cb-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b98cb-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b98cb-123">Один [флаг \_ канала D3DX](d3dx-channel.md) , указывающий источник сведений о высоте.</span><span class="sxs-lookup"><span data-stu-id="b98cb-123">One [D3DX\_CHANNEL](d3dx-channel.md) flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="b98cb-124">*Амплитуда* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b98cb-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b98cb-125">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b98cb-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b98cb-126">Коэффициент величины постоянного значения, увеличивающий (или уменьшающий) значения в нормальном сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="b98cb-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="b98cb-127">Более высокие значения обычно делают выпуклости более видимыми, а более низкие значения обычно делают невидимыми более выпуклости.</span><span class="sxs-lookup"><span data-stu-id="b98cb-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b98cb-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b98cb-128">Return value</span></span>

<span data-ttu-id="b98cb-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b98cb-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b98cb-130">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b98cb-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b98cb-131">Если функция завершается ошибкой, возвращаемое значение может иметь следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="b98cb-131">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b98cb-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="b98cb-132">Remarks</span></span>

<span data-ttu-id="b98cb-133">Этот метод рассчитывает нормальную работу, используя Центральное различие с размером ядра 3X3.</span><span class="sxs-lookup"><span data-stu-id="b98cb-133">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="b98cb-134">В качестве центрального знаменателя разницы используется 2,0.</span><span class="sxs-lookup"><span data-stu-id="b98cb-134">The central differencing denominator used is 2.0.</span></span> <span data-ttu-id="b98cb-135">Каналы RGB в назначении содержат смещенные компоненты (x, y, z) нормали.</span><span class="sxs-lookup"><span data-stu-id="b98cb-135">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="b98cb-136">Требования</span><span class="sxs-lookup"><span data-stu-id="b98cb-136">Requirements</span></span>



| <span data-ttu-id="b98cb-137">Требование</span><span class="sxs-lookup"><span data-stu-id="b98cb-137">Requirement</span></span> | <span data-ttu-id="b98cb-138">Значение</span><span class="sxs-lookup"><span data-stu-id="b98cb-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b98cb-139">Header</span><span class="sxs-lookup"><span data-stu-id="b98cb-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b98cb-140"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b98cb-140"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b98cb-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b98cb-141">Library</span></span><br/> | <dl> <span data-ttu-id="b98cb-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b98cb-142"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b98cb-143">См. также</span><span class="sxs-lookup"><span data-stu-id="b98cb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b98cb-144">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b98cb-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
