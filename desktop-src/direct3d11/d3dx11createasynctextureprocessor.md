---
title: Функция D3DX11CreateAsyncTextureProcessor (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. См. заметки. Создайте обработчик данных, который будет использоваться в конвейере потоков. | Функция D3DX11CreateAsyncTextureProcessor (D3DX11tex. h)
ms.assetid: 4f23d265-b326-4449-b7ca-dd0596511b35
keywords:
- D3DX11CreateAsyncTextureProcessor функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612be6da4dce05ccae368edc4effea83a823dcff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998531"
---
# <a name="d3dx11createasynctextureprocessor-function"></a><span data-ttu-id="31017-107">Функция D3DX11CreateAsyncTextureProcessor</span><span class="sxs-lookup"><span data-stu-id="31017-107">D3DX11CreateAsyncTextureProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="31017-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="31017-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="31017-109">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="31017-109">See Remarks.</span></span>

 

<span data-ttu-id="31017-110">Создайте обработчик данных, который будет использоваться в [**конвейере потоков**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="31017-110">Create a data processor to be used with a [**thread pump**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="31017-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31017-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncTextureProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="31017-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="31017-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31017-113">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31017-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31017-114">Тип: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="31017-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="31017-115">Указатель на девиве (см. [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)).</span><span class="sxs-lookup"><span data-stu-id="31017-115">A pointer to the devive (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)).</span></span>

</dd> <dt>

<span data-ttu-id="31017-116">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31017-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31017-117">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="31017-117">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="31017-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="31017-118">Optional.</span></span> <span data-ttu-id="31017-119">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="31017-119">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="31017-120">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="31017-120">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31017-121">Тип: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="31017-121">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="31017-122">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="31017-122">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31017-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31017-123">Return value</span></span>

<span data-ttu-id="31017-124">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31017-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31017-125">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="31017-125">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="31017-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="31017-126">Remarks</span></span>

<span data-ttu-id="31017-127">Этот API создает интерфейс процессора данных и загружает текстуру. [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) создает интерфейс процессора данных.</span><span class="sxs-lookup"><span data-stu-id="31017-127">This API does creates a data-processor interface and loads the texture; [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

<span data-ttu-id="31017-128">Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="31017-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="31017-129">Для приложений Магазина Windows примеры DirectX (например, [Пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , который использует модель асинхронного программирования среда выполнения Windows ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="31017-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="31017-130">Для классических приложений Win32 можно использовать [Среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.</span><span class="sxs-lookup"><span data-stu-id="31017-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="31017-131">Требования</span><span class="sxs-lookup"><span data-stu-id="31017-131">Requirements</span></span>



| <span data-ttu-id="31017-132">Требование</span><span class="sxs-lookup"><span data-stu-id="31017-132">Requirement</span></span> | <span data-ttu-id="31017-133">Значение</span><span class="sxs-lookup"><span data-stu-id="31017-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31017-134">Header</span><span class="sxs-lookup"><span data-stu-id="31017-134">Header</span></span><br/>  | <dl> <span data-ttu-id="31017-135"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="31017-135"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="31017-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31017-136">Library</span></span><br/> | <dl> <span data-ttu-id="31017-137"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31017-137"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="31017-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31017-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31017-139">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="31017-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

