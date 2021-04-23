---
description: Создает текстуру Куба на основе ресурса, указанного строкой. Это более сложная функция, чем D3DXCreateCubeTextureFromResource.
ms.assetid: 4d263386-8270-4967-8ef5-e9ac69e502a5
title: Функция D3DXCreateCubeTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ed77556681e2ad43302b8608dc213b3ad0f0209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355673"
---
# <a name="d3dxcreatecubetexturefromresourceex-function"></a><span data-ttu-id="24159-104">Функция D3DXCreateCubeTextureFromResourceEx</span><span class="sxs-lookup"><span data-stu-id="24159-104">D3DXCreateCubeTextureFromResourceEx function</span></span>

<span data-ttu-id="24159-105">Создает текстуру Куба на основе ресурса, указанного строкой.</span><span class="sxs-lookup"><span data-stu-id="24159-105">Creates a cube texture from a resource specified by a string.</span></span> <span data-ttu-id="24159-106">Это более сложная функция, чем [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="24159-106">This is a more advanced function than [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="24159-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24159-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    HMODULE                hSrcModule,
  _In_    LPCTSTR                pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="24159-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="24159-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24159-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24159-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="24159-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="24159-111">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой Куба.</span><span class="sxs-lookup"><span data-stu-id="24159-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="24159-112">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24159-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-113">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24159-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24159-114">Указатель на модуль, в котором находится ресурс, или **значение NULL** для модуля, связанного с образом, операционной системой, используемой для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="24159-114">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="24159-115">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24159-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-116">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24159-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24159-117">Указатель на строку, указывающую имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="24159-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="24159-118">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="24159-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="24159-119">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="24159-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="24159-120">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="24159-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="24159-121">*Размер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24159-121">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24159-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24159-123">Ширина и высота текстуры Куба в пикселях.</span><span class="sxs-lookup"><span data-stu-id="24159-123">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="24159-124">Например, если текстура Куба является 8-пиксельным кубом, значение этого параметра должно быть равно 8.</span><span class="sxs-lookup"><span data-stu-id="24159-124">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="24159-125">Если это значение равно 0 или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="24159-125">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="24159-126">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24159-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-127">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24159-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24159-128">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="24159-128">Number of mip levels requested.</span></span> <span data-ttu-id="24159-129">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="24159-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="24159-130">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24159-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-131">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24159-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24159-132">0 или D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="24159-132">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="24159-133">Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="24159-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="24159-134">Затем ресурс можно передать в параметр *пневрендертаржет* метода [**сетрендертаржет**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="24159-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="24159-135">Если указан параметр D3DUSAGE \_ рендертаржет, приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="24159-135">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="24159-136">D3DUSAGE \_ Dynamic указывает, что поверхность должна обрабатываться динамически.</span><span class="sxs-lookup"><span data-stu-id="24159-136">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="24159-137">Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="24159-137">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="24159-138">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24159-138">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-139">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="24159-139">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="24159-140">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="24159-140">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="24159-141">Возвращаемая текстура Куба может иметь другой формат, заданный в *формате*.</span><span class="sxs-lookup"><span data-stu-id="24159-141">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="24159-142">Приложения должны проверять формат полученной текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="24159-142">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="24159-143">Если [D3DFMT \_ Unknown](other-d3dx-constants.md), то формат берется из файла.</span><span class="sxs-lookup"><span data-stu-id="24159-143">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="24159-144">Если D3DFMT \_ из \_ файла, формат принимается точно так же, как в файле, и вызов завершается ошибкой, если это нарушает возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="24159-144">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="24159-145">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24159-145">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-146">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="24159-146">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="24159-147">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура Куба.</span><span class="sxs-lookup"><span data-stu-id="24159-147">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="24159-148">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24159-148">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-149">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24159-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24159-150">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md), управляющих фильтром изображения.</span><span class="sxs-lookup"><span data-stu-id="24159-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="24159-151">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="24159-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="24159-152">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24159-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-153">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24159-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24159-154">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="24159-154">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="24159-155">Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="24159-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="24159-156">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24159-156">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-157">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="24159-157">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="24159-158">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="24159-158">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="24159-159">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="24159-159">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="24159-160">Значение альфа имеет большое значение, поэтому для непрозрачных цветовых ключей обычно должно быть задано FF.</span><span class="sxs-lookup"><span data-stu-id="24159-160">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="24159-161">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="24159-161">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="24159-162">*псрЦинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="24159-162">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-163">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="24159-163">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="24159-164">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="24159-164">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="24159-165">*ппалетте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="24159-165">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-166">Тип: **[ **палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="24159-166">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="24159-167">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , представляющую 256-цветную палитру для заполнения или **null**.</span><span class="sxs-lookup"><span data-stu-id="24159-167">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="24159-168">*ппкубетекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="24159-168">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24159-169">Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="24159-169">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="24159-170">Адрес указателя на интерфейс [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий созданный объект текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="24159-170">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24159-171">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24159-171">Return value</span></span>

<span data-ttu-id="24159-172">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="24159-172">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="24159-173">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="24159-173">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="24159-174">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE, D3DERR \_ аутофвидеомемори, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="24159-174">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="24159-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24159-175">Remarks</span></span>

<span data-ttu-id="24159-176">Параметр компилятора определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="24159-176">The compiler setting determines the function version.</span></span> <span data-ttu-id="24159-177">Если определен Юникод, вызов функции разрешается в **D3DXCreateCubeTextureFromResourceExW**.</span><span class="sxs-lookup"><span data-stu-id="24159-177">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceExW**.</span></span> <span data-ttu-id="24159-178">В противном случае вызов функции разрешается в **D3DXCreateCubeTextureFromResourceExA** , так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="24159-178">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="24159-179">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="24159-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="24159-180">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="24159-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="24159-181">Текстуры Куба отличаются от других поверхностей тем, что они являются коллекциями поверхностей.</span><span class="sxs-lookup"><span data-stu-id="24159-181">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="24159-182">Чтобы вызвать [**сетрендертаржет**](/windows/desktop/api) с текстурой Куба, необходимо выбрать отдельное лицо с помощью [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) и передать полученную область в **сетрендертаржет**.</span><span class="sxs-lookup"><span data-stu-id="24159-182">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="24159-183">**D3DXCreateCubeTextureFromResourceEx** использует формат файла поверхности DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="24159-183">**D3DXCreateCubeTextureFromResourceEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="24159-184">Редактор текстур DirectX (Dxtex.exe) позволяет создать карту Куба на основе других форматов файлов и сохранить ее в формате файлов DDS.</span><span class="sxs-lookup"><span data-stu-id="24159-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="24159-185">Вы можете получить Dxtex.exe и узнать о нем из пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="24159-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="24159-186">Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="24159-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24159-187">Требования</span><span class="sxs-lookup"><span data-stu-id="24159-187">Requirements</span></span>



| <span data-ttu-id="24159-188">Требование</span><span class="sxs-lookup"><span data-stu-id="24159-188">Requirement</span></span> | <span data-ttu-id="24159-189">Значение</span><span class="sxs-lookup"><span data-stu-id="24159-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24159-190">Header</span><span class="sxs-lookup"><span data-stu-id="24159-190">Header</span></span><br/>  | <dl> <span data-ttu-id="24159-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="24159-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="24159-192">Библиотека</span><span class="sxs-lookup"><span data-stu-id="24159-192">Library</span></span><br/> | <dl> <span data-ttu-id="24159-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24159-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="24159-194">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24159-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24159-195">**D3DXCreateCubeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="24159-195">**D3DXCreateCubeTextureFromResource**</span></span>](d3dxcreatecubetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="24159-196">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="24159-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
