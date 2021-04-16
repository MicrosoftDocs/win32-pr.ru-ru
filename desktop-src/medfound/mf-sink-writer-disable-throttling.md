---
description: Указывает, ограничивает ли модуль записи приемника скорость входящих данных.
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: Атрибут MF_SINK_WRITER_DISABLE_THROTTLING (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712858"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a><span data-ttu-id="4fef3-103">Запись \_ приемника MF \_ \_ отключает \_ атрибут регулирования</span><span class="sxs-lookup"><span data-stu-id="4fef3-103">MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute</span></span>

<span data-ttu-id="4fef3-104">Указывает, ограничивает ли модуль записи приемника скорость входящих данных.</span><span class="sxs-lookup"><span data-stu-id="4fef3-104">Specifies whether the sink writer limits the rate of incoming data.</span></span>

## <a name="data-type"></a><span data-ttu-id="4fef3-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4fef3-105">Data type</span></span>

<span data-ttu-id="4fef3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4fef3-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="4fef3-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="4fef3-107">Get/set</span></span>

<span data-ttu-id="4fef3-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4fef3-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4fef3-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4fef3-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="4fef3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fef3-110">Remarks</span></span>

<span data-ttu-id="4fef3-111">По умолчанию метод [**имфсинквритер:: вритесампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) модуля записи в приемник ограничивает скорость передачи данных, блокируя вызывающий поток.</span><span class="sxs-lookup"><span data-stu-id="4fef3-111">By default, the sink writer's [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method limits the data rate by blocking the calling thread.</span></span> <span data-ttu-id="4fef3-112">Это предотвращает слишком быстрое предоставление примеров для приложения.</span><span class="sxs-lookup"><span data-stu-id="4fef3-112">This prevents the application from delivering samples too quickly.</span></span> <span data-ttu-id="4fef3-113">Чтобы отключить это поведение, установите \_ \_ для атрибута регулирования в модуле записи MF Sink \_ \_ **значение true** при создании модуля записи приемника.</span><span class="sxs-lookup"><span data-stu-id="4fef3-113">To disable this behavior, set the MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute to **TRUE** when you create the sink writer.</span></span>

<span data-ttu-id="4fef3-114">Используйте этот атрибут со следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="4fef3-114">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="4fef3-115">**мфкреатесинквритерфроммедиасинк**</span><span class="sxs-lookup"><span data-stu-id="4fef3-115">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="4fef3-116">**мфкреатесинквритерфромурл**</span><span class="sxs-lookup"><span data-stu-id="4fef3-116">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="4fef3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4fef3-117">Requirements</span></span>



| <span data-ttu-id="4fef3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4fef3-118">Requirement</span></span> | <span data-ttu-id="4fef3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4fef3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fef3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fef3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4fef3-121">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="4fef3-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="4fef3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fef3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4fef3-123">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="4fef3-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4fef3-124">Header</span><span class="sxs-lookup"><span data-stu-id="4fef3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fef3-125"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fef3-125"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fef3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fef3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fef3-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4fef3-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4fef3-128">Атрибуты модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="4fef3-128">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




