---
description: Создает текстуру из ресурса. Это более сложная функция, чем D3DXCreateTextureFromResource.
ms.assetid: 6015e2fa-9deb-4e6a-a401-f10fb05f40b7
title: Функция D3DXCreateTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26298f8a63ccfde2171578c27e9208011c16dd28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547911"
---
# <a name="d3dxcreatetexturefromresourceex-function"></a><span data-ttu-id="2b426-104">Функция D3DXCreateTextureFromResourceEx</span><span class="sxs-lookup"><span data-stu-id="2b426-104">D3DXCreateTextureFromResourceEx function</span></span>

<span data-ttu-id="2b426-105">Создает текстуру из ресурса.</span><span class="sxs-lookup"><span data-stu-id="2b426-105">Creates a texture from a resource.</span></span> <span data-ttu-id="2b426-106">Это более сложная функция, чем [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="2b426-106">This is a more advanced function than [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b426-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b426-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    HMODULE            hSrcModule,
  _In_    LPCTSTR            pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="2b426-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b426-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b426-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2b426-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2b426-111">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="2b426-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-112">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-113">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b426-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b426-114">Указатель на модуль, в котором находится ресурс, или **значение NULL** для модуля, связанного с образом, операционной системой, используемой для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="2b426-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-115">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-116">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b426-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b426-117">Указатель на строку, указывающую имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="2b426-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="2b426-118">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="2b426-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2b426-119">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="2b426-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="2b426-120">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="2b426-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-121">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b426-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b426-123">Ширина в пикселях.</span><span class="sxs-lookup"><span data-stu-id="2b426-123">Width in pixels.</span></span> <span data-ttu-id="2b426-124">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="2b426-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-125">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-125">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-126">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b426-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b426-127">Высота в пикселях.</span><span class="sxs-lookup"><span data-stu-id="2b426-127">Height, in pixels.</span></span> <span data-ttu-id="2b426-128">Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="2b426-128">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-129">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-129">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-130">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b426-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b426-131">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="2b426-131">Number of mip levels requested.</span></span> <span data-ttu-id="2b426-132">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="2b426-132">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-133">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-134">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b426-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b426-135">0, D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="2b426-135">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="2b426-136">Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="2b426-136">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="2b426-137">Затем ресурс можно передать в параметр *пневрендертаржет* метода [**сетрендертаржет**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="2b426-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="2b426-138">Если указано значение D3DUSAGE \_ рендертаржет или D3DUSAGE, для *пула* должно быть установлено значение D3DPOOL \_ по умолчанию, и приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="2b426-138">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="2b426-139">D3DUSAGE \_ Dynamic указывает, что поверхность должна обрабатываться динамически.</span><span class="sxs-lookup"><span data-stu-id="2b426-139">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="2b426-140">Дополнительные сведения об использовании динамических текстур см. в разделе [Оптимизация производительности (Direct3D 9)](performance-optimizations.md)с использованием динамических текстур.</span><span class="sxs-lookup"><span data-stu-id="2b426-140">For more information about using dynamic textures, see [Performance Optimizations (Direct3D 9)](performance-optimizations.md)Using Dynamic Textures.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-141">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-142">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2b426-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="2b426-143">Элемент перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры.</span><span class="sxs-lookup"><span data-stu-id="2b426-143">A member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="2b426-144">Возвращаемая текстура может иметь другой формат, заданный в *формате*.</span><span class="sxs-lookup"><span data-stu-id="2b426-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="2b426-145">Приложения должны проверять формат возвращенной текстуры.</span><span class="sxs-lookup"><span data-stu-id="2b426-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="2b426-146">Если [D3DFMT \_ Unknown](other-d3dx-constants.md), то формат берется из файла.</span><span class="sxs-lookup"><span data-stu-id="2b426-146">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="2b426-147">Если D3DFMT \_ из \_ файла, формат принимается точно так же, как в файле, и вызов завершается ошибкой, если это нарушает возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="2b426-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-148">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-149">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="2b426-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="2b426-150">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.</span><span class="sxs-lookup"><span data-stu-id="2b426-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-151">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-152">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b426-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b426-153">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="2b426-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="2b426-154">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="2b426-154">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-155">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-156">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b426-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b426-157">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="2b426-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="2b426-158">Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="2b426-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-159">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b426-159">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-160">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2b426-160">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="2b426-161">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="2b426-161">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="2b426-162">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="2b426-162">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="2b426-163">Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей.</span><span class="sxs-lookup"><span data-stu-id="2b426-163">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="2b426-164">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="2b426-164">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-165">*псрЦинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2b426-165">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-166">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b426-166">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="2b426-167">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b426-167">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-168">*ппалетте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2b426-168">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-169">Тип: **[ **палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="2b426-169">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="2b426-170">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , представляющую 256-цветную палитру для заполнения или **null**.</span><span class="sxs-lookup"><span data-stu-id="2b426-170">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2b426-171">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2b426-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b426-172">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="2b426-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="2b426-173">Адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="2b426-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b426-174">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b426-174">Return value</span></span>

<span data-ttu-id="2b426-175">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b426-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b426-176">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2b426-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2b426-177">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2b426-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b426-178">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b426-178">Remarks</span></span>

<span data-ttu-id="2b426-179">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="2b426-179">The compiler setting also determines the function version.</span></span> <span data-ttu-id="2b426-180">Если определен Юникод, вызов функции разрешается в D3DXCreateTextureFromResourceExW.</span><span class="sxs-lookup"><span data-stu-id="2b426-180">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceExW.</span></span> <span data-ttu-id="2b426-181">В противном случае вызов функции разрешается в D3DXCreateTextureFromResourceExA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="2b426-181">Otherwise, the function call resolves to D3DXCreateTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="2b426-182">Загружаемый ресурс должен иметь тип \_ Bitmap или "RT RCDATA" \_ .</span><span class="sxs-lookup"><span data-stu-id="2b426-182">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="2b426-183">Тип ресурса RT \_ RCDATA используется для загрузки форматов, отличных от точечных рисунков (таких как. TGA,. jpg и. DDS).</span><span class="sxs-lookup"><span data-stu-id="2b426-183">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="2b426-184">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="2b426-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="2b426-185">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="2b426-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b426-186">Требования</span><span class="sxs-lookup"><span data-stu-id="2b426-186">Requirements</span></span>



| <span data-ttu-id="2b426-187">Требование</span><span class="sxs-lookup"><span data-stu-id="2b426-187">Requirement</span></span> | <span data-ttu-id="2b426-188">Значение</span><span class="sxs-lookup"><span data-stu-id="2b426-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b426-189">Header</span><span class="sxs-lookup"><span data-stu-id="2b426-189">Header</span></span><br/>  | <dl> <span data-ttu-id="2b426-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b426-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2b426-191">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b426-191">Library</span></span><br/> | <dl> <span data-ttu-id="2b426-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b426-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2b426-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b426-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b426-194">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="2b426-194">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="2b426-195">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2b426-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
