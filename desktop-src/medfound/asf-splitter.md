---
description: Разделитель ASF
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: Разделитель ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143282"
---
# <a name="asf-splitter"></a><span data-ttu-id="97bc2-103">Разделитель ASF</span><span class="sxs-lookup"><span data-stu-id="97bc2-103">ASF Splitter</span></span>

<span data-ttu-id="97bc2-104">Объект- *Разделитель* ASF — это компонент уровня вмконтаинер, который анализирует объект данных ASF в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="97bc2-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="97bc2-105">С помощью разделителя можно считывать пакеты данных в объекте данных и создавать образцы потоков.</span><span class="sxs-lookup"><span data-stu-id="97bc2-105">You can use the splitter to read the data packets in the Data Object and generate stream samples.</span></span> <span data-ttu-id="97bc2-106">Сведения о структуре файла ASF см. в разделе [Структура файлов ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="97bc2-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="97bc2-107">Разделитель предоставляет интерфейс [**имфасфсплиттер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="97bc2-107">The splitter exposes the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span> <span data-ttu-id="97bc2-108">Разделитель анализирует пакеты данных ASF для выбранных потоков и переупаковывает их в отдельные образцы объектов, которые предоставляют интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="97bc2-108">The splitter parses ASF data packets for the selected streams and repackages them into individual sample objects that expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="97bc2-109">Разделитель — это один из компонентов уровня платформы Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="97bc2-109">The splitter is one of the platform-level components of Media Foundation.</span></span> <span data-ttu-id="97bc2-110">Источник мультимедиа ASF использует разделитель внутри для анализа файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="97bc2-110">The ASF media source uses the splitter internally to parse ASF files.</span></span>

<span data-ttu-id="97bc2-111">На следующей схеме показан пример создания файла ASF с помощью разделителя.</span><span class="sxs-lookup"><span data-stu-id="97bc2-111">The following diagram illustrates sample generation for an ASF file through the splitter.</span></span>

![Диаграмма, на которой показан пример создания файла ASF](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

<span data-ttu-id="97bc2-113">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="97bc2-113">This section contains the following topics:</span></span>



| <span data-ttu-id="97bc2-114">Раздел</span><span class="sxs-lookup"><span data-stu-id="97bc2-114">Topic</span></span>                                                                                                                        | <span data-ttu-id="97bc2-115">Описание</span><span class="sxs-lookup"><span data-stu-id="97bc2-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="97bc2-116">Создание объекта разделителя ASF</span><span class="sxs-lookup"><span data-stu-id="97bc2-116">Creating the ASF Splitter Object</span></span>](creating-the-asf-splitter-object.md)                                                     | <span data-ttu-id="97bc2-117">Создание и инициализация разделителя.</span><span class="sxs-lookup"><span data-stu-id="97bc2-117">How to create and initialize the splitter.</span></span>                              |
| [<span data-ttu-id="97bc2-118">Настройка объекта разделителя ASF</span><span class="sxs-lookup"><span data-stu-id="97bc2-118">Configuring the ASF Splitter Object</span></span>](configuring-the-asf-splitter-object.md)                                               | <span data-ttu-id="97bc2-119">Параметры конфигурации для разделителя.</span><span class="sxs-lookup"><span data-stu-id="97bc2-119">Configuration settings for the splitter.</span></span>                                |
| [<span data-ttu-id="97bc2-120">Создание образцов потоков из существующего объекта данных ASF</span><span class="sxs-lookup"><span data-stu-id="97bc2-120">Generating Stream Samples from an Existing ASF Data Object</span></span>](generating-stream-samples-from-an-existing-asf-data-object.md) | <span data-ttu-id="97bc2-121">Как анализировать объект данных ASF и формировать пакеты Steam.</span><span class="sxs-lookup"><span data-stu-id="97bc2-121">How to parse the ASF Data Object and generate packetized steam samples.</span></span> |



 

<span data-ttu-id="97bc2-122">В следующей таблице показаны соответствующие атрибуты объекта данных.</span><span class="sxs-lookup"><span data-stu-id="97bc2-122">The following table shows the relevant Data Object attributes.</span></span>



| <span data-ttu-id="97bc2-123">attribute</span><span class="sxs-lookup"><span data-stu-id="97bc2-123">Attribute</span></span>                                                                                                    | <span data-ttu-id="97bc2-124">Описание</span><span class="sxs-lookup"><span data-stu-id="97bc2-124">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97bc2-125">**\_пакеты MF PD \_ ASF \_ филепропертиес \_**</span><span class="sxs-lookup"><span data-stu-id="97bc2-125">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)                   | <span data-ttu-id="97bc2-126">Количество пакетов данных в объекте данных ASF.</span><span class="sxs-lookup"><span data-stu-id="97bc2-126">Number of data packets in the ASF Data Object.</span></span>                                                       |
| [<span data-ttu-id="97bc2-127">**MF \_ PD \_ ASF \_ филепропертиес \_ , \_ Минимальный \_ Размер пакета**</span><span class="sxs-lookup"><span data-stu-id="97bc2-127">**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | <span data-ttu-id="97bc2-128">Минимальный размер пакетов данных в файле в байтах.</span><span class="sxs-lookup"><span data-stu-id="97bc2-128">Minimum size of the data packets in the file, in bytes.</span></span>                                              |
| [<span data-ttu-id="97bc2-129">**\_пакет MF PD \_ ASF \_ филепропертиес \_ максимальный \_ \_ Размер пакета**</span><span class="sxs-lookup"><span data-stu-id="97bc2-129">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | <span data-ttu-id="97bc2-130">Максимальный размер пакетов данных в файле, в байтах</span><span class="sxs-lookup"><span data-stu-id="97bc2-130">Maximum size of the data packets in the file, in bytes</span></span>                                               |
| [<span data-ttu-id="97bc2-131">**\_ \_ \_ Длина данных ASF (MF PD) \_**</span><span class="sxs-lookup"><span data-stu-id="97bc2-131">**MF\_PD\_ASF\_DATA\_LENGTH**</span></span>](mf-pd-asf-data-length-attribute.md)                                         | <span data-ttu-id="97bc2-132">Размер объекта данных ASF в байтах.</span><span class="sxs-lookup"><span data-stu-id="97bc2-132">Size of the ASF Data Object, in bytes.</span></span>                                                               |
| [<span data-ttu-id="97bc2-133">**\_ \_ \_ \_ Начальное \_ смещение данных в формате MF PD ASF**</span><span class="sxs-lookup"><span data-stu-id="97bc2-133">**MF\_PD\_ASF\_DATA\_START\_OFFSET**</span></span>](mf-pd-asf-data-start-offset-attribute.md)                            | <span data-ttu-id="97bc2-134">Смещение (в байтах) к первому пакету данных в объекте данных ASF относительно начала файла.</span><span class="sxs-lookup"><span data-stu-id="97bc2-134">Offset, in bytes, to the first data packet in the ASF Data Object relative to the start of the file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="97bc2-135">См. также</span><span class="sxs-lookup"><span data-stu-id="97bc2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97bc2-136">Компоненты ASF Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="97bc2-136">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="97bc2-137">Руководство. чтение файла ASF</span><span class="sxs-lookup"><span data-stu-id="97bc2-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="97bc2-138">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97bc2-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



