---
description: Создайте обработчик данных, который будет использоваться в конвейере потоков.
ms.assetid: e97b6aca-1839-48ea-8dab-b96a52ec2a68
title: Функция D3DX10CreateAsyncTextureInfoProcessor (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureInfoProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fe56fc217af6ebae9255b4f72d3c3af2f279fa29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713908"
---
# <a name="d3dx10createasynctextureinfoprocessor-function"></a><span data-ttu-id="db861-103">Функция D3DX10CreateAsyncTextureInfoProcessor</span><span class="sxs-lookup"><span data-stu-id="db861-103">D3DX10CreateAsyncTextureInfoProcessor function</span></span>

<span data-ttu-id="db861-104">Создайте обработчик данных, который будет использоваться в [**конвейере потоков**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="db861-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="db861-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db861-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureInfoProcessor(
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="db861-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db861-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db861-107">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db861-107">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db861-108">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="db861-108">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="db861-109">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="db861-109">Optional.</span></span> <span data-ttu-id="db861-110">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="db861-110">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="db861-111">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db861-111">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db861-112">Тип: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="db861-112">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="db861-113">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="db861-113">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db861-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db861-114">Return value</span></span>

<span data-ttu-id="db861-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db861-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db861-116">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="db861-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db861-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db861-117">Remarks</span></span>

<span data-ttu-id="db861-118">Этот API создает интерфейс процессора данных; [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) создает интерфейс процессора данных и загружает текстуру.</span><span class="sxs-lookup"><span data-stu-id="db861-118">This API does creates a data-processor interface; [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="db861-119">Требования</span><span class="sxs-lookup"><span data-stu-id="db861-119">Requirements</span></span>



| <span data-ttu-id="db861-120">Требование</span><span class="sxs-lookup"><span data-stu-id="db861-120">Requirement</span></span> | <span data-ttu-id="db861-121">Значение</span><span class="sxs-lookup"><span data-stu-id="db861-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db861-122">Header</span><span class="sxs-lookup"><span data-stu-id="db861-122">Header</span></span><br/>  | <dl> <span data-ttu-id="db861-123"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="db861-123"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="db861-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="db861-124">Library</span></span><br/> | <dl> <span data-ttu-id="db861-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db861-125"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="db861-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db861-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db861-127">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="db861-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




