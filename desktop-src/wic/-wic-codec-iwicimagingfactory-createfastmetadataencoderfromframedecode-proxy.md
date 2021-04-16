---
description: Функция-посредник для метода Креатефастметадатаенкодерфромфрамедекоде.
ms.assetid: 0edc3387-47e9-401c-9153-76c8c32b52de
title: Функция IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 101bb6aca30f3511a8eb370afa8eb8fd6dda1c21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712807"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromframedecode_proxy-function"></a><span data-ttu-id="d3ae3-103">IWICImagingFactory \_ креатефастметадатаенкодерфромфрамедекоде \_ -функция</span><span class="sxs-lookup"><span data-stu-id="d3ae3-103">IWICImagingFactory\_CreateFastMetadataEncoderFromFrameDecode\_Proxy function</span></span>

<span data-ttu-id="d3ae3-104">Функция-посредник для метода [**креатефастметадатаенкодерфромфрамедекоде**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) .</span><span class="sxs-lookup"><span data-stu-id="d3ae3-104">Proxy function for the [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ae3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3ae3-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapFrameDecode   *pIFrameDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="d3ae3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3ae3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3ae3-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d3ae3-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ae3-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="d3ae3-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="d3ae3-109">_pIFrameDecoder \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d3ae3-109">_pIFrameDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ae3-110">Тип: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="d3ae3-110">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="d3ae3-111">[_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) для создания [**ивикфастметадатаенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) из.</span><span class="sxs-lookup"><span data-stu-id="d3ae3-111">The [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) to create the [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="d3ae3-112">*ппифме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d3ae3-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ae3-113">Тип: **[ **ивикфастметадатаенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="d3ae3-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="d3ae3-114">Указатель, получающий указатель на новый [**ивикфастметадатаенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span><span class="sxs-lookup"><span data-stu-id="d3ae3-114">A pointer that receives a pointer to a new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3ae3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3ae3-115">Return value</span></span>

<span data-ttu-id="d3ae3-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d3ae3-116">Type: **HRESULT**</span></span>

<span data-ttu-id="d3ae3-117">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d3ae3-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3ae3-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3ae3-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3ae3-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="d3ae3-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ae3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d3ae3-120">Requirements</span></span>



| <span data-ttu-id="d3ae3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d3ae3-121">Requirement</span></span> | <span data-ttu-id="d3ae3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d3ae3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ae3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3ae3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ae3-124">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3ae3-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d3ae3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3ae3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ae3-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3ae3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d3ae3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d3ae3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3ae3-128"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3ae3-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




