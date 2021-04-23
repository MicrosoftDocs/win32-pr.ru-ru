---
title: Функция D3DX11CreateAsyncShaderPreprocessProcessor (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. См. заметки. Асинхронно Создайте обработчик данных для шейдера.
ms.assetid: a7e9754b-acc1-49d0-bd8e-b116bc3c7e3a
keywords:
- D3DX11CreateAsyncShaderPreprocessProcessor функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderPreprocessProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e58b267f186e5fd0104b10e9f9423f407aaf13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000444"
---
# <a name="d3dx11createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="09390-106">Функция D3DX11CreateAsyncShaderPreprocessProcessor</span><span class="sxs-lookup"><span data-stu-id="09390-106">D3DX11CreateAsyncShaderPreprocessProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="09390-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="09390-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="09390-108">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="09390-108">See Remarks.</span></span>

 

<span data-ttu-id="09390-109">Асинхронно Создайте обработчик данных для шейдера.</span><span class="sxs-lookup"><span data-stu-id="09390-109">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="09390-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09390-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="09390-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="09390-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09390-112">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="09390-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09390-113">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="09390-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="09390-114">Строка, содержащая имя файла шейдера.</span><span class="sxs-lookup"><span data-stu-id="09390-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="09390-115">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="09390-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09390-116">Тип: **const D3D11ный \_ \_ макрос \* шейдера**</span><span class="sxs-lookup"><span data-stu-id="09390-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="09390-117">Массив макросов шейдеров, заканчивающийся нулем; Установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="09390-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="09390-118">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="09390-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09390-119">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="09390-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="09390-120">Указатель на интерфейс include; Установите значение **null** , чтобы указать, что файл не включен.</span><span class="sxs-lookup"><span data-stu-id="09390-120">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="09390-121">*ппшадертекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="09390-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09390-122">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="09390-122">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="09390-123">Адрес указателя на буфер, который содержит текст ASCII шейдера.</span><span class="sxs-lookup"><span data-stu-id="09390-123">Address of a pointer to a buffer that contains the ASCII text of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="09390-124">*пперрорбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="09390-124">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09390-125">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="09390-125">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="09390-126">Адрес указателя на буфер, содержащий ошибки компиляции.</span><span class="sxs-lookup"><span data-stu-id="09390-126">Address of a pointer to a buffer that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="09390-127">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="09390-127">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09390-128">Тип: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="09390-128">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="09390-129">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="09390-129">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09390-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09390-130">Return value</span></span>

<span data-ttu-id="09390-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09390-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09390-132">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="09390-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="09390-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="09390-133">Remarks</span></span>

<span data-ttu-id="09390-134">Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="09390-134">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="09390-135">Для приложений Магазина Windows примеры DirectX (например, [Пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , который использует модель асинхронного программирования среда выполнения Windows ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="09390-135">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="09390-136">Для классических приложений Win32 можно использовать [Среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.</span><span class="sxs-lookup"><span data-stu-id="09390-136">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="09390-137">Требования</span><span class="sxs-lookup"><span data-stu-id="09390-137">Requirements</span></span>



| <span data-ttu-id="09390-138">Требование</span><span class="sxs-lookup"><span data-stu-id="09390-138">Requirement</span></span> | <span data-ttu-id="09390-139">Значение</span><span class="sxs-lookup"><span data-stu-id="09390-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09390-140">Header</span><span class="sxs-lookup"><span data-stu-id="09390-140">Header</span></span><br/>  | <dl> <span data-ttu-id="09390-141"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="09390-141"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="09390-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="09390-142">Library</span></span><br/> | <dl> <span data-ttu-id="09390-143"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09390-143"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="09390-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09390-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09390-145">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="09390-145">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

