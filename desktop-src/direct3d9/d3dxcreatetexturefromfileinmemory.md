---
description: Создает текстуру из файла в памяти.
ms.assetid: 3ea811be-7db8-4436-b138-f0102389bb4d
title: Функция D3DXCreateTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 743a944da52bc6d2ae13b045f854d95b4751712d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821109"
---
# <a name="d3dxcreatetexturefromfileinmemory-function"></a><span data-ttu-id="b1aa0-103">Функция D3DXCreateTextureFromFileInMemory</span><span class="sxs-lookup"><span data-stu-id="b1aa0-103">D3DXCreateTextureFromFileInMemory function</span></span>

<span data-ttu-id="b1aa0-104">Создает текстуру из файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-104">Creates a texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1aa0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1aa0-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCVOID            pSrcData,
  _In_  UINT               SrcDataSize,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="b1aa0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1aa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1aa0-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1aa0-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1aa0-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b1aa0-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b1aa0-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="b1aa0-110">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1aa0-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1aa0-111">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1aa0-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1aa0-112">Указатель на файл в памяти, из которого создается текстура.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-112">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="b1aa0-113">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1aa0-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1aa0-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1aa0-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1aa0-115">Размер (в байтах) файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-115">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="b1aa0-116">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b1aa0-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1aa0-117">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="b1aa0-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="b1aa0-118">Адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1aa0-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1aa0-119">Return value</span></span>

<span data-ttu-id="b1aa0-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1aa0-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1aa0-121">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b1aa0-122">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1aa0-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1aa0-123">Remarks</span></span>

<span data-ttu-id="b1aa0-124">Функция эквивалентна D3DXCreateTextureFromFileInMemoryEx (Пдевице, Псркдата, Сркдатасизе, D3DX \_ Default, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ управляемые, D3DX \_ Default, D3DX \_ по умолчанию, 0, **null**, **null**, пптекстуре).</span><span class="sxs-lookup"><span data-stu-id="b1aa0-124">The function is equivalent to D3DXCreateTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="b1aa0-125">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="b1aa0-126">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="b1aa0-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="b1aa0-127">Обратите внимание, что ресурс, созданный с помощью этой функции при вызове из объекта IDirect3DDevice9, будет помещен в класс Memory, обозначенный D3DPOOL \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="b1aa0-128">При вызове этого метода из объекта IDirect3DDevice9Ex ресурс будет помещен в класс Memory, обозначенный параметром D3DPOOL \_ Default.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="b1aa0-129">Фильтрация автоматически применяется к текстуре, созданной с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="b1aa0-130">Фильтрация эквивалентна D3DX фильтра \_ D3DX Filter \_ \| \_ \_ в [ \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b1aa0-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1aa0-131">Требования</span><span class="sxs-lookup"><span data-stu-id="b1aa0-131">Requirements</span></span>



| <span data-ttu-id="b1aa0-132">Требование</span><span class="sxs-lookup"><span data-stu-id="b1aa0-132">Requirement</span></span> | <span data-ttu-id="b1aa0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b1aa0-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1aa0-134">Header</span><span class="sxs-lookup"><span data-stu-id="b1aa0-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b1aa0-135"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1aa0-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b1aa0-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b1aa0-136">Library</span></span><br/> | <dl> <span data-ttu-id="b1aa0-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1aa0-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b1aa0-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1aa0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1aa0-139">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="b1aa0-139">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="b1aa0-140">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b1aa0-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
