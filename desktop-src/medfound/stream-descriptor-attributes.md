---
description: Атрибуты дескриптора потока
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Атрибуты дескриптора потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811531"
---
# <a name="stream-descriptor-attributes"></a><span data-ttu-id="3699a-103">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="3699a-103">Stream Descriptor Attributes</span></span>

## <a name="common-stream-descriptor-attributes"></a><span data-ttu-id="3699a-104">Общие атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="3699a-104">Common Stream Descriptor Attributes</span></span>

<span data-ttu-id="3699a-105">К дескрипторам потоков применяются следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="3699a-105">The following attributes apply to stream descriptors.</span></span>



| <span data-ttu-id="3699a-106">attribute</span><span class="sxs-lookup"><span data-stu-id="3699a-106">Attribute</span></span>                                                   | <span data-ttu-id="3699a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3699a-107">Description</span></span>                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="3699a-108">**\_язык MF SD \_**</span><span class="sxs-lookup"><span data-stu-id="3699a-108">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)        | <span data-ttu-id="3699a-109">Указывает язык для потока.</span><span class="sxs-lookup"><span data-stu-id="3699a-109">Specifies the language for a stream.</span></span>                                                  |
| [<span data-ttu-id="3699a-110">MF \_ SD \_ взаимно \_ исключающее</span><span class="sxs-lookup"><span data-stu-id="3699a-110">MF\_SD\_MUTUALLY\_EXCLUSIVE</span></span>](mf-sd-mutually-exclusive.md) | <span data-ttu-id="3699a-111">Указывает, является ли поток взаимоисключающим с другими потоками того же типа.</span><span class="sxs-lookup"><span data-stu-id="3699a-111">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span> |
| [<span data-ttu-id="3699a-112">**MF \_ - \_ защищенный SD**</span><span class="sxs-lookup"><span data-stu-id="3699a-112">**MF\_SD\_PROTECTED**</span></span>](mf-sd-protected-attribute.md)      | <span data-ttu-id="3699a-113">Указывает, содержит ли поток защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="3699a-113">Specifies whether a stream contains protected content.</span></span>                                |
| [<span data-ttu-id="3699a-114">\_имя SD- \_ потока \_ MF</span><span class="sxs-lookup"><span data-stu-id="3699a-114">MF\_SD\_STREAM\_NAME</span></span>](mf-sd-stream-name.md)               | <span data-ttu-id="3699a-115">Содержит имя потока.</span><span class="sxs-lookup"><span data-stu-id="3699a-115">Contains the name of a stream.</span></span>                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a><span data-ttu-id="3699a-116">ASF-Specific атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="3699a-116">ASF-Specific Stream Descriptor Attributes</span></span>

<span data-ttu-id="3699a-117">Следующие атрибуты применяются к дескрипторам потоков для файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="3699a-117">The following attributes apply to stream descriptors for Advanced Systems Format (ASF) files.</span></span>



| <span data-ttu-id="3699a-118">attribute</span><span class="sxs-lookup"><span data-stu-id="3699a-118">Attribute</span></span>                                                                                                                | <span data-ttu-id="3699a-119">Описание</span><span class="sxs-lookup"><span data-stu-id="3699a-119">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3699a-120">**MF \_ SD \_ ASF \_ екстстрмпроп \_ AVG- \_ BUFFERSIZE**</span><span class="sxs-lookup"><span data-stu-id="3699a-120">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | <span data-ttu-id="3699a-121">Указывает средний размер буфера, необходимый для потока в ASF-файле, в байтах.</span><span class="sxs-lookup"><span data-stu-id="3699a-121">Specifies the average buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="3699a-122">**\_ \_ \_ \_ Средняя \_ \_ скорость данных (MF SD ASF екстстрмпроп)**</span><span class="sxs-lookup"><span data-stu-id="3699a-122">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | <span data-ttu-id="3699a-123">Указывает среднюю скорость потока данных в файле ASF в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="3699a-123">Specifies the average data bit rate of a stream in an ASF file, in bits per second.</span></span>        |
| [<span data-ttu-id="3699a-124">**\_ \_ \_ индекс екстстрмпроп для \_ идентификатора языка \_ \_ MF SD ASF**</span><span class="sxs-lookup"><span data-stu-id="3699a-124">**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**</span></span>](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | <span data-ttu-id="3699a-125">Указывает язык, используемый потоком в ASF-файле.</span><span class="sxs-lookup"><span data-stu-id="3699a-125">Specifies the language used by a stream in an ASF file.</span></span>                                    |
| [<span data-ttu-id="3699a-126">**MF \_ SD \_ ASF \_ екстстрмпроп \_ Max \_ BUFFERSIZE**</span><span class="sxs-lookup"><span data-stu-id="3699a-126">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | <span data-ttu-id="3699a-127">Указывает максимальный размер буфера, необходимый для потока в ASF-файле, в байтах.</span><span class="sxs-lookup"><span data-stu-id="3699a-127">Specifies the maximum buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="3699a-128">**MF \_ SD \_ ASF \_ екстстрмпроп \_ Максимальная \_ скорость передачи данных \_**</span><span class="sxs-lookup"><span data-stu-id="3699a-128">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | <span data-ttu-id="3699a-129">Указывает максимальную скорость передачи данных в потоке в ASF-файле, в битах в секунду</span><span class="sxs-lookup"><span data-stu-id="3699a-129">Specifies the maximum data bit rate of a stream in an ASF file, in bits per second</span></span>         |
| [<span data-ttu-id="3699a-130">**\_ \_ \_ \_ \_ шаблон сосогласования устройства MF SD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="3699a-130">**MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE**</span></span>](mf-sd-asf-metadata-device-conformance-template-attribute.md) | <span data-ttu-id="3699a-131">Указывает шаблон соответствия устройства для потока в ASF-файле в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="3699a-131">Specifies the device conformance template for a stream in an ASF file, in bits per second.</span></span> |
| [<span data-ttu-id="3699a-132">**MF \_ SD \_ ASF \_ стреамбитратес \_ скорость**</span><span class="sxs-lookup"><span data-stu-id="3699a-132">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | <span data-ttu-id="3699a-133">Указывает среднюю скорость потока в файле ASF в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="3699a-133">Specifies the average bit rate of a stream in an ASF file, in bits per second.</span></span>             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a><span data-ttu-id="3699a-134">Пересаамский атрибуты дескриптора исходного потока носителя</span><span class="sxs-lookup"><span data-stu-id="3699a-134">SAMI Media Source Stream Descriptor Attributes</span></span>

<span data-ttu-id="3699a-135">Следующий атрибут применяется к дескриптору потока для источника на носителе SAMI.</span><span class="sxs-lookup"><span data-stu-id="3699a-135">The following attribute applies to the stream descriptor for the SAMI media source.</span></span>



| <span data-ttu-id="3699a-136">attribute</span><span class="sxs-lookup"><span data-stu-id="3699a-136">Attribute</span></span>                                                       | <span data-ttu-id="3699a-137">Описание</span><span class="sxs-lookup"><span data-stu-id="3699a-137">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3699a-138">**\_язык MF SD \_ Sami \_**</span><span class="sxs-lookup"><span data-stu-id="3699a-138">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="3699a-139">Содержит имя языка для синхронизированного доступного обмена мультимедиа (SAMI), определенное для потока.</span><span class="sxs-lookup"><span data-stu-id="3699a-139">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3699a-140">См. также</span><span class="sxs-lookup"><span data-stu-id="3699a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3699a-141">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="3699a-141">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="3699a-142">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3699a-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



