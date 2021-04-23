---
title: Использование команд сценариев, поддерживаемых проигрывателем Windows Media
description: Использование команд сценариев, поддерживаемых проигрывателем Windows Media
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Пакет SDK для Windows Media Format, команды сценариев
- Windows Media Format SDK, проигрыватель Windows Media
- Расширенный системный формат (ASF), команды сценариев
- ASF (Расширенный системный формат), команды сценариев
- Расширенный системный формат (ASF), проигрыватель Windows Media
- ASF (Расширенный системный формат), проигрыватель Windows Media
- скрипты, команды
- сценарии, проигрыватель Windows Media
- Проигрыватель Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068058"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a><span data-ttu-id="8528d-112">Использование команд сценариев, поддерживаемых проигрывателем Windows Media</span><span class="sxs-lookup"><span data-stu-id="8528d-112">Using Script Commands Supported by Windows Media Player</span></span>

<span data-ttu-id="8528d-113">Пакет SDK для формата Windows Media не предоставляет встроенную поддержку для синтаксического анализа и реагирования на команды сценариев.</span><span class="sxs-lookup"><span data-stu-id="8528d-113">The Windows Media Format SDK does not provide native support for parsing and responding to script commands.</span></span> <span data-ttu-id="8528d-114">В приложение необходимо включить любую логику, связанную с командами сценария.</span><span class="sxs-lookup"><span data-stu-id="8528d-114">You must include any logic related to script commands in your application.</span></span> <span data-ttu-id="8528d-115">Используемые типы скриптов также должны быть определены в приложении.</span><span class="sxs-lookup"><span data-stu-id="8528d-115">The script types that you use must also be defined in your application.</span></span>

<span data-ttu-id="8528d-116">Можно включить код для обработки тех же команд сценария, которые поддерживаются проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8528d-116">You can include code to handle the same script commands that are supported by Windows Media Player.</span></span> <span data-ttu-id="8528d-117">Поддержание совместимости с проигрывателем Windows Media делает файлы более универсальными, чем при внедрении пользовательских команд сценариев.</span><span class="sxs-lookup"><span data-stu-id="8528d-117">Maintaining compatibility with Windows Media Player makes your files more universal than if you embed custom script commands.</span></span>

<span data-ttu-id="8528d-118">В следующей таблице перечислены типы сценариев, поддерживаемые проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8528d-118">The following table lists script types that are supported by Windows Media Player.</span></span>



| <span data-ttu-id="8528d-119">Тип скрипта</span><span class="sxs-lookup"><span data-stu-id="8528d-119">Script type</span></span> | <span data-ttu-id="8528d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="8528d-120">Description</span></span>                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8528d-121">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="8528d-121">URL</span></span>         | <span data-ttu-id="8528d-122">Проигрыватель отправляет указанный URL-адрес в браузер для показа пользователю.</span><span class="sxs-lookup"><span data-stu-id="8528d-122">The player sends the specified URL to the browser for display to the user.</span></span> <span data-ttu-id="8528d-123">Если используется встроенный элемент управления Player, можно добавить ссылку на этот фрейм в URL-адрес с помощью синтаксиса &&*фраменаме* .</span><span class="sxs-lookup"><span data-stu-id="8528d-123">If an embedded player control is being used, you can add a specific frame reference to the URL by using the &&*framename* syntax.</span></span>                                                                             |
| <span data-ttu-id="8528d-124">ФАЙЛОВ</span><span class="sxs-lookup"><span data-stu-id="8528d-124">FILENAME</span></span>    | <span data-ttu-id="8528d-125">URL-адрес другого файла мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8528d-125">A URL to another media file to be played.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="8528d-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="8528d-126">CAPTION</span></span>     | <span data-ttu-id="8528d-127">Текстовая строка, отображаемая в области субтитров проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8528d-127">A text string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="8528d-128">Этот тип поддерживает стандартное форматирование HTML, поэтому текст можно отформатировать по своему усмотрению.</span><span class="sxs-lookup"><span data-stu-id="8528d-128">This type supports standard HTML formatting, so the text can be formatted as you wish.</span></span> <span data-ttu-id="8528d-129">Примером использования является закрытая подпись.</span><span class="sxs-lookup"><span data-stu-id="8528d-129">An example of use is closed captioning.</span></span>                                                                             |
| <span data-ttu-id="8528d-130">ЖУРНАЛЕ</span><span class="sxs-lookup"><span data-stu-id="8528d-130">EVENT</span></span>       | <span data-ttu-id="8528d-131">Имя события, которое будет происходить.</span><span class="sxs-lookup"><span data-stu-id="8528d-131">The name of an event that is to occur.</span></span> <span data-ttu-id="8528d-132">Тип события поддерживает настройку для собственных применений.</span><span class="sxs-lookup"><span data-stu-id="8528d-132">The EVENT type supports customization for your own uses.</span></span> <span data-ttu-id="8528d-133">Код для указанного события должен быть определен в метафайле Windows Media для потока, чтобы проигрыватель мог выполнить указанное событие.</span><span class="sxs-lookup"><span data-stu-id="8528d-133">The code for the specified event must be defined in the Windows Media metafile for the stream in order for the player to perform the specified event.</span></span> <span data-ttu-id="8528d-134">Примером использования является вставка рекламы.</span><span class="sxs-lookup"><span data-stu-id="8528d-134">An example of use is ad insertion.</span></span> |
| <span data-ttu-id="8528d-135">опеневент</span><span class="sxs-lookup"><span data-stu-id="8528d-135">OPENEVENT</span></span>   | <span data-ttu-id="8528d-136">Этот скрипт предшествует фактическому событию.</span><span class="sxs-lookup"><span data-stu-id="8528d-136">This script precedes the actual EVENT.</span></span> <span data-ttu-id="8528d-137">ОПЕНЕВЕНТ позволяет проигрывателю предварительно буферизовать содержимое, чтобы при возникновении события переключение между потоками было неэффективным.</span><span class="sxs-lookup"><span data-stu-id="8528d-137">The OPENEVENT allows the player to pre-buffer the content so that when the EVENT occurs, the switch between streams appears to be seamless.</span></span>                                                                                                       |
| <span data-ttu-id="8528d-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="8528d-138">TEXT</span></span>        | <span data-ttu-id="8528d-139">ТЕКСТовая строка, отображаемая в области субтитров проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8528d-139">A TEXT string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="8528d-140">Может быть обычным текстом, SAMId или текстом в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="8528d-140">Can be plain text, SAMI, or HTML formatted text.</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="8528d-141">См. также</span><span class="sxs-lookup"><span data-stu-id="8528d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8528d-142">**Использование команд сценария**</span><span class="sxs-lookup"><span data-stu-id="8528d-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




