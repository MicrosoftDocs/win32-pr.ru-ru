---
description: Создает текстуру куба из файла в памяти. Это более сложная функция, чем D3DXCreateCubeTextureFromFileInMemory.
ms.assetid: 598016eb-9ea9-4dca-a297-5708a957da6a
title: Функция D3DXCreateCubeTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7813d4532bbde18a5fc7fd7d1d090dc72eccd61f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081928"
---
# <a name="d3dxcreatecubetexturefromfileinmemoryex-function"></a><span data-ttu-id="46744-104">Функция D3DXCreateCubeTextureFromFileInMemoryEx</span><span class="sxs-lookup"><span data-stu-id="46744-104">D3DXCreateCubeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="46744-105">Создает текстуру куба из файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="46744-105">Creates a cube texture from a file in memory.</span></span> <span data-ttu-id="46744-106">Это более сложная функция, чем [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="46744-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="46744-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46744-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    LPCVOID                pSrcData,
  _In_    UINT                   SrcDataSize,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="46744-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="46744-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46744-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46744-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="46744-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="46744-111">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой Куба.</span><span class="sxs-lookup"><span data-stu-id="46744-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="46744-112">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46744-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-113">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46744-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46744-114">Указатель на файл в памяти, из которого создается текстура Куба.</span><span class="sxs-lookup"><span data-stu-id="46744-114">Pointer to the file in memory from which to create the cube texture.</span></span> <span data-ttu-id="46744-115">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="46744-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="46744-116">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46744-116">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46744-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46744-118">Размер файла в памяти, в байтах.</span><span class="sxs-lookup"><span data-stu-id="46744-118">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="46744-119">*Размер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46744-119">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46744-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46744-121">Ширина (или высота) в пикселях.</span><span class="sxs-lookup"><span data-stu-id="46744-121">Width (or height) in pixels.</span></span> <span data-ttu-id="46744-122">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="46744-122">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="46744-123">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46744-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-124">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46744-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46744-125">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="46744-125">Number of mip levels requested.</span></span> <span data-ttu-id="46744-126">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="46744-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="46744-127">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46744-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-128">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46744-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46744-129">0, D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="46744-129">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="46744-130">Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="46744-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="46744-131">Затем ресурс можно передать в параметр *пневрендертаржет* метода [**сетрендертаржет**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="46744-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="46744-132">Если указан параметр D3DUSAGE \_ рендертаржет, приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="46744-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="46744-133">Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="46744-133">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="46744-134">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46744-134">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-135">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="46744-135">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="46744-136">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="46744-136">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="46744-137">Возвращаемая текстура может иметь другой формат, заданный в *формате*.</span><span class="sxs-lookup"><span data-stu-id="46744-137">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="46744-138">Приложения должны проверять формат возвращенной текстуры.</span><span class="sxs-lookup"><span data-stu-id="46744-138">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="46744-139">Если [D3DFMT \_ Unknown](other-d3dx-constants.md), то формат берется из файла.</span><span class="sxs-lookup"><span data-stu-id="46744-139">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="46744-140">Если D3DFMT \_ из \_ файла, формат принимается точно так же, как в файле, и вызов завершается ошибкой, если это нарушает возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="46744-140">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="46744-141">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46744-141">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-142">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="46744-142">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="46744-143">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура Куба.</span><span class="sxs-lookup"><span data-stu-id="46744-143">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="46744-144">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46744-144">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-145">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46744-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46744-146">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="46744-146">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="46744-147">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="46744-147">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="46744-148">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46744-148">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-149">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46744-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46744-150">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="46744-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="46744-151">Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="46744-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="46744-152">Кроме того, используйте BITS 27-31, чтобы указать число MIP уровней, которые будут пропущены (в верхней части цепочки mipmap) при загрузке текстуры. DDS в память. Это позволяет пропустить до 32 уровней.</span><span class="sxs-lookup"><span data-stu-id="46744-152">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="46744-153">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46744-153">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-154">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="46744-154">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="46744-155">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="46744-155">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="46744-156">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="46744-156">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="46744-157">Значение альфа имеет большое значение, поэтому для непрозрачных цветовых ключей обычно должно быть задано FF.</span><span class="sxs-lookup"><span data-stu-id="46744-157">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="46744-158">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="46744-158">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="46744-159">*псрЦинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="46744-159">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-160">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="46744-160">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="46744-161">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="46744-161">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="46744-162">*ппалетте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46744-162">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-163">Тип: **[ **палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="46744-163">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="46744-164">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , представляющую 256-цветную палитру для заполнения, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="46744-164">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="46744-165">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="46744-165">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="46744-166">*ппкубетекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46744-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46744-167">Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="46744-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="46744-168">Адрес указателя на интерфейс [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий созданный объект текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="46744-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46744-169">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46744-169">Return value</span></span>

<span data-ttu-id="46744-170">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46744-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46744-171">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="46744-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="46744-172">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE, D3DERR \_ аутофвидеомемори, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="46744-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="46744-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46744-173">Remarks</span></span>

<span data-ttu-id="46744-174">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="46744-174">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="46744-175">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="46744-175">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="46744-176">Текстуры Куба отличаются от других поверхностей тем, что они являются коллекциями поверхностей.</span><span class="sxs-lookup"><span data-stu-id="46744-176">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="46744-177">Чтобы вызвать [**сетрендертаржет**](/windows/desktop/api) с текстурой Куба, необходимо выбрать отдельное лицо с помощью [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) и передать полученную область в **сетрендертаржет** .</span><span class="sxs-lookup"><span data-stu-id="46744-177">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget** .</span></span>

<span data-ttu-id="46744-178">Этот метод предназначен для использования при загрузке файлов изображений, хранящихся в виде RT \_ RCDATA, который является определяемым приложением ресурсом (необработанные данные).</span><span class="sxs-lookup"><span data-stu-id="46744-178">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="46744-179">В противном случае этот метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="46744-179">Otherwise this method will fail.</span></span>

<span data-ttu-id="46744-180">Дополнительные сведения о [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)см. в разделе пакет SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="46744-180">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="46744-181">Обратите внимание, что начиная с DirectX 8,0, член Пефлагс структуры **палеттинтри** не работает, как описано в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="46744-181">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="46744-182">Теперь элемент Пефлагс является альфа-каналом для 8 – разрядных форматов палеттизед.</span><span class="sxs-lookup"><span data-stu-id="46744-182">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="46744-183">**D3DXCreateCubeTextureFromFileInMemoryEx** использует формат файла поверхности DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="46744-183">**D3DXCreateCubeTextureFromFileInMemoryEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="46744-184">Редактор текстур DirectX (Dxtex.exe) позволяет создать карту Куба на основе других форматов файлов и сохранить ее в формате файлов DDS.</span><span class="sxs-lookup"><span data-stu-id="46744-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="46744-185">Вы можете получить Dxtex.exe и узнать о нем из пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="46744-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="46744-186">Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="46744-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="46744-187">При пропуске mipmap уровней при загрузке DDS-файла используйте \_ макрос D3DX пропуска \_ DDS \_ MIP \_ Levels, чтобы создать значение мипфилтер.</span><span class="sxs-lookup"><span data-stu-id="46744-187">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="46744-188">Этот макрос принимает количество пропускаемых уровней, а тип фильтра и возвращает значение фильтра, которое затем передается в параметр Мипфилтер.</span><span class="sxs-lookup"><span data-stu-id="46744-188">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="46744-189">Требования</span><span class="sxs-lookup"><span data-stu-id="46744-189">Requirements</span></span>



| <span data-ttu-id="46744-190">Требование</span><span class="sxs-lookup"><span data-stu-id="46744-190">Requirement</span></span> | <span data-ttu-id="46744-191">Значение</span><span class="sxs-lookup"><span data-stu-id="46744-191">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46744-192">Header</span><span class="sxs-lookup"><span data-stu-id="46744-192">Header</span></span><br/>  | <dl> <span data-ttu-id="46744-193"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="46744-193"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="46744-194">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46744-194">Library</span></span><br/> | <dl> <span data-ttu-id="46744-195"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46744-195"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="46744-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46744-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46744-197">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="46744-197">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
