---
description: Функция D3DX10CreateAsyncTextureProcessor. Создайте обработчик данных, который будет использоваться в конвейере потоков.
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: Функция D3DX10CreateAsyncTextureProcessor (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e75ab6b796f23399b453a6c7eebfe0d40e3b7b49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102792"
---
# <a name="d3dx10createasynctextureprocessor-function"></a><span data-ttu-id="b4d45-103">Функция D3DX10CreateAsyncTextureProcessor</span><span class="sxs-lookup"><span data-stu-id="b4d45-103">D3DX10CreateAsyncTextureProcessor function</span></span>

<span data-ttu-id="b4d45-104">Создайте обработчик данных, который будет использоваться в [**конвейере потоков**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="b4d45-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4d45-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4d45-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="b4d45-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4d45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4d45-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4d45-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4d45-108">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="b4d45-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="b4d45-109">Указатель на девиве (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span><span class="sxs-lookup"><span data-stu-id="b4d45-109">A pointer to the devive (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span></span>

</dd> <dt>

<span data-ttu-id="b4d45-110">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4d45-110">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4d45-111">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4d45-111">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="b4d45-112">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="b4d45-112">Optional.</span></span> <span data-ttu-id="b4d45-113">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="b4d45-113">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="b4d45-114">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4d45-114">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4d45-115">Тип: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b4d45-115">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="b4d45-116">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="b4d45-116">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4d45-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4d45-117">Return value</span></span>

<span data-ttu-id="b4d45-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4d45-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4d45-119">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b4d45-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4d45-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="b4d45-120">Remarks</span></span>

<span data-ttu-id="b4d45-121">Этот API создает интерфейс процессора данных и загружает текстуру. [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) создает интерфейс процессора данных.</span><span class="sxs-lookup"><span data-stu-id="b4d45-121">This API does creates a data-processor interface and loads the texture; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4d45-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b4d45-122">Requirements</span></span>



| <span data-ttu-id="b4d45-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b4d45-123">Requirement</span></span> | <span data-ttu-id="b4d45-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b4d45-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4d45-125">Header</span><span class="sxs-lookup"><span data-stu-id="b4d45-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b4d45-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4d45-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b4d45-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4d45-127">Library</span></span><br/> | <dl> <span data-ttu-id="b4d45-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4d45-128"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b4d45-129">См. также</span><span class="sxs-lookup"><span data-stu-id="b4d45-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d45-130">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="b4d45-130">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




