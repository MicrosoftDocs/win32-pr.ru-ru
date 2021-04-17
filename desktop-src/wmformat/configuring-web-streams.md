---
title: Настройка веб-потоков
description: Настройка веб-потоков
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- потоки, Настройка веб-потоков
- кодеки, Настройка веб-потоков
- Веб-потоки, Настройка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331944"
---
# <a name="configuring-web-streams"></a><span data-ttu-id="6ab99-106">Настройка веб-потоков</span><span class="sxs-lookup"><span data-stu-id="6ab99-106">Configuring Web Streams</span></span>

<span data-ttu-id="6ab99-107">Веб-потоки являются специализированным типом потока передачи файлов, используемого для доставки файлов, связанных с веб-сайтом, в одном потоке.</span><span class="sxs-lookup"><span data-stu-id="6ab99-107">Web streams are a specialized type of file transfer stream used to deliver the files associated with a Web site in a single stream.</span></span> <span data-ttu-id="6ab99-108">Настройка веб-потока приведена в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6ab99-108">Web stream configuration is summarized in the following table.</span></span>



| <span data-ttu-id="6ab99-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="6ab99-109">Setting</span></span>                                            | <span data-ttu-id="6ab99-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6ab99-110">Description</span></span>                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6ab99-111">**\_Тип мультимедиа WM \_ . мажортипе**</span><span class="sxs-lookup"><span data-stu-id="6ab99-111">**WM\_MEDIA\_TYPE.majortype**</span></span>                      | <span data-ttu-id="6ab99-112">Задайте для параметра значение ВММЕДИАТИПЕ \_ филетрансфер.</span><span class="sxs-lookup"><span data-stu-id="6ab99-112">Set to WMMEDIATYPE\_FileTransfer.</span></span>                                                 |
| <span data-ttu-id="6ab99-113">**\_Тип мультимедиа WM \_ . подтип**</span><span class="sxs-lookup"><span data-stu-id="6ab99-113">**WM\_MEDIA\_TYPE.subtype**</span></span>                        | <span data-ttu-id="6ab99-114">Задайте для ВММЕДИАСУБТИПЕ \_ поток.</span><span class="sxs-lookup"><span data-stu-id="6ab99-114">Set to WMMEDIASUBTYPE\_WebStream.</span></span>                                                 |
| <span data-ttu-id="6ab99-115">**\_Тип мультимедиа WM \_ . бфикседсизесамплес**</span><span class="sxs-lookup"><span data-stu-id="6ab99-115">**WM\_MEDIA\_TYPE.bFixedSizeSamples**</span></span>              | <span data-ttu-id="6ab99-116">Задайте значение false.</span><span class="sxs-lookup"><span data-stu-id="6ab99-116">Set to False.</span></span>                                                                     |
| <span data-ttu-id="6ab99-117">**\_Тип мультимедиа WM \_ . бтемпоралкомпрессион**</span><span class="sxs-lookup"><span data-stu-id="6ab99-117">**WM\_MEDIA\_TYPE.bTemporalCompression**</span></span>           | <span data-ttu-id="6ab99-118">Задайте значение true.</span><span class="sxs-lookup"><span data-stu-id="6ab99-118">Set to True.</span></span>                                                                      |
| <span data-ttu-id="6ab99-119">**\_Тип мультимедиа WM \_ . лсамплесизе**</span><span class="sxs-lookup"><span data-stu-id="6ab99-119">**WM\_MEDIA\_TYPE.lSampleSize**</span></span>                    | <span data-ttu-id="6ab99-120">Задайте значение 0.</span><span class="sxs-lookup"><span data-stu-id="6ab99-120">Set to 0.</span></span>                                                                         |
| <span data-ttu-id="6ab99-121">**\_Тип мультимедиа WM \_ . форматтипе**</span><span class="sxs-lookup"><span data-stu-id="6ab99-121">**WM\_MEDIA\_TYPE.formattype**</span></span>                     | <span data-ttu-id="6ab99-122">Задайте для ВМФОРМАТ \_ поток.</span><span class="sxs-lookup"><span data-stu-id="6ab99-122">Set to WMFORMAT\_WebStream.</span></span>                                                       |
| <span data-ttu-id="6ab99-123">**\_Тип мультимедиа WM \_ . Punk**</span><span class="sxs-lookup"><span data-stu-id="6ab99-123">**WM\_MEDIA\_TYPE.pUnk**</span></span>                           | <span data-ttu-id="6ab99-124">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6ab99-124">Set to **NULL**.</span></span>                                                                  |
| <span data-ttu-id="6ab99-125">**\_Тип мультимедиа WM \_ . кбформат**</span><span class="sxs-lookup"><span data-stu-id="6ab99-125">**WM\_MEDIA\_TYPE.cbFormat**</span></span>                       | <span data-ttu-id="6ab99-126">Задайте значение `sizeof(WMT_WEBSTREAM_FORMAT)`.</span><span class="sxs-lookup"><span data-stu-id="6ab99-126">Set to `sizeof(WMT_WEBSTREAM_FORMAT)`.</span></span>                                            |
| <span data-ttu-id="6ab99-127">**\_Тип мультимедиа WM \_ . пбформат**</span><span class="sxs-lookup"><span data-stu-id="6ab99-127">**WM\_MEDIA\_TYPE.pbFormat**</span></span>                       | <span data-ttu-id="6ab99-128">Укажите адрес правильно настроенной структуры **формата ВМТ в \_ \_ виде потока** .</span><span class="sxs-lookup"><span data-stu-id="6ab99-128">Set to the address of a properly configured **WMT\_WEBSTREAM\_FORMAT** structure.</span></span> |
| <span data-ttu-id="6ab99-129">**\_ \_ Формат ВМТ. кбсамплехеадерфикседдата**</span><span class="sxs-lookup"><span data-stu-id="6ab99-129">**WMT\_WEBSTREAM\_FORMAT.cbSampleHeaderFixedData**</span></span> | <span data-ttu-id="6ab99-130">Задайте значение `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span><span class="sxs-lookup"><span data-stu-id="6ab99-130">Set to `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span></span>                                     |
| <span data-ttu-id="6ab99-131">**\_ \_ Формат ВМТ. вверсион**</span><span class="sxs-lookup"><span data-stu-id="6ab99-131">**WMT\_WEBSTREAM\_FORMAT.wVersion**</span></span>                | <span data-ttu-id="6ab99-132">Задан равным 1.</span><span class="sxs-lookup"><span data-stu-id="6ab99-132">Set to 1.</span></span>                                                                         |
| <span data-ttu-id="6ab99-133">**\_ \_ Формат ВМТ. вресервед**</span><span class="sxs-lookup"><span data-stu-id="6ab99-133">**WMT\_WEBSTREAM\_FORMAT.wreserved**</span></span>               | <span data-ttu-id="6ab99-134">Задайте значение 0.</span><span class="sxs-lookup"><span data-stu-id="6ab99-134">Set to 0.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="6ab99-135">См. также</span><span class="sxs-lookup"><span data-stu-id="6ab99-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab99-136">**Общая конфигурация для всех потоков**</span><span class="sxs-lookup"><span data-stu-id="6ab99-136">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="6ab99-137">**Настройка произвольных типов потоков**</span><span class="sxs-lookup"><span data-stu-id="6ab99-137">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="6ab99-138">**Веб-потоки**</span><span class="sxs-lookup"><span data-stu-id="6ab99-138">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




