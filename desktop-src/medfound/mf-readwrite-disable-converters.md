---
description: Включает или отключает преобразование формата модулем чтения источника или приемником.
ms.assetid: 282b70c3-c81c-47dd-bfa2-7e77138ccb91
title: Атрибут MF_READWRITE_DISABLE_CONVERTERS (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8532c45ca3aeb272fa6b6ef422e0d82e40bd3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272502"
---
# <a name="mf_readwrite_disable_converters-attribute"></a><span data-ttu-id="fd484-103">\_ \_ Атрибут запрета на отключать ReadWrite \_</span><span class="sxs-lookup"><span data-stu-id="fd484-103">MF\_READWRITE\_DISABLE\_CONVERTERS attribute</span></span>

<span data-ttu-id="fd484-104">Включает или отключает преобразование формата модулем чтения источника или приемником.</span><span class="sxs-lookup"><span data-stu-id="fd484-104">Enables or disables format conversions by the source reader or sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd484-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fd484-105">Data type</span></span>

<span data-ttu-id="fd484-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fd484-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="fd484-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="fd484-107">Get/set</span></span>

<span data-ttu-id="fd484-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="fd484-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="fd484-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="fd484-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd484-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd484-110">Remarks</span></span>

<span data-ttu-id="fd484-111">По умолчанию средство чтения исходного кода и модуль записи приемника могут выполнять некоторые преобразования формата в несжатых потоках аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="fd484-111">By default, the source reader and sink writer can perform some format conversions on uncompressed audio and video streams.</span></span> <span data-ttu-id="fd484-112">Чтобы отключить это поведение, задайте для этого атрибута **значение true** при создании модуля чтения источника или модуля записи приемника.</span><span class="sxs-lookup"><span data-stu-id="fd484-112">To disable this behavior, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="fd484-113">Используйте этот атрибут со следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="fd484-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="fd484-114">**мфкреатесаурцереадерфромбитестреам**</span><span class="sxs-lookup"><span data-stu-id="fd484-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="fd484-115">**мфкреатесаурцереадерфроммедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="fd484-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="fd484-116">**мфкреатесаурцереадерфромурл**</span><span class="sxs-lookup"><span data-stu-id="fd484-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="fd484-117">**мфкреатесинквритерфроммедиасинк**</span><span class="sxs-lookup"><span data-stu-id="fd484-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="fd484-118">**мфкреатесинквритерфромурл**</span><span class="sxs-lookup"><span data-stu-id="fd484-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="fd484-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fd484-119">Requirements</span></span>



| <span data-ttu-id="fd484-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fd484-120">Requirement</span></span> | <span data-ttu-id="fd484-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fd484-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd484-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd484-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fd484-123">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="fd484-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="fd484-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd484-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fd484-125">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="fd484-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fd484-126">Header</span><span class="sxs-lookup"><span data-stu-id="fd484-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd484-127"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd484-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd484-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd484-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd484-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd484-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd484-130">Атрибуты модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="fd484-130">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd484-131">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="fd484-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




