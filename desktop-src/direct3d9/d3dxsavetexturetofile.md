---
description: Сохраняет текстуру в файл.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: Функция D3DXSaveTextureToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c11cc8b512527fb0610c288fdbaeba6c976604a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694131"
---
# <a name="d3dxsavetexturetofile-function"></a><span data-ttu-id="b1760-103">Функция D3DXSaveTextureToFile</span><span class="sxs-lookup"><span data-stu-id="b1760-103">D3DXSaveTextureToFile function</span></span>

<span data-ttu-id="b1760-104">Сохраняет текстуру в файл.</span><span class="sxs-lookup"><span data-stu-id="b1760-104">Saves a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1760-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1760-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="b1760-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1760-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1760-107">*пдестфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1760-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1760-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1760-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1760-109">Указатель на строку, указывающую имя файла конечного изображения.</span><span class="sxs-lookup"><span data-stu-id="b1760-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="b1760-110">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="b1760-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b1760-111">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b1760-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="b1760-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="b1760-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b1760-113">*Дестформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1760-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1760-114">Тип: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="b1760-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="b1760-115">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) , указывающий формат файла, используемый при сохранении.</span><span class="sxs-lookup"><span data-stu-id="b1760-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="b1760-116">Эта функция поддерживает сохранение во всех форматах **\_ FILEFORMAT D3DXIMAGE** , кроме переносимых пиксмап (. ppm) и Targa/формат графического адаптера (. TGA).</span><span class="sxs-lookup"><span data-stu-id="b1760-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="b1760-117">*псрктекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1760-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1760-118">Тип: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="b1760-118">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="b1760-119">Указатель на интерфейс [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) , содержащий текстуру, которую необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="b1760-119">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface, containing the texture to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="b1760-120">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1760-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1760-121">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="b1760-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="b1760-122">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , содержащую палитру цветов 256.</span><span class="sxs-lookup"><span data-stu-id="b1760-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="b1760-123">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b1760-123">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1760-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1760-124">Return value</span></span>

<span data-ttu-id="b1760-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1760-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1760-126">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b1760-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b1760-127">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="b1760-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="b1760-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1760-128">Remarks</span></span>

<span data-ttu-id="b1760-129">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="b1760-129">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b1760-130">Если определен Юникод, вызов функции разрешается в D3DXSaveTextureToFileW.</span><span class="sxs-lookup"><span data-stu-id="b1760-130">If Unicode is defined, the function call resolves to D3DXSaveTextureToFileW.</span></span> <span data-ttu-id="b1760-131">В противном случае вызов функции разрешается в D3DXSaveTextureToFileA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="b1760-131">Otherwise, the function call resolves to D3DXSaveTextureToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="b1760-132">Эта функция обрабатывает преобразование в форматы сжатой текстуры и из них.</span><span class="sxs-lookup"><span data-stu-id="b1760-132">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="b1760-133">Если том является нединамическим (из-за параметра использования, установленного в значение 0 при создании) и расположен в видеопамяти (пул памяти со значением D3DPOOL \_ по умолчанию), **D3DXSaveTextureToFile** завершится сбоем, так как D3DX не сможет блокировать нединамические тома, расположенные в видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="b1760-133">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXSaveTextureToFile** will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1760-134">Требования</span><span class="sxs-lookup"><span data-stu-id="b1760-134">Requirements</span></span>



| <span data-ttu-id="b1760-135">Требование</span><span class="sxs-lookup"><span data-stu-id="b1760-135">Requirement</span></span> | <span data-ttu-id="b1760-136">Значение</span><span class="sxs-lookup"><span data-stu-id="b1760-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1760-137">Header</span><span class="sxs-lookup"><span data-stu-id="b1760-137">Header</span></span><br/>  | <dl> <span data-ttu-id="b1760-138"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1760-138"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b1760-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b1760-139">Library</span></span><br/> | <dl> <span data-ttu-id="b1760-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1760-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b1760-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1760-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1760-142">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b1760-142">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="b1760-143">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="b1760-143">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="b1760-144">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="b1760-144">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
