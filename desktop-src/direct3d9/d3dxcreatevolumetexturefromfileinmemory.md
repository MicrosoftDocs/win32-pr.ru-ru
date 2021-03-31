---
description: Создает текстуру тома из файла в памяти.
ms.assetid: 8ea22209-6110-4bef-a0d6-667f59017adc
title: Функция D3DXCreateVolumeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 380aadd9e26940b2a67c2064b3941a0965a782f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821101"
---
# <a name="d3dxcreatevolumetexturefromfileinmemory-function"></a><span data-ttu-id="df606-103">Функция D3DXCreateVolumeTextureFromFileInMemory</span><span class="sxs-lookup"><span data-stu-id="df606-103">D3DXCreateVolumeTextureFromFileInMemory function</span></span>

<span data-ttu-id="df606-104">Создает текстуру тома из файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="df606-104">Creates a volume texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="df606-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df606-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCVOID                  pSrcFile,
  _In_  UINT                     SrcData,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="df606-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df606-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df606-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df606-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df606-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="df606-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="df606-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой тома.</span><span class="sxs-lookup"><span data-stu-id="df606-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="df606-110">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df606-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df606-111">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df606-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df606-112">Указатель на файл в памяти, из которого создается текстура тома.</span><span class="sxs-lookup"><span data-stu-id="df606-112">Pointer to the file in memory from which to create the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="df606-113">*SrcData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df606-113">*SrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df606-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df606-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df606-115">Размер файла в памяти, в байтах.</span><span class="sxs-lookup"><span data-stu-id="df606-115">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="df606-116">*ппволуметекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="df606-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df606-117">Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="df606-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="df606-118">Адрес указателя на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="df606-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df606-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df606-119">Return value</span></span>

<span data-ttu-id="df606-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df606-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df606-121">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="df606-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="df606-122">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="df606-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="df606-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df606-123">Remarks</span></span>

<span data-ttu-id="df606-124">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="df606-124">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="df606-125">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="df606-125">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="df606-126">Функция эквивалентна D3DXCreateVolumeTextureFromFileInMemoryEx (Пдевице, Псркфиле, SrcData, D3DX \_ Default, D3DX \_ по умолчанию, D3DX \_ Default, D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, **null**, **null**, ппволуметекстуре).</span><span class="sxs-lookup"><span data-stu-id="df606-126">The function is equivalent to D3DXCreateVolumeTextureFromFileInMemoryEx(pDevice, pSrcFile, SrcData, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="df606-127">Обратите внимание, что ресурс, созданный с помощью этой функции при вызове из объекта IDirect3DDevice9, будет помещен в класс Memory, обозначенный D3DPOOL \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="df606-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="df606-128">При вызове этого метода из объекта IDirect3DDevice9Ex ресурс будет помещен в класс Memory, обозначенный параметром D3DPOOL \_ Default.</span><span class="sxs-lookup"><span data-stu-id="df606-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="df606-129">Фильтрация автоматически применяется к текстуре, созданной с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="df606-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="df606-130">Фильтрация эквивалентна D3DX фильтра \_ D3DX Filter \_ \| \_ \_ в [ \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="df606-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df606-131">Требования</span><span class="sxs-lookup"><span data-stu-id="df606-131">Requirements</span></span>



| <span data-ttu-id="df606-132">Требование</span><span class="sxs-lookup"><span data-stu-id="df606-132">Requirement</span></span> | <span data-ttu-id="df606-133">Значение</span><span class="sxs-lookup"><span data-stu-id="df606-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df606-134">Header</span><span class="sxs-lookup"><span data-stu-id="df606-134">Header</span></span><br/>  | <dl> <span data-ttu-id="df606-135"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="df606-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="df606-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="df606-136">Library</span></span><br/> | <dl> <span data-ttu-id="df606-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df606-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="df606-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df606-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df606-139">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="df606-139">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="df606-140">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="df606-140">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="df606-141">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="df606-141">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="df606-142">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="df606-142">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="df606-143">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="df606-143">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="df606-144">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="df606-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
