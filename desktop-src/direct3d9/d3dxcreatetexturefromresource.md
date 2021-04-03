---
description: Создает текстуру из ресурса.
ms.assetid: 7c841f21-5565-4923-a2fe-bbd618616f87
title: Функция D3DXCreateTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ce9101caed2a60dc3be7fe0039a1e391423f1fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914720"
---
# <a name="d3dxcreatetexturefromresource-function"></a><span data-ttu-id="f1c22-103">Функция D3DXCreateTextureFromResource</span><span class="sxs-lookup"><span data-stu-id="f1c22-103">D3DXCreateTextureFromResource function</span></span>

<span data-ttu-id="f1c22-104">Создает текстуру из ресурса.</span><span class="sxs-lookup"><span data-stu-id="f1c22-104">Creates a texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c22-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1c22-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResource(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  HMODULE            hSrcModule,
  _In_  LPCTSTR            pSrcResource,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="f1c22-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1c22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1c22-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1c22-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1c22-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f1c22-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f1c22-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="f1c22-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="f1c22-110">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1c22-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1c22-111">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1c22-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1c22-112">Указатель на модуль, в котором находится ресурс, или **значение NULL** для модуля, связанного с образом, операционной системой, используемой для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="f1c22-112">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="f1c22-113">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1c22-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1c22-114">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1c22-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1c22-115">Указатель на строку, указывающую имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="f1c22-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="f1c22-116">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="f1c22-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f1c22-117">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="f1c22-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="f1c22-118">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="f1c22-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f1c22-119">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1c22-119">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1c22-120">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="f1c22-120">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="f1c22-121">Адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="f1c22-121">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1c22-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1c22-122">Return value</span></span>

<span data-ttu-id="f1c22-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1c22-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1c22-124">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f1c22-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f1c22-125">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f1c22-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1c22-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1c22-126">Remarks</span></span>

<span data-ttu-id="f1c22-127">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="f1c22-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f1c22-128">Если определен Юникод, вызов функции разрешается в D3DXCreateTextureFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="f1c22-128">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceW.</span></span> <span data-ttu-id="f1c22-129">В противном случае вызов функции разрешается в D3DXCreateTextureFromResourceA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="f1c22-129">Otherwise, the function call resolves to D3DXCreateTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="f1c22-130">Функция эквивалентна D3DXCreateTextureFromResourceEx (Пдевице, Хсркмодуле, Псркресаурце, D3DX \_ Default, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ управляемые, D3DX \_ Default, D3DX \_ по умолчанию, 0, **null**, **null**, пптекстуре).</span><span class="sxs-lookup"><span data-stu-id="f1c22-130">The function is equivalent to D3DXCreateTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="f1c22-131">Загружаемый ресурс должен иметь тип \_ Bitmap или "RT RCDATA" \_ .</span><span class="sxs-lookup"><span data-stu-id="f1c22-131">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="f1c22-132">Тип ресурса RT \_ RCDATA используется для загрузки форматов, отличных от точечных рисунков (таких как. TGA,. jpg и. DDS).</span><span class="sxs-lookup"><span data-stu-id="f1c22-132">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="f1c22-133">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="f1c22-133">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="f1c22-134">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="f1c22-134">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="f1c22-135">Обратите внимание, что ресурс, созданный с помощью этой функции при вызове из объекта IDirect3DDevice9, будет помещен в класс Memory, обозначенный D3DPOOL \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="f1c22-135">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="f1c22-136">При вызове этого метода из объекта IDirect3DDevice9Ex ресурс будет помещен в класс Memory, обозначенный параметром D3DPOOL \_ Default.</span><span class="sxs-lookup"><span data-stu-id="f1c22-136">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="f1c22-137">Фильтрация автоматически применяется к текстуре, созданной с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="f1c22-137">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="f1c22-138">Фильтрация эквивалентна D3DX фильтра \_ D3DX Filter \_ \| \_ \_ в [ \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f1c22-138">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1c22-139">Требования</span><span class="sxs-lookup"><span data-stu-id="f1c22-139">Requirements</span></span>



| <span data-ttu-id="f1c22-140">Требование</span><span class="sxs-lookup"><span data-stu-id="f1c22-140">Requirement</span></span> | <span data-ttu-id="f1c22-141">Значение</span><span class="sxs-lookup"><span data-stu-id="f1c22-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c22-142">Header</span><span class="sxs-lookup"><span data-stu-id="f1c22-142">Header</span></span><br/>  | <dl> <span data-ttu-id="f1c22-143"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1c22-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f1c22-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f1c22-144">Library</span></span><br/> | <dl> <span data-ttu-id="f1c22-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1c22-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f1c22-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1c22-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c22-147">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="f1c22-147">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="f1c22-148">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f1c22-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
