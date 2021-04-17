---
description: Создает текстуру куба из файла в памяти.
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: Функция D3DXCreateCubeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f1d6de3fba0dcbda959a2811ec665ebc4a6541c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720910"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a><span data-ttu-id="78714-103">Функция D3DXCreateCubeTextureFromFileInMemory</span><span class="sxs-lookup"><span data-stu-id="78714-103">D3DXCreateCubeTextureFromFileInMemory function</span></span>

<span data-ttu-id="78714-104">Создает текстуру куба из файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="78714-104">Creates a cube texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="78714-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78714-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="78714-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78714-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78714-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78714-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78714-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="78714-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="78714-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой Куба.</span><span class="sxs-lookup"><span data-stu-id="78714-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="78714-110">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78714-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78714-111">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78714-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78714-112">Указатель на файл в памяти, из которого создается кубической карты.</span><span class="sxs-lookup"><span data-stu-id="78714-112">Pointer to the file in memory from which to create the cubemap.</span></span> <span data-ttu-id="78714-113">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="78714-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="78714-114">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78714-114">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78714-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78714-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78714-116">Размер файла в памяти, в байтах.</span><span class="sxs-lookup"><span data-stu-id="78714-116">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="78714-117">*ппкубетекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="78714-117">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78714-118">Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="78714-118">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="78714-119">Адрес указателя на интерфейс [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий созданный объект текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="78714-119">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78714-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78714-120">Return value</span></span>

<span data-ttu-id="78714-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78714-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78714-122">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="78714-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="78714-123">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE, D3DERR \_ аутофвидеомемори, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="78714-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="78714-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78714-124">Remarks</span></span>

<span data-ttu-id="78714-125">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="78714-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="78714-126">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="78714-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="78714-127">Функция эквивалентна D3DXCreateCubeTextureFromFileInMemoryEx (Пдевице, Псркдата, Сркдатасизе, D3DX \_ Default, D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, **null**, **null**, ппкубетекстуре).</span><span class="sxs-lookup"><span data-stu-id="78714-127">The function is equivalent to D3DXCreateCubeTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="78714-128">Обратите внимание, что ресурс, созданный с помощью этой функции при вызове из объекта IDirect3DDevice9, будет помещен в класс Memory, обозначенный D3DPOOL \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="78714-128">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="78714-129">При вызове этого метода из объекта IDirect3DDevice9Ex ресурс будет помещен в класс Memory, обозначенный параметром D3DPOOL \_ Default.</span><span class="sxs-lookup"><span data-stu-id="78714-129">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="78714-130">Этот метод предназначен для использования при загрузке файлов изображений, хранящихся в виде RT \_ RCDATA, который является определяемым приложением ресурсом (необработанные данные).</span><span class="sxs-lookup"><span data-stu-id="78714-130">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="78714-131">В противном случае этот метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="78714-131">Otherwise this method will fail.</span></span>

<span data-ttu-id="78714-132">Фильтрация автоматически применяется к текстуре, созданной с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="78714-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="78714-133">Фильтрация эквивалентна D3DX фильтра \_ D3DX Filter \_ \| \_ \_ в [ \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="78714-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="78714-134">**D3DXCreateCubeTextureFromFileInMemory** использует формат файла поверхности DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="78714-134">**D3DXCreateCubeTextureFromFileInMemory** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="78714-135">Редактор текстур DirectX (Dxtex.exe) позволяет создать карту Куба на основе других форматов файлов и сохранить ее в формате файлов DDS.</span><span class="sxs-lookup"><span data-stu-id="78714-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="78714-136">Вы можете получить Dxtex.exe и узнать о нем из пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="78714-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="78714-137">Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="78714-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78714-138">Требования</span><span class="sxs-lookup"><span data-stu-id="78714-138">Requirements</span></span>



| <span data-ttu-id="78714-139">Требование</span><span class="sxs-lookup"><span data-stu-id="78714-139">Requirement</span></span> | <span data-ttu-id="78714-140">Значение</span><span class="sxs-lookup"><span data-stu-id="78714-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78714-141">Header</span><span class="sxs-lookup"><span data-stu-id="78714-141">Header</span></span><br/>  | <dl> <span data-ttu-id="78714-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="78714-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="78714-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="78714-143">Library</span></span><br/> | <dl> <span data-ttu-id="78714-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78714-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="78714-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78714-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78714-146">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="78714-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
