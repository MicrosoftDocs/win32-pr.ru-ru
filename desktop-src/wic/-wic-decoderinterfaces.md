---
description: Интерфейсы декодера
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Интерфейсы декодера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272301"
---
# <a name="decoder-interfaces"></a><span data-ttu-id="f325e-103">Интерфейсы декодера</span><span class="sxs-lookup"><span data-stu-id="f325e-103">Decoder Interfaces</span></span>

<span data-ttu-id="f325e-104">В следующих таблицах показаны интерфейсы, реализованные декодерами компонента Windows Imaging Component (WIC), а на схеме классов показана иерархия наследования.</span><span class="sxs-lookup"><span data-stu-id="f325e-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) decoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="f325e-105">Интерфейсы декодера Container-Level</span><span class="sxs-lookup"><span data-stu-id="f325e-105">Container-Level Decoder Interfaces</span></span>



| <span data-ttu-id="f325e-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f325e-106">Interface</span></span>                                                                                       | <span data-ttu-id="f325e-107">Обязанности</span><span class="sxs-lookup"><span data-stu-id="f325e-107">Responsibilities</span></span>                             | <span data-ttu-id="f325e-108">Реализация</span><span class="sxs-lookup"><span data-stu-id="f325e-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="f325e-109">ивикбитмапдекодер</span><span class="sxs-lookup"><span data-stu-id="f325e-109">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)                                             | <span data-ttu-id="f325e-110">Службы уровня контейнера</span><span class="sxs-lookup"><span data-stu-id="f325e-110">Container-level services</span></span>                     | <span data-ttu-id="f325e-111">Обязательно</span><span class="sxs-lookup"><span data-stu-id="f325e-111">Required</span></span>                                                                   |
| [<span data-ttu-id="f325e-112">ивикбитмапкодекпрогресснотификатион</span><span class="sxs-lookup"><span data-stu-id="f325e-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | <span data-ttu-id="f325e-113">Уведомление о ходе выполнения & поддержка отмены</span><span class="sxs-lookup"><span data-stu-id="f325e-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="f325e-114">Рекомендуется</span><span class="sxs-lookup"><span data-stu-id="f325e-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="f325e-115">ивикметадатаблоккреадер</span><span class="sxs-lookup"><span data-stu-id="f325e-115">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)                                 | <span data-ttu-id="f325e-116">Перечисление метаданных</span><span class="sxs-lookup"><span data-stu-id="f325e-116">Metadata enumeration</span></span>                         | <span data-ttu-id="f325e-117">Необязательный (требуется только для форматов, поддерживающих метаданные уровня контейнера)</span><span class="sxs-lookup"><span data-stu-id="f325e-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="f325e-118">Интерфейсы декодера Frame-Level</span><span class="sxs-lookup"><span data-stu-id="f325e-118">Frame-Level Decoder Interfaces</span></span>



| <span data-ttu-id="f325e-119">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f325e-119">Interface</span></span>                                                           | <span data-ttu-id="f325e-120">Обязанности</span><span class="sxs-lookup"><span data-stu-id="f325e-120">Responsibilities</span></span>          | <span data-ttu-id="f325e-121">Реализация</span><span class="sxs-lookup"><span data-stu-id="f325e-121">Implementation</span></span>                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [<span data-ttu-id="f325e-122">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="f325e-122">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)         | <span data-ttu-id="f325e-123">Службы уровня кадров</span><span class="sxs-lookup"><span data-stu-id="f325e-123">Frame-level services</span></span>      | <span data-ttu-id="f325e-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="f325e-124">Required</span></span>                      |
| [<span data-ttu-id="f325e-125">ивикметадатаблоккреадер</span><span class="sxs-lookup"><span data-stu-id="f325e-125">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)     | <span data-ttu-id="f325e-126">Перечисление метаданных</span><span class="sxs-lookup"><span data-stu-id="f325e-126">Metadata enumeration</span></span>      | <span data-ttu-id="f325e-127">Обязательно</span><span class="sxs-lookup"><span data-stu-id="f325e-127">Required</span></span>                      |
| [<span data-ttu-id="f325e-128">ивикбитмапсаурцетрансформ</span><span class="sxs-lookup"><span data-stu-id="f325e-128">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md) | <span data-ttu-id="f325e-129">Встроенные преобразования декодера</span><span class="sxs-lookup"><span data-stu-id="f325e-129">Native decoder transforms</span></span> | <span data-ttu-id="f325e-130">Рекомендуется</span><span class="sxs-lookup"><span data-stu-id="f325e-130">Recommended</span></span>                   |
| [<span data-ttu-id="f325e-131">ивикдевелоправ</span><span class="sxs-lookup"><span data-stu-id="f325e-131">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)                       | <span data-ttu-id="f325e-132">Службы обработки RAW</span><span class="sxs-lookup"><span data-stu-id="f325e-132">Raw processing services</span></span>   | <span data-ttu-id="f325e-133">Требуется только для необработанных форматов</span><span class="sxs-lookup"><span data-stu-id="f325e-133">Required for Raw formats only</span></span> |



 

![Иерархия наследования интерфейса WIC](graphics/wicinterfaces.png)

## <a name="related-topics"></a><span data-ttu-id="f325e-135">См. также</span><span class="sxs-lookup"><span data-stu-id="f325e-135">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f325e-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f325e-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f325e-137">Реализация декодера WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="f325e-137">Implementing a WIC-Enabled Decoder</span></span>](-wic-implementingwicdecoder.md)
</dt> <dt>

[<span data-ttu-id="f325e-138">Реализация Ивикбитмапдекодер</span><span class="sxs-lookup"><span data-stu-id="f325e-138">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="f325e-139">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="f325e-139">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="f325e-140">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="f325e-140">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



