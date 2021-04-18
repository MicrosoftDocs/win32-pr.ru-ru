---
description: Создает текстуру куба из файла. Это более сложная функция, чем D3DXCreateCubeTextureFromFile.
ms.assetid: 77e64b33-9282-42fa-978c-a93fa9ba11fc
title: Функция D3DXCreateCubeTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4f56ad3f8e314f7ceb5f4efb07562257efab5fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720973"
---
# <a name="d3dxcreatecubetexturefromfileex-function"></a><span data-ttu-id="190e7-104">Функция D3DXCreateCubeTextureFromFileEx</span><span class="sxs-lookup"><span data-stu-id="190e7-104">D3DXCreateCubeTextureFromFileEx function</span></span>

<span data-ttu-id="190e7-105">Создает текстуру куба из файла.</span><span class="sxs-lookup"><span data-stu-id="190e7-105">Creates a cube texture from a file.</span></span> <span data-ttu-id="190e7-106">Это более сложная функция, чем [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="190e7-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="190e7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="190e7-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileEx(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _In_  DWORD                  Filter,
  _In_  DWORD                  MipFilter,
  _In_  D3DCOLOR               ColorKey,
  _Out_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_ PALETTEENTRY           *pPalette,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="190e7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="190e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="190e7-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190e7-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="190e7-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="190e7-111">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой Куба.</span><span class="sxs-lookup"><span data-stu-id="190e7-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="190e7-112">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190e7-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-113">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="190e7-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="190e7-114">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="190e7-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="190e7-115">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="190e7-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="190e7-116">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="190e7-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="190e7-117">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="190e7-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="190e7-118">*Размер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190e7-118">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="190e7-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="190e7-120">Ширина и высота текстуры Куба в пикселях.</span><span class="sxs-lookup"><span data-stu-id="190e7-120">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="190e7-121">Например, если текстура Куба является 8-пиксельным кубом, значение этого параметра должно быть равно 8.</span><span class="sxs-lookup"><span data-stu-id="190e7-121">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="190e7-122">Если это значение равно 0 или D3DX \_ по умолчанию, измерения берутся из файла.</span><span class="sxs-lookup"><span data-stu-id="190e7-122">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="190e7-123">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190e7-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-124">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="190e7-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="190e7-125">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="190e7-125">Number of mip levels requested.</span></span> <span data-ttu-id="190e7-126">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="190e7-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="190e7-127">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190e7-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-128">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="190e7-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="190e7-129">0 или D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="190e7-129">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="190e7-130">Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="190e7-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="190e7-131">Затем ресурс можно передать в параметр *пневрендертаржет* метода [**сетрендертаржет**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="190e7-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="190e7-132">Если указан параметр D3DUSAGE \_ рендертаржет, приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="190e7-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="190e7-133">D3DUSAGE \_ Dynamic указывает, что поверхность должна обрабатываться динамически.</span><span class="sxs-lookup"><span data-stu-id="190e7-133">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="190e7-134">Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="190e7-134">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="190e7-135">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190e7-135">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-136">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="190e7-136">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="190e7-137">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="190e7-137">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="190e7-138">Возвращаемая текстура Куба может иметь другой формат, заданный в *формате*.</span><span class="sxs-lookup"><span data-stu-id="190e7-138">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="190e7-139">Приложения должны проверять формат полученной текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="190e7-139">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="190e7-140">Если [D3DFMT \_ Unknown](other-d3dx-constants.md), то формат берется из файла.</span><span class="sxs-lookup"><span data-stu-id="190e7-140">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="190e7-141">Если D3DFMT \_ из \_ файла, формат принимается точно так же, как в файле, и вызов завершается ошибкой, если это нарушает возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="190e7-141">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="190e7-142">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190e7-142">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-143">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="190e7-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="190e7-144">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура Куба.</span><span class="sxs-lookup"><span data-stu-id="190e7-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="190e7-145">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190e7-145">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-146">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="190e7-146">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="190e7-147">Сочетание одной или нескольких констант [ \_ фильтра D3DX](d3dx-filter.md) , контролирующих фильтрацию изображения.</span><span class="sxs-lookup"><span data-stu-id="190e7-147">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants, controlling how the image is filtered.</span></span> <span data-ttu-id="190e7-148">Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="190e7-148">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="190e7-149">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190e7-149">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-150">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="190e7-150">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="190e7-151">Сочетание одной или нескольких констант [ \_ фильтра D3DX](d3dx-filter.md) , управляющих фильтрацией изображения.</span><span class="sxs-lookup"><span data-stu-id="190e7-151">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="190e7-152">Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="190e7-152">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="190e7-153">Кроме того, используйте BITS 27-31, чтобы указать число MIP уровней, которые будут пропущены (в верхней части цепочки mipmap) при загрузке текстуры. DDS в память. Это позволяет пропустить до 32 уровней.</span><span class="sxs-lookup"><span data-stu-id="190e7-153">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="190e7-154">*ColorKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190e7-154">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-155">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="190e7-155">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="190e7-156">Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey.</span><span class="sxs-lookup"><span data-stu-id="190e7-156">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="190e7-157">Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="190e7-157">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="190e7-158">Значение альфа имеет большое значение, поэтому для непрозрачных цветовых ключей обычно должно быть задано FF.</span><span class="sxs-lookup"><span data-stu-id="190e7-158">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="190e7-159">Таким образом, для непрозрачного черного значение будет равно 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="190e7-159">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="190e7-160">*псрЦинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="190e7-160">*pSrcInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-161">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="190e7-161">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="190e7-162">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="190e7-162">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="190e7-163">*ппалетте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="190e7-163">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-164">Тип: **[ **палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="190e7-164">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="190e7-165">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , представляющую 256-цветную палитру для заполнения, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="190e7-165">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="190e7-166">*ппкубетекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="190e7-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="190e7-167">Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="190e7-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="190e7-168">Адрес указателя на интерфейс [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий созданный объект текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="190e7-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="190e7-169">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="190e7-169">Return value</span></span>

<span data-ttu-id="190e7-170">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="190e7-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="190e7-171">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="190e7-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="190e7-172">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE, D3DERR \_ аутофвидеомемори, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="190e7-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="190e7-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="190e7-173">Remarks</span></span>

<span data-ttu-id="190e7-174">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="190e7-174">The compiler setting also determines the function version.</span></span> <span data-ttu-id="190e7-175">Если определен Юникод, вызов функции разрешается в **D3DXCreateCubeTextureFromFileExW**.</span><span class="sxs-lookup"><span data-stu-id="190e7-175">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileExW**.</span></span> <span data-ttu-id="190e7-176">В противном случае вызов функции разрешается в **D3DXCreateCubeTextureFromFileExA** , так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="190e7-176">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="190e7-177">Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga.</span><span class="sxs-lookup"><span data-stu-id="190e7-177">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="190e7-178">См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="190e7-178">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="190e7-179">Текстуры Куба отличаются от других поверхностей тем, что они являются коллекциями поверхностей.</span><span class="sxs-lookup"><span data-stu-id="190e7-179">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="190e7-180">Чтобы вызвать [**сетрендертаржет**](/windows/desktop/api) с текстурой Куба, необходимо выбрать отдельное лицо с помощью [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) и передать полученную область в **сетрендертаржет**.</span><span class="sxs-lookup"><span data-stu-id="190e7-180">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="190e7-181">**D3DXCreateCubeTextureFromFileEx** использует формат файла поверхности DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="190e7-181">**D3DXCreateCubeTextureFromFileEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="190e7-182">Редактор текстур DirectX (Dxtex.exe) позволяет создать карту Куба на основе других форматов файлов и сохранить ее в формате файлов DDS.</span><span class="sxs-lookup"><span data-stu-id="190e7-182">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="190e7-183">Вы можете получить Dxtex.exe и узнать о нем из пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="190e7-183">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="190e7-184">Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="190e7-184">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="190e7-185">При пропуске mipmap уровней при загрузке DDS-файла используйте \_ макрос D3DX пропуска \_ DDS \_ MIP \_ Levels, чтобы создать значение мипфилтер.</span><span class="sxs-lookup"><span data-stu-id="190e7-185">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="190e7-186">Этот макрос принимает количество пропускаемых уровней, а тип фильтра и возвращает значение фильтра, которое затем передается в параметр Мипфилтер.</span><span class="sxs-lookup"><span data-stu-id="190e7-186">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="190e7-187">Требования</span><span class="sxs-lookup"><span data-stu-id="190e7-187">Requirements</span></span>



| <span data-ttu-id="190e7-188">Требование</span><span class="sxs-lookup"><span data-stu-id="190e7-188">Requirement</span></span> | <span data-ttu-id="190e7-189">Значение</span><span class="sxs-lookup"><span data-stu-id="190e7-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="190e7-190">Header</span><span class="sxs-lookup"><span data-stu-id="190e7-190">Header</span></span><br/>  | <dl> <span data-ttu-id="190e7-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="190e7-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="190e7-192">Библиотека</span><span class="sxs-lookup"><span data-stu-id="190e7-192">Library</span></span><br/> | <dl> <span data-ttu-id="190e7-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="190e7-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="190e7-194">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="190e7-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="190e7-195">**D3DXCreateCubeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="190e7-195">**D3DXCreateCubeTextureFromFile**</span></span>](d3dxcreatecubetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="190e7-196">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="190e7-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
