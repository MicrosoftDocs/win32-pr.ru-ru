---
description: Загружает поверхность из другой поверхности с помощью преобразования цвета.
ms.assetid: eddb420d-fd32-4c09-afec-435887c4e905
title: Функция D3DXLoadSurfaceFromSurface (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b5138ddf540c3e4a87fe65f29938cb3557b2360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821269"
---
# <a name="d3dxloadsurfacefromsurface-function"></a><span data-ttu-id="f1b89-103">Функция D3DXLoadSurfaceFromSurface</span><span class="sxs-lookup"><span data-stu-id="f1b89-103">D3DXLoadSurfaceFromSurface function</span></span>

<span data-ttu-id="f1b89-104">Загружает поверхность из другой поверхности с помощью преобразования цвета.</span><span class="sxs-lookup"><span data-stu-id="f1b89-104">Loads a surface from another surface with color conversion.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b89-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1b89-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromSurface(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPDIRECT3DSURFACE9 pSrcSurface,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="f1b89-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1b89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1b89-107">*пдестсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1b89-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1b89-108">Тип: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="f1b89-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="f1b89-109">Указатель на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="f1b89-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="f1b89-110">Задает поверхность назначения, которая получает изображение.</span><span class="sxs-lookup"><span data-stu-id="f1b89-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="f1b89-111">*пдестпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1b89-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1b89-112">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="f1b89-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="f1b89-113">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f1b89-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f1b89-114">*пдестрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1b89-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1b89-115">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="f1b89-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="f1b89-116">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f1b89-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="f1b89-117">Задает прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="f1b89-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="f1b89-118">Присвойте этому параметру **значение NULL** , чтобы указать всю поверхность.</span><span class="sxs-lookup"><span data-stu-id="f1b89-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="f1b89-119">*псрксурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1b89-119">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1b89-120">Тип: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="f1b89-120">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="f1b89-121">Указатель на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , представляющий поверхность источника.</span><span class="sxs-lookup"><span data-stu-id="f1b89-121">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the source surface.</span></span>

</dd> <dt>

<span data-ttu-id="f1b89-122">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1b89-122">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1b89-123">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="f1b89-123">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="f1b89-124">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , исходную палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f1b89-124">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f1b89-125">*псркрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1b89-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1b89-126">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="f1b89-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="f1b89-127">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f1b89-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="f1b89-128">Задает исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f1b89-128">Specifies the source rectangle.</span></span> <span data-ttu-id="f1b89-129">Присвойте этому параметру **значение NULL** , чтобы указать всю поверхность.</span><span class="sxs-lookup"><span data-stu-id="f1b89-129">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="f1b89-130">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1b89-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1b89-131">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1b89-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1b89-132">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md), управляющих фильтром изображения.</span><span class="sxs-lookup"><span data-stu-id="f1b89-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="f1b89-133">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="f1b89-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="f1b89-134">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1b89-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1b89-135">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="f1b89-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="f1b89-136">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="f1b89-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="f1b89-137">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="f1b89-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="f1b89-138">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="f1b89-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="f1b89-139">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="f1b89-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1b89-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1b89-140">Return value</span></span>

<span data-ttu-id="f1b89-141">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1b89-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1b89-142">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f1b89-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f1b89-143">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="f1b89-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1b89-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1b89-144">Remarks</span></span>

<span data-ttu-id="f1b89-145">Эта функция обрабатывает преобразование в форматы сжатой текстуры и из них.</span><span class="sxs-lookup"><span data-stu-id="f1b89-145">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="f1b89-146">Запись на поверхность без выравнивания не приведет к обновлению «грязного» прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="f1b89-146">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="f1b89-147">Если вызывается **D3DXLoadSurfaceFromSurface** и поверхность не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явно вызвать [**адддиртирект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) на поверхности.</span><span class="sxs-lookup"><span data-stu-id="f1b89-147">If **D3DXLoadSurfaceFromSurface** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b89-148">Требования</span><span class="sxs-lookup"><span data-stu-id="f1b89-148">Requirements</span></span>



| <span data-ttu-id="f1b89-149">Требование</span><span class="sxs-lookup"><span data-stu-id="f1b89-149">Requirement</span></span> | <span data-ttu-id="f1b89-150">Значение</span><span class="sxs-lookup"><span data-stu-id="f1b89-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b89-151">Header</span><span class="sxs-lookup"><span data-stu-id="f1b89-151">Header</span></span><br/>  | <dl> <span data-ttu-id="f1b89-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1b89-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f1b89-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f1b89-153">Library</span></span><br/> | <dl> <span data-ttu-id="f1b89-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1b89-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f1b89-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1b89-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b89-156">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f1b89-156">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
