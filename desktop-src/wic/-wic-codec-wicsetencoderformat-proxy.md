---
description: Функция-посредник для согласования формата пикселей и палитры кодировщика.
ms.assetid: 01179598-ba40-4aed-a7c4-888cb4e851f4
title: Функция WICSetEncoderFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICSetEncoderFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7ea0988d29d1d9ed04668dfbe8ce86b97af6534a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702391"
---
# <a name="wicsetencoderformat_proxy-function"></a><span data-ttu-id="a2068-103">Виксетенкодерформат \_ -функция прокси</span><span class="sxs-lookup"><span data-stu-id="a2068-103">WICSetEncoderFormat\_Proxy function</span></span>

<span data-ttu-id="a2068-104">Функция-посредник для согласования формата пикселей и палитры кодировщика.</span><span class="sxs-lookup"><span data-stu-id="a2068-104">Proxy function for negotiating the pixel format and the palette for the encoder.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2068-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2068-105">Syntax</span></span>


```C++
HRESULT WICSetEncoderFormat_Proxy(
  _In_  IWICBitmapSource      *pSourceIn,
  _In_  IWICPalette           *pIPalette,
  _In_  IWICBitmapFrameEncode *pIFrameEncode,
  _Out_ IWICBitmapSource      **ppSourceOut
);
```



## <a name="parameters"></a><span data-ttu-id="a2068-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2068-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2068-107">*псаурцеин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a2068-107">*pSourceIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2068-108">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="a2068-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="a2068-109">Указатель на исходное растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="a2068-109">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="a2068-110">_pIPalette \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a2068-110">_pIPalette\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2068-111">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="a2068-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="a2068-112">Указатель на палитру, используемую для кодирования.</span><span class="sxs-lookup"><span data-stu-id="a2068-112">Pointer to the palette to use for encoding.</span></span>

</dd> <dt>

<span data-ttu-id="a2068-113">_pIFrameEncode \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a2068-113">_pIFrameEncode\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2068-114">Тип: \**[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="a2068-114">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="a2068-115">Указатель на объект кодирования кадра.</span><span class="sxs-lookup"><span data-stu-id="a2068-115">Pointer to the frame encode object.</span></span>

</dd> <dt>

<span data-ttu-id="a2068-116">_ppSourceOut \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a2068-116">_ppSourceOut\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2068-117">Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="a2068-117">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="a2068-118">Указатель, получающий указатель на источник вывода.</span><span class="sxs-lookup"><span data-stu-id="a2068-118">Pointer that receives a pointer to the output source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2068-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2068-119">Return value</span></span>

<span data-ttu-id="a2068-120">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a2068-120">Type: **HRESULT**</span></span>

<span data-ttu-id="a2068-121">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a2068-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a2068-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a2068-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2068-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="a2068-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a2068-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a2068-124">Requirements</span></span>



| <span data-ttu-id="a2068-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a2068-125">Requirement</span></span> | <span data-ttu-id="a2068-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a2068-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2068-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2068-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a2068-128">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2068-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a2068-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2068-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a2068-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a2068-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a2068-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a2068-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2068-132"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2068-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




