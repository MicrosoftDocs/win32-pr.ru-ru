---
description: Загружает поверхность из памяти.
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: Функция D3DXLoadSurfaceFromMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffb7be05301ae807505242153be902ab30eecf14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081844"
---
# <a name="d3dxloadsurfacefrommemory-function"></a><span data-ttu-id="e44e3-103">Функция D3DXLoadSurfaceFromMemory</span><span class="sxs-lookup"><span data-stu-id="e44e3-103">D3DXLoadSurfaceFromMemory function</span></span>

<span data-ttu-id="e44e3-104">Загружает поверхность из памяти.</span><span class="sxs-lookup"><span data-stu-id="e44e3-104">Loads a surface from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e44e3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e44e3-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromMemory(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPCVOID            pSrcMemory,
  _In_       D3DFORMAT          SrcFormat,
  _In_       UINT               SrcPitch,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="e44e3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e44e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e44e3-107">*пдестсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44e3-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44e3-108">Тип: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="e44e3-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="e44e3-109">Указатель на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="e44e3-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="e44e3-110">Задает поверхность назначения, которая получает изображение.</span><span class="sxs-lookup"><span data-stu-id="e44e3-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="e44e3-111">*пдестпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44e3-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44e3-112">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="e44e3-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e44e3-113">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e44e3-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e44e3-114">*пдестрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44e3-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44e3-115">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="e44e3-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="e44e3-116">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e44e3-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="e44e3-117">Задает прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="e44e3-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="e44e3-118">Присвойте этому параметру **значение NULL** , чтобы указать всю поверхность.</span><span class="sxs-lookup"><span data-stu-id="e44e3-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="e44e3-119">*псркмемори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44e3-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44e3-120">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e44e3-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e44e3-121">Указатель на левый верхний угол исходного изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="e44e3-121">Pointer to the upper left corner of the source image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="e44e3-122">*Сркформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44e3-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44e3-123">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e44e3-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="e44e3-124">Член перечислимого типа [D3DFORMAT](d3dformat.md) — формат пикселей исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="e44e3-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source image.</span></span>

</dd> <dt>

<span data-ttu-id="e44e3-125">*Сркпитч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44e3-125">*SrcPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44e3-126">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e44e3-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e44e3-127">Шаг исходного изображения в байтах.</span><span class="sxs-lookup"><span data-stu-id="e44e3-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="e44e3-128">Для форматов DXT это число должно представлять ширину одной строки ячеек в байтах.</span><span class="sxs-lookup"><span data-stu-id="e44e3-128">For DXT formats, this number should represent the width of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e44e3-129">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44e3-129">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44e3-130">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="e44e3-130">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e44e3-131">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , исходную палитру 256 цветов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e44e3-131">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e44e3-132">*псркрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44e3-132">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44e3-133">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="e44e3-133">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="e44e3-134">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e44e3-134">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="e44e3-135">Задает размеры исходного изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="e44e3-135">Specifies the dimensions of the source image in memory.</span></span> <span data-ttu-id="e44e3-136">Это значение не может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="e44e3-136">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e44e3-137">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44e3-137">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44e3-138">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e44e3-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e44e3-139">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="e44e3-139">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="e44e3-140">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="e44e3-140">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="e44e3-141">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44e3-141">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44e3-142">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="e44e3-142">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="e44e3-143">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="e44e3-143">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="e44e3-144">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="e44e3-144">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="e44e3-145">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="e44e3-145">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="e44e3-146">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="e44e3-146">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e44e3-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e44e3-147">Return value</span></span>

<span data-ttu-id="e44e3-148">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e44e3-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e44e3-149">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e44e3-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e44e3-150">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="e44e3-150">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="e44e3-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e44e3-151">Remarks</span></span>

<span data-ttu-id="e44e3-152">Эта функция обрабатывает преобразование в форматы сжатой текстуры и из них.</span><span class="sxs-lookup"><span data-stu-id="e44e3-152">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="e44e3-153">Запись на поверхность без выравнивания не приведет к обновлению «грязного» прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="e44e3-153">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="e44e3-154">Если вызывается **D3DXLoadSurfaceFromMemory** и поверхность не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явно вызвать [**адддиртирект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) на поверхности.</span><span class="sxs-lookup"><span data-stu-id="e44e3-154">If **D3DXLoadSurfaceFromMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e44e3-155">Требования</span><span class="sxs-lookup"><span data-stu-id="e44e3-155">Requirements</span></span>



| <span data-ttu-id="e44e3-156">Требование</span><span class="sxs-lookup"><span data-stu-id="e44e3-156">Requirement</span></span> | <span data-ttu-id="e44e3-157">Значение</span><span class="sxs-lookup"><span data-stu-id="e44e3-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e44e3-158">Header</span><span class="sxs-lookup"><span data-stu-id="e44e3-158">Header</span></span><br/>  | <dl> <span data-ttu-id="e44e3-159"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e44e3-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e44e3-160">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e44e3-160">Library</span></span><br/> | <dl> <span data-ttu-id="e44e3-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e44e3-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e44e3-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e44e3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e44e3-163">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e44e3-163">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
