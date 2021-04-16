---
description: Создает текстуру куба из файла.
ms.assetid: 7ff3b051-568c-4c77-b8a6-b626ba156eb1
title: Функция D3DXCreateCubeTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2071a1d1e16e769d1a0623138e24c2e0fbab85e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720912"
---
# <a name="d3dxcreatecubetexturefromfile-function"></a><span data-ttu-id="be10f-103">Функция D3DXCreateCubeTextureFromFile</span><span class="sxs-lookup"><span data-stu-id="be10f-103">D3DXCreateCubeTextureFromFile function</span></span>

<span data-ttu-id="be10f-104">Создает текстуру куба из файла.</span><span class="sxs-lookup"><span data-stu-id="be10f-104">Creates a cube texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="be10f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be10f-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="be10f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be10f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be10f-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be10f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be10f-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="be10f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="be10f-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой Куба.</span><span class="sxs-lookup"><span data-stu-id="be10f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="be10f-110">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be10f-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be10f-111">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be10f-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be10f-112">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="be10f-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="be10f-113">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="be10f-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="be10f-114">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="be10f-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="be10f-115">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="be10f-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="be10f-116">*ппкубетекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="be10f-116">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be10f-117">Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="be10f-117">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="be10f-118">Адрес указателя на интерфейс [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий созданный объект текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="be10f-118">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be10f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be10f-119">Return value</span></span>

<span data-ttu-id="be10f-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be10f-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be10f-121">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="be10f-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="be10f-122">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE, D3DERR \_ аутофвидеомемори, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="be10f-122">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="be10f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be10f-123">Remarks</span></span>

<span data-ttu-id="be10f-124">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="be10f-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="be10f-125">Если определен Юникод, вызов функции разрешается в **D3DXCreateCubeTextureFromFileW**.</span><span class="sxs-lookup"><span data-stu-id="be10f-125">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileW**.</span></span> <span data-ttu-id="be10f-126">В противном случае вызов функции разрешается в **D3DXCreateCubeTextureFromFileA** , так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="be10f-126">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileA** because ANSI strings are being used.</span></span>

<span data-ttu-id="be10f-127">Функция эквивалентна D3DXCreateCubeTextureFromFileEx (Пдевице, Псркфиле, D3DX \_ Default, D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, **null**, **null**, ппкубетекстуре).</span><span class="sxs-lookup"><span data-stu-id="be10f-127">The function is equivalent to D3DXCreateCubeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="be10f-128">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="be10f-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="be10f-129">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="be10f-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="be10f-130">Обратите внимание, что ресурс, созданный с помощью этой функции при вызове из объекта IDirect3DDevice9, будет помещен в класс Memory, обозначенный D3DPOOL \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="be10f-130">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="be10f-131">При вызове этого метода из объекта IDirect3DDevice9Ex ресурс будет помещен в класс Memory, обозначенный параметром D3DPOOL \_ Default.</span><span class="sxs-lookup"><span data-stu-id="be10f-131">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="be10f-132">Фильтрация автоматически применяется к текстуре, созданной с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="be10f-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="be10f-133">Фильтрация эквивалентна D3DX фильтра \_ D3DX Filter \_ \| \_ \_ в [ \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="be10f-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="be10f-134">**D3DXCreateCubeTextureFromFile** использует формат файла поверхности DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="be10f-134">**D3DXCreateCubeTextureFromFile** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="be10f-135">Редактор текстур DirectX (Dxtex.exe) позволяет создать карту Куба на основе других форматов файлов и сохранить ее в формате файлов DDS.</span><span class="sxs-lookup"><span data-stu-id="be10f-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="be10f-136">Вы можете получить Dxtex.exe и узнать о нем из пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="be10f-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="be10f-137">Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="be10f-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be10f-138">Требования</span><span class="sxs-lookup"><span data-stu-id="be10f-138">Requirements</span></span>



| <span data-ttu-id="be10f-139">Требование</span><span class="sxs-lookup"><span data-stu-id="be10f-139">Requirement</span></span> | <span data-ttu-id="be10f-140">Значение</span><span class="sxs-lookup"><span data-stu-id="be10f-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be10f-141">Header</span><span class="sxs-lookup"><span data-stu-id="be10f-141">Header</span></span><br/>  | <dl> <span data-ttu-id="be10f-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="be10f-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="be10f-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be10f-143">Library</span></span><br/> | <dl> <span data-ttu-id="be10f-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be10f-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="be10f-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be10f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be10f-146">**D3DXCreateCubeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="be10f-146">**D3DXCreateCubeTextureFromFileEx**</span></span>](d3dxcreatecubetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="be10f-147">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="be10f-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
