---
description: Сохраняет том в файл на диске.
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: Функция D3DXSaveVolumeToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 36550cda8d9ef664f96e236d2770a82c88412772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694130"
---
# <a name="d3dxsavevolumetofile-function"></a><span data-ttu-id="724f9-103">Функция D3DXSaveVolumeToFile</span><span class="sxs-lookup"><span data-stu-id="724f9-103">D3DXSaveVolumeToFile function</span></span>

<span data-ttu-id="724f9-104">Сохраняет том в файл на диске.</span><span class="sxs-lookup"><span data-stu-id="724f9-104">Saves a volume to a file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="724f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="724f9-105">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="724f9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="724f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="724f9-107">*пдестфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="724f9-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="724f9-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="724f9-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="724f9-109">Указатель на строку, указывающую имя файла конечного изображения.</span><span class="sxs-lookup"><span data-stu-id="724f9-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="724f9-110">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="724f9-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="724f9-111">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="724f9-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="724f9-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="724f9-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="724f9-113">*Дестформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="724f9-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="724f9-114">Тип: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="724f9-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="724f9-115">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) , указывающий формат файла, используемый при сохранении.</span><span class="sxs-lookup"><span data-stu-id="724f9-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="724f9-116">Эта функция поддерживает сохранение во всех форматах **\_ FILEFORMAT D3DXIMAGE** , кроме переносимых пиксмап (. ppm) и Targa/формат графического адаптера (. TGA).</span><span class="sxs-lookup"><span data-stu-id="724f9-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="724f9-117">*псркволуме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="724f9-117">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="724f9-118">Тип: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="724f9-118">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="724f9-119">Указатель на интерфейс [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) , содержащий изображение для сохранения.</span><span class="sxs-lookup"><span data-stu-id="724f9-119">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="724f9-120">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="724f9-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="724f9-121">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="724f9-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="724f9-122">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , содержащую палитру цветов 256.</span><span class="sxs-lookup"><span data-stu-id="724f9-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="724f9-123">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="724f9-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="724f9-124">*псркбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="724f9-124">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="724f9-125">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="724f9-125">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="724f9-126">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="724f9-126">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="724f9-127">Указывает поле источника.</span><span class="sxs-lookup"><span data-stu-id="724f9-127">Specifies the source box.</span></span> <span data-ttu-id="724f9-128">Присвойте этому параметру **значение NULL** , чтобы указать весь том.</span><span class="sxs-lookup"><span data-stu-id="724f9-128">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="724f9-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="724f9-129">Return value</span></span>

<span data-ttu-id="724f9-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="724f9-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="724f9-131">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="724f9-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="724f9-132">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="724f9-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="724f9-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="724f9-133">Remarks</span></span>

<span data-ttu-id="724f9-134">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="724f9-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="724f9-135">Если определен Юникод, вызов функции разрешается в D3DXSaveVolumeToFileW.</span><span class="sxs-lookup"><span data-stu-id="724f9-135">If Unicode is defined, the function call resolves to D3DXSaveVolumeToFileW.</span></span> <span data-ttu-id="724f9-136">В противном случае вызов функции разрешается в >D3DXSaveVolumeToFileA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="724f9-136">Otherwise, the function call resolves to >D3DXSaveVolumeToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="724f9-137">Эта функция обрабатывает преобразование в форматы сжатой текстуры и из них.</span><span class="sxs-lookup"><span data-stu-id="724f9-137">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="724f9-138">Если том является нединамическим (из-за параметра использования, установленного в значение 0 при создании) и расположен в видеопамяти (пул памяти со значением D3DPOOL \_ по умолчанию), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) завершится сбоем, так как D3DX не сможет блокировать нединамические тома, расположенные в видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="724f9-138">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="724f9-139">Требования</span><span class="sxs-lookup"><span data-stu-id="724f9-139">Requirements</span></span>



| <span data-ttu-id="724f9-140">Требование</span><span class="sxs-lookup"><span data-stu-id="724f9-140">Requirement</span></span> | <span data-ttu-id="724f9-141">Значение</span><span class="sxs-lookup"><span data-stu-id="724f9-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="724f9-142">Header</span><span class="sxs-lookup"><span data-stu-id="724f9-142">Header</span></span><br/>  | <dl> <span data-ttu-id="724f9-143"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="724f9-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="724f9-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="724f9-144">Library</span></span><br/> | <dl> <span data-ttu-id="724f9-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="724f9-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="724f9-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="724f9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="724f9-147">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="724f9-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="724f9-148">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="724f9-148">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="724f9-149">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="724f9-149">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="724f9-150">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="724f9-150">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
