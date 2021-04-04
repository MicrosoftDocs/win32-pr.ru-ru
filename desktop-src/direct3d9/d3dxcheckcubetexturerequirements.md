---
description: Проверяет параметры создания текстуры.
ms.assetid: 56ced947-1142-4d05-95e3-ca6a26b147d4
title: Функция D3DXCheckCubeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckCubeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f800617920c5d79361b5e6da291fd88b5b963b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821492"
---
# <a name="d3dxcheckcubetexturerequirements-function"></a><span data-ttu-id="1afa7-103">Функция D3DXCheckCubeTextureRequirements</span><span class="sxs-lookup"><span data-stu-id="1afa7-103">D3DXCheckCubeTextureRequirements function</span></span>

<span data-ttu-id="1afa7-104">Проверяет параметры создания текстуры.</span><span class="sxs-lookup"><span data-stu-id="1afa7-104">Checks cube-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="1afa7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1afa7-105">Syntax</span></span>


```C++
HRESULT D3DXCheckCubeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pSize,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="1afa7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1afa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1afa7-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1afa7-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1afa7-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1afa7-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1afa7-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой Куба.</span><span class="sxs-lookup"><span data-stu-id="1afa7-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="1afa7-110">*псизе* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1afa7-110">*pSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1afa7-111">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1afa7-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1afa7-112">Указатель на запрошенную ширину и высоту в пикселях или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1afa7-112">Pointer to the requested width and height in pixels, or **NULL**.</span></span> <span data-ttu-id="1afa7-113">Возвращает исправленный размер.</span><span class="sxs-lookup"><span data-stu-id="1afa7-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="1afa7-114">*пнуммиплевелс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1afa7-114">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1afa7-115">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1afa7-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1afa7-116">Указатель на число запрошенных mipmap уровней или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1afa7-116">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="1afa7-117">Возвращает исправленное число уровней mipmap.</span><span class="sxs-lookup"><span data-stu-id="1afa7-117">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="1afa7-118">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1afa7-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1afa7-119">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1afa7-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1afa7-120">0 или D3DUSAGE \_ рендертаржет.</span><span class="sxs-lookup"><span data-stu-id="1afa7-120">0 or D3DUSAGE\_RENDERTARGET.</span></span> <span data-ttu-id="1afa7-121">Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="1afa7-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="1afa7-122">Затем ресурс можно передать в параметр Пневрендертаржет метода [**сетрендертаржет**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="1afa7-122">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="1afa7-123">Если указан параметр D3DUSAGE \_ рендертаржет, приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span><span class="sxs-lookup"><span data-stu-id="1afa7-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="1afa7-124">*пформат* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1afa7-124">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1afa7-125">Тип: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="1afa7-125">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="1afa7-126">Указатель на член перечисляемого типа [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="1afa7-126">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="1afa7-127">Указывает требуемый формат пикселей или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1afa7-127">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="1afa7-128">Возвращает исправленный формат.</span><span class="sxs-lookup"><span data-stu-id="1afa7-128">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="1afa7-129">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1afa7-129">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1afa7-130">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="1afa7-130">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="1afa7-131">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.</span><span class="sxs-lookup"><span data-stu-id="1afa7-131">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1afa7-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1afa7-132">Return value</span></span>

<span data-ttu-id="1afa7-133">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1afa7-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1afa7-134">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1afa7-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1afa7-135">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="1afa7-135">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1afa7-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1afa7-136">Remarks</span></span>

<span data-ttu-id="1afa7-137">Если параметры для этой функции недопустимы, эта функция возвращает исправленные параметры.</span><span class="sxs-lookup"><span data-stu-id="1afa7-137">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="1afa7-138">Текстуры Куба отличаются от других поверхностей тем, что они являются коллекциями поверхностей.</span><span class="sxs-lookup"><span data-stu-id="1afa7-138">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="1afa7-139">Чтобы вызвать [**сетрендертаржет**](/windows/desktop/api) с текстурой Куба, необходимо выбрать отдельное лицо с помощью [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) и передать полученную область в **сетрендертаржет**.</span><span class="sxs-lookup"><span data-stu-id="1afa7-139">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1afa7-140">Требования</span><span class="sxs-lookup"><span data-stu-id="1afa7-140">Requirements</span></span>



| <span data-ttu-id="1afa7-141">Требование</span><span class="sxs-lookup"><span data-stu-id="1afa7-141">Requirement</span></span> | <span data-ttu-id="1afa7-142">Значение</span><span class="sxs-lookup"><span data-stu-id="1afa7-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1afa7-143">Header</span><span class="sxs-lookup"><span data-stu-id="1afa7-143">Header</span></span><br/>  | <dl> <span data-ttu-id="1afa7-144"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1afa7-144"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1afa7-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1afa7-145">Library</span></span><br/> | <dl> <span data-ttu-id="1afa7-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1afa7-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1afa7-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1afa7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1afa7-148">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="1afa7-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
