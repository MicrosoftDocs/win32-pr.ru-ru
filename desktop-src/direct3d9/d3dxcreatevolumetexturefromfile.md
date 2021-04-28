---
description: Функция D3DXCreateVolumeTextureFromFile — создает текстуру тома из файла.
ms.assetid: e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d
title: Функция D3DXCreateVolumeTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c9355148c0b91a03aabe863fb20b3e312e30784
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094309"
---
# <a name="d3dxcreatevolumetexturefromfile-function"></a><span data-ttu-id="7080b-103">Функция D3DXCreateVolumeTextureFromFile</span><span class="sxs-lookup"><span data-stu-id="7080b-103">D3DXCreateVolumeTextureFromFile function</span></span>

<span data-ttu-id="7080b-104">Создает текстуру тома из файла.</span><span class="sxs-lookup"><span data-stu-id="7080b-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7080b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7080b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="7080b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7080b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7080b-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7080b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7080b-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7080b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7080b-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой тома.</span><span class="sxs-lookup"><span data-stu-id="7080b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="7080b-110">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7080b-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7080b-111">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7080b-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7080b-112">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="7080b-112">Pointer to a string that specifies the file name.</span></span> <span data-ttu-id="7080b-113">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="7080b-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="7080b-114">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="7080b-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="7080b-115">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="7080b-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7080b-116">*ппволуметекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7080b-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7080b-117">Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="7080b-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="7080b-118">Адрес указателя на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="7080b-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7080b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7080b-119">Return value</span></span>

<span data-ttu-id="7080b-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7080b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7080b-121">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7080b-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7080b-122">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7080b-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7080b-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="7080b-123">Remarks</span></span>

<span data-ttu-id="7080b-124">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="7080b-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="7080b-125">Если определен Юникод, вызов функции разрешается в D3DXCreateVolumeTextureFromFileW.</span><span class="sxs-lookup"><span data-stu-id="7080b-125">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileW.</span></span> <span data-ttu-id="7080b-126">В противном случае вызов функции разрешается в D3DXCreateVolumeTextureFromFileA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="7080b-126">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="7080b-127">Функция эквивалентна D3DXCreateVolumeTextureFromFileEx (Пдевице, Псркфиле, D3DX \_ Default, D3DX по \_ умолчанию, D3DX по умолчанию, \_ D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, **null**, **null**, ппволуметекстуре).</span><span class="sxs-lookup"><span data-stu-id="7080b-127">The function is equivalent to D3DXCreateVolumeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="7080b-128">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="7080b-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="7080b-129">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="7080b-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="7080b-130">Текстуры мипмаппед автоматически имеют каждый уровень, заполненный загруженной текстурой.</span><span class="sxs-lookup"><span data-stu-id="7080b-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="7080b-131">При загрузке изображений в текстуры мипмаппед некоторые устройства не могут подключиться к образу 1x1, и эта функция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7080b-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="7080b-132">Если это происходит, образы необходимо загружать вручную.</span><span class="sxs-lookup"><span data-stu-id="7080b-132">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="7080b-133">Обратите внимание, что ресурс, созданный с помощью этой функции при вызове из объекта IDirect3DDevice9, будет помещен в класс Memory, обозначенный D3DPOOL \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="7080b-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="7080b-134">При вызове этого метода из объекта IDirect3DDevice9Ex ресурс будет помещен в класс Memory, обозначенный параметром D3DPOOL \_ Default.</span><span class="sxs-lookup"><span data-stu-id="7080b-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="7080b-135">Фильтрация автоматически применяется к текстуре, созданной с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="7080b-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="7080b-136">Фильтрация эквивалентна D3DX фильтра \_ D3DX Filter \_ \| \_ \_ в [ \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7080b-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7080b-137">Требования</span><span class="sxs-lookup"><span data-stu-id="7080b-137">Requirements</span></span>



| <span data-ttu-id="7080b-138">Требование</span><span class="sxs-lookup"><span data-stu-id="7080b-138">Requirement</span></span> | <span data-ttu-id="7080b-139">Значение</span><span class="sxs-lookup"><span data-stu-id="7080b-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7080b-140">Header</span><span class="sxs-lookup"><span data-stu-id="7080b-140">Header</span></span><br/>  | <dl> <span data-ttu-id="7080b-141"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="7080b-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="7080b-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7080b-142">Library</span></span><br/> | <dl> <span data-ttu-id="7080b-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7080b-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7080b-144">См. также</span><span class="sxs-lookup"><span data-stu-id="7080b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7080b-145">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="7080b-145">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="7080b-146">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="7080b-146">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="7080b-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="7080b-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="7080b-148">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="7080b-148">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="7080b-149">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="7080b-149">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="7080b-150">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="7080b-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
