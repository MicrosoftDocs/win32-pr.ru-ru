---
title: Использование команд сценария
description: Использование команд сценария
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Пакет SDK для Windows Media Format, команды сценариев
- Расширенный системный формат (ASF), команды сценариев
- ASF (Расширенный системный формат), команды сценариев
- скрипты, команды
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068057"
---
# <a name="using-script-commands"></a><span data-ttu-id="fbaa0-107">Использование команд сценария</span><span class="sxs-lookup"><span data-stu-id="fbaa0-107">Using Script Commands</span></span>

<span data-ttu-id="fbaa0-108">Пакет SDK для формата Windows Media поддерживает использование команд сценариев для обмена действиями приложений в файлах ASF.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-108">The Windows Media Format SDK supports the use of script commands to communicate application actions in ASF files.</span></span> <span data-ttu-id="fbaa0-109">Каждая команда сценария состоит из двух строк, первая — это тип команды, а вторая — данные команды.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-109">Each script command is made up of two strings, the first string is the type of command, the second is the command data.</span></span> <span data-ttu-id="fbaa0-110">Например, можно использовать тип скрипта "URL" и передать допустимый URL-адрес в Интернете в качестве данных команды.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-110">For example, you can use the script type "URL" and pass a valid Internet URL as the command data.</span></span> <span data-ttu-id="fbaa0-111">Когда приложение чтения, поддерживающее команды сценария типа "URL", получает эту команду, оно открывает указанный адрес в окне браузера.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-111">When a reading application that supports script commands of type "URL" receives this command, it will open the specified address in a browser window.</span></span>

<span data-ttu-id="fbaa0-112">Пакет Windows Media Format SDK предоставляет два способа доставки сценариев в файлы ASF.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-112">The Windows Media Format SDK provides two options for delivering script in ASF files.</span></span> <span data-ttu-id="fbaa0-113">Можно создать поток скрипта или включить команды сценария в заголовок файла.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-113">You can create a script stream or you can include script commands in the header of the file.</span></span> <span data-ttu-id="fbaa0-114">Потоки сценариев полезны, так как команды сценария доставляются в порядке времени презентации.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-114">Script streams are useful because the script commands are delivered in presentation time order.</span></span> <span data-ttu-id="fbaa0-115">При использовании команд сценария в заголовке файла приложению потребуется получить все команды сценария перед запуском воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-115">If you use script commands in the file header, your application will need to retrieve all of the script commands before starting playback.</span></span> <span data-ttu-id="fbaa0-116">Необходимо учитывать время показа команд сценария и реагировать на них в нужное время.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-116">You must keep track of the presentation times of script commands and respond to them at the right time.</span></span>

<span data-ttu-id="fbaa0-117">В следующих разделах описывается включение команд сценария в файл ASF.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-117">The following sections describe how to include script commands in an ASF file.</span></span>



| <span data-ttu-id="fbaa0-118">Section</span><span class="sxs-lookup"><span data-stu-id="fbaa0-118">Section</span></span>                                                                                                                | <span data-ttu-id="fbaa0-119">Описание</span><span class="sxs-lookup"><span data-stu-id="fbaa0-119">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="fbaa0-120">Использование потока скрипта</span><span class="sxs-lookup"><span data-stu-id="fbaa0-120">To Use a Script Stream</span></span>](to-use-a-script-stream.md)                                                                   | <span data-ttu-id="fbaa0-121">Описывает включение команд скрипта в поток скрипта.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-121">Describes how to include script commands in a script stream.</span></span> |
| [<span data-ttu-id="fbaa0-122">Добавление данных скрипта в заголовок</span><span class="sxs-lookup"><span data-stu-id="fbaa0-122">To Add Script Data to the Header</span></span>](to-add-script-data-to-the-header.md)                                               | <span data-ttu-id="fbaa0-123">Описывает включение команд сценария в заголовок файла.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-123">Describes how to include script commands in the file header.</span></span> |
| [<span data-ttu-id="fbaa0-124">Использование команд сценариев, поддерживаемых проигрывателем Windows Media</span><span class="sxs-lookup"><span data-stu-id="fbaa0-124">Using Script Commands Supported by Windows Media Player</span></span>](using-script-commands-supported-by-windows-media-player.md) | <span data-ttu-id="fbaa0-125">Описание команд сценария, используемых проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-125">Describes the script commands used by Windows Media Player.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="fbaa0-126">В предыдущих версиях пакета SDK для формата Windows Media были использованы потоки сценариев для открытия веб-адресов, соответствующих содержимому файла ASF.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-126">In previous versions of the Windows Media Format SDK, script streams were used to open Web addresses corresponding to the content of an ASF file.</span></span> <span data-ttu-id="fbaa0-127">Теперь веб-потоки можно использовать для работы с синхронизированными веб-страницами.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-127">You can now use Web streams to work with synchronized Web pages.</span></span> <span data-ttu-id="fbaa0-128">Дополнительные сведения см. в записи блога</span><span class="sxs-lookup"><span data-stu-id="fbaa0-128">For more information.</span></span> <span data-ttu-id="fbaa0-129">см. [веб-потоки](web-streams.md).</span><span class="sxs-lookup"><span data-stu-id="fbaa0-129">see [Web Streams](web-streams.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fbaa0-130">См. также</span><span class="sxs-lookup"><span data-stu-id="fbaa0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbaa0-131">**Команды скриптов**</span><span class="sxs-lookup"><span data-stu-id="fbaa0-131">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="fbaa0-132">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="fbaa0-132">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




