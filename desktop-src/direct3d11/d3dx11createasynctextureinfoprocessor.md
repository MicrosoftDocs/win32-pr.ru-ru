---
title: Функция D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. См. заметки. Создайте обработчик данных, который будет использоваться в конвейере потоков. | Функция D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
ms.assetid: 87de73a5-21f7-4abd-b83a-65c6761681c3
keywords:
- D3DX11CreateAsyncTextureInfoProcessor функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureInfoProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aac60b1d496e0f1d4ecb604b18a8ef71cac8b5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998543"
---
# <a name="d3dx11createasynctextureinfoprocessor-function"></a><span data-ttu-id="0e13b-107">Функция D3DX11CreateAsyncTextureInfoProcessor</span><span class="sxs-lookup"><span data-stu-id="0e13b-107">D3DX11CreateAsyncTextureInfoProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="0e13b-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="0e13b-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="0e13b-109">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="0e13b-109">See Remarks.</span></span>

 

<span data-ttu-id="0e13b-110">Создайте обработчик данных, который будет использоваться в [**конвейере потоков**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="0e13b-110">Create a data processor to be used with a [**thread pump**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e13b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e13b-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncTextureInfoProcessor(
  _In_  D3DX11_IMAGE_INFO    *pImageInfo,
  _Out_ ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="0e13b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e13b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e13b-113">*пимажеинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e13b-113">*pImageInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e13b-114">Тип: **[ **\_ \_ сведения об образе D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e13b-114">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="0e13b-115">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0e13b-115">Optional.</span></span> <span data-ttu-id="0e13b-116">Определяет характеристики текстуры (см. [**\_ \_ сведения об образе D3DX11**](d3dx11-image-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="0e13b-116">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="0e13b-117">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0e13b-117">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e13b-118">Тип: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="0e13b-118">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="0e13b-119">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="0e13b-119">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e13b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e13b-120">Return value</span></span>

<span data-ttu-id="0e13b-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e13b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e13b-122">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0e13b-122">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e13b-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e13b-123">Remarks</span></span>

<span data-ttu-id="0e13b-124">Этот API создает интерфейс процессора данных; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) создает интерфейс процессора данных и загружает текстуру.</span><span class="sxs-lookup"><span data-stu-id="0e13b-124">This API does creates a data-processor interface; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

<span data-ttu-id="0e13b-125">Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="0e13b-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="0e13b-126">Для приложений Магазина Windows примеры DirectX (например, [Пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , который использует модель асинхронного программирования среда выполнения Windows ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="0e13b-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="0e13b-127">Для классических приложений Win32 можно использовать [Среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.</span><span class="sxs-lookup"><span data-stu-id="0e13b-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e13b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="0e13b-128">Requirements</span></span>



| <span data-ttu-id="0e13b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="0e13b-129">Requirement</span></span> | <span data-ttu-id="0e13b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="0e13b-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e13b-131">Header</span><span class="sxs-lookup"><span data-stu-id="0e13b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="0e13b-132"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e13b-132"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0e13b-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0e13b-133">Library</span></span><br/> | <dl> <span data-ttu-id="0e13b-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e13b-134"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0e13b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e13b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e13b-136">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="0e13b-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

