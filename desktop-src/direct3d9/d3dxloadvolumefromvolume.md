---
description: Загружает том из другого тома.
ms.assetid: bc162f91-feb7-4571-ae4a-abaa5e7953f6
title: Функция D3DXLoadVolumeFromVolume (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromVolume
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da2cedf42533fa1d170269e97a366f7e4a1a41f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000456"
---
# <a name="d3dxloadvolumefromvolume-function"></a><span data-ttu-id="6d2b9-103">Функция D3DXLoadVolumeFromVolume</span><span class="sxs-lookup"><span data-stu-id="6d2b9-103">D3DXLoadVolumeFromVolume function</span></span>

<span data-ttu-id="6d2b9-104">Загружает том из другого тома.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-104">Loads a volume from another volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d2b9-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromVolume(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPDIRECT3DVOLUME9 pSrcVolume,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="6d2b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d2b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d2b9-107">*пдестволуме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2b9-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2b9-108">Тип: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="6d2b9-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="6d2b9-109">Указатель на интерфейс [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="6d2b9-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="6d2b9-110">Указывает целевой том, который получает образ.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="6d2b9-111">*пдестпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2b9-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2b9-112">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="6d2b9-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="6d2b9-113">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6d2b9-114">*пдестбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2b9-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2b9-115">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="6d2b9-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="6d2b9-116">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="6d2b9-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="6d2b9-117">Задает поле назначения.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-117">Specifies the destination box.</span></span> <span data-ttu-id="6d2b9-118">Присвойте этому параметру **значение NULL** , чтобы указать весь том.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="6d2b9-119">*псркволуме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2b9-119">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2b9-120">Тип: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="6d2b9-120">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="6d2b9-121">Указатель на интерфейс [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="6d2b9-121">A Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="6d2b9-122">Указывает исходный том.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-122">Specifies the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="6d2b9-123">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2b9-123">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2b9-124">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="6d2b9-124">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="6d2b9-125">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , исходную палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-125">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6d2b9-126">*псркбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2b9-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2b9-127">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="6d2b9-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="6d2b9-128">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="6d2b9-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="6d2b9-129">Указывает поле источника.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-129">Specifies the source box.</span></span> <span data-ttu-id="6d2b9-130">Присвойте этому параметру **значение NULL** , чтобы указать весь том.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="6d2b9-131">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2b9-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2b9-132">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d2b9-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d2b9-133">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md), управляющих фильтром изображения.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-133">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="6d2b9-134">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="6d2b9-135">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2b9-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2b9-136">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="6d2b9-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="6d2b9-137">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="6d2b9-138">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="6d2b9-139">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="6d2b9-140">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d2b9-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d2b9-141">Return value</span></span>

<span data-ttu-id="6d2b9-142">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d2b9-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d2b9-143">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6d2b9-144">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d2b9-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d2b9-145">Remarks</span></span>

<span data-ttu-id="6d2b9-146">Запись на поверхность текстуры, не равную нулю, не приведет к обновлению «грязного» прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-146">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="6d2b9-147">Если вызывается **D3DXLoadVolumeFromVolume** и поверхность не была изменена (это маловероятно в нормальных сценариях использования), приложение должно явным образом вызвать [**IDirect3DVolumeTexture9:: адддиртибокс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) на поверхности.</span><span class="sxs-lookup"><span data-stu-id="6d2b9-147">If **D3DXLoadVolumeFromVolume** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d2b9-148">Требования</span><span class="sxs-lookup"><span data-stu-id="6d2b9-148">Requirements</span></span>



| <span data-ttu-id="6d2b9-149">Требование</span><span class="sxs-lookup"><span data-stu-id="6d2b9-149">Requirement</span></span> | <span data-ttu-id="6d2b9-150">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2b9-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2b9-151">Header</span><span class="sxs-lookup"><span data-stu-id="6d2b9-151">Header</span></span><br/>  | <dl> <span data-ttu-id="6d2b9-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d2b9-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6d2b9-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d2b9-153">Library</span></span><br/> | <dl> <span data-ttu-id="6d2b9-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d2b9-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6d2b9-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d2b9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d2b9-156">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="6d2b9-156">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="6d2b9-157">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="6d2b9-157">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="6d2b9-158">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="6d2b9-158">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="6d2b9-159">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="6d2b9-159">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="6d2b9-160">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6d2b9-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
