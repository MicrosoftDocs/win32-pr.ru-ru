---
description: Создает текстуру тома из файла.
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: Функция D3DXCreateVolumeTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d63377394dc123defac565cd11a0d40324a28a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354900"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a><span data-ttu-id="e56bd-103">Функция D3DXCreateVolumeTextureFromFileEx</span><span class="sxs-lookup"><span data-stu-id="e56bd-103">D3DXCreateVolumeTextureFromFileEx function</span></span>

<span data-ttu-id="e56bd-104">Создает текстуру тома из файла.</span><span class="sxs-lookup"><span data-stu-id="e56bd-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e56bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e56bd-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCTSTR                  pSrcFile,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
          D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="e56bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e56bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e56bd-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e56bd-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="e56bd-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-110">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-111">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e56bd-112">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="e56bd-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="e56bd-113">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="e56bd-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e56bd-114">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="e56bd-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="e56bd-115">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="e56bd-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-116">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-116">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e56bd-118">Ширина в пикселях.</span><span class="sxs-lookup"><span data-stu-id="e56bd-118">Width in pixels.</span></span> <span data-ttu-id="e56bd-119">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="e56bd-119">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e56bd-120">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="e56bd-120">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-121">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-121">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e56bd-123">Высота в пикселях.</span><span class="sxs-lookup"><span data-stu-id="e56bd-123">Height, in pixels.</span></span> <span data-ttu-id="e56bd-124">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="e56bd-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e56bd-125">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="e56bd-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-126">*Глубина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-126">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-127">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e56bd-128">Глубина (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="e56bd-128">Depth, in pixels.</span></span> <span data-ttu-id="e56bd-129">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="e56bd-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e56bd-130">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="e56bd-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-131">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-131">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-132">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e56bd-133">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="e56bd-133">Number of mip levels requested.</span></span> <span data-ttu-id="e56bd-134">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="e56bd-134">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-135">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-135">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-136">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-136">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e56bd-137">0, D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="e56bd-137">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="e56bd-138">Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="e56bd-138">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="e56bd-139">Затем ресурс можно передать в параметр *пневрендертаржет* метода [**сетрендертаржет**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="e56bd-139">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="e56bd-140">Если указано значение D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic, для *пула* должно быть задано значение D3DPOOL \_ по умолчанию, и приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="e56bd-140">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="e56bd-141">D3DUSAGE \_ Dynamic указывает, что поверхность должна обрабатываться динамически.</span><span class="sxs-lookup"><span data-stu-id="e56bd-141">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="e56bd-142">Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="e56bd-142">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-143">*Формат*</span><span class="sxs-lookup"><span data-stu-id="e56bd-143">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="e56bd-144">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-144">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="e56bd-145">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры.</span><span class="sxs-lookup"><span data-stu-id="e56bd-145">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="e56bd-146">Возвращаемая текстура может иметь другой формат, заданный в *формате*.</span><span class="sxs-lookup"><span data-stu-id="e56bd-146">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="e56bd-147">Приложения должны проверять формат возвращенной текстуры.</span><span class="sxs-lookup"><span data-stu-id="e56bd-147">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="e56bd-148">Если [D3DFMT \_ Unknown](other-d3dx-constants.md), то формат берется из файла.</span><span class="sxs-lookup"><span data-stu-id="e56bd-148">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="e56bd-149">Если D3DFMT \_ из \_ файла, формат принимается точно так же, как в файле, и вызов завершается ошибкой, если это нарушает возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="e56bd-149">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-150">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-150">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-151">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-151">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="e56bd-152">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.</span><span class="sxs-lookup"><span data-stu-id="e56bd-152">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-153">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-153">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-154">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e56bd-155">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="e56bd-155">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="e56bd-156">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="e56bd-156">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-157">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-157">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-158">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-158">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e56bd-159">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="e56bd-159">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="e56bd-160">Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="e56bd-160">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="e56bd-161">Кроме того, используйте BITS 27-31, чтобы указать число MIP уровней, которые будут пропущены (в верхней части цепочки mipmap) при загрузке текстуры. DDS в память. Это позволяет пропустить до 32 уровней.</span><span class="sxs-lookup"><span data-stu-id="e56bd-161">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-162">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-162">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-163">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-163">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="e56bd-164">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="e56bd-164">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="e56bd-165">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="e56bd-165">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="e56bd-166">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="e56bd-166">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="e56bd-167">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="e56bd-167">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-168">*псрЦинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-168">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-169">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e56bd-169">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="e56bd-170">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) , которая будет заполнена описанием данных в исходном файле изображения, или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="e56bd-170">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-171">*ппалетте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-171">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-172">Тип: **[ **палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="e56bd-172">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e56bd-173">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , представляющую 256-цветную палитру для заполнения, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e56bd-173">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e56bd-174">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e56bd-174">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e56bd-175">Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="e56bd-175">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="e56bd-176">Адрес указателя на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="e56bd-176">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e56bd-177">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e56bd-177">Return value</span></span>

<span data-ttu-id="e56bd-178">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e56bd-178">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e56bd-179">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e56bd-179">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e56bd-180">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e56bd-180">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e56bd-181">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e56bd-181">Remarks</span></span>

<span data-ttu-id="e56bd-182">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="e56bd-182">The compiler setting also determines the function version.</span></span> <span data-ttu-id="e56bd-183">Если определен Юникод, вызов функции разрешается в D3DXCreateVolumeTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="e56bd-183">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileExW.</span></span> <span data-ttu-id="e56bd-184">В противном случае вызов функции разрешается в D3DXCreateVolumeTextureFromFileExA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="e56bd-184">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="e56bd-185">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="e56bd-185">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="e56bd-186">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="e56bd-186">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="e56bd-187">Текстуры мипмаппед автоматически имеют каждый уровень, заполненный загруженной текстурой тома.</span><span class="sxs-lookup"><span data-stu-id="e56bd-187">Mipmapped textures automatically have each level filled with the loaded volume texture.</span></span> <span data-ttu-id="e56bd-188">При загрузке изображений в текстуры мипмаппед некоторые устройства не могут подключиться к образу 1x1, и эта функция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e56bd-188">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="e56bd-189">Если это происходит, образы необходимо загружать вручную.</span><span class="sxs-lookup"><span data-stu-id="e56bd-189">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="e56bd-190">При пропуске mipmap уровней при загрузке DDS-файла используйте \_ макрос D3DX пропуска \_ DDS \_ MIP \_ Levels, чтобы создать значение *мипфилтер* .</span><span class="sxs-lookup"><span data-stu-id="e56bd-190">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="e56bd-191">Этот макрос принимает количество пропускаемых уровней, а тип фильтра и возвращает значение фильтра, которое затем передается в параметр *мипфилтер* .</span><span class="sxs-lookup"><span data-stu-id="e56bd-191">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e56bd-192">Требования</span><span class="sxs-lookup"><span data-stu-id="e56bd-192">Requirements</span></span>



| <span data-ttu-id="e56bd-193">Требование</span><span class="sxs-lookup"><span data-stu-id="e56bd-193">Requirement</span></span> | <span data-ttu-id="e56bd-194">Значение</span><span class="sxs-lookup"><span data-stu-id="e56bd-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e56bd-195">Header</span><span class="sxs-lookup"><span data-stu-id="e56bd-195">Header</span></span><br/>  | <dl> <span data-ttu-id="e56bd-196"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e56bd-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e56bd-197">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e56bd-197">Library</span></span><br/> | <dl> <span data-ttu-id="e56bd-198"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e56bd-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e56bd-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e56bd-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e56bd-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="e56bd-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="e56bd-201">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="e56bd-201">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="e56bd-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="e56bd-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="e56bd-203">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="e56bd-203">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="e56bd-204">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="e56bd-204">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="e56bd-205">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e56bd-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
