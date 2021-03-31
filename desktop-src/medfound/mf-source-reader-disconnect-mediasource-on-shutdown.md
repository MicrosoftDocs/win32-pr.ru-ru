---
description: Указывает, завершает ли модуль чтения источника носитель.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: Атрибут MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351715"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a><span data-ttu-id="08bc0-103">\_ \_ Агент чтения источника MF \_ Отключить \_ медиасаурце \_ при \_ завершении работы</span><span class="sxs-lookup"><span data-stu-id="08bc0-103">MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute</span></span>

<span data-ttu-id="08bc0-104">Указывает, завершает ли [модуль чтения источника](source-reader.md) носитель.</span><span class="sxs-lookup"><span data-stu-id="08bc0-104">Specifies whether the [Source Reader](source-reader.md) shuts down the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="08bc0-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="08bc0-105">Data type</span></span>

<span data-ttu-id="08bc0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="08bc0-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="08bc0-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="08bc0-107">Get/set</span></span>

<span data-ttu-id="08bc0-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="08bc0-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="08bc0-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="08bc0-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="08bc0-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08bc0-110">Remarks</span></span>

<span data-ttu-id="08bc0-111">Этот атрибут применяется только в том случае, если приложение создает модуль чтения исходного кода из существующего объекта источника мультимедиа либо путем вызова [**мфкреатесаурцереадерфроммедиасаурце**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) , либо путем вызова [**Имфреадвритеклассфактори:: креатеинстанцефромобжект**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span><span class="sxs-lookup"><span data-stu-id="08bc0-111">This attribute applies only when the application creates the source reader from an existing media source object, either by calling [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) or by calling [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span></span>

<span data-ttu-id="08bc0-112">По умолчанию, когда приложение освобождает модуль чтения исходного кода, модуль чтения источника завершает работу источника мультимедиа, вызывая [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="08bc0-112">By default, when the application releases the source reader, the source reader shuts down the media source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span> <span data-ttu-id="08bc0-113">На этом этапе приложение больше не может использовать источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="08bc0-113">At that point, the application can no longer use the media source.</span></span>

<span data-ttu-id="08bc0-114">Однако, если \_ \_ атрибуту "чтение источника MF \_ Отключить \_ медиасаурце \_ On Shutdown" \_ присвоено **значение true**, модуль чтения исходного кода не завершает работу источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="08bc0-114">However, if the MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is **TRUE**, the source reader does not shut down the media source.</span></span> <span data-ttu-id="08bc0-115">Это означает, что приложение по-прежнему может использовать источник мультимедиа после освобождения приложением модуля чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="08bc0-115">That means the application can still use the media source after the application releases the source reader.</span></span> <span data-ttu-id="08bc0-116">Это также означает, что приложение отвечает за вызов [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="08bc0-116">It also means the application is responsible for calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>

<span data-ttu-id="08bc0-117">Если приложение создает модуль чтения исходного кода из URL-адреса или потока байтов, модуль чтения исходного кода всегда завершает работу источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="08bc0-117">If the application creates the source reader from a URL or from a byte stream, the source reader always shuts down the media source.</span></span> <span data-ttu-id="08bc0-118">\_ \_ \_ \_ \_ \_ В этом случае в этом случае пропускается атрибут MF Source DataReader Disconnect медиасаурце on Shutdown.</span><span class="sxs-lookup"><span data-stu-id="08bc0-118">The MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is ignored in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="08bc0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="08bc0-119">Requirements</span></span>



| <span data-ttu-id="08bc0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="08bc0-120">Requirement</span></span> | <span data-ttu-id="08bc0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="08bc0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08bc0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08bc0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="08bc0-123">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="08bc0-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="08bc0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08bc0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="08bc0-125">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="08bc0-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="08bc0-126">Header</span><span class="sxs-lookup"><span data-stu-id="08bc0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="08bc0-127"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="08bc0-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08bc0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08bc0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08bc0-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08bc0-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="08bc0-130">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="08bc0-130">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="08bc0-131">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="08bc0-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




