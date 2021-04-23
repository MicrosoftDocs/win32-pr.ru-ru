---
description: Загружает том из файла в памяти.
ms.assetid: d450b652-3a74-45ea-9506-e05da87821d7
title: Функция D3DXLoadVolumeFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ac67ab66a0072598bfea3b190bdf2c81ceba9a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000346"
---
# <a name="d3dxloadvolumefromfileinmemory-function"></a><span data-ttu-id="d8c1f-103">Функция D3DXLoadVolumeFromFileInMemory</span><span class="sxs-lookup"><span data-stu-id="d8c1f-103">D3DXLoadVolumeFromFileInMemory function</span></span>

<span data-ttu-id="d8c1f-104">Загружает том из файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-104">Loads a volume from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c1f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8c1f-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromFileInMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcData,
  _In_       UINT              SrcDataSize,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d8c1f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8c1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8c1f-107">*пдестволуме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8c1f-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1f-108">Тип: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="d8c1f-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="d8c1f-109">Указатель на интерфейс [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="d8c1f-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="d8c1f-110">Указывает целевой том.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8c1f-111">*пдестпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8c1f-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1f-112">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="d8c1f-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="d8c1f-113">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d8c1f-114">*пдестбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8c1f-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1f-115">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8c1f-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="d8c1f-116">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="d8c1f-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="d8c1f-117">Задает поле назначения.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-117">Specifies the destination box.</span></span> <span data-ttu-id="d8c1f-118">Присвойте этому параметру **значение NULL** , чтобы указать весь том.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8c1f-119">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8c1f-119">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1f-120">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8c1f-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8c1f-121">Указатель на файл в памяти, из которого загружается том.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-121">Pointer to the file in memory from which to load the volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8c1f-122">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8c1f-122">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1f-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8c1f-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8c1f-124">Размер (в байтах) файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-124">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="d8c1f-125">*псркбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8c1f-125">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1f-126">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8c1f-126">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="d8c1f-127">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="d8c1f-127">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="d8c1f-128">Указывает поле источника.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-128">Specifies the source box.</span></span> <span data-ttu-id="d8c1f-129">Присвойте этому параметру **значение NULL** , чтобы указать весь том.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-129">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8c1f-130">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8c1f-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1f-131">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8c1f-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8c1f-132">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md), контролирующих фильтрацию изображения.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="d8c1f-133">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="d8c1f-134">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8c1f-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1f-135">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="d8c1f-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="d8c1f-136">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="d8c1f-137">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="d8c1f-138">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="d8c1f-139">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="d8c1f-140">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8c1f-140">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1f-141">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8c1f-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="d8c1f-142">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8c1f-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8c1f-143">Return value</span></span>

<span data-ttu-id="d8c1f-144">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8c1f-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8c1f-145">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d8c1f-146">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-146">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8c1f-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8c1f-147">Remarks</span></span>

<span data-ttu-id="d8c1f-148">Эта функция обрабатывает преобразование в форматы сжатия и из сжатых форматов текстур и поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-148">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="d8c1f-149">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="d8c1f-149">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="d8c1f-150">Запись на поверхность текстуры, не равную нулю, не приведет к обновлению «грязного» прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-150">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="d8c1f-151">Если вызывается **D3DXLoadVolumeFromFileInMemory** и текстура еще не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явным образом вызвать [**IDirect3DVolumeTexture9:: адддиртибокс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) в текстуре тома.</span><span class="sxs-lookup"><span data-stu-id="d8c1f-151">If **D3DXLoadVolumeFromFileInMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8c1f-152">Требования</span><span class="sxs-lookup"><span data-stu-id="d8c1f-152">Requirements</span></span>



| <span data-ttu-id="d8c1f-153">Требование</span><span class="sxs-lookup"><span data-stu-id="d8c1f-153">Requirement</span></span> | <span data-ttu-id="d8c1f-154">Значение</span><span class="sxs-lookup"><span data-stu-id="d8c1f-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c1f-155">Header</span><span class="sxs-lookup"><span data-stu-id="d8c1f-155">Header</span></span><br/>  | <dl> <span data-ttu-id="d8c1f-156"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8c1f-156"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d8c1f-157">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d8c1f-157">Library</span></span><br/> | <dl> <span data-ttu-id="d8c1f-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8c1f-158"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d8c1f-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8c1f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c1f-160">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="d8c1f-160">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="d8c1f-161">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="d8c1f-161">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="d8c1f-162">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="d8c1f-162">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="d8c1f-163">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="d8c1f-163">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="d8c1f-164">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="d8c1f-164">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
