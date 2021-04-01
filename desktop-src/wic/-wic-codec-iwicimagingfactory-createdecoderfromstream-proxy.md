---
description: Функция-посредник для метода Креатедекодерфромстреам.
ms.assetid: 8395d647-c8c9-4715-b15d-a30755ae0a98
title: Функция IWICImagingFactory_CreateDecoderFromStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1f6f84c9c29d10243f1b3bcb2cad43967547eeae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818609"
---
# <a name="iwicimagingfactory_createdecoderfromstream_proxy-function"></a><span data-ttu-id="fed68-103">IWICImagingFactory \_ креатедекодерфромстреам \_ -функция</span><span class="sxs-lookup"><span data-stu-id="fed68-103">IWICImagingFactory\_CreateDecoderFromStream\_Proxy function</span></span>

<span data-ttu-id="fed68-104">Функция-посредник для метода [**креатедекодерфромстреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="fed68-104">Proxy function for the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fed68-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fed68-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromStream_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        IStream            *pIStream,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="fed68-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fed68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fed68-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fed68-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fed68-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="fed68-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="fed68-109">_pIStream \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="fed68-109">_pIStream\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fed68-110">Тип: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="fed68-110">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="fed68-111">Поток, из которого создается декодер.</span><span class="sxs-lookup"><span data-stu-id="fed68-111">The stream to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="fed68-112">_pguidVendor \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="fed68-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fed68-113">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="fed68-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="fed68-114">Идентификатор GUID поставщика для декодера.</span><span class="sxs-lookup"><span data-stu-id="fed68-114">The vendor GUID for the decoder .</span></span>

</dd> <dt>

<span data-ttu-id="fed68-115">_metadataOptions \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="fed68-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fed68-116">Тип: **[ **викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="fed68-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="fed68-117">[**Викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) , используемый при создании декодера.</span><span class="sxs-lookup"><span data-stu-id="fed68-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="fed68-118">*ппидекодер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fed68-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fed68-119">Тип: **[ **ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="fed68-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="fed68-120">Указатель, получающий указатель на новый [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="fed68-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fed68-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fed68-121">Return value</span></span>

<span data-ttu-id="fed68-122">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fed68-122">Type: **HRESULT**</span></span>

<span data-ttu-id="fed68-123">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fed68-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fed68-124">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fed68-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fed68-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="fed68-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fed68-126">Требования</span><span class="sxs-lookup"><span data-stu-id="fed68-126">Requirements</span></span>



| <span data-ttu-id="fed68-127">Требование</span><span class="sxs-lookup"><span data-stu-id="fed68-127">Requirement</span></span> | <span data-ttu-id="fed68-128">Значение</span><span class="sxs-lookup"><span data-stu-id="fed68-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed68-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fed68-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fed68-130">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fed68-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="fed68-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fed68-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fed68-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fed68-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="fed68-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fed68-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fed68-134"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fed68-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

