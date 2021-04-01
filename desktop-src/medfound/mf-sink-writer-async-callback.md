---
description: Содержит указатель на интерфейс обратного вызова приложений для модуля записи приемника.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: Атрибут MF_SINK_WRITER_ASYNC_CALLBACK (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817784"
---
# <a name="mf_sink_writer_async_callback-attribute"></a><span data-ttu-id="601a5-103">\_ \_ \_ Атрибут асинхронного \_ обратного вызова для записи MF SINK</span><span class="sxs-lookup"><span data-stu-id="601a5-103">MF\_SINK\_WRITER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="601a5-104">Содержит указатель на интерфейс обратного вызова приложения для модуля записи приемника.</span><span class="sxs-lookup"><span data-stu-id="601a5-104">Contains a pointer to the application's callback interface for the sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="601a5-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="601a5-105">Data type</span></span>

<span data-ttu-id="601a5-106">**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) Имфсинквритеркаллбакк \** _ хранится как _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="601a5-106">**[**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="601a5-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="601a5-107">Get/set</span></span>

<span data-ttu-id="601a5-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="601a5-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="601a5-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="601a5-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="601a5-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="601a5-110">Remarks</span></span>

<span data-ttu-id="601a5-111">Значение этого атрибута является указателем на интерфейс [**имфсинквритеркаллбакк**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) приложения.</span><span class="sxs-lookup"><span data-stu-id="601a5-111">The value of this attribute is a pointer to the application's [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) interface.</span></span>

<span data-ttu-id="601a5-112">Используйте этот атрибут со следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="601a5-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="601a5-113">**мфкреатесинквритерфроммедиасинк**</span><span class="sxs-lookup"><span data-stu-id="601a5-113">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="601a5-114">**мфкреатесинквритерфромурл**</span><span class="sxs-lookup"><span data-stu-id="601a5-114">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="601a5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="601a5-115">Requirements</span></span>



| <span data-ttu-id="601a5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="601a5-116">Requirement</span></span> | <span data-ttu-id="601a5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="601a5-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="601a5-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="601a5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="601a5-119">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="601a5-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="601a5-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="601a5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="601a5-121">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="601a5-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="601a5-122">Header</span><span class="sxs-lookup"><span data-stu-id="601a5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="601a5-123"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="601a5-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="601a5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="601a5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601a5-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="601a5-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="601a5-126">Атрибуты модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="601a5-126">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




