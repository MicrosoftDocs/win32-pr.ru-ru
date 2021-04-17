---
description: Загружает том из памяти.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: Функция D3DXLoadVolumeFromMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d6c3f1bdfe40f19eeb57b4f0d8a38c40a239404
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703649"
---
# <a name="d3dxloadvolumefrommemory-function"></a><span data-ttu-id="7a7bc-103">Функция D3DXLoadVolumeFromMemory</span><span class="sxs-lookup"><span data-stu-id="7a7bc-103">D3DXLoadVolumeFromMemory function</span></span>

<span data-ttu-id="7a7bc-104">Загружает том из памяти.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-104">Loads a volume from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a7bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a7bc-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="7a7bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a7bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a7bc-107">*пдестволуме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a7bc-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7bc-108">Тип: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="7a7bc-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="7a7bc-109">Указатель на интерфейс [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="7a7bc-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="7a7bc-110">Указывает целевой том, который получает образ.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="7a7bc-111">*пдестпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a7bc-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7bc-112">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="7a7bc-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="7a7bc-113">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7a7bc-114">*пдестбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a7bc-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7bc-115">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a7bc-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="7a7bc-116">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="7a7bc-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="7a7bc-117">Задает поле назначения.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-117">Specifies the destination box.</span></span> <span data-ttu-id="7a7bc-118">Присвойте этому параметру **значение NULL** , чтобы указать весь том.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="7a7bc-119">*псркмемори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a7bc-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7bc-120">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a7bc-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a7bc-121">Указатель на левый верхний угол исходного тома в памяти.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-121">Pointer to the top-left corner of the source volume in memory.</span></span>

</dd> <dt>

<span data-ttu-id="7a7bc-122">*Сркформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a7bc-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7bc-123">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="7a7bc-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="7a7bc-124">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , являющийся форматом пикселей исходного тома.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="7a7bc-125">*Сркровпитч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a7bc-125">*SrcRowPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7bc-126">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a7bc-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a7bc-127">Шаг исходного изображения в байтах.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="7a7bc-128">Для форматов DXT (сжатых форматов текстур) это число должно представлять размер одной строки ячеек в байтах.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-128">For DXT formats (compressed texture formats), this number should represent the size of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7a7bc-129">*Сркслицепитч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a7bc-129">*SrcSlicePitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7bc-130">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a7bc-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a7bc-131">Шаг исходного изображения в байтах.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-131">Pitch of source image, in bytes.</span></span> <span data-ttu-id="7a7bc-132">Для форматов DXT (сжатых форматов текстур) это число должно представлять размер одного среза ячеек в байтах.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-132">For DXT formats (compressed texture formats), this number should represent the size of one slice of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7a7bc-133">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a7bc-133">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7bc-134">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="7a7bc-134">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="7a7bc-135">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , исходную палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-135">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7a7bc-136">*псркбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a7bc-136">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7bc-137">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a7bc-137">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="7a7bc-138">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="7a7bc-138">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="7a7bc-139">Указывает поле источника.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-139">Specifies the source box.</span></span> <span data-ttu-id="7a7bc-140">Значение **null** не является допустимым значением для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-140">**NULL** is not a valid value for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7a7bc-141">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a7bc-141">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7bc-142">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a7bc-142">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a7bc-143">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-143">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="7a7bc-144">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-144">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="7a7bc-145">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a7bc-145">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7bc-146">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="7a7bc-146">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="7a7bc-147">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-147">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="7a7bc-148">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-148">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="7a7bc-149">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-149">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="7a7bc-150">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-150">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a7bc-151">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a7bc-151">Return value</span></span>

<span data-ttu-id="7a7bc-152">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7a7bc-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7a7bc-153">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7a7bc-154">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-154">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a7bc-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a7bc-155">Remarks</span></span>

<span data-ttu-id="7a7bc-156">Запись на поверхность текстуры, не равную нулю, не приведет к обновлению «грязного» прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-156">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="7a7bc-157">Если вызывается **D3DXLoadVolumeFromMemory** и текстура еще не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явным образом вызвать [**IDirect3DVolumeTexture9:: адддиртибокс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) в текстуре тома.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-157">If **D3DXLoadVolumeFromMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a7bc-158">Требования</span><span class="sxs-lookup"><span data-stu-id="7a7bc-158">Requirements</span></span>



| <span data-ttu-id="7a7bc-159">Требование</span><span class="sxs-lookup"><span data-stu-id="7a7bc-159">Requirement</span></span> | <span data-ttu-id="7a7bc-160">Значение</span><span class="sxs-lookup"><span data-stu-id="7a7bc-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a7bc-161">Header</span><span class="sxs-lookup"><span data-stu-id="7a7bc-161">Header</span></span><br/>  | <dl> <span data-ttu-id="7a7bc-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a7bc-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="7a7bc-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7a7bc-163">Library</span></span><br/> | <dl> <span data-ttu-id="7a7bc-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a7bc-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7a7bc-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a7bc-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a7bc-166">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="7a7bc-166">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="7a7bc-167">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="7a7bc-167">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="7a7bc-168">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="7a7bc-168">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="7a7bc-169">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="7a7bc-169">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
