---
description: Указывает скорость кодирования видео для презентации в битах в секунду. Этот атрибут применяется к дескрипторам представления.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: Атрибут MF_PD_VIDEO_ENCODING_BITRATE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477d0954b4db8fa11c1540153c096e42f6d255b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703143"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a><span data-ttu-id="ef18f-104">\_Атрибут скорости \_ кодирования для записи MF PD \_ \_</span><span class="sxs-lookup"><span data-stu-id="ef18f-104">MF\_PD\_VIDEO\_ENCODING\_BITRATE attribute</span></span>

<span data-ttu-id="ef18f-105">Указывает скорость кодирования видео для презентации в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="ef18f-105">Specifies the video encoding bit rate for the presentation, in bits per second.</span></span> <span data-ttu-id="ef18f-106">Этот атрибут применяется к дескрипторам представления.</span><span class="sxs-lookup"><span data-stu-id="ef18f-106">This attribute applies to presentation descriptors.</span></span>

## <a name="data-type"></a><span data-ttu-id="ef18f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ef18f-107">Data type</span></span>

<span data-ttu-id="ef18f-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ef18f-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ef18f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef18f-109">Remarks</span></span>

<span data-ttu-id="ef18f-110">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ef18f-110">This attribute is optional.</span></span> <span data-ttu-id="ef18f-111">Некоторые форматы имеют более сложные схемы кодирования, которые не могут быть обобщены с помощью этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="ef18f-111">Some formats have more complex encoding schemes that cannot be summarized by using this attribute.</span></span> <span data-ttu-id="ef18f-112">Для файлов формата ASF следующие атрибуты вместе описывают скорость кодирования:</span><span class="sxs-lookup"><span data-stu-id="ef18f-112">For Advanced Systems Format (ASF) files, the following attributes collectively describe the encoding bit rate:</span></span>

-   [<span data-ttu-id="ef18f-113">**MF \_ PD \_ ASF \_ филепропертиес \_ Максимальная \_ скорость**</span><span class="sxs-lookup"><span data-stu-id="ef18f-113">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE**</span></span>](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [<span data-ttu-id="ef18f-114">**\_ \_ \_ \_ Средняя \_ \_ скорость данных (MF SD ASF екстстрмпроп)**</span><span class="sxs-lookup"><span data-stu-id="ef18f-114">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [<span data-ttu-id="ef18f-115">**MF \_ SD \_ ASF \_ екстстрмпроп \_ Максимальная \_ скорость передачи данных \_**</span><span class="sxs-lookup"><span data-stu-id="ef18f-115">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [<span data-ttu-id="ef18f-116">**MF \_ SD \_ ASF \_ стреамбитратес \_ скорость**</span><span class="sxs-lookup"><span data-stu-id="ef18f-116">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)

<span data-ttu-id="ef18f-117">Сторонние форматы могут использовать другие настраиваемые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="ef18f-117">Third-party formats might use other custom attributes.</span></span>

<span data-ttu-id="ef18f-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="ef18f-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef18f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ef18f-119">Requirements</span></span>



| <span data-ttu-id="ef18f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ef18f-120">Requirement</span></span> | <span data-ttu-id="ef18f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ef18f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef18f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef18f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ef18f-123">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="ef18f-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ef18f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef18f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ef18f-125">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ef18f-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ef18f-126">Header</span><span class="sxs-lookup"><span data-stu-id="ef18f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef18f-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef18f-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef18f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef18f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef18f-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ef18f-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ef18f-130">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="ef18f-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ef18f-131">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ef18f-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ef18f-132">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="ef18f-132">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="ef18f-133">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="ef18f-133">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




