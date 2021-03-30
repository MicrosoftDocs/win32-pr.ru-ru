---
description: Создание воздействия на ресурс.
ms.assetid: 239a3b14-9eea-4a0f-96b5-3959b7be3e19
title: Функция D3DX10CreateEffectFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6c5f7b7805e126f02c2658ddce6ec5029978de53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355100"
---
# <a name="d3dx10createeffectfromresource-function"></a><span data-ttu-id="5d4d2-103">Функция D3DX10CreateEffectFromResource</span><span class="sxs-lookup"><span data-stu-id="5d4d2-103">D3DX10CreateEffectFromResource function</span></span>

<span data-ttu-id="5d4d2-104">Создание воздействия на ресурс.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-104">Create an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d4d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d4d2-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3D10EffectPool   *pEffectPool,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Effect       **ppEffect,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="5d4d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d4d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d4d2-107">*хмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-107">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-108">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d4d2-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d4d2-109">Маркер модуля ресурсов, который содержит результат.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-109">A handle to the resource module containing the effect.</span></span> <span data-ttu-id="5d4d2-110">ХМОДУЛЕ можно получить с помощью [функции ошибка GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="5d4d2-110">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-111">*пресаурценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-111">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-112">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d4d2-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d4d2-113">Имя ресурса в Хмодуле.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-113">Name of the resource in hModule.</span></span> <span data-ttu-id="5d4d2-114">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5d4d2-115">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-116">*псркфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-116">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-117">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d4d2-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d4d2-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-118">Optional.</span></span> <span data-ttu-id="5d4d2-119">Имя файла эффектов, которое используется только для сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-119">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="5d4d2-120">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-120">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-121">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-122">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="5d4d2-122">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="5d4d2-123">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-123">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-124">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-125">Тип: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="5d4d2-125">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="5d4d2-126">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="5d4d2-126">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="5d4d2-127">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-128">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-128">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-129">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d4d2-129">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d4d2-130">Строка, указывающая [профиль шейдера](../direct3dhlsl/dx-graphics-hlsl-models.md)или модель шейдера.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-130">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-131">*Хлслфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-131">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-132">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d4d2-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d4d2-133">Параметры компиляции HLSL (см. раздел [ \_ константы шейдера D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="5d4d2-133">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-134">*Фксфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-134">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-135">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d4d2-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d4d2-136">Параметры компиляции эффектов (см. раздел [флаги компиляции и влияния](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="5d4d2-136">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-137">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-137">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-138">Тип: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="5d4d2-138">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="5d4d2-139">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-139">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-140">*пеффектпул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-140">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-141">Тип: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="5d4d2-141">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="5d4d2-142">Указатель на пул эффектов (см. [**интерфейс ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) для совместного использования переменных между различными эффектами.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-142">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-143">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-144">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d4d2-144">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="5d4d2-145">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="5d4d2-145">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="5d4d2-146">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-147">*ппеффект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-147">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-148">Тип: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="5d4d2-148">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="5d4d2-149">Адрес указателя на результат (см. [**интерфейс ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)), который был создан.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-149">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-150">*пперрорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-150">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-151">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="5d4d2-151">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="5d4d2-152">Адрес указателя на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки компиляции эффектов, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-152">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="5d4d2-153">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5d4d2-153">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4d2-154">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="5d4d2-154">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="5d4d2-155">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-155">A pointer to the return value.</span></span> <span data-ttu-id="5d4d2-156">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-156">May be **NULL**.</span></span> <span data-ttu-id="5d4d2-157">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="5d4d2-157">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d4d2-158">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d4d2-158">Return value</span></span>

<span data-ttu-id="5d4d2-159">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d4d2-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d4d2-160">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5d4d2-160">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d4d2-161">Требования</span><span class="sxs-lookup"><span data-stu-id="5d4d2-161">Requirements</span></span>



| <span data-ttu-id="5d4d2-162">Требование</span><span class="sxs-lookup"><span data-stu-id="5d4d2-162">Requirement</span></span> | <span data-ttu-id="5d4d2-163">Значение</span><span class="sxs-lookup"><span data-stu-id="5d4d2-163">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d4d2-164">Header</span><span class="sxs-lookup"><span data-stu-id="5d4d2-164">Header</span></span><br/> | <dl> <span data-ttu-id="5d4d2-165"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d4d2-165"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d4d2-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d4d2-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d4d2-167">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="5d4d2-167">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
