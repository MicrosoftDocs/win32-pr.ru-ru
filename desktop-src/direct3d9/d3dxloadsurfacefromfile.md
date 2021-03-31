---
description: Загружает поверхность из файла.
ms.assetid: cbd360b6-6cee-418b-8c45-506e190eb2f6
title: Функция D3DXLoadSurfaceFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f53343e436ac78b93bcee30c7da5c9d8eb2dc415
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821469"
---
# <a name="d3dxloadsurfacefromfile-function"></a><span data-ttu-id="95766-103">Функция D3DXLoadSurfaceFromFile</span><span class="sxs-lookup"><span data-stu-id="95766-103">D3DXLoadSurfaceFromFile function</span></span>

<span data-ttu-id="95766-104">Загружает поверхность из файла.</span><span class="sxs-lookup"><span data-stu-id="95766-104">Loads a surface from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="95766-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95766-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFile(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCTSTR            pSrcFile,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="95766-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="95766-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95766-107">*пдестсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95766-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95766-108">Тип: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="95766-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="95766-109">Указатель на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="95766-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="95766-110">Задает поверхность назначения, которая получает изображение.</span><span class="sxs-lookup"><span data-stu-id="95766-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="95766-111">*пдестпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95766-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95766-112">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="95766-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="95766-113">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="95766-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="95766-114">*пдестрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95766-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95766-115">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="95766-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="95766-116">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="95766-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="95766-117">Задает прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="95766-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="95766-118">Присвойте этому параметру **значение NULL** , чтобы указать всю поверхность.</span><span class="sxs-lookup"><span data-stu-id="95766-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="95766-119">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95766-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95766-120">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95766-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95766-121">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="95766-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="95766-122">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="95766-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="95766-123">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="95766-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="95766-124">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="95766-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="95766-125">*псркрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95766-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95766-126">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="95766-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="95766-127">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="95766-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="95766-128">Задает исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="95766-128">Specifies the source rectangle.</span></span> <span data-ttu-id="95766-129">Присвойте этому параметру **значение NULL** , чтобы указать все изображение.</span><span class="sxs-lookup"><span data-stu-id="95766-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="95766-130">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95766-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95766-131">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95766-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95766-132">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="95766-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="95766-133">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="95766-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="95766-134">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95766-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95766-135">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="95766-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="95766-136">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="95766-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="95766-137">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="95766-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="95766-138">Альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей. Таким образом, для непрозрачного черного значения будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="95766-138">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="95766-139">*псрЦинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="95766-139">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="95766-140">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="95766-140">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="95766-141">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="95766-141">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95766-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95766-142">Return value</span></span>

<span data-ttu-id="95766-143">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95766-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95766-144">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="95766-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="95766-145">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="95766-145">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="95766-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95766-146">Remarks</span></span>

<span data-ttu-id="95766-147">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="95766-147">The compiler setting also determines the function version.</span></span> <span data-ttu-id="95766-148">Если определен Юникод, вызов функции разрешается в D3DXLoadSurfaceFromFileW.</span><span class="sxs-lookup"><span data-stu-id="95766-148">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromFileW.</span></span> <span data-ttu-id="95766-149">В противном случае вызов функции разрешается в D3DXLoadSurfaceFromFileA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="95766-149">Otherwise, the function call resolves to D3DXLoadSurfaceFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="95766-150">Эта функция обрабатывает преобразование в форматы сжатия и из сжатых форматов текстур и поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="95766-150">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="95766-151">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="95766-151">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="95766-152">Запись на поверхность без выравнивания не приведет к обновлению «грязного» прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="95766-152">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="95766-153">Если вызывается **D3DXLoadSurfaceFromFile** и поверхность не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явно вызвать [**адддиртирект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) на поверхности.</span><span class="sxs-lookup"><span data-stu-id="95766-153">If **D3DXLoadSurfaceFromFile** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="95766-154">Требования</span><span class="sxs-lookup"><span data-stu-id="95766-154">Requirements</span></span>



| <span data-ttu-id="95766-155">Требование</span><span class="sxs-lookup"><span data-stu-id="95766-155">Requirement</span></span> | <span data-ttu-id="95766-156">Значение</span><span class="sxs-lookup"><span data-stu-id="95766-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95766-157">Header</span><span class="sxs-lookup"><span data-stu-id="95766-157">Header</span></span><br/>  | <dl> <span data-ttu-id="95766-158"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="95766-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="95766-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95766-159">Library</span></span><br/> | <dl> <span data-ttu-id="95766-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95766-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="95766-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95766-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95766-162">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="95766-162">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
