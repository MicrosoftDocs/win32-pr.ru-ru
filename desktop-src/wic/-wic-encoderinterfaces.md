---
description: Интерфейсы кодировщика
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Интерфейсы кодировщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265297"
---
# <a name="encoder-interfaces"></a><span data-ttu-id="a037c-103">Интерфейсы кодировщика</span><span class="sxs-lookup"><span data-stu-id="a037c-103">Encoder Interfaces</span></span>


<span data-ttu-id="a037c-104">В следующих таблицах показаны интерфейсы, реализованные кодировщиками компонента Windows Imaging Component (WIC), а на схеме классов показана иерархия наследования.</span><span class="sxs-lookup"><span data-stu-id="a037c-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) encoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="a037c-105">Интерфейсы кодировщика Container-Level</span><span class="sxs-lookup"><span data-stu-id="a037c-105">Container-Level Encoder Interfaces</span></span>



| <span data-ttu-id="a037c-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="a037c-106">Interface</span></span>                                                                                       | <span data-ttu-id="a037c-107">Обязанности</span><span class="sxs-lookup"><span data-stu-id="a037c-107">Responsibilities</span></span>                             | <span data-ttu-id="a037c-108">Реализация</span><span class="sxs-lookup"><span data-stu-id="a037c-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="a037c-109">ивикбитмапенкодер</span><span class="sxs-lookup"><span data-stu-id="a037c-109">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)                                             | <span data-ttu-id="a037c-110">Службы уровня контейнера</span><span class="sxs-lookup"><span data-stu-id="a037c-110">Container-level services</span></span>                     | <span data-ttu-id="a037c-111">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a037c-111">Required</span></span>                                                                   |
| [<span data-ttu-id="a037c-112">ивикбитмапкодекпрогресснотификатион</span><span class="sxs-lookup"><span data-stu-id="a037c-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | <span data-ttu-id="a037c-113">Уведомление о ходе выполнения & поддержка отмены</span><span class="sxs-lookup"><span data-stu-id="a037c-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="a037c-114">Рекомендуется</span><span class="sxs-lookup"><span data-stu-id="a037c-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="a037c-115">ивикметадатаблокквритер</span><span class="sxs-lookup"><span data-stu-id="a037c-115">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)                                 | <span data-ttu-id="a037c-116">Службы сериализации метаданных</span><span class="sxs-lookup"><span data-stu-id="a037c-116">Metadata serialization services</span></span>              | <span data-ttu-id="a037c-117">Необязательный (требуется только для форматов, поддерживающих метаданные уровня контейнера)</span><span class="sxs-lookup"><span data-stu-id="a037c-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="a037c-118">Интерфейсы кодировщика Frame-Level</span><span class="sxs-lookup"><span data-stu-id="a037c-118">Frame-Level Encoder Interfaces</span></span>



| <span data-ttu-id="a037c-119">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="a037c-119">Interface</span></span>                                                       | <span data-ttu-id="a037c-120">Обязанности</span><span class="sxs-lookup"><span data-stu-id="a037c-120">Responsibilities</span></span>                | <span data-ttu-id="a037c-121">Реализация</span><span class="sxs-lookup"><span data-stu-id="a037c-121">Implementation</span></span> |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [<span data-ttu-id="a037c-122">ивикбитмапфраминкоде</span><span class="sxs-lookup"><span data-stu-id="a037c-122">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)     | <span data-ttu-id="a037c-123">Службы уровня кадров</span><span class="sxs-lookup"><span data-stu-id="a037c-123">Frame-level services</span></span>            | <span data-ttu-id="a037c-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a037c-124">Required</span></span>       |
| [<span data-ttu-id="a037c-125">ивикметадатаблокквритер</span><span class="sxs-lookup"><span data-stu-id="a037c-125">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md) | <span data-ttu-id="a037c-126">Службы сериализации метаданных</span><span class="sxs-lookup"><span data-stu-id="a037c-126">Metadata serialization services</span></span> | <span data-ttu-id="a037c-127">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a037c-127">Required</span></span>       |



 

![Иерархия наследования интерфейса кодировщика WIC](graphics/wicencoderinterfaces.png)

<span data-ttu-id="a037c-129">Вы заметите, что интерфейсы кодировщика являются практически зеркальными изображениями интерфейсов декодера, и что большинство методов в этих интерфейсах соответствуют методам в связанных интерфейсах декодера.</span><span class="sxs-lookup"><span data-stu-id="a037c-129">You'll notice that the encoder interfaces are almost mirror images of the decoder interfaces, and that most of the methods on these interfaces correspond to methods on the related decoder interfaces.</span></span> <span data-ttu-id="a037c-130">Теперь, когда вы знакомы с реализацией декодера с поддержкой WIC, реализация кодировщика с поддержкой WIC будет казаться знакомой.</span><span class="sxs-lookup"><span data-stu-id="a037c-130">Now that you're familiar with the implementation of a WIC-enabled decoder, the implementation of a WIC-enabled encoder will seem familiar as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a037c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="a037c-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a037c-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a037c-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a037c-133">Реализация кодировщика WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="a037c-133">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="a037c-134">Реализация Ивикбитмапенкодер</span><span class="sxs-lookup"><span data-stu-id="a037c-134">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="a037c-135">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="a037c-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="a037c-136">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="a037c-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



