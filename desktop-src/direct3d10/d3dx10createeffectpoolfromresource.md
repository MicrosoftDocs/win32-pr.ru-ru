---
description: Создание пула эффектов на основе ресурса.
ms.assetid: 594ab788-fd96-4ea9-ad93-ef02fefa5d61
title: Функция D3DX10CreateEffectPoolFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fccc9c399a4573440318b92d1157738589da8a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720881"
---
# <a name="d3dx10createeffectpoolfromresource-function"></a><span data-ttu-id="dcd63-103">Функция D3DX10CreateEffectPoolFromResource</span><span class="sxs-lookup"><span data-stu-id="dcd63-103">D3DX10CreateEffectPoolFromResource function</span></span>

<span data-ttu-id="dcd63-104">Создание пула эффектов на основе ресурса.</span><span class="sxs-lookup"><span data-stu-id="dcd63-104">Create an effect pool from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcd63-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcd63-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _In_        ID3D10EffectPool   **ppEffectPool,
  _In_        ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="dcd63-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcd63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcd63-107">*хмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-107">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-108">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcd63-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcd63-109">Маркер модуля ресурсов, который содержит результат.</span><span class="sxs-lookup"><span data-stu-id="dcd63-109">A handle to the resource module containing the effect.</span></span> <span data-ttu-id="dcd63-110">ХМОДУЛЕ можно получить с помощью [функции ошибка GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="dcd63-110">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-111">*пресаурценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-111">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-112">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcd63-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcd63-113">Имя ресурса в Хмодуле.</span><span class="sxs-lookup"><span data-stu-id="dcd63-113">The name of the resource in hModule.</span></span> <span data-ttu-id="dcd63-114">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="dcd63-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="dcd63-115">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="dcd63-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-116">*псркфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-116">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-117">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcd63-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcd63-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="dcd63-118">Optional.</span></span> <span data-ttu-id="dcd63-119">Имя файла эффектов, которое используется только для сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="dcd63-119">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="dcd63-120">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dcd63-120">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-121">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-122">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="dcd63-122">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="dcd63-123">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="dcd63-123">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-124">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-125">Тип: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="dcd63-125">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="dcd63-126">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="dcd63-126">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="dcd63-127">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dcd63-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-128">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-128">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-129">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcd63-129">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcd63-130">Строка, указывающая [профиль шейдера](../direct3dhlsl/dx-graphics-hlsl-models.md)или модель шейдера.</span><span class="sxs-lookup"><span data-stu-id="dcd63-130">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-131">*Хлслфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-131">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-132">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcd63-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcd63-133">Параметры компиляции HLSL (см. раздел [ \_ константы шейдера D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="dcd63-133">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-134">*Фксфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-134">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-135">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcd63-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcd63-136">Параметры компиляции эффектов (см. раздел [флаги компиляции и влияния](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="dcd63-136">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-137">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-137">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-138">Тип: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="dcd63-138">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="dcd63-139">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="dcd63-139">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-140">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-140">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-141">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="dcd63-141">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="dcd63-142">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="dcd63-142">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="dcd63-143">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="dcd63-143">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-144">*ппеффектпул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-144">*ppEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-145">Тип: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="dcd63-145">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="dcd63-146">Адрес указателя на пул эффектов (см. [**интерфейс ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="dcd63-146">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-147">*пперрорс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-147">*ppErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-148">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="dcd63-148">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="dcd63-149">Адрес указателя на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки компиляции эффектов, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="dcd63-149">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="dcd63-150">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dcd63-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd63-151">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="dcd63-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="dcd63-152">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="dcd63-152">A pointer to the return value.</span></span> <span data-ttu-id="dcd63-153">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dcd63-153">May be **NULL**.</span></span> <span data-ttu-id="dcd63-154">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="dcd63-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcd63-155">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcd63-155">Return value</span></span>

<span data-ttu-id="dcd63-156">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dcd63-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dcd63-157">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="dcd63-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dcd63-158">Требования</span><span class="sxs-lookup"><span data-stu-id="dcd63-158">Requirements</span></span>



| <span data-ttu-id="dcd63-159">Требование</span><span class="sxs-lookup"><span data-stu-id="dcd63-159">Requirement</span></span> | <span data-ttu-id="dcd63-160">Значение</span><span class="sxs-lookup"><span data-stu-id="dcd63-160">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd63-161">Header</span><span class="sxs-lookup"><span data-stu-id="dcd63-161">Header</span></span><br/> | <dl> <span data-ttu-id="dcd63-162"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcd63-162"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcd63-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcd63-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd63-164">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="dcd63-164">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
