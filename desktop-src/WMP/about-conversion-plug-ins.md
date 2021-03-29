---
title: О подключаемых модулях преобразования
description: О подключаемых модулях преобразования
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Проигрыватель Windows Media, подключаемые модули преобразования
- Подключаемые модули проигрывателя Windows Media, преобразование
- подключаемые модули, преобразование
- подключаемые модули преобразования, сведения
- Advanced Systems Format (ASF)
- ASF (Расширенный системный формат)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773589"
---
# <a name="about-conversion-plug-ins"></a><span data-ttu-id="f2b04-109">О подключаемых модулях преобразования</span><span class="sxs-lookup"><span data-stu-id="f2b04-109">About Conversion Plug-ins</span></span>

<span data-ttu-id="f2b04-110">Вы можете создать подключаемый модуль проигрывателя Windows Media для преобразования цифровых файлов мультимедиа, созданных с помощью технологий, не предоставляемых корпорацией Майкрософт, в расширенный формат систем (ASF).</span><span class="sxs-lookup"><span data-stu-id="f2b04-110">You can create a Windows Media Player plug-in to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="f2b04-111">Подключаемые модули преобразования являются объектами модели COM, упакованными и распространяемыми в виде исполняемых файлов (exe).</span><span class="sxs-lookup"><span data-stu-id="f2b04-111">Conversion plug-ins are Component Object Model (COM) objects that are packaged and distributed as executable (.exe) files.</span></span> <span data-ttu-id="f2b04-112">Проигрыватель Windows Media создает экземпляры подключаемых модулей преобразования для преобразования форматов цифрового мультимедиа сторонних производителей в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="f2b04-112">Windows Media Player instantiates conversion plug-ins to convert third-party digital media formats in the following scenarios:</span></span>

-   <span data-ttu-id="f2b04-113">Цифровое мультимедийное содержимое копируется на компьютер с портативного устройства.</span><span class="sxs-lookup"><span data-stu-id="f2b04-113">Digital media content is copied to the computer from a portable device.</span></span>
-   <span data-ttu-id="f2b04-114">Цифровое содержимое мультимедиа добавляется в библиотеку с помощью **ивмпмедиаколлектион:: Add**.</span><span class="sxs-lookup"><span data-stu-id="f2b04-114">Digital media content is added to the library by using **IWMPMediaCollection::add**.</span></span>
-   <span data-ttu-id="f2b04-115">Мультимедийное содержимое добавляется в библиотеку с помощью функции поиска проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f2b04-115">Digital media content is added to the library by using the search feature of Windows Media Player.</span></span>
-   <span data-ttu-id="f2b04-116">Мультимедийное содержимое добавляется в библиотеку с помощью функции мониторинга папок проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f2b04-116">Digital media content is added to the library by the folder monitoring feature of Windows Media Player.</span></span>
-   <span data-ttu-id="f2b04-117">Мультимедийное содержимое добавляется в список синхронизации, когда пользователь перетаскивает и удаляет файл.</span><span class="sxs-lookup"><span data-stu-id="f2b04-117">Digital media content is added to the sync list when the user drags and drops a file.</span></span>

<span data-ttu-id="f2b04-118">После того как проигрыватель Windows Media создаст экземпляр подключаемого модуля преобразования, подключаемый модуль должен преобразовать указанный файл в формат ASF или WMA и добавить соответствующие метаданные.</span><span class="sxs-lookup"><span data-stu-id="f2b04-118">After Windows Media Player creates an instance of a conversion plug-in, the plug-in must convert the supplied file to ASF or WMA and add relevant metadata.</span></span> <span data-ttu-id="f2b04-119">(Не используйте подключаемый модуль преобразования для перекодирования файла.) Затем подключаемый модуль должен скопировать преобразованный файл в указанную папку и вернуть путь к новому файлу в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f2b04-119">(Do not use the conversion plug-in to transcode the file.) The plug-in must then copy the converted file to the specified folder and return the path to the new file to Windows Media Player.</span></span>

<span data-ttu-id="f2b04-120">Подключаемые модули преобразования должны реализовывать интерфейс **ивмпконверт** .</span><span class="sxs-lookup"><span data-stu-id="f2b04-120">Conversion plug-ins must implement the **IWMPConvert** interface.</span></span> <span data-ttu-id="f2b04-121">См. раздел [Справочник по программированию подключаемых модулей преобразования](conversion-plug-ins-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f2b04-121">See [Conversion Plug-ins Programming Reference](conversion-plug-ins-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2b04-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f2b04-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2b04-123">**О процессе преобразования**</span><span class="sxs-lookup"><span data-stu-id="f2b04-123">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="f2b04-124">**Добавление метаданных в преобразованные файлы**</span><span class="sxs-lookup"><span data-stu-id="f2b04-124">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="f2b04-125">**Подключаемые модули преобразования проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f2b04-125">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




