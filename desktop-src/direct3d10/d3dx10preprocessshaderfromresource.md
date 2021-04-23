---
description: Примечание. вместо использования этой устаревшей функции рекомендуется использовать API D3DPreprocess. Создание шейдера из ресурса без его компиляции.
ms.assetid: ca93e208-7627-4bf5-ab83-d4e906e149eb
title: Функция D3DX10PreprocessShaderFromResource (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 81a9f272cb0769d4313a4375f98bdc25b9e403e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424538"
---
# <a name="d3dx10preprocessshaderfromresource-function"></a><span data-ttu-id="90e28-104">Функция D3DX10PreprocessShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="90e28-104">D3DX10PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="90e28-105">Вместо использования этой устаревшей функции рекомендуется использовать API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="90e28-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="90e28-106">Создание шейдера из ресурса без его компиляции.</span><span class="sxs-lookup"><span data-stu-id="90e28-106">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e28-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90e28-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="90e28-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="90e28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90e28-109">*хмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90e28-109">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e28-110">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90e28-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90e28-111">Обработчик для модуля ресурсов, содержащего шейдер.</span><span class="sxs-lookup"><span data-stu-id="90e28-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="90e28-112">ХМОДУЛЕ можно получить с помощью [функции ошибка GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="90e28-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="90e28-113">*пресаурценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90e28-113">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e28-114">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90e28-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90e28-115">Имя ресурса в Side Хмодуле, содержащего шейдер.</span><span class="sxs-lookup"><span data-stu-id="90e28-115">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="90e28-116">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="90e28-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="90e28-117">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="90e28-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="90e28-118">*псркфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90e28-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e28-119">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90e28-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90e28-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="90e28-120">Optional.</span></span> <span data-ttu-id="90e28-121">Имя файла эффектов, которое используется только для сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="90e28-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="90e28-122">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="90e28-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="90e28-123">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90e28-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e28-124">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="90e28-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="90e28-125">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="90e28-125">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="90e28-126">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90e28-126">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e28-127">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="90e28-127">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="90e28-128">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Установите значение **null** , чтобы указать, что файл не включен.</span><span class="sxs-lookup"><span data-stu-id="90e28-128">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="90e28-129">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90e28-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e28-130">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="90e28-130">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="90e28-131">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="90e28-131">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="90e28-132">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="90e28-132">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="90e28-133">*ппшадертекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="90e28-133">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90e28-134">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="90e28-134">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="90e28-135">Указатель на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), содержащий некомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="90e28-135">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="90e28-136">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="90e28-136">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90e28-137">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="90e28-137">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="90e28-138">Адрес указателя на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки создания эффектов, если таковые возникли.</span><span class="sxs-lookup"><span data-stu-id="90e28-138">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90e28-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90e28-139">Return value</span></span>

<span data-ttu-id="90e28-140">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90e28-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90e28-141">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="90e28-141">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90e28-142">Требования</span><span class="sxs-lookup"><span data-stu-id="90e28-142">Requirements</span></span>



| <span data-ttu-id="90e28-143">Требование</span><span class="sxs-lookup"><span data-stu-id="90e28-143">Requirement</span></span> | <span data-ttu-id="90e28-144">Значение</span><span class="sxs-lookup"><span data-stu-id="90e28-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90e28-145">Header</span><span class="sxs-lookup"><span data-stu-id="90e28-145">Header</span></span><br/>  | <dl> <span data-ttu-id="90e28-146"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="90e28-146"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="90e28-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="90e28-147">Library</span></span><br/> | <dl> <span data-ttu-id="90e28-148"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90e28-148"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90e28-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90e28-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e28-150">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="90e28-150">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
