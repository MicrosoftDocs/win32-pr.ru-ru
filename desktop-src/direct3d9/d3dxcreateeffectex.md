---
description: Создает результат из описания результата ASCII или двоичного файла. Эта функция является расширенной версией D3DXCreateEffect, позволяющей приложению контролировать, какие параметры игнорируются системой эффектов.
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: Функция D3DXCreateEffectEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 979b09f852e692b4c25414607f79cd8792342755
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720905"
---
# <a name="d3dxcreateeffectex-function"></a><span data-ttu-id="63edc-104">Функция D3DXCreateEffectEx</span><span class="sxs-lookup"><span data-stu-id="63edc-104">D3DXCreateEffectEx function</span></span>

<span data-ttu-id="63edc-105">Создает результат из описания результата ASCII или двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="63edc-105">Creates an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="63edc-106">Эта функция является расширенной версией [**D3DXCreateEffect**](d3dxcreateeffect.md) , позволяющей приложению контролировать, какие параметры игнорируются системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="63edc-106">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="63edc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63edc-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="63edc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="63edc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63edc-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63edc-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63edc-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="63edc-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="63edc-111">Указатель на устройство, которое создаст результат.</span><span class="sxs-lookup"><span data-stu-id="63edc-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="63edc-112">См. [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="63edc-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="63edc-113">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63edc-113">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63edc-114">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63edc-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63edc-115">Указатель на буфер, содержащий описание действия.</span><span class="sxs-lookup"><span data-stu-id="63edc-115">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="63edc-116">*Сркдатален* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63edc-116">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63edc-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63edc-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63edc-118">Длина данных эффектов в байтах.</span><span class="sxs-lookup"><span data-stu-id="63edc-118">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="63edc-119">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63edc-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63edc-120">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="63edc-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="63edc-121">Необязательный завершающий **нуль** массив структур [**D3DXMACRO**](d3dxmacro.md) , описывающих определения препроцессора.</span><span class="sxs-lookup"><span data-stu-id="63edc-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="63edc-122">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="63edc-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="63edc-123">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63edc-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63edc-124">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="63edc-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="63edc-125">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="63edc-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="63edc-126">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="63edc-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="63edc-127">*пскипконстантс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63edc-127">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63edc-128">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63edc-128">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63edc-129">Строка параметров действия, которая будет игнорироваться системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="63edc-129">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="63edc-130">Строка **должна завершаться нулем и** должна содержать имя каждой управляемой приложением константы, разделенной точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="63edc-130">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="63edc-131">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63edc-131">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63edc-132">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63edc-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63edc-133">Если *псркдата* содержит текстовый результат, флаги могут быть сочетанием флагов [D3DXSHADER](d3dxshader-flags.md) и [D3DXFX](d3dxfx.md) . в противном случае *псркдата* содержит двоичный результат, а только соблюдаются флаги D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="63edc-133">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="63edc-134">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="63edc-134">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="63edc-135">Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="63edc-135">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="63edc-136">*ппул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63edc-136">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63edc-137">Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="63edc-137">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="63edc-138">Указатель на объект [**ID3DXEffectPool**](id3dxeffectpool.md) , используемый для общих параметров.</span><span class="sxs-lookup"><span data-stu-id="63edc-138">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="63edc-139">Если это значение равно **null**, общий доступ к параметрам не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="63edc-139">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="63edc-140">*ппеффект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63edc-140">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63edc-141">Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="63edc-141">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="63edc-142">Возвращает указатель на интерфейс [**ID3DXEffect**](id3dxeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="63edc-142">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="63edc-143">*ппкомпилатионеррорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63edc-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63edc-144">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="63edc-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="63edc-145">Возвращает буфер, содержащий список ошибок компиляции.</span><span class="sxs-lookup"><span data-stu-id="63edc-145">Returns a buffer containing a list of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63edc-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63edc-146">Return value</span></span>

<span data-ttu-id="63edc-147">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63edc-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63edc-148">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="63edc-148">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="63edc-149">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="63edc-149">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="63edc-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63edc-150">Remarks</span></span>

<span data-ttu-id="63edc-151">Эта функция является расширенной версией [**D3DXCreateEffect**](d3dxcreateeffect.md) , позволяющей приложению указывать, какие константы эффектов будут управляться приложением.</span><span class="sxs-lookup"><span data-stu-id="63edc-151">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="63edc-152">Константа, управляемая приложением, игнорируется системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="63edc-152">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="63edc-153">Это значит, что приложение отвечает за инициализацию константы, а также сохранение и восстановление состояния при необходимости.</span><span class="sxs-lookup"><span data-stu-id="63edc-153">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="63edc-154">Эта функция проверяет каждую константу в Пскипконстантс, чтобы увидеть, что:</span><span class="sxs-lookup"><span data-stu-id="63edc-154">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="63edc-155">Он привязан к регистру констант.</span><span class="sxs-lookup"><span data-stu-id="63edc-155">It is bound to a constant register.</span></span>
-   <span data-ttu-id="63edc-156">Он используется только в коде шейдера HLSL.</span><span class="sxs-lookup"><span data-stu-id="63edc-156">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="63edc-157">Если константа имеет имя в строке, которая отсутствует в результате, она игнорируется.</span><span class="sxs-lookup"><span data-stu-id="63edc-157">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="63edc-158">Требования</span><span class="sxs-lookup"><span data-stu-id="63edc-158">Requirements</span></span>



| <span data-ttu-id="63edc-159">Требование</span><span class="sxs-lookup"><span data-stu-id="63edc-159">Requirement</span></span> | <span data-ttu-id="63edc-160">Значение</span><span class="sxs-lookup"><span data-stu-id="63edc-160">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63edc-161">Header</span><span class="sxs-lookup"><span data-stu-id="63edc-161">Header</span></span><br/>  | <dl> <span data-ttu-id="63edc-162"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="63edc-162"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="63edc-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="63edc-163">Library</span></span><br/> | <dl> <span data-ttu-id="63edc-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63edc-164"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="63edc-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63edc-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63edc-166">Функции эффектов</span><span class="sxs-lookup"><span data-stu-id="63edc-166">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="63edc-167">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="63edc-167">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[<span data-ttu-id="63edc-168">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="63edc-168">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
