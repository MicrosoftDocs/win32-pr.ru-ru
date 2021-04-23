---
description: Указывает, поддерживает ли приемник мультимедиа поток данных оборудования.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: Атрибут MF_STREAM_SINK_SUPPORTS_HW_CONNECTION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95bfecba4cf53b6ef7c8863ec0456e310d8bcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497658"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a><span data-ttu-id="d7c95-103">\_Сток потока \_ MF \_ поддерживает \_ \_ атрибут подключения HW</span><span class="sxs-lookup"><span data-stu-id="d7c95-103">MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="d7c95-104">Указывает, поддерживает ли приемник мультимедиа поток данных оборудования.</span><span class="sxs-lookup"><span data-stu-id="d7c95-104">Indicates whether a media sink supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="d7c95-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d7c95-105">Data type</span></span>

<span data-ttu-id="d7c95-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="d7c95-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d7c95-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7c95-107">Remarks</span></span>

<span data-ttu-id="d7c95-108">Этот атрибут используется, когда приемник носителей использует прокси-сервер и может получать данные через аппаратную шину.</span><span class="sxs-lookup"><span data-stu-id="d7c95-108">This attribute is used when a media sink proxies a hardware device and is able to receive data over a hardware bus.</span></span> <span data-ttu-id="d7c95-109">Например, аппаратный декодер может отсылать аудио данные непосредственно на оборудование для воспроизведения аудио.</span><span class="sxs-lookup"><span data-stu-id="d7c95-109">For example, a hardware audio decoder might send audio data directly to the audio rendering hardware.</span></span>

<span data-ttu-id="d7c95-110">В этом сценарии декодер и приемник по-прежнему представлены в Microsoft Media Foundation с помощью [Media Foundation преобразования](media-foundation-transforms.md) (MFT) и приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d7c95-110">In this scenario, the decoder and the sink are still represented in the Microsoft Media Foundation by a [Media Foundation transform](media-foundation-transforms.md) (MFT) and a media sink.</span></span> <span data-ttu-id="d7c95-111">Однако потоки данных между этими двумя объектами на уровне конвейера не передаются только на уровне оборудования, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="d7c95-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![Схема, на которой показан источник аппаратного прокси-сервера.](images/proxy-mft4.png)

<span data-ttu-id="d7c95-113">Соединение между MFT и приемником мультимедиа согласовывается следующим образом.</span><span class="sxs-lookup"><span data-stu-id="d7c95-113">The connection between the MFT and the media sink is negotiated as follows.</span></span>

1.  <span data-ttu-id="d7c95-114">Конвейер проверяет, является ли MFT прокси-сервером, проверяя атрибут атрибута " [ \_ \_ атрибут аппаратного \_ URL \_ -адреса перечисления MFT](mft-enum-hardware-url-attribute.md) " в MFT.</span><span class="sxs-lookup"><span data-stu-id="d7c95-114">The pipeline checks if the MFT is a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="d7c95-115">Дополнительные сведения см. в разделе [Hardware МФТС](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="d7c95-115">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="d7c95-116">Конвейер получает указатель на интерфейс [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) приемника потока в приемнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d7c95-116">The pipeline gets a pointer to the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface of the stream sink on the media sink.</span></span>
3.  <span data-ttu-id="d7c95-117">Конвейер использует указатель [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) для запроса \_ приемника потока MF, \_ \_ поддерживающего \_ \_ атрибут подключения HW.</span><span class="sxs-lookup"><span data-stu-id="d7c95-117">The pipeline uses the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer to query for the MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="d7c95-118">Если этот атрибут представлен и равен **true**, источник мультимедиа поддерживает аппаратные подключения.</span><span class="sxs-lookup"><span data-stu-id="d7c95-118">If this attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="d7c95-119">Конвейер задает атрибут [ \_ \_ \_ атрибута потока MFT для подключения](mft-connected-stream-attribute.md) к приемнику потока.</span><span class="sxs-lookup"><span data-stu-id="d7c95-119">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the stream sink.</span></span> <span data-ttu-id="d7c95-120">Значением этого атрибута является указатель [**имфаттрибуте**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) из MFT.</span><span class="sxs-lookup"><span data-stu-id="d7c95-120">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer from the MFT.</span></span>
5.  <span data-ttu-id="d7c95-121">Конвейер устанавливает **значение true** для [MFT, \_ подключенного к атрибуту \_ \_ \_ аудиопотока](mft-connected-to-hw-stream.md) , как к приемнику потока, так и к таблице MFT.</span><span class="sxs-lookup"><span data-stu-id="d7c95-121">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the stream sink and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c95-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d7c95-122">Requirements</span></span>



| <span data-ttu-id="d7c95-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d7c95-123">Requirement</span></span> | <span data-ttu-id="d7c95-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d7c95-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c95-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7c95-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d7c95-126">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="d7c95-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d7c95-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7c95-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d7c95-128">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="d7c95-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d7c95-129">Header</span><span class="sxs-lookup"><span data-stu-id="d7c95-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7c95-130"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7c95-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c95-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7c95-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c95-132">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7c95-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




