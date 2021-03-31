---
description: Создание результата из описания ASCII или двоичного действия.
ms.assetid: b5868ba3-0869-46f7-804f-3103358a3ef5
title: Функция D3DXCreateEffectFromFile (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f34d0cdb3ae19772f21d8307fffb395c4d1ac9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821396"
---
# <a name="d3dxcreateeffectfromfile-function"></a><span data-ttu-id="6821d-103">Функция D3DXCreateEffectFromFile</span><span class="sxs-lookup"><span data-stu-id="6821d-103">D3DXCreateEffectFromFile function</span></span>

<span data-ttu-id="6821d-104">Создание результата из описания ASCII или двоичного действия.</span><span class="sxs-lookup"><span data-stu-id="6821d-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6821d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6821d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFile(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="6821d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6821d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6821d-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6821d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6821d-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6821d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6821d-109">Указатель на устройство, которое создаст результат.</span><span class="sxs-lookup"><span data-stu-id="6821d-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="6821d-110">См. [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="6821d-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="6821d-111">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6821d-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6821d-112">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6821d-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6821d-113">Указатель на имя файла.</span><span class="sxs-lookup"><span data-stu-id="6821d-113">Pointer to the filename.</span></span> <span data-ttu-id="6821d-114">Этот параметр поддерживает строки в Юникоде и ANSI.</span><span class="sxs-lookup"><span data-stu-id="6821d-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="6821d-115">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="6821d-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6821d-116">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6821d-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6821d-117">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="6821d-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="6821d-118">Необязательный завершающий нуль массив определений макросов препроцессора.</span><span class="sxs-lookup"><span data-stu-id="6821d-118">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="6821d-119">См. [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="6821d-119">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="6821d-120">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6821d-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6821d-121">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="6821d-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="6821d-122">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="6821d-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="6821d-123">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="6821d-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="6821d-124">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6821d-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6821d-125">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6821d-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6821d-126">Если *псркфиле* содержит текстовый результат, флаги могут быть сочетанием флагов [D3DXSHADER](d3dxshader-flags.md) и [D3DXFX](d3dxfx.md) . в противном случае *псркфиле* содержит двоичный результат, а только соблюдаются флаги D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="6821d-126">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="6821d-127">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6821d-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="6821d-128">Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="6821d-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="6821d-129">*ппул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6821d-129">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6821d-130">Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="6821d-130">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="6821d-131">Указатель на объект [**ID3DXEffectPool**](id3dxeffectpool.md) , используемый для общих параметров.</span><span class="sxs-lookup"><span data-stu-id="6821d-131">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="6821d-132">Если это значение равно **null**, общий доступ к параметрам не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="6821d-132">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="6821d-133">*ппеффект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6821d-133">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6821d-134">Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="6821d-134">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="6821d-135">Возвращает указатель на буфер, содержащий скомпилированный результат.</span><span class="sxs-lookup"><span data-stu-id="6821d-135">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="6821d-136">См. [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="6821d-136">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="6821d-137">*ппкомпилатионеррорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6821d-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6821d-138">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6821d-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6821d-139">Возвращает указатель на буфер, содержащий список ошибок компиляции.</span><span class="sxs-lookup"><span data-stu-id="6821d-139">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="6821d-140">См. [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="6821d-140">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6821d-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6821d-141">Return value</span></span>

<span data-ttu-id="6821d-142">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6821d-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6821d-143">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6821d-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6821d-144">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6821d-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6821d-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6821d-145">Remarks</span></span>

<span data-ttu-id="6821d-146">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="6821d-146">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6821d-147">В противном случае тип данных LPCTSTR разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6821d-147">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="6821d-148">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="6821d-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="6821d-149">Если определен Юникод, вызов функции разрешается в D3DXCreateEffectFromFileW.</span><span class="sxs-lookup"><span data-stu-id="6821d-149">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="6821d-150">В противном случае вызов функции разрешается в D3DXCreateEffectFromFileA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="6821d-150">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6821d-151">Требования</span><span class="sxs-lookup"><span data-stu-id="6821d-151">Requirements</span></span>



| <span data-ttu-id="6821d-152">Требование</span><span class="sxs-lookup"><span data-stu-id="6821d-152">Requirement</span></span> | <span data-ttu-id="6821d-153">Значение</span><span class="sxs-lookup"><span data-stu-id="6821d-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6821d-154">Header</span><span class="sxs-lookup"><span data-stu-id="6821d-154">Header</span></span><br/>  | <dl> <span data-ttu-id="6821d-155"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6821d-155"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6821d-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6821d-156">Library</span></span><br/> | <dl> <span data-ttu-id="6821d-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6821d-157"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6821d-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6821d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6821d-159">Функции эффектов</span><span class="sxs-lookup"><span data-stu-id="6821d-159">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="6821d-160">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="6821d-160">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="6821d-161">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="6821d-161">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
