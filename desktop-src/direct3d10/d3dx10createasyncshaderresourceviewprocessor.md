---
description: Создайте обработчик данных, который загрузит ресурс, а затем создайте для него представление "шейдер — ресурс". Обработчики данных являются компонентом функции асинхронной загрузки данных в D3DX10, использующей потоки.
ms.assetid: 6e5a6138-c218-4200-a24e-d906d34933b8
title: Функция D3DX10CreateAsyncShaderResourceViewProcessor (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderResourceViewProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bd55e4191382c5abde52ce05d0a16b5533d79eac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713909"
---
# <a name="d3dx10createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="44bfd-104">Функция D3DX10CreateAsyncShaderResourceViewProcessor</span><span class="sxs-lookup"><span data-stu-id="44bfd-104">D3DX10CreateAsyncShaderResourceViewProcessor function</span></span>

<span data-ttu-id="44bfd-105">Создайте обработчик данных, который загрузит ресурс, а затем создайте для него представление "шейдер — ресурс".</span><span class="sxs-lookup"><span data-stu-id="44bfd-105">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="44bfd-106">Обработчики данных являются компонентом функции асинхронной загрузки данных в D3DX10, использующей [**потоки**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="44bfd-106">Data processors are a component of the asynchronous data loading feature in D3DX10 that uses [**thread pumps**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="44bfd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44bfd-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="44bfd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="44bfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44bfd-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44bfd-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44bfd-110">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="44bfd-110">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="44bfd-111">Указатель на устройство Direct3D (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), которое будет использоваться для создания ресурса и представления шейдер-ресурса для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="44bfd-111">Pointer to the Direct3D device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="44bfd-112">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44bfd-112">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44bfd-113">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="44bfd-113">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="44bfd-114">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="44bfd-114">Optional.</span></span> <span data-ttu-id="44bfd-115">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="44bfd-115">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="44bfd-116">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="44bfd-116">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44bfd-117">Тип: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="44bfd-117">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="44bfd-118">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="44bfd-118">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44bfd-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44bfd-119">Return value</span></span>

<span data-ttu-id="44bfd-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44bfd-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44bfd-121">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="44bfd-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44bfd-122">Требования</span><span class="sxs-lookup"><span data-stu-id="44bfd-122">Requirements</span></span>



| <span data-ttu-id="44bfd-123">Требование</span><span class="sxs-lookup"><span data-stu-id="44bfd-123">Requirement</span></span> | <span data-ttu-id="44bfd-124">Значение</span><span class="sxs-lookup"><span data-stu-id="44bfd-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44bfd-125">Header</span><span class="sxs-lookup"><span data-stu-id="44bfd-125">Header</span></span><br/> | <dl> <span data-ttu-id="44bfd-126"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="44bfd-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44bfd-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44bfd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44bfd-128">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="44bfd-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




