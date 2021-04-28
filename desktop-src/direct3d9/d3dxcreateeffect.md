---
description: Функция D3DXCreateEffect — создание результата из описания ASCII-или двоичного воздействия.
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: Функция D3DXCreateEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6821375dfc672d4937c335cf85dab12ba31b726c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115782"
---
# <a name="d3dxcreateeffect-function"></a><span data-ttu-id="3000b-103">Функция D3DXCreateEffect</span><span class="sxs-lookup"><span data-stu-id="3000b-103">D3DXCreateEffect function</span></span>

<span data-ttu-id="3000b-104">Создание результата из описания ASCII или двоичного действия.</span><span class="sxs-lookup"><span data-stu-id="3000b-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3000b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3000b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="3000b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3000b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3000b-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3000b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3000b-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3000b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3000b-109">Указатель на устройство, которое создаст результат.</span><span class="sxs-lookup"><span data-stu-id="3000b-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="3000b-110">См. [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="3000b-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="3000b-111">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3000b-111">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3000b-112">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3000b-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3000b-113">Указатель на буфер, содержащий описание действия.</span><span class="sxs-lookup"><span data-stu-id="3000b-113">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="3000b-114">*Сркдатален* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3000b-114">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3000b-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3000b-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3000b-116">Длина данных эффектов в байтах.</span><span class="sxs-lookup"><span data-stu-id="3000b-116">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3000b-117">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3000b-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3000b-118">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="3000b-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="3000b-119">Необязательный завершающий **нуль** массив структур [**D3DXMACRO**](d3dxmacro.md) , описывающих определения препроцессора.</span><span class="sxs-lookup"><span data-stu-id="3000b-119">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="3000b-120">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="3000b-120">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3000b-121">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3000b-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3000b-122">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="3000b-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="3000b-123">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="3000b-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="3000b-124">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="3000b-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="3000b-125">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3000b-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3000b-126">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3000b-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3000b-127">Если *псркдата* содержит текстовый результат, флаги могут быть сочетанием флагов [D3DXSHADER](d3dxshader-flags.md) и [D3DXFX](d3dxfx.md) . в противном случае *псркдата* содержит двоичный результат, а только соблюдаются флаги D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="3000b-127">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="3000b-128">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3000b-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="3000b-129">Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="3000b-129">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="3000b-130">*ппул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3000b-130">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3000b-131">Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="3000b-131">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="3000b-132">Указатель на объект [**ID3DXEffectPool**](id3dxeffectpool.md) , используемый для общих параметров.</span><span class="sxs-lookup"><span data-stu-id="3000b-132">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="3000b-133">Если это значение равно **null**, общий доступ к параметрам не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="3000b-133">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="3000b-134">*ппеффект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3000b-134">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3000b-135">Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="3000b-135">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="3000b-136">Возвращает указатель на интерфейс [**ID3DXEffect**](id3dxeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="3000b-136">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="3000b-137">*ппкомпилатионеррорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3000b-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3000b-138">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3000b-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3000b-139">Возвращает буфер, содержащий список ошибок компиляции.</span><span class="sxs-lookup"><span data-stu-id="3000b-139">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3000b-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3000b-140">Return value</span></span>

<span data-ttu-id="3000b-141">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3000b-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3000b-142">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3000b-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3000b-143">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3000b-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3000b-144">Требования</span><span class="sxs-lookup"><span data-stu-id="3000b-144">Requirements</span></span>



| <span data-ttu-id="3000b-145">Требование</span><span class="sxs-lookup"><span data-stu-id="3000b-145">Requirement</span></span> | <span data-ttu-id="3000b-146">Значение</span><span class="sxs-lookup"><span data-stu-id="3000b-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3000b-147">Header</span><span class="sxs-lookup"><span data-stu-id="3000b-147">Header</span></span><br/>  | <dl> <span data-ttu-id="3000b-148"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3000b-148"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3000b-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3000b-149">Library</span></span><br/> | <dl> <span data-ttu-id="3000b-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3000b-150"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3000b-151">См. также</span><span class="sxs-lookup"><span data-stu-id="3000b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3000b-152">Функции эффектов</span><span class="sxs-lookup"><span data-stu-id="3000b-152">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="3000b-153">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="3000b-153">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="3000b-154">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="3000b-154">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
