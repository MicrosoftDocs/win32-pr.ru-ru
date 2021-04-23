---
description: Мультиплексор ASF
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: Мультиплексор ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072587"
---
# <a name="asf-multiplexer"></a><span data-ttu-id="7fb33-103">Мультиплексор ASF</span><span class="sxs-lookup"><span data-stu-id="7fb33-103">ASF Multiplexer</span></span>

<span data-ttu-id="7fb33-104">*МУЛЬТИПЛЕКСОР* ASF — это объект слоя вмконтаинер, который работает с [объектом данных ASF](asf-file-structure.md) и дает приложению возможность создавать пакеты данных для контейнера ASF.</span><span class="sxs-lookup"><span data-stu-id="7fb33-104">The ASF *multiplexer* is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate data packets for an ASF container.</span></span> <span data-ttu-id="7fb33-105">Мультиплексор принимает данные мультимедиа в виде [образцов мультимедиа](media-samples.md) и выводит образцы мультимедиа на основе потоковой передачи и параметров пакетов ASF, определенных в [объекте заголовка ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="7fb33-105">The multiplexer accepts media data in the form of [Media Samples](media-samples.md) and outputs media samples based on streaming and ASF packet parameters defined in the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="7fb33-106">Примеры выходных данных содержат ссылки на один или несколько буферов мультимедиа, содержащих Пакетированные цифровые данные мультимедиа. Этот объект можно использовать в сценарии кодирования файлов, где он получает закодированные образцы потоков из кодировщика или для преобразования ASF-ASF (ремуксинг).</span><span class="sxs-lookup"><span data-stu-id="7fb33-106">The output media samples hold references to one or more media buffers that contain packetized digital media data.You can use this object in a file encoding scenario where it receives encoded stream samples from the encoder or for ASF-ASF transcoding (remuxing).</span></span>

<span data-ttu-id="7fb33-107">На следующей схеме показано создание пакета данных ASF для файла ASF с помощью мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="7fb33-107">The following diagram illustrates ASF data packet generation for an ASF file using the multiplexer.</span></span>

![Схема, демонстрирующая создание пакета данных ASF](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

<span data-ttu-id="7fb33-109">Сведения о структуре файла ASF см. в разделе [Структура файлов ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="7fb33-109">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="7fb33-110">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="7fb33-110">This section contains the following topics:</span></span>



| <span data-ttu-id="7fb33-111">Раздел</span><span class="sxs-lookup"><span data-stu-id="7fb33-111">Topic</span></span>                                                                  | <span data-ttu-id="7fb33-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7fb33-112">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="7fb33-113">Создание объекта мультиплексора</span><span class="sxs-lookup"><span data-stu-id="7fb33-113">Creating the Multiplexer Object</span></span>](creating-the-multiplexer-object.md) | <span data-ttu-id="7fb33-114">Создание и инициализация мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="7fb33-114">How to create and initialize the multiplexer.</span></span>                     |
| [<span data-ttu-id="7fb33-115">Создание новых пакетов данных ASF</span><span class="sxs-lookup"><span data-stu-id="7fb33-115">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md) | <span data-ttu-id="7fb33-116">Создание пакетов данных для создания нового объекта данных ASF.</span><span class="sxs-lookup"><span data-stu-id="7fb33-116">How to generate data packets to constitute a new ASF Data Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7fb33-117">См. также</span><span class="sxs-lookup"><span data-stu-id="7fb33-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fb33-118">Компоненты ASF Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="7fb33-118">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="7fb33-119">Учебник. копирование потоков ASF из одного файла в другой</span><span class="sxs-lookup"><span data-stu-id="7fb33-119">Tutorial: Copying ASF Streams from One File to Another</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="7fb33-120">Руководство. запись файла WMA с помощью CBR Encoding</span><span class="sxs-lookup"><span data-stu-id="7fb33-120">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



