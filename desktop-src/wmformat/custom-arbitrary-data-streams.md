---
title: Настраиваемые произвольные потоки данных
description: Настраиваемые произвольные потоки данных
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows Media Format SDK, настраиваемые произвольные потоки данных
- Расширенный системный формат (ASF), настраиваемые произвольные потоки данных
- ASF (Расширенный системный формат), пользовательские потоки произвольных данных
- Windows Media Format SDK, потоки
- Расширенный системный формат (ASF), потоки
- ASF (Расширенный системный формат), потоки
- настраиваемые произвольные потоки данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710161"
---
# <a name="custom-arbitrary-data-streams"></a><span data-ttu-id="821de-110">Настраиваемые произвольные потоки данных</span><span class="sxs-lookup"><span data-stu-id="821de-110">Custom Arbitrary Data Streams</span></span>

<span data-ttu-id="821de-111">Можно создать поток в ASF-файле, который будет содержать данные любого рода.</span><span class="sxs-lookup"><span data-stu-id="821de-111">You can create a stream in an ASF file to contain any sort of data.</span></span> <span data-ttu-id="821de-112">Если ни один из поддерживаемых типов потоков не подходит для ваших нужд, необходимо использовать произвольный поток данных.</span><span class="sxs-lookup"><span data-stu-id="821de-112">If none of the supported stream types suits your needs, you must use an arbitrary data stream.</span></span> <span data-ttu-id="821de-113">Объект модуля записи обрабатывает произвольный поток данных точно так же, как и любой несжатый поток; Примеры объединяются в пакеты и объединяются с образцами из других потоков в разделе данных файла.</span><span class="sxs-lookup"><span data-stu-id="821de-113">The writer object handles an arbitrary data stream just as it does any uncompressed stream; the samples are packetized and combined with the samples from other streams in the data section of the file.</span></span> <span data-ttu-id="821de-114">Конечно, только приложение чтения, которое было специально запрограммирован для работы с произвольным типом, сможет обрабатывать данные после их доставки объектом Read.</span><span class="sxs-lookup"><span data-stu-id="821de-114">Of course, only a reading application that has been specifically programmed to deal with your arbitrary type will be able to handle the data after it is delivered by the reading object.</span></span>

<span data-ttu-id="821de-115">Чаще всего произвольные потоки данных используются для кодирования мультимедийных данных с помощью стороннего кодека.</span><span class="sxs-lookup"><span data-stu-id="821de-115">One common use of arbitrary data streams is for media data encoded by using a third-party codec.</span></span> <span data-ttu-id="821de-116">Поскольку объекты этого пакета SDK не взаимодействуют напрямую с кодеками сторонних производителей, приложение для письма должно обработать образцы с помощью кодировки кодека и передать сжатые образцы в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="821de-116">Because the objects of this SDK do not interact directly with third-party codecs, your writing application must process the samples with the encoding portion of the codec and pass the compressed samples to the writer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="821de-117">См. также</span><span class="sxs-lookup"><span data-stu-id="821de-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="821de-118">**Произвольные потоки**</span><span class="sxs-lookup"><span data-stu-id="821de-118">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="821de-119">**Настройка настраиваемых произвольных потоков**</span><span class="sxs-lookup"><span data-stu-id="821de-119">**Configuring Custom Arbitrary Streams**</span></span>](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




