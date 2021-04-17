---
description: Создает пустую текстуру Куба и настраивает вызывающие параметры по мере необходимости.
ms.assetid: 96cf3fc1-9efc-4b97-a082-2956386145c7
title: Функция D3DXCreateCubeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fa31945cea5e65cdf00eae512059308090bcbab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720974"
---
# <a name="d3dxcreatecubetexture-function"></a><span data-ttu-id="d6838-103">Функция D3DXCreateCubeTexture</span><span class="sxs-lookup"><span data-stu-id="d6838-103">D3DXCreateCubeTexture function</span></span>

<span data-ttu-id="d6838-104">Создает пустую текстуру Куба и настраивает вызывающие параметры по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="d6838-104">Creates an empty cube texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6838-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6838-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTexture(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="d6838-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6838-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6838-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6838-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6838-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d6838-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d6838-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="d6838-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="d6838-110">*Размер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6838-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6838-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6838-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6838-112">Ширина и высота текстуры Куба в пикселях.</span><span class="sxs-lookup"><span data-stu-id="d6838-112">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="d6838-113">Например, если текстура Куба является 8-пиксельным кубом, значение этого параметра должно быть равно 8.</span><span class="sxs-lookup"><span data-stu-id="d6838-113">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span>

</dd> <dt>

<span data-ttu-id="d6838-114">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6838-114">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6838-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6838-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6838-116">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="d6838-116">Number of mip levels requested.</span></span> <span data-ttu-id="d6838-117">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="d6838-117">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="d6838-118">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6838-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6838-119">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6838-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6838-120">0, D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="d6838-120">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="d6838-121">Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="d6838-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="d6838-122">Затем ресурс можно передать в параметр *пневрендертаржет* метода [**сетрендертаржет**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="d6838-122">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="d6838-123">Если указан параметр D3DUSAGE \_ рендертаржет, приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="d6838-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="d6838-124">Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="d6838-124">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6838-125">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6838-125">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6838-126">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="d6838-126">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="d6838-127">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="d6838-127">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="d6838-128">Возвращаемая текстура Куба может иметь другой формат, заданный в *формате*.</span><span class="sxs-lookup"><span data-stu-id="d6838-128">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="d6838-129">Приложения должны проверять формат полученной текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="d6838-129">Applications should check the format of the returned cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="d6838-130">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6838-130">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6838-131">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="d6838-131">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="d6838-132">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура Куба.</span><span class="sxs-lookup"><span data-stu-id="d6838-132">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="d6838-133">*ппкубетекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d6838-133">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6838-134">Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="d6838-134">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="d6838-135">Адрес указателя на интерфейс [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий созданный объект текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="d6838-135">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6838-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6838-136">Return value</span></span>

<span data-ttu-id="d6838-137">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d6838-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d6838-138">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d6838-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d6838-139">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE, D3DERR \_ аутофвидеомемори, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d6838-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6838-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6838-140">Remarks</span></span>

<span data-ttu-id="d6838-141">Текстуры Куба отличаются от других поверхностей тем, что они являются коллекциями поверхностей.</span><span class="sxs-lookup"><span data-stu-id="d6838-141">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span>

<span data-ttu-id="d6838-142">На внутреннем уровне D3DXCreateCubeTexture использует [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) для настройки параметров вызова.</span><span class="sxs-lookup"><span data-stu-id="d6838-142">Internally, D3DXCreateCubeTexture uses [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="d6838-143">Таким образом, вызовы D3DXCreateCubeTexture часто завершаются успешно, когда вызовы [**креатекубетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) завершатся сбоем.</span><span class="sxs-lookup"><span data-stu-id="d6838-143">Therefore, calls to D3DXCreateCubeTexture will often succeed where calls to [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6838-144">Требования</span><span class="sxs-lookup"><span data-stu-id="d6838-144">Requirements</span></span>



| <span data-ttu-id="d6838-145">Требование</span><span class="sxs-lookup"><span data-stu-id="d6838-145">Requirement</span></span> | <span data-ttu-id="d6838-146">Значение</span><span class="sxs-lookup"><span data-stu-id="d6838-146">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6838-147">Header</span><span class="sxs-lookup"><span data-stu-id="d6838-147">Header</span></span><br/>  | <dl> <span data-ttu-id="d6838-148"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6838-148"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d6838-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d6838-149">Library</span></span><br/> | <dl> <span data-ttu-id="d6838-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6838-150"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d6838-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6838-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6838-152">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="d6838-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
