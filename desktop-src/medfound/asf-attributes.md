---
description: Атрибуты ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Атрибуты ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692094"
---
# <a name="asf-attributes"></a><span data-ttu-id="c49bb-103">Атрибуты ASF</span><span class="sxs-lookup"><span data-stu-id="c49bb-103">ASF Attributes</span></span>

### <a name="profile-attributes"></a><span data-ttu-id="c49bb-104">Атрибуты профиля</span><span class="sxs-lookup"><span data-stu-id="c49bb-104">Profile Attributes</span></span>

<span data-ttu-id="c49bb-105">К профилям ASF применяются следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="c49bb-105">The following attributes apply to ASF profiles.</span></span>



| <span data-ttu-id="c49bb-106">attribute</span><span class="sxs-lookup"><span data-stu-id="c49bb-106">Attribute</span></span>                                                                      | <span data-ttu-id="c49bb-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c49bb-107">Description</span></span>                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="c49bb-108">**MF \_ асфпрофиле \_ макспаккетсизе**</span><span class="sxs-lookup"><span data-stu-id="c49bb-108">**MF\_ASFPROFILE\_MAXPACKETSIZE**</span></span>](mf-asfprofile-maxpacketsize-attribute.md) | <span data-ttu-id="c49bb-109">Указывает максимальный размер пакета для файла ASF в байтах.</span><span class="sxs-lookup"><span data-stu-id="c49bb-109">Specifies the maximum packet size for an ASF file, in bytes.</span></span> |
| [<span data-ttu-id="c49bb-110">**MF \_ асфпрофиле \_ минпаккетсизе**</span><span class="sxs-lookup"><span data-stu-id="c49bb-110">**MF\_ASFPROFILE\_MINPACKETSIZE**</span></span>](mf-asfprofile-minpacketsize-attribute.md) | <span data-ttu-id="c49bb-111">Указывает минимальный размер пакета для файла ASF в байтах.</span><span class="sxs-lookup"><span data-stu-id="c49bb-111">Specifies the minimum packet size for an ASF file, in bytes.</span></span> |



 

### <a name="stream-configuration-attributes"></a><span data-ttu-id="c49bb-112">Атрибуты конфигурации потока</span><span class="sxs-lookup"><span data-stu-id="c49bb-112">Stream Configuration Attributes</span></span>

<span data-ttu-id="c49bb-113">Следующие атрибуты применяются к объекту конфигурации потока ASF.</span><span class="sxs-lookup"><span data-stu-id="c49bb-113">The following attributes apply to the ASF stream configuration object.</span></span>



| <span data-ttu-id="c49bb-114">attribute</span><span class="sxs-lookup"><span data-stu-id="c49bb-114">Attribute</span></span>                                                                              | <span data-ttu-id="c49bb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c49bb-115">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="c49bb-116">**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="c49bb-116">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md) | <span data-ttu-id="c49bb-117">Задает среднее значение параметра "сегмент утечки" для кодирования файла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c49bb-117">Sets the average "leaky bucket" parameters for encoding a Windows Media file.</span></span> |
| [<span data-ttu-id="c49bb-118">**MF \_ асфстреамконфиг \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="c49bb-118">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md) | <span data-ttu-id="c49bb-119">Задает пиковый параметр "сегмент утечки" для кодирования файла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c49bb-119">Sets the peak "leaky bucket" parameters for encoding a Windows Media file.</span></span>    |



 

### <a name="media-buffer-attributes"></a><span data-ttu-id="c49bb-120">Атрибуты буфера мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c49bb-120">Media Buffer Attributes</span></span>

<span data-ttu-id="c49bb-121">Следующие атрибуты применяются к буферам мультимедиа для пакетов ASF.</span><span class="sxs-lookup"><span data-stu-id="c49bb-121">The following attributes apply to media buffers for ASF packets.</span></span>



| <span data-ttu-id="c49bb-122">attribute</span><span class="sxs-lookup"><span data-stu-id="c49bb-122">Attribute</span></span>                                                                          | <span data-ttu-id="c49bb-123">Описание</span><span class="sxs-lookup"><span data-stu-id="c49bb-123">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c49bb-124">**\_граница пакета \_ мфасфсплиттер**</span><span class="sxs-lookup"><span data-stu-id="c49bb-124">**MFASFSPLITTER\_PACKET\_BOUNDARY**</span></span>](mfasfsplitter-packet-boundary-attribute.md) | <span data-ttu-id="c49bb-125">Указывает, содержит ли буфер начало пакета расширенного системного формата (ASF).</span><span class="sxs-lookup"><span data-stu-id="c49bb-125">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span> |



 

### <a name="presentation-descriptor-attributes"></a><span data-ttu-id="c49bb-126">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="c49bb-126">Presentation Descriptor Attributes</span></span>

<span data-ttu-id="c49bb-127">Список атрибутов, применяемых к дескрипторам представления ASF, см. в разделе [атрибуты дескриптора представления](presentation-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="c49bb-127">For a list of attributes that apply to ASF presentation descriptors, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c49bb-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c49bb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c49bb-129">**имфасфпрофиле**</span><span class="sxs-lookup"><span data-stu-id="c49bb-129">**IMFASFProfile**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[<span data-ttu-id="c49bb-130">**имфасфстреамконфиг**</span><span class="sxs-lookup"><span data-stu-id="c49bb-130">**IMFASFStreamConfig**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[<span data-ttu-id="c49bb-131">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c49bb-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



