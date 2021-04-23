---
title: Функция D3DX11CreateAsyncShaderResourceViewProcessor (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- D3DX11CreateAsyncShaderResourceViewProcessor функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3164aac5ddaec3d61108a2cf129b76991b8f76a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998537"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="d866a-104">Функция D3DX11CreateAsyncShaderResourceViewProcessor</span><span class="sxs-lookup"><span data-stu-id="d866a-104">D3DX11CreateAsyncShaderResourceViewProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="d866a-105">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="d866a-105">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="d866a-106">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="d866a-106">See Remarks.</span></span>

 

<span data-ttu-id="d866a-107">Создайте обработчик данных, который загрузит ресурс, а затем создайте для него представление "шейдер — ресурс".</span><span class="sxs-lookup"><span data-stu-id="d866a-107">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="d866a-108">Обработчики данных являются компонентом функции асинхронной загрузки данных в D3DX11, использующей [**потоки**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="d866a-108">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses [**thread pumps**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d866a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d866a-109">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="d866a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d866a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d866a-111">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d866a-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d866a-112">Тип: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="d866a-112">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="d866a-113">Указатель на устройство Direct3D (см. [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), которое будет использоваться для создания ресурса и представления шейдер-ресурса для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="d866a-113">Pointer to the Direct3D device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="d866a-114">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d866a-114">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d866a-115">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="d866a-115">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="d866a-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d866a-116">Optional.</span></span> <span data-ttu-id="d866a-117">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="d866a-117">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d866a-118">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d866a-118">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d866a-119">Тип: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d866a-119">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="d866a-120">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="d866a-120">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d866a-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d866a-121">Return value</span></span>

<span data-ttu-id="d866a-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d866a-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d866a-123">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d866a-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d866a-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="d866a-124">Remarks</span></span>

<span data-ttu-id="d866a-125">Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="d866a-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="d866a-126">Для приложений Магазина Windows примеры DirectX (например, [Пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , который использует модель асинхронного программирования среда выполнения Windows ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="d866a-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="d866a-127">Для классических приложений Win32 можно использовать [Среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.</span><span class="sxs-lookup"><span data-stu-id="d866a-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="d866a-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d866a-128">Requirements</span></span>



| <span data-ttu-id="d866a-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d866a-129">Requirement</span></span> | <span data-ttu-id="d866a-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d866a-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d866a-131">Header</span><span class="sxs-lookup"><span data-stu-id="d866a-131">Header</span></span><br/>  | <dl> <span data-ttu-id="d866a-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="d866a-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="d866a-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d866a-133">Library</span></span><br/> | <dl> <span data-ttu-id="d866a-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d866a-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d866a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d866a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d866a-136">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="d866a-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

