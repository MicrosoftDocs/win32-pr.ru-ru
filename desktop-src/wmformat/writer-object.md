---
title: Объект модуля записи
description: Объект модуля записи
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- Windows Media Format SDK, объекты записи
- Расширенный системный формат (ASF), объекты модуля записи
- ASF (Расширенный системный формат), объекты записи
- объекты, объекты записи
- объекты модуля записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d4783a8330ac1f0f16bc2ca2de4e843cbacc06
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789240"
---
# <a name="writer-object"></a><span data-ttu-id="5de37-108">Объект модуля записи</span><span class="sxs-lookup"><span data-stu-id="5de37-108">Writer Object</span></span>

<span data-ttu-id="5de37-109">Объект модуля записи используется для записи цифровых мультимедийных файлов с помощью структуры файлов в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="5de37-109">The writer object is used to write digital media files using the advanced systems format (ASF) file structure.</span></span> <span data-ttu-id="5de37-110">Процесс написания файла цифрового мультимедиа включает в себя множество шагов, внутренних для модуля записи, которые координирует сжатие, пакетирование и мультиплексирование.</span><span class="sxs-lookup"><span data-stu-id="5de37-110">The process of writing a digital media file involves many steps internal to the writer, which coordinates compression, packetization, and multiplexing.</span></span>

<span data-ttu-id="5de37-111">Объект модуля записи включает интерфейсы для вывода в файлы или сеть, поддерживает один интерфейс обратного вызова и может создавать один или несколько объектов входных свойств носителя.</span><span class="sxs-lookup"><span data-stu-id="5de37-111">The writer object includes interfaces for output to files or a network, supports one callback interface, and can create one or more input media properties objects.</span></span>

<span data-ttu-id="5de37-112">Объект модуля записи создается функцией [**вмкреатевритер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), которая устанавливает указатель на интерфейс **ивмвритер** .</span><span class="sxs-lookup"><span data-stu-id="5de37-112">The writer object is created by the function [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), which sets a pointer to an **IWMWriter** interface.</span></span> <span data-ttu-id="5de37-113">Другие интерфейсы объекта модуля записи можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="5de37-113">The other interfaces of the writer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="5de37-114">Объект модуля записи поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="5de37-114">The following interfaces are supported by the writer object.</span></span>



