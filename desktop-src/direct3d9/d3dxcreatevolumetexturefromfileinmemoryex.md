---
description: Создает текстуру тома из файла. Это более сложная функция, чем D3DXCreateVolumeTextureFromFileInMemory.
ms.assetid: 1a43f906-1826-40a3-a7a9-a0536c977164
title: Функция D3DXCreateVolumeTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f09439be9410b59ccaa446c2f00ee79963a21cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694166"
---
# <a name="d3dxcreatevolumetexturefromfileinmemoryex-function"></a><span data-ttu-id="6e205-104">Функция D3DXCreateVolumeTextureFromFileInMemoryEx</span><span class="sxs-lookup"><span data-stu-id="6e205-104">D3DXCreateVolumeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="6e205-105">Создает текстуру тома из файла.</span><span class="sxs-lookup"><span data-stu-id="6e205-105">Creates a volume texture from a file.</span></span> <span data-ttu-id="6e205-106">Это более сложная функция, чем [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="6e205-106">This is a more advanced function than [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e205-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e205-107">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCVOID                  pSrcData,
  _In_    UINT                     SrcDataSize,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
  _In_    D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="6e205-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e205-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e205-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6e205-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6e205-111">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="6e205-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="6e205-112">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-113">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e205-114">Указатель на файл в памяти, из которого создается текстура тома.</span><span class="sxs-lookup"><span data-stu-id="6e205-114">Pointer to the file in memory from which to create the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="6e205-115">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e205-117">Размер файла в памяти, в байтах.</span><span class="sxs-lookup"><span data-stu-id="6e205-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6e205-118">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e205-120">Ширина в пикселях.</span><span class="sxs-lookup"><span data-stu-id="6e205-120">Width in pixels.</span></span> <span data-ttu-id="6e205-121">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="6e205-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="6e205-122">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="6e205-122">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="6e205-123">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-124">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e205-125">Высота в пикселях.</span><span class="sxs-lookup"><span data-stu-id="6e205-125">Height, in pixels.</span></span> <span data-ttu-id="6e205-126">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="6e205-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="6e205-127">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="6e205-127">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="6e205-128">*Глубина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-128">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-129">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e205-130">Глубина (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="6e205-130">Depth, in pixels.</span></span> <span data-ttu-id="6e205-131">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="6e205-131">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="6e205-132">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="6e205-132">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="6e205-133">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-133">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-134">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e205-135">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="6e205-135">Number of mip levels requested.</span></span> <span data-ttu-id="6e205-136">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="6e205-136">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="6e205-137">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-137">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-138">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e205-139">0, D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="6e205-139">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="6e205-140">Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="6e205-140">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="6e205-141">Затем ресурс можно передать в параметр *пневрендертаржет* метода [**сетрендертаржет**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="6e205-141">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="6e205-142">Если указано значение D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic, для *пула* должно быть задано значение D3DPOOL \_ по умолчанию, и приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="6e205-142">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="6e205-143">D3DUSAGE \_ Dynamic указывает, что поверхность должна обрабатываться динамически.</span><span class="sxs-lookup"><span data-stu-id="6e205-143">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="6e205-144">Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="6e205-144">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e205-145">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-145">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-146">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-146">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="6e205-147">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры.</span><span class="sxs-lookup"><span data-stu-id="6e205-147">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="6e205-148">Возвращаемая текстура может иметь другой формат, заданный в *формате*.</span><span class="sxs-lookup"><span data-stu-id="6e205-148">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="6e205-149">Приложения должны проверять формат возвращенной текстуры.</span><span class="sxs-lookup"><span data-stu-id="6e205-149">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="6e205-150">Если [D3DFMT \_ Unknown](other-d3dx-constants.md), то формат берется из файла.</span><span class="sxs-lookup"><span data-stu-id="6e205-150">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="6e205-151">Если D3DFMT \_ из \_ файла, формат принимается точно так же, как в файле, и вызов завершается ошибкой, если это нарушает возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="6e205-151">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="6e205-152">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-152">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-153">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-153">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="6e205-154">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.</span><span class="sxs-lookup"><span data-stu-id="6e205-154">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="6e205-155">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-155">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-156">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e205-157">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="6e205-157">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="6e205-158">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="6e205-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="6e205-159">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-159">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-160">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-160">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e205-161">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="6e205-161">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="6e205-162">Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="6e205-162">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="6e205-163">Кроме того, используйте BITS 27-31, чтобы указать число MIP уровней, которые будут пропущены (в верхней части цепочки mipmap) при загрузке текстуры. DDS в память. Это позволяет пропустить до 32 уровней.</span><span class="sxs-lookup"><span data-stu-id="6e205-163">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="6e205-164">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e205-164">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-165">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="6e205-165">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="6e205-166">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="6e205-166">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="6e205-167">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="6e205-167">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="6e205-168">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="6e205-168">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="6e205-169">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="6e205-169">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="6e205-170">*псрЦинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6e205-170">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-171">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e205-171">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="6e205-172">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) , которая будет заполнена описанием данных в исходном файле изображения, или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="6e205-172">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6e205-173">*ппалетте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6e205-173">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-174">Тип: **[ **палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="6e205-174">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="6e205-175">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , представляющую 256-цветную палитру для заполнения, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6e205-175">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6e205-176">*ппволуметекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6e205-176">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e205-177">Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="6e205-177">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="6e205-178">Адрес указателя на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="6e205-178">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e205-179">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e205-179">Return value</span></span>

<span data-ttu-id="6e205-180">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6e205-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6e205-181">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6e205-181">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6e205-182">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6e205-182">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e205-183">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e205-183">Remarks</span></span>

<span data-ttu-id="6e205-184">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="6e205-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="6e205-185">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="6e205-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="6e205-186">При пропуске mipmap уровней при загрузке DDS-файла используйте \_ макрос D3DX пропуска \_ DDS \_ MIP \_ Levels, чтобы создать значение *мипфилтер* .</span><span class="sxs-lookup"><span data-stu-id="6e205-186">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="6e205-187">Этот макрос принимает количество пропускаемых уровней, а тип фильтра и возвращает значение фильтра, которое затем передается в параметр *мипфилтер* .</span><span class="sxs-lookup"><span data-stu-id="6e205-187">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e205-188">Требования</span><span class="sxs-lookup"><span data-stu-id="6e205-188">Requirements</span></span>



| <span data-ttu-id="6e205-189">Требование</span><span class="sxs-lookup"><span data-stu-id="6e205-189">Requirement</span></span> | <span data-ttu-id="6e205-190">Значение</span><span class="sxs-lookup"><span data-stu-id="6e205-190">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e205-191">Header</span><span class="sxs-lookup"><span data-stu-id="6e205-191">Header</span></span><br/>  | <dl> <span data-ttu-id="6e205-192"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e205-192"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6e205-193">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6e205-193">Library</span></span><br/> | <dl> <span data-ttu-id="6e205-194"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e205-194"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6e205-195">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e205-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e205-196">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="6e205-196">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="6e205-197">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="6e205-197">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="6e205-198">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="6e205-198">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="6e205-199">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="6e205-199">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="6e205-200">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="6e205-200">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="6e205-201">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6e205-201">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
