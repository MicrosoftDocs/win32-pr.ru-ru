---
description: Содержит указатель на интерфейс обратного вызова приложений для модуля чтения исходного кода.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: Атрибут MF_SOURCE_READER_ASYNC_CALLBACK (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66542a155fbb6fa3e56958733626b1d0b750ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265355"
---
# <a name="mf_source_reader_async_callback-attribute"></a><span data-ttu-id="562bd-103">\_ \_ \_ Атрибут асинхронного \_ обратного вызова для чтения источника MF</span><span class="sxs-lookup"><span data-stu-id="562bd-103">MF\_SOURCE\_READER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="562bd-104">Содержит указатель на интерфейс обратного вызова приложения для [модуля чтения исходного кода](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="562bd-104">Contains a pointer to the application's callback interface for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="562bd-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="562bd-105">Data type</span></span>

<span data-ttu-id="562bd-106">**Имфсаурцереадеркаллбакк \** _ хранится как _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="562bd-106">**IMFSourceReaderCallback\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="562bd-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="562bd-107">Get/set</span></span>

<span data-ttu-id="562bd-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="562bd-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="562bd-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="562bd-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="562bd-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="562bd-110">Remarks</span></span>

<span data-ttu-id="562bd-111">Значение этого атрибута является указателем на интерфейс [**имфсаурцереадеркаллбакк**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) приложения.</span><span class="sxs-lookup"><span data-stu-id="562bd-111">The value of this attribute is a pointer to the application's [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) interface.</span></span>

<span data-ttu-id="562bd-112">Используйте этот атрибут со следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="562bd-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="562bd-113">**мфкреатесаурцереадерфромбитестреам**</span><span class="sxs-lookup"><span data-stu-id="562bd-113">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="562bd-114">**мфкреатесаурцереадерфроммедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="562bd-114">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="562bd-115">**мфкреатесаурцереадерфромурл**</span><span class="sxs-lookup"><span data-stu-id="562bd-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a><span data-ttu-id="562bd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="562bd-116">Requirements</span></span>



| <span data-ttu-id="562bd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="562bd-117">Requirement</span></span> | <span data-ttu-id="562bd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="562bd-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="562bd-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="562bd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="562bd-120">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="562bd-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="562bd-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="562bd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="562bd-122">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="562bd-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="562bd-123">Header</span><span class="sxs-lookup"><span data-stu-id="562bd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="562bd-124"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="562bd-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="562bd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="562bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562bd-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="562bd-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="562bd-127">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="562bd-127">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="562bd-128">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="562bd-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




