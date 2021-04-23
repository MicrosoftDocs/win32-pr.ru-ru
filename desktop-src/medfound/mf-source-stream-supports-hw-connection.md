---
description: Указывает, поддерживает ли источник мультимедиа поток данных оборудования.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: Атрибут MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712576"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a><span data-ttu-id="baee6-103">В \_ исходном \_ потоке MF \_ поддерживается \_ \_ атрибут подключения HW</span><span class="sxs-lookup"><span data-stu-id="baee6-103">MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="baee6-104">Указывает, поддерживает ли источник мультимедиа поток данных оборудования.</span><span class="sxs-lookup"><span data-stu-id="baee6-104">Indicates whether a media source supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="baee6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="baee6-105">Data type</span></span>

<span data-ttu-id="baee6-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="baee6-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="baee6-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="baee6-107">Remarks</span></span>

<span data-ttu-id="baee6-108">Этот атрибут используется, когда источник мультимедиа использует прокси-сервер и может передавать данные на аппаратную шину, не отправляя данные в ЦП.</span><span class="sxs-lookup"><span data-stu-id="baee6-108">This attribute is used when a media source proxies a hardware device and is able to transfer data downstream over a hardware bus, without sending data up to the CPU.</span></span> <span data-ttu-id="baee6-109">Например, веб-камера может доставлять видео в формате H. 264 непосредственно в Интегрированный аппаратный декодер.</span><span class="sxs-lookup"><span data-stu-id="baee6-109">For example, a webcam might deliver H.264-encoded video directly to an integrated hardware decoder.</span></span>

<span data-ttu-id="baee6-110">В этом сценарии источник и декодер по-прежнему представлены в Microsoft Media Foundation объектом [источника мультимедиа](media-sources.md) и [преобразованием Media Foundation](media-foundation-transforms.md) (MFT).</span><span class="sxs-lookup"><span data-stu-id="baee6-110">In this scenario, the source and decoder are still represented in the Microsoft Media Foundation by a [media source](media-sources.md) object and a [Media Foundation transform](media-foundation-transforms.md) (MFT).</span></span> <span data-ttu-id="baee6-111">Однако потоки данных между этими двумя объектами на уровне конвейера не передаются только на уровне оборудования, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="baee6-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![Схема, на которой показан источник аппаратного прокси-сервера.](images/proxy-mft3.png)

<span data-ttu-id="baee6-113">Соединение между источником мультимедиа и MFT согласовывается следующим образом.</span><span class="sxs-lookup"><span data-stu-id="baee6-113">The connection between the media source and the MFT is negotiated as follows.</span></span>

1.  <span data-ttu-id="baee6-114">Конвейер запрашивает источник мультимедиа для интерфейса [**имфмедиасаурцеекс**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="baee6-114">The pipeline queries the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span> <span data-ttu-id="baee6-115">(Этот интерфейс является необязательным для поддержки источников мультимедиа.)</span><span class="sxs-lookup"><span data-stu-id="baee6-115">(This interface is optional for media sources to support.)</span></span>
2.  <span data-ttu-id="baee6-116">Конвейер вызывает [**имфмедиасаурцеекс:: жетстреаматтрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="baee6-116">The pipeline calls [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
3.  <span data-ttu-id="baee6-117">Конвейерные запросы к \_ исходному \_ потоку \_ MF \_ поддерживают \_ атрибут подключения HW.</span><span class="sxs-lookup"><span data-stu-id="baee6-117">The pipeline queries for the MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="baee6-118">Если атрибут представлен и равен **true**, источник мультимедиа поддерживает аппаратные подключения.</span><span class="sxs-lookup"><span data-stu-id="baee6-118">If the attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="baee6-119">Конвейер проверяет, является ли таблица MFT также прокси-сервером, проверяя атрибут [атрибута " \_ \_ \_ \_ атрибут аппаратного URL-адреса перечисления MFT](mft-enum-hardware-url-attribute.md) " в MFT.</span><span class="sxs-lookup"><span data-stu-id="baee6-119">The pipeline checks if the MFT is also a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="baee6-120">Дополнительные сведения см. в разделе [Hardware МФТС](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="baee6-120">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
5.  <span data-ttu-id="baee6-121">Конвейер задает атрибут [ \_ \_ \_ атрибута потока MFT, подключенного к](mft-connected-stream-attribute.md) MFT.</span><span class="sxs-lookup"><span data-stu-id="baee6-121">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="baee6-122">Значением этого атрибута является указатель [**имфаттрибуте**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , полученный из источника мультимедиа на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="baee6-122">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer obtained from the media source in step 2.</span></span>
6.  <span data-ttu-id="baee6-123">Конвейер задает **значение true** для файла [MFT, \_ подключенного к атрибуту \_ \_ \_ аудиопотока](mft-connected-to-hw-stream.md) , как к источнику мультимедиа, так и к таблице MFT.</span><span class="sxs-lookup"><span data-stu-id="baee6-123">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the media source and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="baee6-124">Требования</span><span class="sxs-lookup"><span data-stu-id="baee6-124">Requirements</span></span>



| <span data-ttu-id="baee6-125">Требование</span><span class="sxs-lookup"><span data-stu-id="baee6-125">Requirement</span></span> | <span data-ttu-id="baee6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="baee6-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="baee6-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="baee6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="baee6-128">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="baee6-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="baee6-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="baee6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="baee6-130">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="baee6-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="baee6-131">Header</span><span class="sxs-lookup"><span data-stu-id="baee6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="baee6-132"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="baee6-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baee6-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="baee6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baee6-134">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="baee6-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="baee6-135">Оборудование МФТС</span><span class="sxs-lookup"><span data-stu-id="baee6-135">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> </dl>

 

 




