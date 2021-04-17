---
description: Загружает том из ресурса.
ms.assetid: 3fa1243b-5e31-4737-8d3c-08852d6528d9
title: Функция D3DXLoadVolumeFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d57ce492db24ac9920662d4de5baed4650dd801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703648"
---
# <a name="d3dxloadvolumefromresource-function"></a><span data-ttu-id="1a19f-103">Функция D3DXLoadVolumeFromResource</span><span class="sxs-lookup"><span data-stu-id="1a19f-103">D3DXLoadVolumeFromResource function</span></span>

<span data-ttu-id="1a19f-104">Загружает том из ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a19f-104">Loads a volume from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a19f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a19f-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromResource(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       HMODULE           hSrcModule,
  _In_       LPCSTR            pSrcResource,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1a19f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a19f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a19f-107">*пдестволуме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a19f-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a19f-108">Тип: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="1a19f-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="1a19f-109">Указатель на интерфейс [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="1a19f-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="1a19f-110">Указывает целевой том.</span><span class="sxs-lookup"><span data-stu-id="1a19f-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="1a19f-111">*пдестпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a19f-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a19f-112">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="1a19f-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="1a19f-113">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1a19f-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1a19f-114">*пдестбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a19f-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a19f-115">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a19f-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="1a19f-116">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="1a19f-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="1a19f-117">Задает поле назначения.</span><span class="sxs-lookup"><span data-stu-id="1a19f-117">Specifies the destination box.</span></span> <span data-ttu-id="1a19f-118">Присвойте этому параметру **значение NULL** , чтобы указать весь том.</span><span class="sxs-lookup"><span data-stu-id="1a19f-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="1a19f-119">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a19f-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a19f-120">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a19f-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a19f-121">Указатель на модуль, в котором находится ресурс, или **значение NULL** для модуля, связанного с образом, операционной системой, используемой для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="1a19f-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="1a19f-122">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a19f-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a19f-123">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a19f-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a19f-124">Указатель на строку, указывающую имя файла исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="1a19f-124">Pointer to a string that specifies the file name of the source image.</span></span> <span data-ttu-id="1a19f-125">Если определен Юникод или \_ Unicode, этот параметр имеет тип лпквстр, в противном случае — тип LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="1a19f-125">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="1a19f-126">*псркбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a19f-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a19f-127">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a19f-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="1a19f-128">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="1a19f-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="1a19f-129">Указывает поле источника.</span><span class="sxs-lookup"><span data-stu-id="1a19f-129">Specifies the source box.</span></span> <span data-ttu-id="1a19f-130">Присвойте этому параметру **значение NULL** , чтобы указать весь том.</span><span class="sxs-lookup"><span data-stu-id="1a19f-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="1a19f-131">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a19f-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a19f-132">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a19f-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a19f-133">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md), контролирующих фильтрацию изображения.</span><span class="sxs-lookup"><span data-stu-id="1a19f-133">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="1a19f-134">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="1a19f-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="1a19f-135">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a19f-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a19f-136">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="1a19f-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="1a19f-137">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="1a19f-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="1a19f-138">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="1a19f-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="1a19f-139">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="1a19f-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="1a19f-140">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="1a19f-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="1a19f-141">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a19f-141">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a19f-142">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a19f-142">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="1a19f-143">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="1a19f-143">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a19f-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a19f-144">Return value</span></span>

<span data-ttu-id="1a19f-145">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1a19f-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1a19f-146">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1a19f-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1a19f-147">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="1a19f-147">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a19f-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a19f-148">Remarks</span></span>

<span data-ttu-id="1a19f-149">Загружаемый ресурс должен быть ресурсом Bitmap ( \_ точечный рисунок RT).</span><span class="sxs-lookup"><span data-stu-id="1a19f-149">The resource being loaded must be a bitmap resource(RT\_BITMAP).</span></span>

<span data-ttu-id="1a19f-150">Эта функция обрабатывает преобразование в форматы сжатой текстуры и из них.</span><span class="sxs-lookup"><span data-stu-id="1a19f-150">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="1a19f-151">Запись на поверхность текстуры, не равную нулю, не приведет к обновлению «грязного» прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="1a19f-151">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="1a19f-152">Если вызывается [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) и текстура еще не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явным образом вызвать [**IDirect3DVolumeTexture9:: адддиртибокс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) в текстуре тома.</span><span class="sxs-lookup"><span data-stu-id="1a19f-152">If [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

<span data-ttu-id="1a19f-153">Эта функция поддерживает строки в Юникоде и ANSI.</span><span class="sxs-lookup"><span data-stu-id="1a19f-153">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a19f-154">Требования</span><span class="sxs-lookup"><span data-stu-id="1a19f-154">Requirements</span></span>



| <span data-ttu-id="1a19f-155">Требование</span><span class="sxs-lookup"><span data-stu-id="1a19f-155">Requirement</span></span> | <span data-ttu-id="1a19f-156">Значение</span><span class="sxs-lookup"><span data-stu-id="1a19f-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a19f-157">Header</span><span class="sxs-lookup"><span data-stu-id="1a19f-157">Header</span></span><br/>  | <dl> <span data-ttu-id="1a19f-158"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a19f-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1a19f-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1a19f-159">Library</span></span><br/> | <dl> <span data-ttu-id="1a19f-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a19f-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1a19f-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a19f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a19f-162">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="1a19f-162">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="1a19f-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="1a19f-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="1a19f-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="1a19f-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="1a19f-165">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="1a19f-165">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="1a19f-166">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="1a19f-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
