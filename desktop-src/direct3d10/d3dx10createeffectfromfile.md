---
description: Создание результата из файла.
ms.assetid: 1418857e-bda1-4ffb-bbb9-dfa3709313b1
title: Функция D3DX10CreateEffectFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 60bc52e5b149a2fa69cc4a16f12900b12ab81db8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713905"
---
# <a name="d3dx10createeffectfromfile-function"></a><span data-ttu-id="a26f3-103">Функция D3DX10CreateEffectFromFile</span><span class="sxs-lookup"><span data-stu-id="a26f3-103">D3DX10CreateEffectFromFile function</span></span>

<span data-ttu-id="a26f3-104">Создание результата из файла.</span><span class="sxs-lookup"><span data-stu-id="a26f3-104">Create an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a26f3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a26f3-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromFile(
  _In_        LPCTSTR            pFileName,
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



## <a name="parameters"></a><span data-ttu-id="a26f3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a26f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a26f3-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a26f3-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a26f3-109">Имя файла эффектов ASCII.</span><span class="sxs-lookup"><span data-stu-id="a26f3-109">Name of the ASCII effect file.</span></span> <span data-ttu-id="a26f3-110">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="a26f3-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="a26f3-111">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="a26f3-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="a26f3-112">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-113">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="a26f3-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="a26f3-114">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="a26f3-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="a26f3-115">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-116">Тип: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="a26f3-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="a26f3-117">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="a26f3-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="a26f3-118">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a26f3-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a26f3-119">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-120">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a26f3-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a26f3-121">Строка, указывающая [профиль шейдера](../direct3dhlsl/dx-graphics-hlsl-models.md)или модель шейдера.</span><span class="sxs-lookup"><span data-stu-id="a26f3-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="a26f3-122">*Хлслфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a26f3-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a26f3-124">Параметры компиляции HLSL (см. раздел [ \_ константы шейдера D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="a26f3-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a26f3-125">*Фксфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-126">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a26f3-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a26f3-127">Параметры компиляции эффектов (см. раздел [флаги компиляции и влияния](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="a26f3-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a26f3-128">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-129">Тип: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="a26f3-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="a26f3-130">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a26f3-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="a26f3-131">*пеффектпул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-131">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-132">Тип: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="a26f3-132">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="a26f3-133">Указатель на пул эффектов (см. [**интерфейс ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) для совместного использования переменных между различными эффектами.</span><span class="sxs-lookup"><span data-stu-id="a26f3-133">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="a26f3-134">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-134">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-135">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a26f3-135">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="a26f3-136">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="a26f3-136">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="a26f3-137">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="a26f3-137">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="a26f3-138">*ппеффект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-138">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-139">Тип: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="a26f3-139">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="a26f3-140">Адрес указателя на результат (см. [**интерфейс ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)), который был создан.</span><span class="sxs-lookup"><span data-stu-id="a26f3-140">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="a26f3-141">*пперрорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-141">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-142">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a26f3-142">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a26f3-143">Адрес указателя на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки компиляции эффектов, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="a26f3-143">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="a26f3-144">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a26f3-144">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a26f3-145">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="a26f3-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="a26f3-146">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="a26f3-146">A pointer to the return value.</span></span> <span data-ttu-id="a26f3-147">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a26f3-147">May be **NULL**.</span></span> <span data-ttu-id="a26f3-148">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="a26f3-148">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a26f3-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a26f3-149">Return value</span></span>

<span data-ttu-id="a26f3-150">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a26f3-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a26f3-151">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a26f3-151">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a26f3-152">Требования</span><span class="sxs-lookup"><span data-stu-id="a26f3-152">Requirements</span></span>



| <span data-ttu-id="a26f3-153">Требование</span><span class="sxs-lookup"><span data-stu-id="a26f3-153">Requirement</span></span> | <span data-ttu-id="a26f3-154">Значение</span><span class="sxs-lookup"><span data-stu-id="a26f3-154">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a26f3-155">Header</span><span class="sxs-lookup"><span data-stu-id="a26f3-155">Header</span></span><br/> | <dl> <span data-ttu-id="a26f3-156"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="a26f3-156"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a26f3-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a26f3-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a26f3-158">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="a26f3-158">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
