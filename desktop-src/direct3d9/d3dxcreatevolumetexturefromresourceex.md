---
description: Создает текстуру тома на основе ресурса, указанного строкой. Это более сложная функция, чем D3DXCreateVolumeTextureFromResource.
ms.assetid: 02f2cb9e-4750-4854-aa74-202426427af5
title: Функция D3DXCreateVolumeTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44d842df2da1d5c3db374e838e0ffd2492683961
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000366"
---
# <a name="d3dxcreatevolumetexturefromresourceex-function"></a><span data-ttu-id="34e84-104">Функция D3DXCreateVolumeTextureFromResourceEx</span><span class="sxs-lookup"><span data-stu-id="34e84-104">D3DXCreateVolumeTextureFromResourceEx function</span></span>

<span data-ttu-id="34e84-105">Создает текстуру тома на основе ресурса, указанного строкой.</span><span class="sxs-lookup"><span data-stu-id="34e84-105">Creates a volume texture from a resource specified by a string.</span></span> <span data-ttu-id="34e84-106">Это более сложная функция, чем [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="34e84-106">This is a more advanced function than [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="34e84-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34e84-107">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    HMODULE                  hSrcModule,
  _In_    LPCTSTR                  pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="34e84-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="34e84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e84-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="34e84-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="34e84-111">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="34e84-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="34e84-112">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-113">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34e84-114">Указатель на модуль, в котором находится ресурс, или **значение NULL** для модуля, связанного с образом, операционной системой, используемой для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="34e84-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="34e84-115">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-116">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34e84-117">Указатель на строку, указывающую имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="34e84-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="34e84-118">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="34e84-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="34e84-119">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="34e84-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="34e84-120">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="34e84-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="34e84-121">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34e84-123">Ширина в пикселях.</span><span class="sxs-lookup"><span data-stu-id="34e84-123">Width in pixels.</span></span> <span data-ttu-id="34e84-124">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="34e84-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="34e84-125">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="34e84-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="34e84-126">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-126">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-127">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34e84-128">Высота в пикселях.</span><span class="sxs-lookup"><span data-stu-id="34e84-128">Height, in pixels.</span></span> <span data-ttu-id="34e84-129">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="34e84-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="34e84-130">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="34e84-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="34e84-131">*Глубина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-131">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-132">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34e84-133">Глубина (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="34e84-133">Depth, in pixels.</span></span> <span data-ttu-id="34e84-134">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="34e84-134">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="34e84-135">Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="34e84-135">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="34e84-136">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-136">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-137">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34e84-138">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="34e84-138">Number of mip levels requested.</span></span> <span data-ttu-id="34e84-139">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="34e84-139">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="34e84-140">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-140">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-141">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34e84-142">0, D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="34e84-142">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="34e84-143">Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="34e84-143">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="34e84-144">Затем ресурс можно передать в параметр *пневрендертаржет* метода [**сетрендертаржет**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="34e84-144">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="34e84-145">Если указано значение D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic, для *пула* должно быть задано значение D3DPOOL \_ по умолчанию, и приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="34e84-145">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="34e84-146">D3DUSAGE \_ Dynamic указывает, что поверхность должна обрабатываться динамически.</span><span class="sxs-lookup"><span data-stu-id="34e84-146">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="34e84-147">Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="34e84-147">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="34e84-148">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-148">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-149">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-149">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="34e84-150">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры.</span><span class="sxs-lookup"><span data-stu-id="34e84-150">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="34e84-151">Возвращаемая текстура может иметь другой формат, заданный в *формате*.</span><span class="sxs-lookup"><span data-stu-id="34e84-151">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="34e84-152">Приложения должны проверять формат возвращенной текстуры.</span><span class="sxs-lookup"><span data-stu-id="34e84-152">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="34e84-153">Если [D3DFMT \_ Unknown](other-d3dx-constants.md), то формат берется из файла.</span><span class="sxs-lookup"><span data-stu-id="34e84-153">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="34e84-154">Если D3DFMT \_ из \_ файла, формат принимается точно так же, как в файле, и вызов завершается ошибкой, если это нарушает возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="34e84-154">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="34e84-155">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-155">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-156">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-156">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="34e84-157">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.</span><span class="sxs-lookup"><span data-stu-id="34e84-157">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="34e84-158">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-158">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-159">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-159">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34e84-160">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="34e84-160">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="34e84-161">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="34e84-161">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="34e84-162">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-162">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-163">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-163">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34e84-164">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="34e84-164">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="34e84-165">Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="34e84-165">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="34e84-166">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e84-166">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-167">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="34e84-167">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="34e84-168">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="34e84-168">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="34e84-169">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="34e84-169">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="34e84-170">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="34e84-170">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="34e84-171">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="34e84-171">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="34e84-172">*псрЦинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="34e84-172">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-173">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="34e84-173">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="34e84-174">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) , которая будет заполнена описанием данных в исходном файле изображения, или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="34e84-174">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="34e84-175">*ппалетте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="34e84-175">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-176">Тип: **[ **палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="34e84-176">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="34e84-177">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , представляющую 256-цветную палитру для заполнения, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="34e84-177">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="34e84-178">*ппволуметекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="34e84-178">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34e84-179">Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="34e84-179">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="34e84-180">Адрес указателя на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="34e84-180">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e84-181">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34e84-181">Return value</span></span>

<span data-ttu-id="34e84-182">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="34e84-182">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="34e84-183">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="34e84-183">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="34e84-184">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="34e84-184">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="34e84-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34e84-185">Remarks</span></span>

<span data-ttu-id="34e84-186">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="34e84-186">The compiler setting also determines the function version.</span></span> <span data-ttu-id="34e84-187">Если определен Юникод, вызов функции разрешается в D3DXCreateVolumeTextureFromResourceExW.</span><span class="sxs-lookup"><span data-stu-id="34e84-187">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceExW.</span></span> <span data-ttu-id="34e84-188">В противном случае вызов функции разрешается в D3DXCreateVolumeTextureFromResourceExA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="34e84-188">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="34e84-189">Загружаемый ресурс должен быть ресурсом, определяемым приложением (RT \_ RCDATA).</span><span class="sxs-lookup"><span data-stu-id="34e84-189">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="34e84-190">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="34e84-190">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="34e84-191">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="34e84-191">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34e84-192">Требования</span><span class="sxs-lookup"><span data-stu-id="34e84-192">Requirements</span></span>



| <span data-ttu-id="34e84-193">Требование</span><span class="sxs-lookup"><span data-stu-id="34e84-193">Requirement</span></span> | <span data-ttu-id="34e84-194">Значение</span><span class="sxs-lookup"><span data-stu-id="34e84-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34e84-195">Header</span><span class="sxs-lookup"><span data-stu-id="34e84-195">Header</span></span><br/>  | <dl> <span data-ttu-id="34e84-196"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="34e84-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="34e84-197">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34e84-197">Library</span></span><br/> | <dl> <span data-ttu-id="34e84-198"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34e84-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="34e84-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34e84-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e84-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="34e84-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="34e84-201">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="34e84-201">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="34e84-202">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="34e84-202">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="34e84-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="34e84-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="34e84-204">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="34e84-204">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="34e84-205">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="34e84-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
