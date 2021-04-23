---
description: Сохраняет том в буфере. Метод создает буфер ID3DXBuffer для хранения данных и возвращает этот объект.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: Функция D3DXSaveVolumeToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7daaa41e0cc87ea03a0aedc5fc2f7ca96653329f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273761"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a><span data-ttu-id="d54d9-104">Функция D3DXSaveVolumeToFileInMemory</span><span class="sxs-lookup"><span data-stu-id="d54d9-104">D3DXSaveVolumeToFileInMemory function</span></span>

<span data-ttu-id="d54d9-105">Сохраняет том в буфере.</span><span class="sxs-lookup"><span data-stu-id="d54d9-105">Saves a volume to a buffer.</span></span> <span data-ttu-id="d54d9-106">Метод создает буфер [**ID3DXBuffer**](id3dxbuffer.md) для хранения данных и возвращает этот объект.</span><span class="sxs-lookup"><span data-stu-id="d54d9-106">The method creates an [**ID3DXBuffer**](id3dxbuffer.md) buffer to store the data, and returns that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d54d9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d54d9-107">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="d54d9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d54d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d54d9-109">*ппдестбуф* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d54d9-109">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d54d9-110">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d54d9-110">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d54d9-111">Адрес указателя на буфер [**ID3DXBuffer**](id3dxbuffer.md) , в котором будет храниться изображение.</span><span class="sxs-lookup"><span data-stu-id="d54d9-111">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) buffer that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="d54d9-112">*Дестформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d54d9-112">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d54d9-113">Тип: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="d54d9-113">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="d54d9-114">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) , указывающий формат файла, используемый при сохранении.</span><span class="sxs-lookup"><span data-stu-id="d54d9-114">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="d54d9-115">Эта функция поддерживает сохранение во всех форматах **\_ FILEFORMAT D3DXIMAGE** , кроме переносимых пиксмап (. ppm) и Targa/формат графического адаптера (. TGA).</span><span class="sxs-lookup"><span data-stu-id="d54d9-115">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="d54d9-116">*псркволуме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d54d9-116">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d54d9-117">Тип: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="d54d9-117">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="d54d9-118">Указатель на интерфейс [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) , содержащий изображение для сохранения.</span><span class="sxs-lookup"><span data-stu-id="d54d9-118">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="d54d9-119">*псркпалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d54d9-119">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d54d9-120">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="d54d9-120">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="d54d9-121">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , содержащую палитру цветов 256.</span><span class="sxs-lookup"><span data-stu-id="d54d9-121">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="d54d9-122">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d54d9-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d54d9-123">*псркбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d54d9-123">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d54d9-124">Тип: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="d54d9-124">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="d54d9-125">Указатель на структуру [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="d54d9-125">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="d54d9-126">Указывает поле источника.</span><span class="sxs-lookup"><span data-stu-id="d54d9-126">Specifies the source box.</span></span> <span data-ttu-id="d54d9-127">Присвойте этому параметру **значение NULL** , чтобы указать весь том.</span><span class="sxs-lookup"><span data-stu-id="d54d9-127">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d54d9-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d54d9-128">Return value</span></span>

<span data-ttu-id="d54d9-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d54d9-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d54d9-130">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d54d9-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d54d9-131">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="d54d9-131">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="d54d9-132">Требования</span><span class="sxs-lookup"><span data-stu-id="d54d9-132">Requirements</span></span>



| <span data-ttu-id="d54d9-133">Требование</span><span class="sxs-lookup"><span data-stu-id="d54d9-133">Requirement</span></span> | <span data-ttu-id="d54d9-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d54d9-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d54d9-135">Header</span><span class="sxs-lookup"><span data-stu-id="d54d9-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d54d9-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d54d9-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d54d9-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d54d9-137">Library</span></span><br/> | <dl> <span data-ttu-id="d54d9-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d54d9-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d54d9-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d54d9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d54d9-140">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="d54d9-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="d54d9-141">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="d54d9-141">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
