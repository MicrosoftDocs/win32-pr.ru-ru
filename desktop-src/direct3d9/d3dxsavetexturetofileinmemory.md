---
description: Сохраняет текстуру в файл изображения.
ms.assetid: 8dcfd58a-ae1e-43c3-8ff1-94e3fa398b0f
title: Функция D3DXSaveTextureToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c58da1663abc5295e8ce17c500bd46d6c365a2d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157175"
---
# <a name="d3dxsavetexturetofileinmemory-function"></a><span data-ttu-id="23591-103">Функция D3DXSaveTextureToFileInMemory</span><span class="sxs-lookup"><span data-stu-id="23591-103">D3DXSaveTextureToFileInMemory function</span></span>

<span data-ttu-id="23591-104">Сохраняет текстуру в файл изображения.</span><span class="sxs-lookup"><span data-stu-id="23591-104">Saves a texture to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="23591-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23591-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFileInMemory(
  _Out_       LPD3DXBUFFER           *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_        LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="23591-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="23591-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23591-107">*ппдестбуф* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="23591-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23591-108">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="23591-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="23591-109">Адрес указателя на [**ID3DXBuffer**](id3dxbuffer.md) , который будет хранить изображение.</span><span class="sxs-lookup"><span data-stu-id="23591-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="23591-110">*Дестформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23591-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23591-111">Тип: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="23591-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="23591-112">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) , указывающий формат файла, используемый при сохранении.</span><span class="sxs-lookup"><span data-stu-id="23591-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="23591-113">Эта функция поддерживает сохранение во всех форматах **\_ FILEFORMAT D3DXIMAGE** , кроме переносимых пиксмап (. ppm) и Targa/формат графического адаптера (. TGA).</span><span class="sxs-lookup"><span data-stu-id="23591-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="23591-114">*псрктекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23591-114">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23591-115">Тип: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="23591-115">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="23591-116">Указатель на интерфейс [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) , содержащий изображение для сохранения.</span><span class="sxs-lookup"><span data-stu-id="23591-116">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="23591-117">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23591-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23591-118">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="23591-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="23591-119">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , содержащую палитру цветов 256.</span><span class="sxs-lookup"><span data-stu-id="23591-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="23591-120">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="23591-120">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23591-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23591-121">Return value</span></span>

<span data-ttu-id="23591-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23591-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23591-123">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="23591-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="23591-124">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="23591-124">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="23591-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23591-125">Remarks</span></span>

<span data-ttu-id="23591-126">Эта функция обрабатывает преобразование в форматы сжатой текстуры и из них.</span><span class="sxs-lookup"><span data-stu-id="23591-126">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="23591-127">Требования</span><span class="sxs-lookup"><span data-stu-id="23591-127">Requirements</span></span>



| <span data-ttu-id="23591-128">Требование</span><span class="sxs-lookup"><span data-stu-id="23591-128">Requirement</span></span> | <span data-ttu-id="23591-129">Значение</span><span class="sxs-lookup"><span data-stu-id="23591-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23591-130">Header</span><span class="sxs-lookup"><span data-stu-id="23591-130">Header</span></span><br/>  | <dl> <span data-ttu-id="23591-131"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="23591-131"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="23591-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="23591-132">Library</span></span><br/> | <dl> <span data-ttu-id="23591-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23591-133"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="23591-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23591-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23591-135">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="23591-135">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="23591-136">**D3DXSaveSurfaceToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="23591-136">**D3DXSaveSurfaceToFileInMemory**</span></span>](d3dxsavesurfacetofileinmemory.md)
</dt> <dt>

[<span data-ttu-id="23591-137">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="23591-137">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
