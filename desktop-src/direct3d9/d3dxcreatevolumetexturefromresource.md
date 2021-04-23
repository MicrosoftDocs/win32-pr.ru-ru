---
description: Создает текстуру тома из ресурса.
ms.assetid: 82a0b7aa-69fa-450d-b0d2-769f05fd75ea
title: Функция D3DXCreateVolumeTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5f0a0faf97f773c3174ced22ec7259091d6e07e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547903"
---
# <a name="d3dxcreatevolumetexturefromresource-function"></a><span data-ttu-id="0ef0e-103">Функция D3DXCreateVolumeTextureFromResource</span><span class="sxs-lookup"><span data-stu-id="0ef0e-103">D3DXCreateVolumeTextureFromResource function</span></span>

<span data-ttu-id="0ef0e-104">Создает текстуру тома из ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-104">Creates a volume texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef0e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ef0e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="0ef0e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ef0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef0e-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ef0e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef0e-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0ef0e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0ef0e-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой тома.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="0ef0e-110">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ef0e-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef0e-111">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef0e-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ef0e-112">Указатель на модуль, в котором находится ресурс, или **значение NULL** для модуля, связанного с образом, операционной системой, используемой для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="0ef0e-113">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ef0e-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef0e-114">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef0e-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ef0e-115">Указатель на строку, указывающую имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="0ef0e-116">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0ef0e-117">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="0ef0e-118">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0ef0e-119">*ппволуметекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0ef0e-119">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef0e-120">Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="0ef0e-120">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="0ef0e-121">Адрес указателя на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-121">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef0e-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ef0e-122">Return value</span></span>

<span data-ttu-id="0ef0e-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ef0e-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ef0e-124">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0ef0e-125">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef0e-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ef0e-126">Remarks</span></span>

<span data-ttu-id="0ef0e-127">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0ef0e-128">Если определен Юникод, вызов функции разрешается в D3DXCreateVolumeTextureFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-128">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceW.</span></span> <span data-ttu-id="0ef0e-129">В противном случае вызов функции разрешается в D3DXCreateVolumeTextureFromResourceA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-129">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="0ef0e-130">Функция эквивалентна D3DXCreateVolumeTextureFromResourceEx (Пдевице, Хсркмодуле, Псркресаурце, D3DX \_ Default, D3DX \_ по умолчанию, D3DX \_ Default, D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, **null**, **null**, ппволуметекстуре).</span><span class="sxs-lookup"><span data-stu-id="0ef0e-130">The function is equivalent to D3DXCreateVolumeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="0ef0e-131">Загружаемый ресурс должен быть ресурсом, определяемым приложением (RT \_ RCDATA).</span><span class="sxs-lookup"><span data-stu-id="0ef0e-131">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="0ef0e-132">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-132">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="0ef0e-133">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="0ef0e-133">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="0ef0e-134">Обратите внимание, что ресурс, созданный с помощью этой функции при вызове из объекта IDirect3DDevice9, будет помещен в класс Memory, обозначенный D3DPOOL \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-134">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="0ef0e-135">При вызове этого метода из объекта IDirect3DDevice9Ex ресурс будет помещен в класс Memory, обозначенный параметром D3DPOOL \_ Default.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-135">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="0ef0e-136">Фильтрация автоматически применяется к текстуре, созданной с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-136">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="0ef0e-137">Фильтрация эквивалентна D3DX фильтра \_ D3DX Filter \_ \| \_ \_ в [ \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="0ef0e-137">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef0e-138">Требования</span><span class="sxs-lookup"><span data-stu-id="0ef0e-138">Requirements</span></span>



| <span data-ttu-id="0ef0e-139">Требование</span><span class="sxs-lookup"><span data-stu-id="0ef0e-139">Requirement</span></span> | <span data-ttu-id="0ef0e-140">Значение</span><span class="sxs-lookup"><span data-stu-id="0ef0e-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef0e-141">Header</span><span class="sxs-lookup"><span data-stu-id="0ef0e-141">Header</span></span><br/>  | <dl> <span data-ttu-id="0ef0e-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef0e-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0ef0e-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ef0e-143">Library</span></span><br/> | <dl> <span data-ttu-id="0ef0e-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ef0e-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0ef0e-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ef0e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef0e-146">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="0ef0e-146">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="0ef0e-147">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="0ef0e-147">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="0ef0e-148">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="0ef0e-148">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="0ef0e-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="0ef0e-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="0ef0e-150">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="0ef0e-150">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="0ef0e-151">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0ef0e-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
