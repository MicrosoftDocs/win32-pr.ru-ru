---
description: Создание результата из описания ASCII или двоичного действия. Это расширенная версия D3DXCreateEffectFromResource, которая позволяет приложению контролировать, какие параметры игнорируются системой эффектов.
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: Функция D3DXCreateEffectFromResourceEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResourceEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d0ae7a0ee43f93019f3c4c1f6145b3d8aa0e4367
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713877"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a><span data-ttu-id="4260c-104">Функция D3DXCreateEffectFromResourceEx</span><span class="sxs-lookup"><span data-stu-id="4260c-104">D3DXCreateEffectFromResourceEx function</span></span>

<span data-ttu-id="4260c-105">Создание результата из описания ASCII или двоичного действия.</span><span class="sxs-lookup"><span data-stu-id="4260c-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="4260c-106">Это расширенная версия [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) , которая позволяет приложению контролировать, какие параметры игнорируются системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="4260c-106">This is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4260c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4260c-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResourceEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="4260c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4260c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4260c-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4260c-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4260c-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4260c-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4260c-111">Указатель на устройство.</span><span class="sxs-lookup"><span data-stu-id="4260c-111">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="4260c-112">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4260c-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4260c-113">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4260c-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4260c-114">Обработчик для модуля, содержащего описание результата.</span><span class="sxs-lookup"><span data-stu-id="4260c-114">Handle to a module containing the effect description.</span></span> <span data-ttu-id="4260c-115">Если этот параметр имеет **значение NULL**, будет использоваться текущий модуль.</span><span class="sxs-lookup"><span data-stu-id="4260c-115">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="4260c-116">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4260c-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4260c-117">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4260c-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4260c-118">Указатель на ресурс.</span><span class="sxs-lookup"><span data-stu-id="4260c-118">Pointer to the resource.</span></span> <span data-ttu-id="4260c-119">Этот параметр поддерживает строки в Юникоде и ANSI.</span><span class="sxs-lookup"><span data-stu-id="4260c-119">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="4260c-120">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="4260c-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4260c-121">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4260c-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4260c-122">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="4260c-122">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="4260c-123">Необязательный завершающий **нуль** массив структур [**D3DXMACRO**](d3dxmacro.md) , описывающих определения препроцессора.</span><span class="sxs-lookup"><span data-stu-id="4260c-123">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="4260c-124">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="4260c-124">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4260c-125">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4260c-125">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4260c-126">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="4260c-126">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="4260c-127">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="4260c-127">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="4260c-128">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="4260c-128">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="4260c-129">*пскипконстантс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4260c-129">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4260c-130">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4260c-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4260c-131">Строка параметров действия, которая будет игнорироваться системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="4260c-131">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="4260c-132">Строка **должна завершаться нулем и** должна содержать имя каждой управляемой приложением константы, разделенной точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="4260c-132">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="4260c-133">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4260c-133">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4260c-134">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4260c-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4260c-135">Если *псркресаурце* содержит текстовый результат, флаги могут быть сочетанием флагов [D3DXSHADER](d3dxshader-flags.md) и [D3DXFX](d3dxfx.md) . в противном случае *псркресаурце* содержит двоичный результат, а только соблюдаются флаги D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="4260c-135">If *pSrcResource* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcResource* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="4260c-136">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4260c-136">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="4260c-137">Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="4260c-137">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="4260c-138">*ппул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4260c-138">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4260c-139">Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="4260c-139">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="4260c-140">Указатель на объект [**ID3DXEffectPool**](id3dxeffectpool.md) , используемый для общих параметров.</span><span class="sxs-lookup"><span data-stu-id="4260c-140">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="4260c-141">Если это значение равно **null**, общий доступ к параметрам не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="4260c-141">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="4260c-142">*ппеффект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4260c-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4260c-143">Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="4260c-143">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="4260c-144">Возвращает буфер, содержащий скомпилированный результат.</span><span class="sxs-lookup"><span data-stu-id="4260c-144">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="4260c-145">*ппкомпилатионеррорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4260c-145">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4260c-146">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4260c-146">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4260c-147">Возвращает буфер, содержащий список ошибок компиляции.</span><span class="sxs-lookup"><span data-stu-id="4260c-147">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4260c-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4260c-148">Return value</span></span>

<span data-ttu-id="4260c-149">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4260c-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4260c-150">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4260c-150">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4260c-151">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4260c-151">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4260c-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4260c-152">Remarks</span></span>

<span data-ttu-id="4260c-153">Эта функция является расширенной версией [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) , позволяющей приложению указывать, какие константы эффектов будут управляться приложением.</span><span class="sxs-lookup"><span data-stu-id="4260c-153">This function is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="4260c-154">Константа, управляемая приложением, игнорируется системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="4260c-154">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="4260c-155">Это значит, что приложение отвечает за инициализацию константы, а также сохранение и восстановление состояния при необходимости.</span><span class="sxs-lookup"><span data-stu-id="4260c-155">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="4260c-156">Эта функция проверяет каждую константу в Пскипконстантс, чтобы увидеть, что:</span><span class="sxs-lookup"><span data-stu-id="4260c-156">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="4260c-157">Он привязан к регистру констант.</span><span class="sxs-lookup"><span data-stu-id="4260c-157">It is bound to a constant register.</span></span>
-   <span data-ttu-id="4260c-158">Он используется только в коде шейдера HLSL.</span><span class="sxs-lookup"><span data-stu-id="4260c-158">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="4260c-159">Если константа имеет имя в строке, которая отсутствует в результате, она игнорируется.</span><span class="sxs-lookup"><span data-stu-id="4260c-159">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="4260c-160">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="4260c-160">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4260c-161">В противном случае тип данных LPCTSTR разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="4260c-161">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="4260c-162">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="4260c-162">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4260c-163">Если определен Юникод, вызов функции разрешается в D3DXCreateEffectFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="4260c-163">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="4260c-164">В противном случае вызов функции разрешается в D3DXCreateEffectFromResourceA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="4260c-164">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="4260c-165">D3DXCreateEffectFromResource загружает данные из ресурса типа RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="4260c-165">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="4260c-166">Дополнительные сведения о ресурсах Windows см. на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="4260c-166">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="4260c-167">Требования</span><span class="sxs-lookup"><span data-stu-id="4260c-167">Requirements</span></span>



| <span data-ttu-id="4260c-168">Требование</span><span class="sxs-lookup"><span data-stu-id="4260c-168">Requirement</span></span> | <span data-ttu-id="4260c-169">Значение</span><span class="sxs-lookup"><span data-stu-id="4260c-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4260c-170">Header</span><span class="sxs-lookup"><span data-stu-id="4260c-170">Header</span></span><br/>  | <dl> <span data-ttu-id="4260c-171"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4260c-171"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="4260c-172">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4260c-172">Library</span></span><br/> | <dl> <span data-ttu-id="4260c-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4260c-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4260c-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4260c-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4260c-175">Функции эффектов</span><span class="sxs-lookup"><span data-stu-id="4260c-175">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="4260c-176">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="4260c-176">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="4260c-177">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="4260c-177">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
