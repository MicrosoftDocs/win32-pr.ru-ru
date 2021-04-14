---
description: Создает текстуру из файла.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: Функция D3DXCreateTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19453986405ee4d46a3e72145c2117bb113663bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424397"
---
# <a name="d3dxcreatetexturefromfile-function"></a><span data-ttu-id="369d8-103">Функция D3DXCreateTextureFromFile</span><span class="sxs-lookup"><span data-stu-id="369d8-103">D3DXCreateTextureFromFile function</span></span>

<span data-ttu-id="369d8-104">Создает текстуру из файла.</span><span class="sxs-lookup"><span data-stu-id="369d8-104">Creates a texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="369d8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="369d8-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="369d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="369d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="369d8-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="369d8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="369d8-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="369d8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="369d8-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="369d8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="369d8-110">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="369d8-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="369d8-111">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="369d8-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="369d8-112">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="369d8-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="369d8-113">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="369d8-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="369d8-114">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="369d8-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="369d8-115">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="369d8-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="369d8-116">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="369d8-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="369d8-117">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="369d8-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="369d8-118">Адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="369d8-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="369d8-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="369d8-119">Return value</span></span>

<span data-ttu-id="369d8-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="369d8-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="369d8-121">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="369d8-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="369d8-122">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="369d8-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="369d8-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="369d8-123">Remarks</span></span>

<span data-ttu-id="369d8-124">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="369d8-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="369d8-125">Если определен Юникод, вызов функции разрешается в D3DXCreateTextureFromFileW.</span><span class="sxs-lookup"><span data-stu-id="369d8-125">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileW.</span></span> <span data-ttu-id="369d8-126">В противном случае вызов функции разрешается в D3DXCreateTextureFromFileA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="369d8-126">Otherwise, the function call resolves to D3DXCreateTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="369d8-127">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="369d8-127">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="369d8-128">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="369d8-128">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="369d8-129">Функция эквивалентна D3DXCreateTextureFromFileEx (Пдевице, Псркфиле, D3DX \_ Default, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ управляемый, D3DX \_ Default, D3DX \_ по умолчанию, 0, **null**, **null**, пптекстуре).</span><span class="sxs-lookup"><span data-stu-id="369d8-129">The function is equivalent to D3DXCreateTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="369d8-130">Текстуры мипмаппед автоматически имеют каждый уровень, заполненный загруженной текстурой.</span><span class="sxs-lookup"><span data-stu-id="369d8-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="369d8-131">При загрузке изображений в текстуры мипмаппед некоторые устройства не могут подключиться к образу 1x1, и эта функция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="369d8-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="369d8-132">Если это происходит, образы необходимо загружать вручную.</span><span class="sxs-lookup"><span data-stu-id="369d8-132">If this happens, the images need to be loaded manually.</span></span>

<span data-ttu-id="369d8-133">Обратите внимание, что ресурс, созданный с помощью этой функции, будет помещен в класс Memory, обозначенный D3DPOOL \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="369d8-133">Note that a resource created with this function will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span>

<span data-ttu-id="369d8-134">Фильтрация автоматически применяется к текстуре, созданной с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="369d8-134">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="369d8-135">Фильтрация эквивалентна D3DX фильтра \_ D3DX Filter \_ \| \_ \_ в [ \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="369d8-135">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="369d8-136">Для лучшей производительности при использовании **D3DXCreateTextureFromFile**:</span><span class="sxs-lookup"><span data-stu-id="369d8-136">For the best performance when using **D3DXCreateTextureFromFile**:</span></span>

1.  <span data-ttu-id="369d8-137">Масштабирование изображения и преобразование формата во время загрузки могут выполняться слишком долго.</span><span class="sxs-lookup"><span data-stu-id="369d8-137">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="369d8-138">Храните изображения в формате и разрешении, которые они будут использовать.</span><span class="sxs-lookup"><span data-stu-id="369d8-138">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="369d8-139">Если целевому оборудованию требуется мощность двух измерений, создайте и сохраните образы с помощью возможностей двух измерений.</span><span class="sxs-lookup"><span data-stu-id="369d8-139">If the target hardware requires power of two dimensions, create and store images using power of two dimensions.</span></span>
2.  <span data-ttu-id="369d8-140">Рассмотрите возможность использования файлов поверхности DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="369d8-140">Consider using DirectDraw surface (DDS) files.</span></span> <span data-ttu-id="369d8-141">Так как файлы DDS могут использоваться для представления любого формата текстуры Direct3D 9, они очень просты в D3DX для чтения.</span><span class="sxs-lookup"><span data-stu-id="369d8-141">Because DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="369d8-142">Кроме того, они могут хранить MIP-карты, поэтому для создания образов можно использовать любые алгоритмы создания mipmap.</span><span class="sxs-lookup"><span data-stu-id="369d8-142">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

## <a name="requirements"></a><span data-ttu-id="369d8-143">Требования</span><span class="sxs-lookup"><span data-stu-id="369d8-143">Requirements</span></span>



| <span data-ttu-id="369d8-144">Требование</span><span class="sxs-lookup"><span data-stu-id="369d8-144">Requirement</span></span> | <span data-ttu-id="369d8-145">Значение</span><span class="sxs-lookup"><span data-stu-id="369d8-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="369d8-146">Header</span><span class="sxs-lookup"><span data-stu-id="369d8-146">Header</span></span><br/>  | <dl> <span data-ttu-id="369d8-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="369d8-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="369d8-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="369d8-148">Library</span></span><br/> | <dl> <span data-ttu-id="369d8-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="369d8-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="369d8-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="369d8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="369d8-151">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="369d8-151">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="369d8-152">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="369d8-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
