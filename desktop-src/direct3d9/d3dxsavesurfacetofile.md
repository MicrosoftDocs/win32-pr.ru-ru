---
description: Сохраняет поверхность в файле.
ms.assetid: 28bbf728-afde-4d25-8562-9d6a957aab2d
title: Функция D3DXSaveSurfaceToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd19e0a8f7b9557b6bcbe6c71afcdca7c9037b70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713649"
---
# <a name="d3dxsavesurfacetofile-function"></a><span data-ttu-id="00dcd-103">Функция D3DXSaveSurfaceToFile</span><span class="sxs-lookup"><span data-stu-id="00dcd-103">D3DXSaveSurfaceToFile function</span></span>

<span data-ttu-id="00dcd-104">Сохраняет поверхность в файле.</span><span class="sxs-lookup"><span data-stu-id="00dcd-104">Saves a surface to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="00dcd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00dcd-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DSURFACE9   pSrcSurface,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="00dcd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00dcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00dcd-107">*пдестфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00dcd-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dcd-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00dcd-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00dcd-109">Указатель на строку, указывающую имя файла конечного изображения.</span><span class="sxs-lookup"><span data-stu-id="00dcd-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="00dcd-110">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="00dcd-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="00dcd-111">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="00dcd-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="00dcd-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="00dcd-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="00dcd-113">*Дестформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00dcd-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dcd-114">Тип: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="00dcd-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="00dcd-115">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) , указывающий формат файла, используемый при сохранении.</span><span class="sxs-lookup"><span data-stu-id="00dcd-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="00dcd-116">Эта функция поддерживает сохранение во всех форматах **\_ FILEFORMAT D3DXIMAGE** , кроме переносимых пиксмап (. ppm) и Targa/формат графического адаптера (. TGA).</span><span class="sxs-lookup"><span data-stu-id="00dcd-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="00dcd-117">*псрксурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00dcd-117">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dcd-118">Тип: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="00dcd-118">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="00dcd-119">Указатель на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , содержащий изображение, которое необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="00dcd-119">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="00dcd-120">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00dcd-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dcd-121">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="00dcd-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="00dcd-122">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , содержащую палитру цветов 256.</span><span class="sxs-lookup"><span data-stu-id="00dcd-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="00dcd-123">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="00dcd-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="00dcd-124">*псркрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00dcd-124">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dcd-125">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="00dcd-125">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="00dcd-126">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="00dcd-126">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="00dcd-127">Задает исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="00dcd-127">Specifies the source rectangle.</span></span> <span data-ttu-id="00dcd-128">Присвойте этому параметру **значение NULL** , чтобы указать все изображение.</span><span class="sxs-lookup"><span data-stu-id="00dcd-128">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00dcd-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00dcd-129">Return value</span></span>

<span data-ttu-id="00dcd-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="00dcd-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="00dcd-131">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="00dcd-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="00dcd-132">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="00dcd-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="00dcd-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00dcd-133">Remarks</span></span>

<span data-ttu-id="00dcd-134">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="00dcd-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="00dcd-135">Если определен Юникод, вызов функции разрешается в D3DXSaveSurfaceToFileW.</span><span class="sxs-lookup"><span data-stu-id="00dcd-135">If Unicode is defined, the function call resolves to D3DXSaveSurfaceToFileW.</span></span> <span data-ttu-id="00dcd-136">В противном случае вызов функции разрешается в D3DXSaveSurfaceToFileA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="00dcd-136">Otherwise, the function call resolves to D3DXSaveSurfaceToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="00dcd-137">Эта функция обрабатывает преобразование в форматы сжатой текстуры и из них.</span><span class="sxs-lookup"><span data-stu-id="00dcd-137">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="00dcd-138">Требования</span><span class="sxs-lookup"><span data-stu-id="00dcd-138">Requirements</span></span>



| <span data-ttu-id="00dcd-139">Требование</span><span class="sxs-lookup"><span data-stu-id="00dcd-139">Requirement</span></span> | <span data-ttu-id="00dcd-140">Значение</span><span class="sxs-lookup"><span data-stu-id="00dcd-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00dcd-141">Header</span><span class="sxs-lookup"><span data-stu-id="00dcd-141">Header</span></span><br/>  | <dl> <span data-ttu-id="00dcd-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="00dcd-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="00dcd-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="00dcd-143">Library</span></span><br/> | <dl> <span data-ttu-id="00dcd-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00dcd-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="00dcd-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00dcd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00dcd-146">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="00dcd-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="00dcd-147">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="00dcd-147">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="00dcd-148">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="00dcd-148">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
