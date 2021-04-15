---
description: Создает пустую текстуру, настраивая параметры вызова по мере необходимости.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: Функция D3DXCreateTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547914"
---
# <a name="d3dxcreatetexture-function"></a><span data-ttu-id="38c7e-103">Функция D3DXCreateTexture</span><span class="sxs-lookup"><span data-stu-id="38c7e-103">D3DXCreateTexture function</span></span>

<span data-ttu-id="38c7e-104">Создает пустую текстуру, настраивая параметры вызова по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="38c7e-104">Creates an empty texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="38c7e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38c7e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="38c7e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38c7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38c7e-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38c7e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c7e-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="38c7e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="38c7e-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="38c7e-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="38c7e-110">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38c7e-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c7e-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38c7e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38c7e-112">Ширина в пикселях.</span><span class="sxs-lookup"><span data-stu-id="38c7e-112">Width in pixels.</span></span> <span data-ttu-id="38c7e-113">Если это значение равно 0, то используется значение 1.</span><span class="sxs-lookup"><span data-stu-id="38c7e-113">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="38c7e-114">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="38c7e-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="38c7e-115">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38c7e-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c7e-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38c7e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38c7e-117">Высота в пикселях.</span><span class="sxs-lookup"><span data-stu-id="38c7e-117">Height in pixels.</span></span> <span data-ttu-id="38c7e-118">Если это значение равно 0, то используется значение 1.</span><span class="sxs-lookup"><span data-stu-id="38c7e-118">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="38c7e-119">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="38c7e-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="38c7e-120">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38c7e-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c7e-121">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38c7e-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38c7e-122">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="38c7e-122">Number of mip levels requested.</span></span> <span data-ttu-id="38c7e-123">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="38c7e-123">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="38c7e-124">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38c7e-124">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c7e-125">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38c7e-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38c7e-126">0, [**D3DUSAGE \_ Рендертаржет**](d3dusage.md)или **D3DUSAGE \_ dynamic**.</span><span class="sxs-lookup"><span data-stu-id="38c7e-126">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="38c7e-127">Установка этого флага в значение **D3DUSAGE \_ рендертаржет** указывает, что поверхность должна использоваться в качестве целевого объекта отрисовки путем вызова метода [**сетрендертаржет**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="38c7e-127">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target by calling the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="38c7e-128">Если указано значение **D3DUSAGE \_ Рендертаржет** или **D3DUSAGE \_ dynamic** , приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="38c7e-128">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="38c7e-129">Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="38c7e-129">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="38c7e-130">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38c7e-130">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c7e-131">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="38c7e-131">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="38c7e-132">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры.</span><span class="sxs-lookup"><span data-stu-id="38c7e-132">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="38c7e-133">Возвращаемая текстура может иметь другой формат из указанного, если устройство не поддерживает запрошенный формат.</span><span class="sxs-lookup"><span data-stu-id="38c7e-133">The returned texture may be of a different format from that specified, if the device does not support the requested format.</span></span> <span data-ttu-id="38c7e-134">Приложения должны проверить формат возвращенной текстуры, чтобы узнать, соответствует ли он требуемому формату.</span><span class="sxs-lookup"><span data-stu-id="38c7e-134">Applications should check the format of the returned texture to see if it matches the format requested.</span></span>

</dd> <dt>

<span data-ttu-id="38c7e-135">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38c7e-135">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c7e-136">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="38c7e-136">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="38c7e-137">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.</span><span class="sxs-lookup"><span data-stu-id="38c7e-137">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="38c7e-138">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="38c7e-138">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38c7e-139">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="38c7e-139">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="38c7e-140">Адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="38c7e-140">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38c7e-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38c7e-141">Return value</span></span>

<span data-ttu-id="38c7e-142">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38c7e-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38c7e-143">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="38c7e-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="38c7e-144">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE, D3DERR \_ аутофвидеомемори, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="38c7e-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="38c7e-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38c7e-145">Remarks</span></span>

<span data-ttu-id="38c7e-146">На внутреннем уровне D3DXCreateTexture использует [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) для настройки параметров вызова.</span><span class="sxs-lookup"><span data-stu-id="38c7e-146">Internally, D3DXCreateTexture uses [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="38c7e-147">Таким образом, вызовы D3DXCreateTexture часто завершаются успешно, когда вызовы [**креатетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) завершатся сбоем.</span><span class="sxs-lookup"><span data-stu-id="38c7e-147">Therefore, calls to D3DXCreateTexture will often succeed where calls to [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) would fail.</span></span>

<span data-ttu-id="38c7e-148">Если для высоты и ширины задано значение [D3DX \_ по умолчанию](other-d3dx-constants.md), для обоих параметров будет использоваться 256.</span><span class="sxs-lookup"><span data-stu-id="38c7e-148">If both Height and Width are set to [D3DX\_DEFAULT](other-d3dx-constants.md), a value of 256 is used for both parameters.</span></span> <span data-ttu-id="38c7e-149">Если для высоты или ширины задано значение D3DX \_ по умолчанию, а для другого параметра задано числовое значение, то текстура будет квадратной и высотой и шириной, равной числу значений.</span><span class="sxs-lookup"><span data-stu-id="38c7e-149">If either Height or Width is set to D3DX\_DEFAULT And the other parameter is set to a numeric value, the texture will be square with both the height and width equal to the numeric value.</span></span>

## <a name="requirements"></a><span data-ttu-id="38c7e-150">Требования</span><span class="sxs-lookup"><span data-stu-id="38c7e-150">Requirements</span></span>



| <span data-ttu-id="38c7e-151">Требование</span><span class="sxs-lookup"><span data-stu-id="38c7e-151">Requirement</span></span> | <span data-ttu-id="38c7e-152">Значение</span><span class="sxs-lookup"><span data-stu-id="38c7e-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38c7e-153">Header</span><span class="sxs-lookup"><span data-stu-id="38c7e-153">Header</span></span><br/>  | <dl> <span data-ttu-id="38c7e-154"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="38c7e-154"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="38c7e-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="38c7e-155">Library</span></span><br/> | <dl> <span data-ttu-id="38c7e-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38c7e-156"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="38c7e-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38c7e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38c7e-158">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="38c7e-158">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