| <span data-ttu-id="5de37-115">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="5de37-115">Interface</span></span>                                          | <span data-ttu-id="5de37-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5de37-116">Description</span></span>                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5de37-117">**ивмдрмвритер**</span><span class="sxs-lookup"><span data-stu-id="5de37-117">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | <span data-ttu-id="5de37-118">Предоставляет методы для создания ключей [*DRM*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="5de37-118">Provides methods to generate [*DRM*](wmformat-glossary.md) keys.</span></span>                                                                                                |
| [<span data-ttu-id="5de37-119">**IWMDRMWriter2**</span><span class="sxs-lookup"><span data-stu-id="5de37-119">**IWMDRMWriter2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | <span data-ttu-id="5de37-120">Настраивает объект модуля записи для записи файла, содержащего предварительно зашифрованный поток, который соответствует протоколу Windows Media DRM 10 для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="5de37-120">Configures the writer object to write a file containing a pre-encrypted stream that conforms to the Windows Media DRM 10 for Network Devices protocol.</span></span>                                                    |
| [<span data-ttu-id="5de37-121">**ивмхеадеринфо**</span><span class="sxs-lookup"><span data-stu-id="5de37-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | <span data-ttu-id="5de37-122">Управляет спецификацией и получением сведений о заголовках, таких как метаданные, [*маркеры*](wmformat-glossary.md)и т. д.</span><span class="sxs-lookup"><span data-stu-id="5de37-122">Manages the specification and retrieval of header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                                           |
| [<span data-ttu-id="5de37-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="5de37-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | <span data-ttu-id="5de37-124">Управляет перечислением доступных сведений о кодека.</span><span class="sxs-lookup"><span data-stu-id="5de37-124">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="5de37-125">Наследует все методы **ивмхеадеринфо**.</span><span class="sxs-lookup"><span data-stu-id="5de37-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                            |
| [<span data-ttu-id="5de37-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="5de37-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | <span data-ttu-id="5de37-127">Управляет перечислением доступных сведений о кодека.</span><span class="sxs-lookup"><span data-stu-id="5de37-127">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="5de37-128">Наследует все методы **ивмхеадеринфо** и **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="5de37-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>                                                                     |
| [<span data-ttu-id="5de37-129">**ивмватермаркинфо**</span><span class="sxs-lookup"><span data-stu-id="5de37-129">**IWMWatermarkInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | <span data-ttu-id="5de37-130">Предоставляет доступ к сведениям о системах подложки, имеющихся в системе.</span><span class="sxs-lookup"><span data-stu-id="5de37-130">Provides access to information about watermarking systems present on the system.</span></span>                                                                                                                          |
| [<span data-ttu-id="5de37-131">**ивмвритер**</span><span class="sxs-lookup"><span data-stu-id="5de37-131">**IWMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | <span data-ttu-id="5de37-132">Запускает и останавливает запись файлов ASF; Он содержит методы для выделения буферов, настройки и извлечения входных свойств, установки профилей и имен выходных файлов, а также разблокировки модуля записи.</span><span class="sxs-lookup"><span data-stu-id="5de37-132">Starts and stops the writing of ASF files; it includes methods for allocating buffers, setting and retrieving input properties, setting profiles and output file names, and unlocking the writer.</span></span>         |
| [<span data-ttu-id="5de37-133">**ивмвритерадванцед**</span><span class="sxs-lookup"><span data-stu-id="5de37-133">**IWMWriterAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | <span data-ttu-id="5de37-134">Добавляет, получает и удаляет указанные объекты приемника; Получает статистику, число приемников и время, в которое работает модуль записи. и выполняет другие расширенные функции.</span><span class="sxs-lookup"><span data-stu-id="5de37-134">Adds, gets, and removes specified sink objects; retrieves statistics, number of sinks, and the clock time the writer is working to; and performs other advanced functions.</span></span>                                |
| [<span data-ttu-id="5de37-135">**IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="5de37-135">**IWMWriterAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | <span data-ttu-id="5de37-136">Предоставляет некоторые дополнительные функции, особенно для обработки видео с чередованием.</span><span class="sxs-lookup"><span data-stu-id="5de37-136">Provides some advanced functionality, particularly for handling deinterlaced video.</span></span> <span data-ttu-id="5de37-137">Наследует все методы **ивмвритерадванцед**.</span><span class="sxs-lookup"><span data-stu-id="5de37-137">Inherits all of the methods of **IWMWriterAdvanced**.</span></span>                                                                 |
| [<span data-ttu-id="5de37-138">**IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="5de37-138">**IWMWriterAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | <span data-ttu-id="5de37-139">Предоставляет дополнительные возможности модуля записи, включая возможность получения подробных сведений о записи.</span><span class="sxs-lookup"><span data-stu-id="5de37-139">Provides additional writer functionality, including the ability to get detailed writer statistics.</span></span> <span data-ttu-id="5de37-140">Наследует все методы **ивмвритерадванцед** и **IWMWriterAdvanced2**.</span><span class="sxs-lookup"><span data-stu-id="5de37-140">Inherits all of the methods of **IWMWriterAdvanced** and **IWMWriterAdvanced2**.</span></span>                       |
| [<span data-ttu-id="5de37-141">**ивмвритерпоствиев**</span><span class="sxs-lookup"><span data-stu-id="5de37-141">**IWMWriterPostView**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | <span data-ttu-id="5de37-142">Управляет некоторыми расширенными функциями записи, относящимися к примерам просмотра.</span><span class="sxs-lookup"><span data-stu-id="5de37-142">Manages some advanced writing functionality related to postviewing samples.</span></span> <span data-ttu-id="5de37-143">Просмотр вывода (обычно из кодировщика) позволяет проверить правильность работы процесса кодирования и декодирования.</span><span class="sxs-lookup"><span data-stu-id="5de37-143">Postviewing is viewing the output, usually from an encoder, to check that the encoding/decoding process is working correctly.</span></span> |
| [<span data-ttu-id="5de37-144">**ивмвритерпрепроцесс**</span><span class="sxs-lookup"><span data-stu-id="5de37-144">**IWMWriterPreprocess**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | <span data-ttu-id="5de37-145">Управляет проходами предварительной обработки, выполненными модулем записи.</span><span class="sxs-lookup"><span data-stu-id="5de37-145">Manages preprocessing passes made by the writer.</span></span> <span data-ttu-id="5de37-146">Для повышения качества закодированных выходных данных используются этапы предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="5de37-146">Preprocessing passes are used to improve the quality of encoded output.</span></span>                                                                                  |



 

<span data-ttu-id="5de37-147">Для отслеживания хода выполнения просмотра в приложении должен быть реализован следующий интерфейс обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="5de37-147">The following callback interface must be implemented by the application to track the progress of postviewing.</span></span>



| <span data-ttu-id="5de37-148">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="5de37-148">Interface</span></span>                                                      | <span data-ttu-id="5de37-149">Описание</span><span class="sxs-lookup"><span data-stu-id="5de37-149">Description</span></span>                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5de37-150">**ивмвритерпоствиевкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="5de37-150">**IWMWriterPostViewCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | <span data-ttu-id="5de37-151">Управляет получением несжатых образцов из объекта модуля записи для предварительного просмотра действий, выполняемых кодеком.</span><span class="sxs-lookup"><span data-stu-id="5de37-151">Manages how uncompressed samples are received from the writer object to preview what the codec is doing.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5de37-152">См. также</span><span class="sxs-lookup"><span data-stu-id="5de37-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5de37-153">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="5de37-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="5de37-154">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="5de37-154">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




