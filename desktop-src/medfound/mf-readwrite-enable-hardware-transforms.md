---
description: Позволяет модулю чтения источника или записи приемника использовать Media Foundation преобразования на основе оборудования (МФТС).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: Атрибут MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347505"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a><span data-ttu-id="33d2c-103">\_Атрибут MF ReadWrite \_ включить \_ аппаратные \_ преобразования</span><span class="sxs-lookup"><span data-stu-id="33d2c-103">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="33d2c-104">Позволяет модулю чтения источника или записи приемника использовать Media Foundation преобразования на основе оборудования (МФТС).</span><span class="sxs-lookup"><span data-stu-id="33d2c-104">Enables the source reader or sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>

## <a name="data-type"></a><span data-ttu-id="33d2c-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="33d2c-105">Data type</span></span>

<span data-ttu-id="33d2c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="33d2c-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="33d2c-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="33d2c-107">Get/set</span></span>

<span data-ttu-id="33d2c-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="33d2c-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="33d2c-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="33d2c-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="33d2c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33d2c-110">Remarks</span></span>

<span data-ttu-id="33d2c-111">По умолчанию модуль чтения источника и модуль записи приемника не используют аппаратные декодеры или кодировщики.</span><span class="sxs-lookup"><span data-stu-id="33d2c-111">By default, the source reader and sink writer do not use hardware decoders or encoders.</span></span> <span data-ttu-id="33d2c-112">Чтобы включить использование оборудования МФТС, установите для этого атрибута значение **true** при создании модуля чтения исходного кода или модуля записи приемника.</span><span class="sxs-lookup"><span data-stu-id="33d2c-112">To enable the use of hardware MFTs, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="33d2c-113">Используйте этот атрибут со следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="33d2c-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="33d2c-114">**мфкреатесаурцереадерфромбитестреам**</span><span class="sxs-lookup"><span data-stu-id="33d2c-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="33d2c-115">**мфкреатесаурцереадерфроммедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="33d2c-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="33d2c-116">**мфкреатесаурцереадерфромурл**</span><span class="sxs-lookup"><span data-stu-id="33d2c-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="33d2c-117">**мфкреатесинквритерфроммедиасинк**</span><span class="sxs-lookup"><span data-stu-id="33d2c-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="33d2c-118">**мфкреатесинквритерфромурл**</span><span class="sxs-lookup"><span data-stu-id="33d2c-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="33d2c-119">Существует одно исключение, связанное с поведением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="33d2c-119">There is one exception to the default behavior.</span></span> <span data-ttu-id="33d2c-120">Средство чтения исходного кода и модуль записи приемника автоматически используют МФТС, которые зарегистрированы локально в процессе вызывающего.</span><span class="sxs-lookup"><span data-stu-id="33d2c-120">The source reader and sink writer automatically use MFTs that are registered locally in the caller's process.</span></span> <span data-ttu-id="33d2c-121">Чтобы зарегистрировать таблицу MFT локально, вызовите [**мфтрегистерлокал**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) или [**мфтрегистерлокалбиклсид**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span><span class="sxs-lookup"><span data-stu-id="33d2c-121">To register an MFT locally, call [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span></span> <span data-ttu-id="33d2c-122">МФТС оборудования, зарегистрированные локально, используются, даже если не установлен атрибут **\_ Enable ReadWrite ( \_ включить \_ аппаратное \_ Преобразование** ).</span><span class="sxs-lookup"><span data-stu-id="33d2c-122">Hardware MFTs that are registered locally are used even if the **MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS** attribute is not set.</span></span>

<span data-ttu-id="33d2c-123">Этот атрибут не влияет на декодирование видео с аппаратным ускорением, которое использует ускорение видео DirectX (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="33d2c-123">This attribute does not affect hardware-accelerated video decoding that uses DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="33d2c-124">Чтобы включить декодирование ДКСВА в модуле чтения исходного кода, установите [атрибут \_ \_ \_ \_ диспетчера D3D источника MF](mf-source-reader-d3d-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="33d2c-124">To enable DXVA decoding in the source reader, set the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="33d2c-125">Если этот атрибут имеет **значение true**, не устанавливайте [атрибут \_ \_ \_ преобразователей MF ReadWrite Disable](mf-readwrite-disable-converters.md) .</span><span class="sxs-lookup"><span data-stu-id="33d2c-125">If this attribute is **TRUE**, do not set the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="33d2c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="33d2c-126">Requirements</span></span>



| <span data-ttu-id="33d2c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="33d2c-127">Requirement</span></span> | <span data-ttu-id="33d2c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="33d2c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33d2c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33d2c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="33d2c-130">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="33d2c-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="33d2c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33d2c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="33d2c-132">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="33d2c-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="33d2c-133">Header</span><span class="sxs-lookup"><span data-stu-id="33d2c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="33d2c-134"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="33d2c-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33d2c-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33d2c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33d2c-136">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33d2c-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="33d2c-137">Атрибуты модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="33d2c-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="33d2c-138">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="33d2c-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




