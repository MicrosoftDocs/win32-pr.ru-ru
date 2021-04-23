---
description: Функция-посредник для метода Креатефастметадатаенкодерфромдекодер.
ms.assetid: eae7ed9c-9205-4e41-91b2-461fd1f5d093
title: Функция IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cdeb682139feb03c19cd66e999b6e3b8b7b366d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693134"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromdecoder_proxy-function"></a><span data-ttu-id="70b60-103">IWICImagingFactory \_ креатефастметадатаенкодерфромдекодер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="70b60-103">IWICImagingFactory\_CreateFastMetadataEncoderFromDecoder\_Proxy function</span></span>

<span data-ttu-id="70b60-104">Функция-посредник для метода [**креатефастметадатаенкодерфромдекодер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) .</span><span class="sxs-lookup"><span data-stu-id="70b60-104">Proxy function for the [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b60-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70b60-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapDecoder       *pIDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="70b60-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="70b60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70b60-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70b60-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b60-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="70b60-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="70b60-109">_pIDecoder \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="70b60-109">_pIDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b60-110">Тип: \**[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="70b60-110">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="70b60-111">Декодер для создания [_ *ивикфастметадатаенкодер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) из.</span><span class="sxs-lookup"><span data-stu-id="70b60-111">The decoder to create the [_ *IWICFastMetadataEncoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="70b60-112">*ппифме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="70b60-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70b60-113">Тип: **[ **ивикфастметадатаенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="70b60-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="70b60-114">Указатель, получающий указатель на новый [**ивикфастметадатаенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span><span class="sxs-lookup"><span data-stu-id="70b60-114">A pointer that receives a pointer to the new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70b60-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70b60-115">Return value</span></span>

<span data-ttu-id="70b60-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="70b60-116">Type: **HRESULT**</span></span>

<span data-ttu-id="70b60-117">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="70b60-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="70b60-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70b60-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="70b60-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="70b60-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="70b60-120">Требования</span><span class="sxs-lookup"><span data-stu-id="70b60-120">Requirements</span></span>



| <span data-ttu-id="70b60-121">Требование</span><span class="sxs-lookup"><span data-stu-id="70b60-121">Requirement</span></span> | <span data-ttu-id="70b60-122">Значение</span><span class="sxs-lookup"><span data-stu-id="70b60-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b60-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70b60-123">Minimum supported client</span></span><br/> | <span data-ttu-id="70b60-124">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70b60-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="70b60-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70b60-125">Minimum supported server</span></span><br/> | <span data-ttu-id="70b60-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70b60-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="70b60-127">DLL</span><span class="sxs-lookup"><span data-stu-id="70b60-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70b60-128"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70b60-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




