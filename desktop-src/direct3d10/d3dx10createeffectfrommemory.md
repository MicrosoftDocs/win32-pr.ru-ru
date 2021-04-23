---
description: Создание воздействия из памяти.
ms.assetid: 6903a695-bb87-45fe-9913-25beeaf17233
title: Функция D3DX10CreateEffectFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 03cbbc70e633f8289f99e094602cb1a912b711c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703851"
---
# <a name="d3dx10createeffectfrommemory-function"></a><span data-ttu-id="d17b5-103">Функция D3DX10CreateEffectFromMemory</span><span class="sxs-lookup"><span data-stu-id="d17b5-103">D3DX10CreateEffectFromMemory function</span></span>

<span data-ttu-id="d17b5-104">Создание воздействия из памяти.</span><span class="sxs-lookup"><span data-stu-id="d17b5-104">Create an effect from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d17b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d17b5-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
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



## <a name="parameters"></a><span data-ttu-id="d17b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d17b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d17b5-107">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d17b5-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d17b5-109">Указатель на воздействие в памяти.</span><span class="sxs-lookup"><span data-stu-id="d17b5-109">Pointer to the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-110">*Длина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-111">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d17b5-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d17b5-112">Размер воздействия в памяти.</span><span class="sxs-lookup"><span data-stu-id="d17b5-112">Size of the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-113">*псркфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-114">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d17b5-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d17b5-115">Имя файла эффектов в памяти.</span><span class="sxs-lookup"><span data-stu-id="d17b5-115">Name of the effect file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-116">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-117">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="d17b5-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="d17b5-118">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="d17b5-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-119">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-120">Тип: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="d17b5-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="d17b5-121">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="d17b5-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="d17b5-122">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d17b5-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-123">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-124">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d17b5-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d17b5-125">Строка, указывающая [профиль шейдера](../direct3dhlsl/dx-graphics-hlsl-models.md)или модель шейдера.</span><span class="sxs-lookup"><span data-stu-id="d17b5-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-126">*Хлслфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-127">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d17b5-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d17b5-128">Параметры компиляции HLSL (см. раздел [ \_ константы шейдера D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="d17b5-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-129">*Фксфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-130">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d17b5-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d17b5-131">Параметры компиляции эффектов (см [. \_ константы D3D10 Effect](d3d10-effect.md)).</span><span class="sxs-lookup"><span data-stu-id="d17b5-131">Effect compile options (see [D3D10\_EFFECT Constants](d3d10-effect.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-132">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-133">Тип: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="d17b5-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="d17b5-134">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d17b5-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-135">*пеффектпул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-135">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-136">Тип: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="d17b5-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="d17b5-137">Указатель на пул эффектов (см. [**интерфейс ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) для совместного использования переменных между различными эффектами.</span><span class="sxs-lookup"><span data-stu-id="d17b5-137">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-138">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-138">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-139">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="d17b5-139">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="d17b5-140">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="d17b5-140">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="d17b5-141">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="d17b5-141">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-142">*ппеффект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-143">Тип: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="d17b5-143">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="d17b5-144">Адрес указателя на результат (см. [**интерфейс ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)), который был создан.</span><span class="sxs-lookup"><span data-stu-id="d17b5-144">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-145">*пперрорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-145">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-146">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d17b5-146">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d17b5-147">Адрес указателя на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки компиляции эффектов, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="d17b5-147">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="d17b5-148">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d17b5-148">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d17b5-149">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="d17b5-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="d17b5-150">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="d17b5-150">A pointer to the return value.</span></span> <span data-ttu-id="d17b5-151">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d17b5-151">May be **NULL**.</span></span> <span data-ttu-id="d17b5-152">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="d17b5-152">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d17b5-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d17b5-153">Return value</span></span>

<span data-ttu-id="d17b5-154">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d17b5-154">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d17b5-155">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d17b5-155">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d17b5-156">Требования</span><span class="sxs-lookup"><span data-stu-id="d17b5-156">Requirements</span></span>



| <span data-ttu-id="d17b5-157">Требование</span><span class="sxs-lookup"><span data-stu-id="d17b5-157">Requirement</span></span> | <span data-ttu-id="d17b5-158">Значение</span><span class="sxs-lookup"><span data-stu-id="d17b5-158">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d17b5-159">Header</span><span class="sxs-lookup"><span data-stu-id="d17b5-159">Header</span></span><br/> | <dl> <span data-ttu-id="d17b5-160"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="d17b5-160"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d17b5-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d17b5-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d17b5-162">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="d17b5-162">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
