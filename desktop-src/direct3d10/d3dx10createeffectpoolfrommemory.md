---
description: Создание пула эффектов на основе воздействия в памяти.
ms.assetid: 634bcb23-a73f-4493-b805-e2aa5420fa2a
title: Функция D3DX10CreateEffectPoolFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 7dc93b7e73f336e75432debfe9bde6659ea4707c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720882"
---
# <a name="d3dx10createeffectpoolfrommemory-function"></a><span data-ttu-id="5891f-103">Функция D3DX10CreateEffectPoolFromMemory</span><span class="sxs-lookup"><span data-stu-id="5891f-103">D3DX10CreateEffectPoolFromMemory function</span></span>

<span data-ttu-id="5891f-104">Создание пула эффектов на основе воздействия в памяти.</span><span class="sxs-lookup"><span data-stu-id="5891f-104">Create an effect pool from an effect in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="5891f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5891f-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="5891f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5891f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5891f-107">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5891f-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5891f-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5891f-109">Указатель на результат.</span><span class="sxs-lookup"><span data-stu-id="5891f-109">A pointer to the effect.</span></span>

</dd> <dt>

<span data-ttu-id="5891f-110">*Длина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5891f-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-111">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5891f-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5891f-112">Размер результата.</span><span class="sxs-lookup"><span data-stu-id="5891f-112">The size of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="5891f-113">*псркфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5891f-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-114">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5891f-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5891f-115">Имя файла эффектов.</span><span class="sxs-lookup"><span data-stu-id="5891f-115">The name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="5891f-116">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5891f-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-117">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="5891f-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="5891f-118">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="5891f-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="5891f-119">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5891f-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-120">Тип: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="5891f-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="5891f-121">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="5891f-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="5891f-122">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5891f-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5891f-123">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5891f-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-124">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5891f-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5891f-125">Строка, указывающая [профиль шейдера](../direct3dhlsl/dx-graphics-hlsl-models.md)или модель шейдера.</span><span class="sxs-lookup"><span data-stu-id="5891f-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="5891f-126">*Хлслфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5891f-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-127">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5891f-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5891f-128">Параметры компиляции HLSL (см. раздел [ \_ константы шейдера D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="5891f-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5891f-129">*Фксфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5891f-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-130">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5891f-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5891f-131">Параметры компиляции эффектов (см. раздел [флаги компиляции и влияния](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="5891f-131">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5891f-132">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5891f-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-133">Тип: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="5891f-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="5891f-134">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5891f-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="5891f-135">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5891f-135">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-136">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="5891f-136">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="5891f-137">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="5891f-137">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="5891f-138">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="5891f-138">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="5891f-139">*ппеффектпул* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5891f-139">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-140">Тип: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="5891f-140">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="5891f-141">Адрес указателя на пул эффектов (см. [**интерфейс ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="5891f-141">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="5891f-142">*пперрорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5891f-142">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-143">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="5891f-143">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="5891f-144">Адрес указателя на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки компиляции эффектов, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="5891f-144">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="5891f-145">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5891f-145">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5891f-146">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="5891f-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="5891f-147">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="5891f-147">A pointer to the return value.</span></span> <span data-ttu-id="5891f-148">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5891f-148">May be **NULL**.</span></span> <span data-ttu-id="5891f-149">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="5891f-149">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5891f-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5891f-150">Return value</span></span>

<span data-ttu-id="5891f-151">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5891f-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5891f-152">Возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5891f-152">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5891f-153">Требования</span><span class="sxs-lookup"><span data-stu-id="5891f-153">Requirements</span></span>



| <span data-ttu-id="5891f-154">Требование</span><span class="sxs-lookup"><span data-stu-id="5891f-154">Requirement</span></span> | <span data-ttu-id="5891f-155">Значение</span><span class="sxs-lookup"><span data-stu-id="5891f-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5891f-156">Header</span><span class="sxs-lookup"><span data-stu-id="5891f-156">Header</span></span><br/> | <dl> <span data-ttu-id="5891f-157"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="5891f-157"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5891f-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5891f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5891f-159">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="5891f-159">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
