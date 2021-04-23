---
description: Создайте пул эффектов из файла эффектов.
ms.assetid: be738374-a91e-43d3-9cec-14882e6317ee
title: Функция D3DX10CreateEffectPoolFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 418ea287b9bbf2021f3b2e5379b209cf87745a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720883"
---
# <a name="d3dx10createeffectpoolfromfile-function"></a><span data-ttu-id="bab50-103">Функция D3DX10CreateEffectPoolFromFile</span><span class="sxs-lookup"><span data-stu-id="bab50-103">D3DX10CreateEffectPoolFromFile function</span></span>

<span data-ttu-id="bab50-104">Создайте пул эффектов из файла эффектов.</span><span class="sxs-lookup"><span data-stu-id="bab50-104">Create an effect pool from an effect file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bab50-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromFile(
  _In_        LPCTSTR            pFileName,
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



## <a name="parameters"></a><span data-ttu-id="bab50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bab50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab50-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bab50-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab50-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bab50-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bab50-109">Имя файла действия.</span><span class="sxs-lookup"><span data-stu-id="bab50-109">The effect filename.</span></span> <span data-ttu-id="bab50-110">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="bab50-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="bab50-111">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="bab50-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="bab50-112">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bab50-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab50-113">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="bab50-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="bab50-114">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="bab50-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="bab50-115">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bab50-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab50-116">Тип: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="bab50-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="bab50-117">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="bab50-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="bab50-118">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bab50-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bab50-119">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bab50-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab50-120">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bab50-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bab50-121">Строка, указывающая [профиль шейдера](../direct3dhlsl/dx-graphics-hlsl-models.md)или модель шейдера.</span><span class="sxs-lookup"><span data-stu-id="bab50-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="bab50-122">*Хлслфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bab50-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab50-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bab50-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bab50-124">Параметры компиляции HLSL (см. раздел [ \_ константы шейдера D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="bab50-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="bab50-125">*Фксфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bab50-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab50-126">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bab50-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bab50-127">Параметры компиляции эффектов (см. раздел [флаги компиляции и влияния](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="bab50-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="bab50-128">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bab50-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab50-129">Тип: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="bab50-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="bab50-130">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="bab50-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="bab50-131">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bab50-131">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab50-132">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="bab50-132">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="bab50-133">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="bab50-133">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="bab50-134">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="bab50-134">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="bab50-135">*ппеффектпул* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bab50-135">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bab50-136">Тип: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="bab50-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="bab50-137">Адрес указателя на пул эффектов (см. [**интерфейс ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="bab50-137">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="bab50-138">*пперрорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bab50-138">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bab50-139">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="bab50-139">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="bab50-140">Адрес указателя на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки компиляции эффектов, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="bab50-140">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="bab50-141">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bab50-141">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bab50-142">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="bab50-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="bab50-143">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="bab50-143">A pointer to the return value.</span></span> <span data-ttu-id="bab50-144">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bab50-144">May be **NULL**.</span></span> <span data-ttu-id="bab50-145">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="bab50-145">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab50-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bab50-146">Return value</span></span>

<span data-ttu-id="bab50-147">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bab50-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bab50-148">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bab50-148">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bab50-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bab50-149">Remarks</span></span>

<span data-ttu-id="bab50-150">В этом примере создается пул эффектов на основе воздействия, используемого в [примере BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="bab50-150">This example creates an effect pool from the effect used in the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```
   
// Create an effect pool from an effect in memory
ID3D10EffectPool * l_pEffectPool = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
WCHAR str[MAX_PATH];
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CreateEffectPoolFromFile( str, 
    NULL, NULL, D3D10_SHADER_ENABLE_STRICTNESS, 
    0, pd3dDevice, NULL, &l_pEffectPool,
    &l_pBlob_Errors );
```



## <a name="requirements"></a><span data-ttu-id="bab50-151">Требования</span><span class="sxs-lookup"><span data-stu-id="bab50-151">Requirements</span></span>



| <span data-ttu-id="bab50-152">Требование</span><span class="sxs-lookup"><span data-stu-id="bab50-152">Requirement</span></span> | <span data-ttu-id="bab50-153">Значение</span><span class="sxs-lookup"><span data-stu-id="bab50-153">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bab50-154">Header</span><span class="sxs-lookup"><span data-stu-id="bab50-154">Header</span></span><br/> | <dl> <span data-ttu-id="bab50-155"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab50-155"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bab50-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bab50-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab50-157">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="bab50-157">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
