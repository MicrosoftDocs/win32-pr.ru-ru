---
title: Функция D3DX11GetImageInfoFromResource (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать функции ресурсов, а затем использовать библиотеку Директкстекс (Tools), Лоадфромксксксмемори (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Извлекает сведения об определенном изображении в ресурсе.
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- D3DX11GetImageInfoFromResource функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967a7b2c2ff03faefc12a48be18a4756e4ed3962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987002"
---
# <a name="d3dx11getimageinfofromresource-function"></a><span data-ttu-id="ebd53-106">Функция D3DX11GetImageInfoFromResource</span><span class="sxs-lookup"><span data-stu-id="ebd53-106">D3DX11GetImageInfoFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="ebd53-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="ebd53-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="ebd53-108">Вместо использования этой функции рекомендуется использовать [функции ресурсов](/windows/desktop/menurc/resources-functions), а затем использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) (Tools), **лоадфромксксксмемори** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр).</span><span class="sxs-lookup"><span data-stu-id="ebd53-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then use [DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="ebd53-109">Извлекает сведения об определенном изображении в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="ebd53-109">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd53-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebd53-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="ebd53-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebd53-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd53-112">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebd53-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd53-113">Тип: **[ **хмодуле**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ebd53-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ebd53-114">Модуль, в котором загружен ресурс.</span><span class="sxs-lookup"><span data-stu-id="ebd53-114">Module where the resource is loaded.</span></span> <span data-ttu-id="ebd53-115">Присвойте этому параметру **значение NULL** , чтобы указать модуль, связанный с образом, который операционная система использовала для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="ebd53-115">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="ebd53-116">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebd53-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd53-117">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ebd53-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ebd53-118">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="ebd53-118">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="ebd53-119">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="ebd53-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ebd53-120">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ebd53-120">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="ebd53-121">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="ebd53-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ebd53-122">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebd53-122">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd53-123">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="ebd53-123">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="ebd53-124">Дополнительный конвейер потока, который можно использовать для асинхронной загрузки информации.</span><span class="sxs-lookup"><span data-stu-id="ebd53-124">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="ebd53-125">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ebd53-125">Can be **NULL**.</span></span> <span data-ttu-id="ebd53-126">См. раздел [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="ebd53-126">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebd53-127">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebd53-127">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd53-128">Тип: **[ **\_ \_ сведения об образе D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ebd53-128">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="ebd53-129">Указатель на \_ \_ структуру сведений об изображении D3DX11, которая должна быть заполнена описанием данных в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="ebd53-129">Pointer to a D3DX11\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="ebd53-130">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ebd53-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd53-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="ebd53-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="ebd53-132">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="ebd53-132">A pointer to the return value.</span></span> <span data-ttu-id="ebd53-133">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ebd53-133">May be **NULL**.</span></span> <span data-ttu-id="ebd53-134">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="ebd53-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebd53-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebd53-135">Return value</span></span>

<span data-ttu-id="ebd53-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ebd53-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ebd53-137">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ebd53-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ebd53-138">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="ebd53-138">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="ebd53-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="ebd53-139">Remarks</span></span>

<span data-ttu-id="ebd53-140">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="ebd53-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ebd53-141">Если определен Юникод, вызов функции разрешается в **D3DX11GetImageInfoFromResourceW**.</span><span class="sxs-lookup"><span data-stu-id="ebd53-141">If Unicode is defined, the function call resolves to **D3DX11GetImageInfoFromResourceW**.</span></span> <span data-ttu-id="ebd53-142">В противном случае вызов функции разрешается в **D3DX11GetImageInfoFromResourceA** , так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="ebd53-142">Otherwise, the function call resolves to **D3DX11GetImageInfoFromResourceA** because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd53-143">Требования</span><span class="sxs-lookup"><span data-stu-id="ebd53-143">Requirements</span></span>



| <span data-ttu-id="ebd53-144">Требование</span><span class="sxs-lookup"><span data-stu-id="ebd53-144">Requirement</span></span> | <span data-ttu-id="ebd53-145">Значение</span><span class="sxs-lookup"><span data-stu-id="ebd53-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd53-146">Header</span><span class="sxs-lookup"><span data-stu-id="ebd53-146">Header</span></span><br/>  | <dl> <span data-ttu-id="ebd53-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebd53-147"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ebd53-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ebd53-148">Library</span></span><br/> | <dl> <span data-ttu-id="ebd53-149"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebd53-149"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ebd53-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebd53-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd53-151">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="ebd53-151">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

