---
description: Создает текстуру из файла. Это более сложная функция, чем D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: Функция D3DXCreateTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4dba1424f98389a9282fdebf9dae55c7e1601f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914723"
---
# <a name="d3dxcreatetexturefromfileex-function"></a><span data-ttu-id="44db9-104">Функция D3DXCreateTextureFromFileEx</span><span class="sxs-lookup"><span data-stu-id="44db9-104">D3DXCreateTextureFromFileEx function</span></span>

<span data-ttu-id="44db9-105">Создает текстуру из файла.</span><span class="sxs-lookup"><span data-stu-id="44db9-105">Creates a texture from a file.</span></span> <span data-ttu-id="44db9-106">Это более сложная функция, чем [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="44db9-106">This is a more advanced function than [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="44db9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44db9-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="44db9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="44db9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44db9-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44db9-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="44db9-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="44db9-111">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="44db9-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-112">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44db9-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-113">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44db9-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44db9-114">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="44db9-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="44db9-115">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="44db9-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="44db9-116">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="44db9-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="44db9-117">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="44db9-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-118">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44db9-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44db9-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44db9-120">Ширина в пикселях.</span><span class="sxs-lookup"><span data-stu-id="44db9-120">Width in pixels.</span></span> <span data-ttu-id="44db9-121">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла и округляются в степень двух.</span><span class="sxs-lookup"><span data-stu-id="44db9-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="44db9-122">Если устройство поддерживает не мощность 2 текстур и [D3DX \_ по умолчанию \_ NONPOW2](other-d3dx-constants.md) , то размер не будет округляться.</span><span class="sxs-lookup"><span data-stu-id="44db9-122">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is specified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-123">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44db9-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-124">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44db9-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44db9-125">Высота в пикселях.</span><span class="sxs-lookup"><span data-stu-id="44db9-125">Height, in pixels.</span></span> <span data-ttu-id="44db9-126">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла и округляются в степень двух.</span><span class="sxs-lookup"><span data-stu-id="44db9-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="44db9-127">Если устройство поддерживает 2 текстуры, а [D3DX \_ по умолчанию \_ NONPOW2](other-d3dx-constants.md) — сепЦифиед, то размер не будет округляться.</span><span class="sxs-lookup"><span data-stu-id="44db9-127">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is sepcified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-128">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44db9-128">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-129">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44db9-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44db9-130">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="44db9-130">Number of mip levels requested.</span></span> <span data-ttu-id="44db9-131">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="44db9-131">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="44db9-132">Если D3DX \_ из \_ файла, размер будет задаваться точно так же, как в файле, и вызов завершится ошибкой, если это нарушает возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="44db9-132">If D3DX\_FROM\_FILE, the size will be taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-133">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44db9-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-134">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44db9-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44db9-135">0, [**D3DUSAGE \_ Рендертаржет**](d3dusage.md)или **D3DUSAGE \_ dynamic**.</span><span class="sxs-lookup"><span data-stu-id="44db9-135">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="44db9-136">Установка этого флага в значение **D3DUSAGE \_ рендертаржет** указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="44db9-136">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="44db9-137">Затем ресурс можно передать в параметр *пневрендертаржет* метода [**сетрендертаржет**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="44db9-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="44db9-138">Если указано значение **D3DUSAGE \_ Рендертаржет** или **D3DUSAGE \_ dynamic** , для *пула* должно быть задано значение D3DPOOL \_ по умолчанию, и приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="44db9-138">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="44db9-139">**D3DUSAGE \_ DYNAMIC** указывает, что поверхность должна обрабатываться динамически.</span><span class="sxs-lookup"><span data-stu-id="44db9-139">**D3DUSAGE\_DYNAMIC** indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="44db9-140">См. раздел [Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="44db9-140">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="44db9-141">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44db9-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-142">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="44db9-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="44db9-143">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры.</span><span class="sxs-lookup"><span data-stu-id="44db9-143">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="44db9-144">Возвращаемая текстура может иметь другой формат, заданный в *формате*.</span><span class="sxs-lookup"><span data-stu-id="44db9-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="44db9-145">Приложения должны проверять формат возвращенной текстуры.</span><span class="sxs-lookup"><span data-stu-id="44db9-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="44db9-146">Если D3DFMT \_ Unknown, то формат берется из файла.</span><span class="sxs-lookup"><span data-stu-id="44db9-146">If D3DFMT\_UNKNOWN, the format is taken from the file.</span></span> <span data-ttu-id="44db9-147">Если D3DFMT \_ из \_ файла, формат принимается точно так же, как в файле, и вызов завершается ошибкой, если это нарушает возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="44db9-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-148">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44db9-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-149">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="44db9-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="44db9-150">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.</span><span class="sxs-lookup"><span data-stu-id="44db9-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-151">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44db9-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-152">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44db9-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44db9-153">Сочетание одной или нескольких констант [ \_ фильтра D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="44db9-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="44db9-154">Указание [D3DX \_ по умолчанию](other-d3dx-constants.md) для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="44db9-154">Specifying [D3DX\_DEFAULT](other-d3dx-constants.md) for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-155">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44db9-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-156">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44db9-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44db9-157">Сочетание одной или нескольких констант [ \_ фильтра D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="44db9-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="44db9-158">Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="44db9-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="44db9-159">Кроме того, используйте BITS 27-31, чтобы указать число MIP уровней, которые будут пропущены (в верхней части цепочки mipmap) при загрузке текстуры. DDS в память. Это позволяет пропустить до 32 уровней.</span><span class="sxs-lookup"><span data-stu-id="44db9-159">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-160">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44db9-160">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-161">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="44db9-161">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="44db9-162">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ключ цвета.</span><span class="sxs-lookup"><span data-stu-id="44db9-162">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the color key.</span></span> <span data-ttu-id="44db9-163">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="44db9-163">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="44db9-164">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="44db9-164">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="44db9-165">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="44db9-165">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-166">*псрЦинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="44db9-166">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-167">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="44db9-167">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="44db9-168">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) , которая будет заполнена описанием данных в исходном файле изображения, или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="44db9-168">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-169">*ппалетте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="44db9-169">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-170">Тип: **[ **палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="44db9-170">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="44db9-171">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , представляющую 256-цветную палитру для заполнения, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="44db9-171">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="44db9-172">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="44db9-172">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44db9-173">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="44db9-173">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="44db9-174">Адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="44db9-174">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44db9-175">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44db9-175">Return value</span></span>

<span data-ttu-id="44db9-176">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44db9-176">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44db9-177">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="44db9-177">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="44db9-178">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE, D3DERR \_ аутофвидеомемори, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="44db9-178">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="44db9-179">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44db9-179">Remarks</span></span>

<span data-ttu-id="44db9-180">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="44db9-180">The compiler setting also determines the function version.</span></span> <span data-ttu-id="44db9-181">Если определен Юникод, вызов функции разрешается в D3DXCreateTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="44db9-181">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileExW.</span></span> <span data-ttu-id="44db9-182">В противном случае вызов функции разрешается в D3DXCreateTextureFromFileExA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="44db9-182">Otherwise, the function call resolves to D3DXCreateTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="44db9-183">Используйте [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) , чтобы определить, может ли устройство поддерживать текстуру в текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="44db9-183">Use [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to determine if your device can support the texture given the current state.</span></span>

<span data-ttu-id="44db9-184">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="44db9-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="44db9-185">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="44db9-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="44db9-186">Текстуры мипмаппед автоматически имеют каждый уровень, заполненный загруженной текстурой.</span><span class="sxs-lookup"><span data-stu-id="44db9-186">Mipmapped textures automatically have each level filled with the loaded texture.</span></span> <span data-ttu-id="44db9-187">При загрузке изображений в текстуры мипмаппед некоторые устройства не могут подключиться к образу 1x1, и эта функция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="44db9-187">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="44db9-188">Если это происходит, образы необходимо загружать вручную.</span><span class="sxs-lookup"><span data-stu-id="44db9-188">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="44db9-189">Для лучшей производительности при использовании **D3DXCreateTextureFromFileEx**:</span><span class="sxs-lookup"><span data-stu-id="44db9-189">For the best performance when using **D3DXCreateTextureFromFileEx**:</span></span>

1.  <span data-ttu-id="44db9-190">Масштабирование изображения и преобразование формата во время загрузки могут выполняться слишком долго.</span><span class="sxs-lookup"><span data-stu-id="44db9-190">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="44db9-191">Храните изображения в формате и разрешении, которые они будут использовать.</span><span class="sxs-lookup"><span data-stu-id="44db9-191">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="44db9-192">Если целевому оборудованию требуется сила 2 измерений, создайте и сохраните образы с использованием возможностей 2 измерений.</span><span class="sxs-lookup"><span data-stu-id="44db9-192">If the target hardware requires power of 2 dimensions, then create and store images using power of 2 dimensions.</span></span>
2.  <span data-ttu-id="44db9-193">Для создания образа mipmap во время загрузки отфильтруйте с помощью [ \_ \_ поля фильтра D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="44db9-193">For mipmap image creation at load time, filter using [D3DX\_FILTER\_BOX](d3dx-filter.md).</span></span> <span data-ttu-id="44db9-194">Фильтр Box работает гораздо быстрее, чем другие типы фильтров, такие как D3DX \_ фильтр \_ .</span><span class="sxs-lookup"><span data-stu-id="44db9-194">A box filter is much faster than other filter types such as D3DX\_FILTER\_TRIANGLE.</span></span>
3.  <span data-ttu-id="44db9-195">Рассмотрите возможность использования файлов DDS.</span><span class="sxs-lookup"><span data-stu-id="44db9-195">Consider using DDS files.</span></span> <span data-ttu-id="44db9-196">Так как файлы DDS можно использовать для представления любого формата текстуры Direct3D 9, они очень просты в D3DX для чтения.</span><span class="sxs-lookup"><span data-stu-id="44db9-196">Since DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="44db9-197">Кроме того, они могут хранить MIP-карты, поэтому для создания образов можно использовать любые алгоритмы создания mipmap.</span><span class="sxs-lookup"><span data-stu-id="44db9-197">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

<span data-ttu-id="44db9-198">При пропуске mipmap уровней при загрузке DDS-файла используйте \_ макрос D3DX пропуска \_ DDS \_ MIP \_ Levels, чтобы создать значение мипфилтер.</span><span class="sxs-lookup"><span data-stu-id="44db9-198">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="44db9-199">Этот макрос принимает количество пропускаемых уровней, а тип фильтра и возвращает значение фильтра, которое затем передается в параметр Мипфилтер.</span><span class="sxs-lookup"><span data-stu-id="44db9-199">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="44db9-200">Требования</span><span class="sxs-lookup"><span data-stu-id="44db9-200">Requirements</span></span>



| <span data-ttu-id="44db9-201">Требование</span><span class="sxs-lookup"><span data-stu-id="44db9-201">Requirement</span></span> | <span data-ttu-id="44db9-202">Значение</span><span class="sxs-lookup"><span data-stu-id="44db9-202">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44db9-203">Header</span><span class="sxs-lookup"><span data-stu-id="44db9-203">Header</span></span><br/>  | <dl> <span data-ttu-id="44db9-204"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="44db9-204"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="44db9-205">Библиотека</span><span class="sxs-lookup"><span data-stu-id="44db9-205">Library</span></span><br/> | <dl> <span data-ttu-id="44db9-206"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44db9-206"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="44db9-207">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44db9-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44db9-208">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="44db9-208">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="44db9-209">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="44db9-209">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
