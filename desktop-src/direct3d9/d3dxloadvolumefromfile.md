---
description: Загружает том из файла.
ms.assetid: ea0fc588-094e-4488-bd82-54507ee0fc91
title: Функция D3DXLoadVolumeFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ff427c58b62d99c2c4716081aab82bd94f146edd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703650"
---
# <a name="d3dxloadvolumefromfile-function"></a><span data-ttu-id="520be-103">Функция D3DXLoadVolumeFromFile</span><span class="sxs-lookup"><span data-stu-id="520be-103">D3DXLoadVolumeFromFile function</span></span>

<span data-ttu-id="520be-104">Загружает том из файла.</span><span class="sxs-lookup"><span data-stu-id="520be-104">Loads a volume from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="520be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="520be-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromFile(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCTSTR           pSrcFile,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="520be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="520be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="520be-107">*пдестволуме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="520be-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520be-108">Тип: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="520be-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="520be-109">Указатель на интерфейс [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="520be-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="520be-110">Указывает целевой том.</span><span class="sxs-lookup"><span data-stu-id="520be-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="520be-111">*пдестпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="520be-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520be-112">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="520be-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="520be-113">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="520be-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="520be-114">*пдестбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="520be-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520be-115">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="520be-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="520be-116">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="520be-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="520be-117">Задает поле назначения.</span><span class="sxs-lookup"><span data-stu-id="520be-117">Specifies the destination box.</span></span> <span data-ttu-id="520be-118">Присвойте этому параметру **значение NULL** , чтобы указать весь том.</span><span class="sxs-lookup"><span data-stu-id="520be-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="520be-119">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="520be-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520be-120">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="520be-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="520be-121">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="520be-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="520be-122">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="520be-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="520be-123">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="520be-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="520be-124">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="520be-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="520be-125">*псркбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="520be-125">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520be-126">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="520be-126">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="520be-127">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="520be-127">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="520be-128">Указывает поле источника.</span><span class="sxs-lookup"><span data-stu-id="520be-128">Specifies the source box.</span></span> <span data-ttu-id="520be-129">Присвойте этому параметру **значение NULL** , чтобы указать весь том.</span><span class="sxs-lookup"><span data-stu-id="520be-129">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="520be-130">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="520be-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520be-131">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="520be-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="520be-132">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md), контролирующих фильтрацию изображения.</span><span class="sxs-lookup"><span data-stu-id="520be-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="520be-133">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="520be-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="520be-134">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="520be-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520be-135">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="520be-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="520be-136">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="520be-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="520be-137">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="520be-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="520be-138">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="520be-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="520be-139">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="520be-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="520be-140">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="520be-140">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520be-141">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="520be-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="520be-142">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="520be-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="520be-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="520be-143">Return value</span></span>

<span data-ttu-id="520be-144">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="520be-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="520be-145">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="520be-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="520be-146">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="520be-146">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="520be-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="520be-147">Remarks</span></span>

<span data-ttu-id="520be-148">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="520be-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="520be-149">Если определен Юникод, вызов функции разрешается в D3DXLoadVolumeFromFileW.</span><span class="sxs-lookup"><span data-stu-id="520be-149">If Unicode is defined, the function call resolves to D3DXLoadVolumeFromFileW.</span></span> <span data-ttu-id="520be-150">В противном случае вызов функции разрешается в D3DXLoadVolumeFromFileA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="520be-150">Otherwise, the function call resolves to D3DXLoadVolumeFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="520be-151">Эта функция обрабатывает преобразование в форматы сжатия и из сжатых форматов текстур и поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="520be-151">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="520be-152">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="520be-152">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="520be-153">Запись на поверхность текстуры, не равную нулю, не приведет к обновлению «грязного» прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="520be-153">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="520be-154">Если вызывается **D3DXLoadVolumeFromFile** и текстура еще не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явным образом вызвать [**IDirect3DVolumeTexture9:: адддиртибокс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) в текстуре тома.</span><span class="sxs-lookup"><span data-stu-id="520be-154">If **D3DXLoadVolumeFromFile** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="520be-155">Требования</span><span class="sxs-lookup"><span data-stu-id="520be-155">Requirements</span></span>



| <span data-ttu-id="520be-156">Требование</span><span class="sxs-lookup"><span data-stu-id="520be-156">Requirement</span></span> | <span data-ttu-id="520be-157">Значение</span><span class="sxs-lookup"><span data-stu-id="520be-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="520be-158">Header</span><span class="sxs-lookup"><span data-stu-id="520be-158">Header</span></span><br/>  | <dl> <span data-ttu-id="520be-159"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="520be-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="520be-160">Библиотека</span><span class="sxs-lookup"><span data-stu-id="520be-160">Library</span></span><br/> | <dl> <span data-ttu-id="520be-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="520be-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="520be-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="520be-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="520be-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="520be-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="520be-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="520be-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="520be-165">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="520be-165">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="520be-166">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="520be-166">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="520be-167">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="520be-167">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
