---
title: Функция D3DX11CreateAsyncCompilerProcessor (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. См. заметки. Создайте обработчик асинхронных данных для шейдера.
ms.assetid: 90756ac3-946d-49fa-9f97-70dc5da812c6
keywords:
- D3DX11CreateAsyncCompilerProcessor функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncCompilerProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533e487e65640b8c17a0ff8d061388e8b5a6c0f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998564"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a><span data-ttu-id="c4ebb-106">Функция D3DX11CreateAsyncCompilerProcessor</span><span class="sxs-lookup"><span data-stu-id="c4ebb-106">D3DX11CreateAsyncCompilerProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="c4ebb-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="c4ebb-108">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-108">See Remarks.</span></span>

 

<span data-ttu-id="c4ebb-109">Создайте обработчик асинхронных данных для шейдера.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-109">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ebb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4ebb-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="c4ebb-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4ebb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ebb-112">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4ebb-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ebb-113">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c4ebb-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c4ebb-114">Строка, содержащая имя файла шейдера.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="c4ebb-115">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4ebb-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ebb-116">Тип: **const D3D11ный \_ \_ макрос \* шейдера**</span><span class="sxs-lookup"><span data-stu-id="c4ebb-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="c4ebb-117">Массив макросов шейдеров, заканчивающийся нулем; Установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="c4ebb-118">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4ebb-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ebb-119">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c4ebb-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="c4ebb-120">Указатель на интерфейс include.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-120">A pointer to an include interface.</span></span> <span data-ttu-id="c4ebb-121">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c4ebb-122">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4ebb-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ebb-123">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c4ebb-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c4ebb-124">Имя функции-точки входа шейдера, где начинается выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-124">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="c4ebb-125">При компиляции результата **D3DX11CreateAsyncCompilerProcessor** игнорирует *пфунктионнаме*; рекомендуется установить *пфунктионнаме* в **значение NULL** , так как рекомендуется установить параметр указателя на **null** , если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-125">When you compile an effect, **D3DX11CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it..</span></span>

</dd> <dt>

<span data-ttu-id="c4ebb-126">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4ebb-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ebb-127">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c4ebb-127">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c4ebb-128">Строка, указывающая профиль шейдера или модель шейдера; может быть любым профилем в шейдере Model 2, Shader Model 3, Shader Model 4 или Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-128">A string that specifies the shader profile or shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="c4ebb-129">Профиль также может иметь тип действия (например, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="c4ebb-129">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="c4ebb-130">*Flags1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4ebb-130">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ebb-131">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c4ebb-131">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c4ebb-132">Флаги компиляции шейдера.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-132">Shader compile flags.</span></span>

</dd> <dt>

<span data-ttu-id="c4ebb-133">*Flags2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4ebb-133">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ebb-134">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c4ebb-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c4ebb-135">Флаги компиляции эффектов.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-135">Effect compile flags.</span></span> <span data-ttu-id="c4ebb-136">При компиляции шейдера, а не файла эффектов **D3DX11CreateAsyncCompilerProcessor** игнорирует *Flags2*. рекомендуется установить *Flags2* в нулевое значение, так как рекомендуется установить неуказательный параметр в нуль, если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-136">When you compile a shader and not an effect file, **D3DX11CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="c4ebb-137">*ппкомпиледшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c4ebb-137">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ebb-138">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c4ebb-138">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c4ebb-139">Адрес указателя на скомпилированный результат.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-139">Address of a pointer to the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="c4ebb-140">*пперрорбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c4ebb-140">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ebb-141">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c4ebb-141">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c4ebb-142">Адрес указателя для ошибок компиляции.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-142">Address of a pointer to compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="c4ebb-143">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c4ebb-143">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ebb-144">Тип: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c4ebb-144">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="c4ebb-145">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="c4ebb-145">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ebb-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4ebb-146">Return value</span></span>

<span data-ttu-id="c4ebb-147">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4ebb-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4ebb-148">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c4ebb-148">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4ebb-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4ebb-149">Remarks</span></span>

<span data-ttu-id="c4ebb-150">Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-150">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="c4ebb-151">Для приложений Магазина Windows примеры DirectX (например, [Пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , который использует модель асинхронного программирования среда выполнения Windows ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="c4ebb-151">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="c4ebb-152">Для классических приложений Win32 можно использовать [Среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.</span><span class="sxs-lookup"><span data-stu-id="c4ebb-152">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ebb-153">Требования</span><span class="sxs-lookup"><span data-stu-id="c4ebb-153">Requirements</span></span>



| <span data-ttu-id="c4ebb-154">Требование</span><span class="sxs-lookup"><span data-stu-id="c4ebb-154">Requirement</span></span> | <span data-ttu-id="c4ebb-155">Значение</span><span class="sxs-lookup"><span data-stu-id="c4ebb-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ebb-156">Header</span><span class="sxs-lookup"><span data-stu-id="c4ebb-156">Header</span></span><br/>  | <dl> <span data-ttu-id="c4ebb-157"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4ebb-157"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="c4ebb-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c4ebb-158">Library</span></span><br/> | <dl> <span data-ttu-id="c4ebb-159"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4ebb-159"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c4ebb-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4ebb-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ebb-161">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="c4ebb-161">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

