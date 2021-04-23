---
description: Создание результата из описания ASCII или двоичного действия.
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: Функция D3DXCreateEffectFromResource (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36db2c82debc542301ba44d4baa74ecaaf01245e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703919"
---
# <a name="d3dxcreateeffectfromresource-function"></a><span data-ttu-id="1b7ce-103">Функция D3DXCreateEffectFromResource</span><span class="sxs-lookup"><span data-stu-id="1b7ce-103">D3DXCreateEffectFromResource function</span></span>

<span data-ttu-id="1b7ce-104">Создание результата из описания ASCII или двоичного действия.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7ce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b7ce-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResource(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="1b7ce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b7ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b7ce-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b7ce-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7ce-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1b7ce-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1b7ce-109">Указатель на устройство.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-109">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="1b7ce-110">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b7ce-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7ce-111">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b7ce-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b7ce-112">Обработчик для модуля, содержащего описание результата.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-112">Handle to a module containing the effect description.</span></span> <span data-ttu-id="1b7ce-113">Если этот параметр имеет **значение NULL**, будет использоваться текущий модуль.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-113">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="1b7ce-114">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b7ce-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7ce-115">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b7ce-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b7ce-116">Указатель на ресурс.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-116">Pointer to the resource.</span></span> <span data-ttu-id="1b7ce-117">Этот параметр поддерживает строки в Юникоде и ANSI.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-117">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="1b7ce-118">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1b7ce-119">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b7ce-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7ce-120">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b7ce-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="1b7ce-121">Необязательный завершающий **нуль** массив структур [**D3DXMACRO**](d3dxmacro.md) , описывающих определения препроцессора.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="1b7ce-122">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1b7ce-123">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b7ce-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7ce-124">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="1b7ce-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="1b7ce-125">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="1b7ce-126">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="1b7ce-127">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b7ce-127">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7ce-128">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b7ce-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b7ce-129">Если *хсркмодуле* содержит текстовый результат, флаги могут быть сочетанием флагов [D3DXSHADER](d3dxshader-flags.md) и [D3DXFX](d3dxfx.md) . в противном случае *хсркмодуле* содержит двоичный результат, а только соблюдаются флаги D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-129">If *hSrcModule* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *hSrcModule* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="1b7ce-130">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-130">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="1b7ce-131">Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="1b7ce-131">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="1b7ce-132">*ппул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b7ce-132">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7ce-133">Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="1b7ce-133">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="1b7ce-134">Указатель на объект [**ID3DXEffectPool**](id3dxeffectpool.md) , используемый для общих параметров.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-134">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="1b7ce-135">Если это значение равно **null**, общий доступ к параметрам не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-135">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="1b7ce-136">*ппеффект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1b7ce-136">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7ce-137">Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b7ce-137">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="1b7ce-138">Возвращает буфер, содержащий скомпилированный результат.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-138">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="1b7ce-139">*ппкомпилатионеррорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1b7ce-139">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7ce-140">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b7ce-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1b7ce-141">Возвращает буфер, содержащий список ошибок компиляции.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-141">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b7ce-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b7ce-142">Return value</span></span>

<span data-ttu-id="1b7ce-143">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1b7ce-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1b7ce-144">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1b7ce-145">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-145">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b7ce-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b7ce-146">Remarks</span></span>

<span data-ttu-id="1b7ce-147">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-147">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="1b7ce-148">В противном случае тип данных LPCTSTR разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-148">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="1b7ce-149">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-149">The compiler setting also determines the function version.</span></span> <span data-ttu-id="1b7ce-150">Если определен Юникод, вызов функции разрешается в D3DXCreateEffectFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-150">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="1b7ce-151">В противном случае вызов функции разрешается в D3DXCreateEffectFromResourceA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-151">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="1b7ce-152">D3DXCreateEffectFromResource загружает данные из ресурса типа RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-152">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="1b7ce-153">Дополнительные сведения о ресурсах Windows см. на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-153">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b7ce-154">Требования</span><span class="sxs-lookup"><span data-stu-id="1b7ce-154">Requirements</span></span>



| <span data-ttu-id="1b7ce-155">Требование</span><span class="sxs-lookup"><span data-stu-id="1b7ce-155">Requirement</span></span> | <span data-ttu-id="1b7ce-156">Значение</span><span class="sxs-lookup"><span data-stu-id="1b7ce-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b7ce-157">Header</span><span class="sxs-lookup"><span data-stu-id="1b7ce-157">Header</span></span><br/>  | <dl> <span data-ttu-id="1b7ce-158"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b7ce-158"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1b7ce-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1b7ce-159">Library</span></span><br/> | <dl> <span data-ttu-id="1b7ce-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b7ce-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1b7ce-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b7ce-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b7ce-162">Функции эффектов</span><span class="sxs-lookup"><span data-stu-id="1b7ce-162">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="1b7ce-163">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="1b7ce-163">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="1b7ce-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="1b7ce-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
