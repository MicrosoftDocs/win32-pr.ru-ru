---
description: Содержит указатель на диспетчер устройств DXGI для модуля записи приемника.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: Атрибут MF_SINK_WRITER_D3D_MANAGER (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712857"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a><span data-ttu-id="7daa7-103">\_ \_ \_ Атрибут диспетчера D3D модуля записи MF SINK \_</span><span class="sxs-lookup"><span data-stu-id="7daa7-103">MF\_SINK\_WRITER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="7daa7-104">Содержит указатель на диспетчер устройств DXGI для [модуля записи приемника](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="7daa7-104">Contains a pointer to the DXGI Device Manager for the [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="7daa7-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7daa7-105">Data type</span></span>

<span data-ttu-id="7daa7-106">**Имфдксгидевицеманажер \** _ хранится как _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="7daa7-106">**IMFDXGIDeviceManager\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="remarks"></a><span data-ttu-id="7daa7-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7daa7-107">Remarks</span></span>

<span data-ttu-id="7daa7-108">Значение этого атрибута является указателем на интерфейс [_ *имфдксгидевицеманажер* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="7daa7-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="7daa7-109">Используйте этот атрибут, чтобы предоставить устройство Direct3D для любых видеокодировщиков или приемников мультимедиа, загруженных модулем записи приемника.</span><span class="sxs-lookup"><span data-stu-id="7daa7-109">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the Sink Writer.</span></span>

<span data-ttu-id="7daa7-110">Используйте этот атрибут со следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="7daa7-110">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="7daa7-111">**мфкреатесинквритерфроммедиасинк**</span><span class="sxs-lookup"><span data-stu-id="7daa7-111">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="7daa7-112">**мфкреатесинквритерфромурл**</span><span class="sxs-lookup"><span data-stu-id="7daa7-112">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="7daa7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7daa7-113">Requirements</span></span>



| <span data-ttu-id="7daa7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7daa7-114">Requirement</span></span> | <span data-ttu-id="7daa7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7daa7-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7daa7-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7daa7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7daa7-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="7daa7-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7daa7-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7daa7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7daa7-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="7daa7-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7daa7-120">Header</span><span class="sxs-lookup"><span data-stu-id="7daa7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7daa7-121"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="7daa7-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7daa7-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7daa7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7daa7-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7daa7-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7daa7-124">Модуль записи приемников</span><span class="sxs-lookup"><span data-stu-id="7daa7-124">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 




