---
description: Загружает поверхность из ресурса.
ms.assetid: 16d49f61-8c84-4e15-aacc-1d26099e65e0
title: Функция D3DXLoadSurfaceFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae802a1b7e18ce5f2b0a11c6679628ea1deb25aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000312"
---
# <a name="d3dxloadsurfacefromresource-function"></a><span data-ttu-id="ef361-103">Функция D3DXLoadSurfaceFromResource</span><span class="sxs-lookup"><span data-stu-id="ef361-103">D3DXLoadSurfaceFromResource function</span></span>

<span data-ttu-id="ef361-104">Загружает поверхность из ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef361-104">Loads a surface from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef361-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef361-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromResource(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          HMODULE            hSrcModule,
  _In_          LPCTSTR            pSrcResource,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ef361-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef361-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef361-107">*пдестсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef361-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef361-108">Тип: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="ef361-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="ef361-109">Указатель на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="ef361-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="ef361-110">Задает поверхность назначения, которая получает изображение.</span><span class="sxs-lookup"><span data-stu-id="ef361-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="ef361-111">*пдестпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef361-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef361-112">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="ef361-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ef361-113">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ef361-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ef361-114">*пдестрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef361-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef361-115">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="ef361-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="ef361-116">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ef361-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="ef361-117">Задает прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="ef361-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="ef361-118">Присвойте этому параметру **значение NULL** , чтобы указать всю поверхность.</span><span class="sxs-lookup"><span data-stu-id="ef361-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="ef361-119">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef361-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef361-120">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef361-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ef361-121">Указатель на модуль, в котором находится ресурс, или **значение NULL** для модуля, связанного с образом, операционной системой, используемой для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="ef361-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="ef361-122">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef361-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef361-123">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef361-123">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ef361-124">Указатель на строку, указывающую имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef361-124">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="ef361-125">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="ef361-125">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ef361-126">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ef361-126">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ef361-127">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="ef361-127">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ef361-128">*псркрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef361-128">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef361-129">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="ef361-129">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="ef361-130">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ef361-130">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="ef361-131">Задает исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="ef361-131">Specifies the source rectangle.</span></span> <span data-ttu-id="ef361-132">Присвойте этому параметру **значение NULL** , чтобы указать все изображение.</span><span class="sxs-lookup"><span data-stu-id="ef361-132">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="ef361-133">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef361-133">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef361-134">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef361-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ef361-135">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="ef361-135">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ef361-136">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="ef361-136">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ef361-137">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef361-137">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef361-138">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ef361-138">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ef361-139">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="ef361-139">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ef361-140">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="ef361-140">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ef361-141">Альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей. Таким образом, для непрозрачного черного значения будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="ef361-141">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="ef361-142">*псрЦинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ef361-142">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef361-143">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef361-143">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ef361-144">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="ef361-144">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef361-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef361-145">Return value</span></span>

<span data-ttu-id="ef361-146">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef361-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef361-147">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ef361-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ef361-148">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ef361-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef361-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef361-149">Remarks</span></span>

<span data-ttu-id="ef361-150">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="ef361-150">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ef361-151">Если определен Юникод, вызов функции разрешается в D3DXLoadSurfaceFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="ef361-151">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromResourceW.</span></span> <span data-ttu-id="ef361-152">В противном случае вызов функции разрешается в D3DXLoadSurfaceFromResourceA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="ef361-152">Otherwise, the function call resolves to D3DXLoadSurfaceFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="ef361-153">Загружаемый ресурс должен иметь тип \_ Bitmap или "RT RCDATA" \_ .</span><span class="sxs-lookup"><span data-stu-id="ef361-153">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="ef361-154">Тип ресурса RT \_ RCDATA используется для загрузки форматов, отличных от точечных рисунков (таких как. TGA,. jpg и. DDS).</span><span class="sxs-lookup"><span data-stu-id="ef361-154">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="ef361-155">Эта функция обрабатывает преобразование в форматы сжатой текстуры и из них.</span><span class="sxs-lookup"><span data-stu-id="ef361-155">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="ef361-156">Запись на поверхность без выравнивания не приведет к обновлению «грязного» прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ef361-156">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="ef361-157">Если вызывается [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) и поверхность не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явно вызвать [**адддиртирект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) на поверхности.</span><span class="sxs-lookup"><span data-stu-id="ef361-157">If [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef361-158">Требования</span><span class="sxs-lookup"><span data-stu-id="ef361-158">Requirements</span></span>



| <span data-ttu-id="ef361-159">Требование</span><span class="sxs-lookup"><span data-stu-id="ef361-159">Requirement</span></span> | <span data-ttu-id="ef361-160">Значение</span><span class="sxs-lookup"><span data-stu-id="ef361-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef361-161">Header</span><span class="sxs-lookup"><span data-stu-id="ef361-161">Header</span></span><br/>  | <dl> <span data-ttu-id="ef361-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef361-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ef361-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef361-163">Library</span></span><br/> | <dl> <span data-ttu-id="ef361-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef361-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ef361-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef361-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef361-166">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ef361-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
