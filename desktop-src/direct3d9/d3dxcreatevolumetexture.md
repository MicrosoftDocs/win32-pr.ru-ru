---
description: Создает пустую текстуру тома, настраивая параметры вызова по мере необходимости.
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: Функция D3DXCreateVolumeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50baf125d2e5375bddb63a41a0d10ae063a57b78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000367"
---
# <a name="d3dxcreatevolumetexture-function"></a><span data-ttu-id="ff55e-103">Функция D3DXCreateVolumeTexture</span><span class="sxs-lookup"><span data-stu-id="ff55e-103">D3DXCreateVolumeTexture function</span></span>

<span data-ttu-id="ff55e-104">Создает пустую текстуру тома, настраивая параметры вызова по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="ff55e-104">Creates an empty volume texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff55e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff55e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ff55e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff55e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff55e-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff55e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff55e-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ff55e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ff55e-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой тома.</span><span class="sxs-lookup"><span data-stu-id="ff55e-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="ff55e-110">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff55e-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff55e-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff55e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff55e-112">Ширина в пикселях.</span><span class="sxs-lookup"><span data-stu-id="ff55e-112">Width in pixels.</span></span> <span data-ttu-id="ff55e-113">Это значение должно быть ненулевым.</span><span class="sxs-lookup"><span data-stu-id="ff55e-113">This value must be nonzero.</span></span> <span data-ttu-id="ff55e-114">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ff55e-114">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ff55e-115">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff55e-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff55e-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff55e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff55e-117">Высота в пикселях.</span><span class="sxs-lookup"><span data-stu-id="ff55e-117">Height in pixels.</span></span> <span data-ttu-id="ff55e-118">Это значение должно быть ненулевым.</span><span class="sxs-lookup"><span data-stu-id="ff55e-118">This value must be nonzero.</span></span> <span data-ttu-id="ff55e-119">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ff55e-119">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ff55e-120">*Глубина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff55e-120">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff55e-121">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff55e-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff55e-122">Глубина в пикселях.</span><span class="sxs-lookup"><span data-stu-id="ff55e-122">Depth in pixels.</span></span> <span data-ttu-id="ff55e-123">Это значение должно быть ненулевым.</span><span class="sxs-lookup"><span data-stu-id="ff55e-123">This value must be nonzero.</span></span> <span data-ttu-id="ff55e-124">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ff55e-124">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ff55e-125">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff55e-125">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff55e-126">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff55e-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff55e-127">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="ff55e-127">Number of mip levels requested.</span></span> <span data-ttu-id="ff55e-128">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="ff55e-128">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="ff55e-129">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff55e-129">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff55e-130">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff55e-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff55e-131">0 или D3DUSAGE \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="ff55e-131">0 or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="ff55e-132">Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="ff55e-132">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff55e-133">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff55e-133">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff55e-134">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ff55e-134">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ff55e-135">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="ff55e-135">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the volume texture.</span></span> <span data-ttu-id="ff55e-136">Возвращаемая текстура тома может иметь другой формат, заданный в формате.</span><span class="sxs-lookup"><span data-stu-id="ff55e-136">The returned volume texture might have a different format from that specified by Format.</span></span> <span data-ttu-id="ff55e-137">Приложения должны проверить формат полученной текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="ff55e-137">Applications should check the format of the returned volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="ff55e-138">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff55e-138">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff55e-139">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ff55e-139">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="ff55e-140">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура тома.</span><span class="sxs-lookup"><span data-stu-id="ff55e-140">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="ff55e-141">*ппволуметекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ff55e-141">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff55e-142">Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ff55e-142">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="ff55e-143">Адрес указателя на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий созданный объект текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="ff55e-143">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created volume texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff55e-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff55e-144">Return value</span></span>

<span data-ttu-id="ff55e-145">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ff55e-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ff55e-146">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ff55e-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ff55e-147">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ff55e-147">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY .</span></span>

## <a name="remarks"></a><span data-ttu-id="ff55e-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff55e-148">Remarks</span></span>

<span data-ttu-id="ff55e-149">На внутреннем уровне D3DXCreateVolumeTexture использует [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) для настройки параметров вызова.</span><span class="sxs-lookup"><span data-stu-id="ff55e-149">Internally, D3DXCreateVolumeTexture uses [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="ff55e-150">Таким образом, вызовы D3DXCreateVolumeTexture часто завершаются успешно, когда вызовы [**креатеволуметекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) завершатся сбоем.</span><span class="sxs-lookup"><span data-stu-id="ff55e-150">Therefore, calls to D3DXCreateVolumeTexture will often succeed where calls to [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff55e-151">Требования</span><span class="sxs-lookup"><span data-stu-id="ff55e-151">Requirements</span></span>



| <span data-ttu-id="ff55e-152">Требование</span><span class="sxs-lookup"><span data-stu-id="ff55e-152">Requirement</span></span> | <span data-ttu-id="ff55e-153">Значение</span><span class="sxs-lookup"><span data-stu-id="ff55e-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff55e-154">Header</span><span class="sxs-lookup"><span data-stu-id="ff55e-154">Header</span></span><br/>  | <dl> <span data-ttu-id="ff55e-155"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff55e-155"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ff55e-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ff55e-156">Library</span></span><br/> | <dl> <span data-ttu-id="ff55e-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff55e-157"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ff55e-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff55e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff55e-159">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ff55e-159">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
