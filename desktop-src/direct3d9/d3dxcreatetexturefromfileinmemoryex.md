---
description: Создает текстуру из файла в памяти. Это более сложная функция, чем D3DXCreateTextureFromFileInMemory.
ms.assetid: e515697c-0e24-4d96-b58a-dc4f27683021
title: Функция D3DXCreateTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da85af9e70a7971ba0bab1f76e9c3d30c3cc2884
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000370"
---
# <a name="d3dxcreatetexturefromfileinmemoryex-function"></a><span data-ttu-id="e21a8-104">Функция D3DXCreateTextureFromFileInMemoryEx</span><span class="sxs-lookup"><span data-stu-id="e21a8-104">D3DXCreateTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="e21a8-105">Создает текстуру из файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="e21a8-105">Creates a texture from a file in memory.</span></span> <span data-ttu-id="e21a8-106">Это более сложная функция, чем [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="e21a8-106">This is a more advanced function than [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e21a8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e21a8-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCVOID            pSrcData,
  _In_    UINT               SrcDataSize,
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



## <a name="parameters"></a><span data-ttu-id="e21a8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e21a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e21a8-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e21a8-111">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="e21a8-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-112">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-113">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e21a8-114">Указатель на файл в памяти, из которого создается текстура.</span><span class="sxs-lookup"><span data-stu-id="e21a8-114">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-115">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e21a8-117">Размер файла в памяти, в байтах.</span><span class="sxs-lookup"><span data-stu-id="e21a8-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-118">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e21a8-120">Ширина в пикселях.</span><span class="sxs-lookup"><span data-stu-id="e21a8-120">Width in pixels.</span></span> <span data-ttu-id="e21a8-121">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="e21a8-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-122">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-122">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e21a8-124">Высота в пикселях.</span><span class="sxs-lookup"><span data-stu-id="e21a8-124">Height, in pixels.</span></span> <span data-ttu-id="e21a8-125">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="e21a8-125">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-126">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-127">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e21a8-128">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="e21a8-128">Number of mip levels requested.</span></span> <span data-ttu-id="e21a8-129">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="e21a8-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-130">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-131">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e21a8-132">0, D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="e21a8-132">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="e21a8-133">Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="e21a8-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="e21a8-134">Затем ресурс можно передать в параметр *пневрендертаржет* метода [**сетрендертаржет**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="e21a8-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="e21a8-135">Если указано значение D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic, для *пула* должно быть задано значение D3DPOOL \_ по умолчанию, и приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="e21a8-135">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="e21a8-136">Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="e21a8-136">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-137">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-137">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-138">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-138">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="e21a8-139">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры.</span><span class="sxs-lookup"><span data-stu-id="e21a8-139">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="e21a8-140">Возвращаемая текстура может иметь другой формат, заданный в *формате*.</span><span class="sxs-lookup"><span data-stu-id="e21a8-140">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="e21a8-141">Приложения должны проверять формат возвращенной текстуры.</span><span class="sxs-lookup"><span data-stu-id="e21a8-141">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="e21a8-142">Если [D3DFMT \_ Unknown](other-d3dx-constants.md), то формат берется из файла.</span><span class="sxs-lookup"><span data-stu-id="e21a8-142">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="e21a8-143">Если D3DFMT \_ из \_ файла, формат принимается точно так же, как в файле, и вызов завершается ошибкой, если это нарушает возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="e21a8-143">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-144">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-144">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-145">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-145">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="e21a8-146">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.</span><span class="sxs-lookup"><span data-stu-id="e21a8-146">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-147">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-147">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-148">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-148">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e21a8-149">Сочетание одного или нескольких флагов, управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="e21a8-149">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="e21a8-150">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="e21a8-150">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="e21a8-151">Каждый допустимый фильтр должен содержать один из флагов [в \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="e21a8-151">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-152">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-153">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e21a8-154">Сочетание одного или нескольких флагов, управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="e21a8-154">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="e21a8-155">Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="e21a8-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="e21a8-156">Каждый допустимый фильтр должен содержать один из флагов [в \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="e21a8-156">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span> <span data-ttu-id="e21a8-157">Кроме того, используйте BITS 27-31, чтобы указать число MIP уровней, которые будут пропущены (в верхней части цепочки mipmap) при загрузке текстуры. DDS в память. Это позволяет пропустить до 32 уровней.</span><span class="sxs-lookup"><span data-stu-id="e21a8-157">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-158">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-158">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-159">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-159">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="e21a8-160">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="e21a8-160">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="e21a8-161">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="e21a8-161">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="e21a8-162">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="e21a8-162">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="e21a8-163">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="e21a8-163">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-164">*псрЦинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-164">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-165">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e21a8-165">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="e21a8-166">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="e21a8-166">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-167">*ппалетте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-167">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-168">Тип: **[ **палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="e21a8-168">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e21a8-169">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , представляющую 256-цветную палитру для заполнения, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e21a8-169">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="e21a8-170">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="e21a8-170">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e21a8-171">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e21a8-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e21a8-172">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="e21a8-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="e21a8-173">Адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="e21a8-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e21a8-174">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e21a8-174">Return value</span></span>

<span data-ttu-id="e21a8-175">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e21a8-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e21a8-176">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e21a8-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e21a8-177">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e21a8-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e21a8-178">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e21a8-178">Remarks</span></span>

<span data-ttu-id="e21a8-179">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="e21a8-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="e21a8-180">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="e21a8-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="e21a8-181">Дополнительные сведения о [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)см. в разделе пакет SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="e21a8-181">For details about [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="e21a8-182">Обратите внимание, что начиная с DirectX 8,0, член Пефлагс структуры **палеттинтри** не работает, как описано в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="e21a8-182">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="e21a8-183">Теперь элемент Пефлагс является альфа-каналом для 8 – разрядных форматов палеттизед.</span><span class="sxs-lookup"><span data-stu-id="e21a8-183">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="e21a8-184">При пропуске mipmap уровней при загрузке DDS-файла используйте \_ макрос D3DX пропуска \_ DDS \_ MIP \_ Levels, чтобы создать значение мипфилтер.</span><span class="sxs-lookup"><span data-stu-id="e21a8-184">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="e21a8-185">Этот макрос принимает количество пропускаемых уровней, а тип фильтра и возвращает значение фильтра, которое затем передается в параметр Мипфилтер.</span><span class="sxs-lookup"><span data-stu-id="e21a8-185">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e21a8-186">Требования</span><span class="sxs-lookup"><span data-stu-id="e21a8-186">Requirements</span></span>



| <span data-ttu-id="e21a8-187">Требование</span><span class="sxs-lookup"><span data-stu-id="e21a8-187">Requirement</span></span> | <span data-ttu-id="e21a8-188">Значение</span><span class="sxs-lookup"><span data-stu-id="e21a8-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e21a8-189">Header</span><span class="sxs-lookup"><span data-stu-id="e21a8-189">Header</span></span><br/>  | <dl> <span data-ttu-id="e21a8-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e21a8-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e21a8-191">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e21a8-191">Library</span></span><br/> | <dl> <span data-ttu-id="e21a8-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e21a8-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e21a8-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e21a8-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e21a8-194">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="e21a8-194">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="e21a8-195">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e21a8-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
