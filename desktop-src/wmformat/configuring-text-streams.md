---
title: Настройка текстовых потоков
description: Настройка текстовых потоков
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- потоки, Настройка текстовых потоков
- кодеки, Настройка текстовых потоков
- текстовые потоки, Настройка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486813"
---
# <a name="configuring-text-streams"></a><span data-ttu-id="75ec2-106">Настройка текстовых потоков</span><span class="sxs-lookup"><span data-stu-id="75ec2-106">Configuring Text Streams</span></span>

<span data-ttu-id="75ec2-107">Текстовые потоки в основном совпадают с пользовательскими произвольными потоками.</span><span class="sxs-lookup"><span data-stu-id="75ec2-107">Text streams are essentially the same as custom arbitrary streams.</span></span> <span data-ttu-id="75ec2-108">Нет сведений о конфигурации, связанных с текстовым потоком для определения типа кодировки текста, поэтому объект модуля записи не может проверить образцы.</span><span class="sxs-lookup"><span data-stu-id="75ec2-108">There is no configuration information associated with a text stream to identify the type of text encoding, so the writer object cannot verify samples.</span></span>

<span data-ttu-id="75ec2-109">Чтобы настроить текстовый поток, необходимо убедиться, что структура [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) содержит основной тип носителя вммедиатипе \_ текста.</span><span class="sxs-lookup"><span data-stu-id="75ec2-109">To configure a text stream, you must ensure that the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains a major media type of WMMEDIATYPE\_TEXT.</span></span> <span data-ttu-id="75ec2-110">Кроме того, необходимо задать скорость потока и окно буфера для него.</span><span class="sxs-lookup"><span data-stu-id="75ec2-110">You must also set a bit rate and buffer window for the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75ec2-111">См. также</span><span class="sxs-lookup"><span data-stu-id="75ec2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75ec2-112">**Вычисление скорости потока и значений окна буфера для произвольных потоков**</span><span class="sxs-lookup"><span data-stu-id="75ec2-112">**Calculating Bit Rate and Buffer Window Values for Arbitrary Streams**</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="75ec2-113">**Общая конфигурация для всех потоков**</span><span class="sxs-lookup"><span data-stu-id="75ec2-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="75ec2-114">**Настройка произвольных типов потоков**</span><span class="sxs-lookup"><span data-stu-id="75ec2-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="75ec2-115">**Текстовые потоки**</span><span class="sxs-lookup"><span data-stu-id="75ec2-115">**Text Streams**</span></span>](text-streams.md)
</dt> </dl>

 

 




