---
description: Сохраняет поверхность в файле изображения.
ms.assetid: 6320e5ed-e43d-43bf-a746-5478df42941d
title: Функция D3DXSaveSurfaceToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e8bbdd447b7154e150b3469a4b12180252ed516
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694132"
---
# <a name="d3dxsavesurfacetofileinmemory-function"></a><span data-ttu-id="b5223-103">Функция D3DXSaveSurfaceToFileInMemory</span><span class="sxs-lookup"><span data-stu-id="b5223-103">D3DXSaveSurfaceToFileInMemory function</span></span>

<span data-ttu-id="b5223-104">Сохраняет поверхность в файле изображения.</span><span class="sxs-lookup"><span data-stu-id="b5223-104">Saves a surface to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5223-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5223-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DSURFACE9   pSrcSurface,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="b5223-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5223-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5223-107">*ппдестбуф* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b5223-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5223-108">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5223-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b5223-109">Адрес указателя на [**ID3DXBuffer**](id3dxbuffer.md) , который будет хранить изображение.</span><span class="sxs-lookup"><span data-stu-id="b5223-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="b5223-110">*Дестформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5223-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5223-111">Тип: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="b5223-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="b5223-112">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) , указывающий формат файла, используемый при сохранении.</span><span class="sxs-lookup"><span data-stu-id="b5223-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="b5223-113">Эта функция поддерживает сохранение во всех форматах **\_ FILEFORMAT D3DXIMAGE** , кроме переносимых пиксмап (. ppm) и Targa/формат графического адаптера (. TGA).</span><span class="sxs-lookup"><span data-stu-id="b5223-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="b5223-114">*псрксурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5223-114">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5223-115">Тип: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="b5223-115">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="b5223-116">Указатель на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , содержащий изображение для сохранения.</span><span class="sxs-lookup"><span data-stu-id="b5223-116">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="b5223-117">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5223-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5223-118">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="b5223-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="b5223-119">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , содержащую палитру цветов 256.</span><span class="sxs-lookup"><span data-stu-id="b5223-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="b5223-120">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5223-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5223-121">*псркрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5223-121">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5223-122">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="b5223-122">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="b5223-123">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b5223-123">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="b5223-124">Задает исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="b5223-124">Specifies the source rectangle.</span></span> <span data-ttu-id="b5223-125">Присвойте этому параметру **значение NULL** , чтобы указать все изображение.</span><span class="sxs-lookup"><span data-stu-id="b5223-125">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5223-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5223-126">Return value</span></span>

<span data-ttu-id="b5223-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5223-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5223-128">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b5223-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b5223-129">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="b5223-129">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5223-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5223-130">Remarks</span></span>

<span data-ttu-id="b5223-131">Эта функция обрабатывает преобразование в форматы сжатой текстуры и из них.</span><span class="sxs-lookup"><span data-stu-id="b5223-131">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5223-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b5223-132">Requirements</span></span>



| <span data-ttu-id="b5223-133">Требование</span><span class="sxs-lookup"><span data-stu-id="b5223-133">Requirement</span></span> | <span data-ttu-id="b5223-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b5223-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5223-135">Header</span><span class="sxs-lookup"><span data-stu-id="b5223-135">Header</span></span><br/>  | <dl> <span data-ttu-id="b5223-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5223-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b5223-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b5223-137">Library</span></span><br/> | <dl> <span data-ttu-id="b5223-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5223-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b5223-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5223-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5223-140">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b5223-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="b5223-141">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="b5223-141">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
