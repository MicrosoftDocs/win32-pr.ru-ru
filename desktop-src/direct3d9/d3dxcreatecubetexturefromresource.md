---
description: Создает текстуру куба из ресурса.
ms.assetid: 9153944a-af8b-4365-9e91-fc1136a84caa
title: Функция D3DXCreateCubeTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c0bd65799bada2df8a3c9e0b113db3c911a53536
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720908"
---
# <a name="d3dxcreatecubetexturefromresource-function"></a><span data-ttu-id="fcae1-103">Функция D3DXCreateCubeTextureFromResource</span><span class="sxs-lookup"><span data-stu-id="fcae1-103">D3DXCreateCubeTextureFromResource function</span></span>

<span data-ttu-id="fcae1-104">Создает текстуру куба из ресурса.</span><span class="sxs-lookup"><span data-stu-id="fcae1-104">Creates a cube texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcae1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcae1-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="fcae1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fcae1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcae1-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fcae1-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcae1-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="fcae1-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="fcae1-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой Куба.</span><span class="sxs-lookup"><span data-stu-id="fcae1-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="fcae1-110">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fcae1-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcae1-111">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcae1-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcae1-112">Указатель на модуль, в котором находится ресурс, или **значение NULL** для модуля, связанного с образом, операционной системой, используемой для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="fcae1-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="fcae1-113">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fcae1-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcae1-114">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcae1-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcae1-115">Указатель на строку, указывающую имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="fcae1-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="fcae1-116">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="fcae1-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="fcae1-117">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="fcae1-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="fcae1-118">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="fcae1-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fcae1-119">*ппкубетекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fcae1-119">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcae1-120">Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="fcae1-120">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="fcae1-121">Адрес указателя на интерфейс [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий созданный объект текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="fcae1-121">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcae1-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fcae1-122">Return value</span></span>

<span data-ttu-id="fcae1-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fcae1-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fcae1-124">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fcae1-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fcae1-125">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE, D3DERR \_ аутофвидеомемори, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fcae1-125">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcae1-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fcae1-126">Remarks</span></span>

<span data-ttu-id="fcae1-127">Параметр компилятора определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="fcae1-127">The compiler setting determines the function version.</span></span> <span data-ttu-id="fcae1-128">Если определен Юникод, вызов функции разрешается в **D3DXCreateCubeTextureFromResourceW**.</span><span class="sxs-lookup"><span data-stu-id="fcae1-128">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceW**.</span></span> <span data-ttu-id="fcae1-129">В противном случае вызов функции разрешается в **D3DXCreateCubeTextureFromResourceA** , так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="fcae1-129">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceA** because ANSI strings are being used.</span></span>

<span data-ttu-id="fcae1-130">Функция эквивалентна D3DXCreateCubeTextureFromResourceEx (Пдевице, Хсркмодуле, Псркресаурце, D3DX \_ Default, D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, **null**, **null**, ппкубетекстуре).</span><span class="sxs-lookup"><span data-stu-id="fcae1-130">The function is equivalent to D3DXCreateCubeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="fcae1-131">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="fcae1-131">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="fcae1-132">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="fcae1-132">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="fcae1-133">Обратите внимание, что ресурс, созданный с помощью этой функции при вызове из объекта IDirect3DDevice9, будет помещен в класс Memory, обозначенный D3DPOOL \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="fcae1-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="fcae1-134">При вызове этого метода из объекта IDirect3DDevice9Ex ресурс будет помещен в класс Memory, обозначенный параметром D3DPOOL \_ Default.</span><span class="sxs-lookup"><span data-stu-id="fcae1-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="fcae1-135">Фильтрация автоматически применяется к текстуре, созданной с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="fcae1-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="fcae1-136">Фильтрация эквивалентна D3DX фильтра \_ D3DX Filter \_ \| \_ \_ в [ \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="fcae1-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="fcae1-137">**D3DXCreateCubeTextureFromResource** использует формат файла поверхности DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="fcae1-137">**D3DXCreateCubeTextureFromResource** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="fcae1-138">Редактор текстур DirectX (Dxtex.exe) позволяет создать карту Куба на основе других форматов файлов и сохранить ее в формате файлов DDS.</span><span class="sxs-lookup"><span data-stu-id="fcae1-138">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="fcae1-139">Вы можете получить Dxtex.exe и узнать о нем из пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="fcae1-139">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="fcae1-140">Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="fcae1-140">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcae1-141">Требования</span><span class="sxs-lookup"><span data-stu-id="fcae1-141">Requirements</span></span>



| <span data-ttu-id="fcae1-142">Требование</span><span class="sxs-lookup"><span data-stu-id="fcae1-142">Requirement</span></span> | <span data-ttu-id="fcae1-143">Значение</span><span class="sxs-lookup"><span data-stu-id="fcae1-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcae1-144">Header</span><span class="sxs-lookup"><span data-stu-id="fcae1-144">Header</span></span><br/>  | <dl> <span data-ttu-id="fcae1-145"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcae1-145"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fcae1-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fcae1-146">Library</span></span><br/> | <dl> <span data-ttu-id="fcae1-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcae1-147"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fcae1-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcae1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcae1-149">**D3DXCreateCubeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="fcae1-149">**D3DXCreateCubeTextureFromResourceEx**</span></span>](d3dxcreatecubetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="fcae1-150">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="fcae1-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
