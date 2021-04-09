---
description: Загружает поверхность из файла в памяти.
ms.assetid: 436a6151-2819-44eb-bd56-1b3777f709e5
title: Функция D3DXLoadSurfaceFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a447c4c5b65e3085d84e26ef202283cf0c31c6b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821468"
---
# <a name="d3dxloadsurfacefromfileinmemory-function"></a><span data-ttu-id="1e4ae-103">Функция D3DXLoadSurfaceFromFileInMemory</span><span class="sxs-lookup"><span data-stu-id="1e4ae-103">D3DXLoadSurfaceFromFileInMemory function</span></span>

<span data-ttu-id="1e4ae-104">Загружает поверхность из файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-104">Loads a surface from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e4ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e4ae-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFileInMemory(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCVOID            pSrcData,
  _In_          UINT               SrcData,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1e4ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e4ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e4ae-107">*пдестсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e4ae-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4ae-108">Тип: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="1e4ae-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="1e4ae-109">Указатель на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="1e4ae-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="1e4ae-110">Задает поверхность назначения, которая получает изображение.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="1e4ae-111">*пдестпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e4ae-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4ae-112">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="1e4ae-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="1e4ae-113">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1e4ae-114">*пдестрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e4ae-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4ae-115">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="1e4ae-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="1e4ae-116">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1e4ae-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="1e4ae-117">Задает прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="1e4ae-118">Присвойте этому параметру **значение NULL** , чтобы указать всю поверхность.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="1e4ae-119">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e4ae-119">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4ae-120">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e4ae-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e4ae-121">Указатель на файл в памяти, из которого загружается поверхность.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-121">Pointer to the file in memory from which to load the surface.</span></span>

</dd> <dt>

<span data-ttu-id="1e4ae-122">*SrcData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e4ae-122">*SrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4ae-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e4ae-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e4ae-124">Размер файла в памяти, в байтах.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-124">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1e4ae-125">*псркрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e4ae-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4ae-126">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="1e4ae-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="1e4ae-127">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1e4ae-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="1e4ae-128">Задает исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-128">Specifies the source rectangle.</span></span> <span data-ttu-id="1e4ae-129">Присвойте этому параметру **значение NULL** , чтобы указать все изображение.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="1e4ae-130">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e4ae-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4ae-131">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e4ae-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e4ae-132">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="1e4ae-133">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="1e4ae-134">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e4ae-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4ae-135">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="1e4ae-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="1e4ae-136">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="1e4ae-137">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="1e4ae-138">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="1e4ae-139">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="1e4ae-140">*псрЦинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1e4ae-140">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4ae-141">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e4ae-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="1e4ae-142">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e4ae-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e4ae-143">Return value</span></span>

<span data-ttu-id="1e4ae-144">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e4ae-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e4ae-145">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1e4ae-146">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-146">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e4ae-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e4ae-147">Remarks</span></span>

<span data-ttu-id="1e4ae-148">Эта функция обрабатывает преобразование в форматы сжатия и из сжатых форматов текстур и поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-148">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="1e4ae-149">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="1e4ae-149">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="1e4ae-150">Запись на поверхность без выравнивания не приведет к обновлению «грязного» прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-150">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="1e4ae-151">Если вызывается **D3DXLoadSurfaceFromFileInMemory** и поверхность не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явно вызвать [**адддиртирект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) на поверхности.</span><span class="sxs-lookup"><span data-stu-id="1e4ae-151">If **D3DXLoadSurfaceFromFileInMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e4ae-152">Требования</span><span class="sxs-lookup"><span data-stu-id="1e4ae-152">Requirements</span></span>



| <span data-ttu-id="1e4ae-153">Требование</span><span class="sxs-lookup"><span data-stu-id="1e4ae-153">Requirement</span></span> | <span data-ttu-id="1e4ae-154">Значение</span><span class="sxs-lookup"><span data-stu-id="1e4ae-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4ae-155">Header</span><span class="sxs-lookup"><span data-stu-id="1e4ae-155">Header</span></span><br/>  | <dl> <span data-ttu-id="1e4ae-156"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e4ae-156"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1e4ae-157">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e4ae-157">Library</span></span><br/> | <dl> <span data-ttu-id="1e4ae-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e4ae-158"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1e4ae-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e4ae-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e4ae-160">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="1e4ae-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
