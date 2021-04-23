---
description: Функция-посредник для метода Креатедекодерфромфилехандле.
ms.assetid: bc7f8a07-6d82-4d95-88ef-979d571758f4
title: Функция IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 15c515bb17641e2e7b70b79552fe3bacf1f1c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998704"
---
# <a name="iwicimagingfactory_createdecoderfromfilehandle_proxy-function"></a><span data-ttu-id="e6329-103">IWICImagingFactory \_ креатедекодерфромфилехандле \_ -функция</span><span class="sxs-lookup"><span data-stu-id="e6329-103">IWICImagingFactory\_CreateDecoderFromFileHandle\_Proxy function</span></span>

<span data-ttu-id="e6329-104">Функция-посредник для метода [**креатедекодерфромфилехандле**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) .</span><span class="sxs-lookup"><span data-stu-id="e6329-104">Proxy function for the [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6329-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6329-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFileHandle_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        ULONG_PTR          hFile,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="e6329-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6329-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6329-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6329-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6329-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="e6329-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="e6329-109">_hFile \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e6329-109">_hFile\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6329-110">Тип: **ulong \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="e6329-110">Type: **ULONG\_PTR**</span></span>

<span data-ttu-id="e6329-111">Описатель файла, из которого создается декодер.</span><span class="sxs-lookup"><span data-stu-id="e6329-111">The file handle to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="e6329-112">*пгуидвендор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6329-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6329-113">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="e6329-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="e6329-114">Идентификатор GUID поставщика для декодера.</span><span class="sxs-lookup"><span data-stu-id="e6329-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="e6329-115">_metadataOptions \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e6329-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6329-116">Тип: **[ **викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="e6329-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="e6329-117">[**Викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) , используемый при создании декодера.</span><span class="sxs-lookup"><span data-stu-id="e6329-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="e6329-118">*ппидекодер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e6329-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6329-119">Тип: **[ **ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="e6329-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="e6329-120">Указатель, получающий указатель на новый [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="e6329-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6329-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6329-121">Return value</span></span>

<span data-ttu-id="e6329-122">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e6329-122">Type: **HRESULT**</span></span>

<span data-ttu-id="e6329-123">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e6329-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6329-124">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6329-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6329-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="e6329-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e6329-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e6329-126">Requirements</span></span>



| <span data-ttu-id="e6329-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e6329-127">Requirement</span></span> | <span data-ttu-id="e6329-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e6329-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6329-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6329-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e6329-130">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6329-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e6329-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6329-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e6329-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6329-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e6329-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e6329-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6329-134"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6329-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




