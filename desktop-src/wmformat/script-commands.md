---
title: Команды скриптов
description: Команды скриптов
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Пакет SDK для Windows Media Format, команды сценариев
- Расширенный системный формат (ASF), команды сценариев
- ASF (Расширенный системный формат), команды сценариев
- Пакет Windows Media Format SDK, скриптовые потоки
- Расширенный системный формат (ASF), скриптовые потоки
- ASF (Расширенный системный формат), скриптовые потоки
- Windows Media Format SDK, потоки
- Расширенный системный формат (ASF), потоки
- ASF (Расширенный системный формат), потоки
- скрипты, команды
- скрипты, потоки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070826"
---
# <a name="script-commands"></a><span data-ttu-id="0909e-114">Команды скриптов</span><span class="sxs-lookup"><span data-stu-id="0909e-114">Script Commands</span></span>

<span data-ttu-id="0909e-115">Команды сценария, поддерживаемые пакетом Windows Media Format SDK, представляют собой простые пары "имя — значение" и "строка значений".</span><span class="sxs-lookup"><span data-stu-id="0909e-115">The script commands supported by the Windows Media Format SDK are simple name and value string pairs.</span></span> <span data-ttu-id="0909e-116">Например, распространенной командой сценария является URL-адрес, который используется проигрывателем Windows Media и другими воспроизводимыми приложениями для открытия веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="0909e-116">For example, a common script command is "URL", which is used by Windows Media Player and other playing applications to open Web pages.</span></span> <span data-ttu-id="0909e-117">Вторая половина пары скриптов для команды "URL" содержит допустимый URL-адрес (URI), например `https://www.adatum.com` .</span><span class="sxs-lookup"><span data-stu-id="0909e-117">The other half of the script pair for "URL" command contains a valid uniform resource locator (URL), such as `https://www.adatum.com`.</span></span> <span data-ttu-id="0909e-118">Объекты этого пакета SDK не поддерживаются для каких-либо конкретных команд. приложение должно включать логику для обработки любых используемых команд.</span><span class="sxs-lookup"><span data-stu-id="0909e-118">No support is provided by the objects of this SDK for any specific commands; your application must include logic to handle whatever commands you use.</span></span> <span data-ttu-id="0909e-119">Для обеспечения совместимости с большинством игроков можно использовать команды, поддерживаемые проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0909e-119">You can use the commands supported by Windows Media Player to maintain compatibility with most players.</span></span>

<span data-ttu-id="0909e-120">Команды сценария могут доставляться одним из двух способов: в потоке скрипта или в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="0909e-120">Script commands can be delivered in one of two ways: in a script stream or in the file header.</span></span>

## <a name="script-streams"></a><span data-ttu-id="0909e-121">Создать скрипт для потоков</span><span class="sxs-lookup"><span data-stu-id="0909e-121">Script Streams</span></span>

<span data-ttu-id="0909e-122">Команды сценария можно доставлять в свой собственный поток в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="0909e-122">You can deliver script commands in their own stream in an ASF file.</span></span> <span data-ttu-id="0909e-123">Каждый пример в потоке скрипта содержит две строки пары "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="0909e-123">Each sample in a script stream contains the two strings of the name/value pair.</span></span> <span data-ttu-id="0909e-124">Преимущество использования потока скрипта заключается в том, что команды будут доставляться в нужное время презентации.</span><span class="sxs-lookup"><span data-stu-id="0909e-124">The advantage of using a script stream is that the commands will be delivered at the correct presentation time.</span></span>

## <a name="script-commands-in-the-file-header"></a><span data-ttu-id="0909e-125">Создать скрипт для команд в заголовке файла</span><span class="sxs-lookup"><span data-stu-id="0909e-125">Script Commands in the File Header</span></span>

<span data-ttu-id="0909e-126">Команды сценария могут включаться в заголовок файла для получения во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0909e-126">Script commands can be included in the file header for retrieval at the time of playback.</span></span> <span data-ttu-id="0909e-127">Воспроизводимое приложение отвечает за выполнение команд сценария в нужное время.</span><span class="sxs-lookup"><span data-stu-id="0909e-127">The playing application is responsible for executing the script commands at the proper time.</span></span> <span data-ttu-id="0909e-128">Преимущество использования команд сценария в заголовке файла состоит в том, что все команды сценария доступны до начала получения образцов.</span><span class="sxs-lookup"><span data-stu-id="0909e-128">The advantage of using script commands in the file header is that all of the script commands are available before beginning to receive samples.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0909e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0909e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0909e-130">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="0909e-130">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="0909e-131">**Использование команд сценария**</span><span class="sxs-lookup"><span data-stu-id="0909e-131">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




