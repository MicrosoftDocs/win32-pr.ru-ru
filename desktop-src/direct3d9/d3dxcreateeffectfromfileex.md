---
description: Создание результата из описания ASCII или двоичного действия. Эта функция является расширенной версией D3DXCreateEffectFromFile, позволяющей приложению контролировать, какие параметры игнорируются системой эффектов.
ms.assetid: 963caa1e-bc1a-4d4b-bdb1-50b17d8b4132
title: Функция D3DXCreateEffectFromFileEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFileEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b3d97c5aa23dd0711cfb00585e5b8ba7d410fc02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720935"
---
# <a name="d3dxcreateeffectfromfileex-function"></a><span data-ttu-id="66f44-104">Функция D3DXCreateEffectFromFileEx</span><span class="sxs-lookup"><span data-stu-id="66f44-104">D3DXCreateEffectFromFileEx function</span></span>

<span data-ttu-id="66f44-105">Создание результата из описания ASCII или двоичного действия.</span><span class="sxs-lookup"><span data-stu-id="66f44-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="66f44-106">Эта функция является расширенной версией [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) , позволяющей приложению контролировать, какие параметры игнорируются системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="66f44-106">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f44-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66f44-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFileEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="66f44-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="66f44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66f44-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66f44-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f44-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="66f44-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="66f44-111">Указатель на устройство, которое создаст результат.</span><span class="sxs-lookup"><span data-stu-id="66f44-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="66f44-112">См. [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="66f44-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="66f44-113">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66f44-113">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f44-114">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66f44-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66f44-115">Указатель на имя файла.</span><span class="sxs-lookup"><span data-stu-id="66f44-115">Pointer to the filename.</span></span> <span data-ttu-id="66f44-116">Этот параметр поддерживает строки в Юникоде и ANSI.</span><span class="sxs-lookup"><span data-stu-id="66f44-116">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="66f44-117">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="66f44-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="66f44-118">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66f44-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f44-119">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="66f44-119">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="66f44-120">Необязательный завершающий нуль массив определений макросов препроцессора.</span><span class="sxs-lookup"><span data-stu-id="66f44-120">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="66f44-121">См. [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="66f44-121">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="66f44-122">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66f44-122">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f44-123">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="66f44-123">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="66f44-124">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="66f44-124">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="66f44-125">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="66f44-125">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="66f44-126">*пскипконстантс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66f44-126">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f44-127">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66f44-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66f44-128">Строка параметров действия, которая будет игнорироваться системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="66f44-128">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="66f44-129">Строка **должна завершаться нулем и** должна содержать имя каждой управляемой приложением константы, разделенной точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="66f44-129">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="66f44-130">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66f44-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f44-131">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66f44-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66f44-132">Если *псркфиле* содержит текстовый результат, флаги могут быть сочетанием флагов [D3DXSHADER](d3dxshader-flags.md) и [D3DXFX](d3dxfx.md) . в противном случае *псркфиле* содержит двоичный результат, а только соблюдаются флаги D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="66f44-132">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="66f44-133">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66f44-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="66f44-134">Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="66f44-134">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="66f44-135">*ппул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66f44-135">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f44-136">Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="66f44-136">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="66f44-137">Указатель на объект [**ID3DXEffectPool**](id3dxeffectpool.md) , используемый для общих параметров.</span><span class="sxs-lookup"><span data-stu-id="66f44-137">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="66f44-138">Если это значение равно **null**, общий доступ к параметрам не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="66f44-138">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="66f44-139">*ппеффект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="66f44-139">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66f44-140">Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="66f44-140">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="66f44-141">Возвращает указатель на буфер, содержащий скомпилированный результат.</span><span class="sxs-lookup"><span data-stu-id="66f44-141">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="66f44-142">См. [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="66f44-142">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="66f44-143">*ппкомпилатионеррорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="66f44-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66f44-144">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="66f44-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="66f44-145">Возвращает указатель на буфер, содержащий список ошибок компиляции.</span><span class="sxs-lookup"><span data-stu-id="66f44-145">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="66f44-146">См. [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="66f44-146">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66f44-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66f44-147">Return value</span></span>

<span data-ttu-id="66f44-148">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66f44-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66f44-149">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="66f44-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="66f44-150">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="66f44-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="66f44-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66f44-151">Remarks</span></span>

<span data-ttu-id="66f44-152">Эта функция является расширенной версией [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) , позволяющей приложению указывать, какие константы эффектов будут управляться приложением.</span><span class="sxs-lookup"><span data-stu-id="66f44-152">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="66f44-153">Константа, управляемая приложением, игнорируется системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="66f44-153">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="66f44-154">Это значит, что приложение отвечает за инициализацию константы, а также сохранение и восстановление состояния при необходимости.</span><span class="sxs-lookup"><span data-stu-id="66f44-154">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="66f44-155">Эта функция проверяет каждую константу в Пскипконстантс, чтобы увидеть, что:</span><span class="sxs-lookup"><span data-stu-id="66f44-155">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="66f44-156">Он привязан к регистру констант.</span><span class="sxs-lookup"><span data-stu-id="66f44-156">It is bound to a constant register.</span></span>
-   <span data-ttu-id="66f44-157">Он используется только в коде шейдера HLSL.</span><span class="sxs-lookup"><span data-stu-id="66f44-157">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="66f44-158">Если константа имеет имя в строке, которая отсутствует в результате, она игнорируется.</span><span class="sxs-lookup"><span data-stu-id="66f44-158">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="66f44-159">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="66f44-159">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="66f44-160">В противном случае тип данных LPCTSTR разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="66f44-160">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="66f44-161">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="66f44-161">The compiler setting also determines the function version.</span></span> <span data-ttu-id="66f44-162">Если определен Юникод, вызов функции разрешается в D3DXCreateEffectFromFileW.</span><span class="sxs-lookup"><span data-stu-id="66f44-162">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="66f44-163">В противном случае вызов функции разрешается в D3DXCreateEffectFromFileA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="66f44-163">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f44-164">Требования</span><span class="sxs-lookup"><span data-stu-id="66f44-164">Requirements</span></span>



| <span data-ttu-id="66f44-165">Требование</span><span class="sxs-lookup"><span data-stu-id="66f44-165">Requirement</span></span> | <span data-ttu-id="66f44-166">Значение</span><span class="sxs-lookup"><span data-stu-id="66f44-166">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f44-167">Header</span><span class="sxs-lookup"><span data-stu-id="66f44-167">Header</span></span><br/>  | <dl> <span data-ttu-id="66f44-168"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f44-168"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="66f44-169">Библиотека</span><span class="sxs-lookup"><span data-stu-id="66f44-169">Library</span></span><br/> | <dl> <span data-ttu-id="66f44-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66f44-170"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="66f44-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66f44-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f44-172">Функции эффектов</span><span class="sxs-lookup"><span data-stu-id="66f44-172">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="66f44-173">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="66f44-173">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="66f44-174">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="66f44-174">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
