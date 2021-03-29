---
title: Инициализация страницы
description: Инициализация страницы
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Интернет-магазины проигрывателя Windows Media, диспетчер загрузки
- Интернет-магазины, диспетчер загрузки
- Тип 2 Интернет-магазинов, диспетчер загрузки
- Интернет-магазины проигрывателя Windows Media, инициализация страниц
- Интернет-магазины, инициализация страниц
- Тип 2 Интернет-магазинов, инициализация страниц
- Проигрыватель Windows Media, диспетчер загрузки
- Диспетчер загрузки проигрывателя Windows Media
- Диспетчер загрузки
- Инициализация страниц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258717"
---
# <a name="initializing-the-page"></a><span data-ttu-id="364b7-113">Инициализация страницы</span><span class="sxs-lookup"><span data-stu-id="364b7-113">Initializing the Page</span></span>

<span data-ttu-id="364b7-114">При загрузке веб-страницы выполняется функция **init** .</span><span class="sxs-lookup"><span data-stu-id="364b7-114">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="364b7-115">Этот код сначала извлекает все данные, хранящиеся в предыдущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="364b7-115">This code first retrieves any data stored in a previous session.</span></span> <span data-ttu-id="364b7-116">Дополнительные сведения см. в разделе [обслуживание сведений о сеансах](maintaining-session-information.md).</span><span class="sxs-lookup"><span data-stu-id="364b7-116">For details, see [Maintaining Session Information](maintaining-session-information.md).</span></span> <span data-ttu-id="364b7-117">Затем он создает объект **довнлоадманажер** и сохраняет его в глобальной переменной с именем g \_ оманажер.</span><span class="sxs-lookup"><span data-stu-id="364b7-117">It then creates the **DownloadManager** object and stores it in the global variable named g\_oManager.</span></span>


```C++
g_oManager = external.DownloadManager;

```



<span data-ttu-id="364b7-118">Затем функция подключает событие **онколорчанже** к функции с именем **онаппколор** , а затем вызывает функцию напрямую для инициализации цвета фона.</span><span class="sxs-lookup"><span data-stu-id="364b7-118">Next, the function connects the **OnColorChange** event to the function named **OnAppColor** and then calls the function directly to initialize the background color.</span></span> <span data-ttu-id="364b7-119">См. раздел [Сопоставление цветов проигрывателя Windows Media](matching-the-windows-media-player-colors.md).</span><span class="sxs-lookup"><span data-stu-id="364b7-119">See [Matching the Windows Media Player Colors](matching-the-windows-media-player-colors.md).</span></span>

<span data-ttu-id="364b7-120">Наконец, функция запускает таймер с интервалом в 1 секунду и инициализирует списки, отображающие ожидающие загрузки коллекции и элементы загрузки.</span><span class="sxs-lookup"><span data-stu-id="364b7-120">Finally, the function starts a timer with a one-second interval and initializes the list boxes that display the pending download collections and download items.</span></span> <span data-ttu-id="364b7-121">Это важно, так как в последний раз при закрытии Интернет-магазина были запущены сеансы, и эти сведения необходимо отобразить снова.</span><span class="sxs-lookup"><span data-stu-id="364b7-121">This is important because there may have been sessions in progress the last time the online store closed and this information needs to be displayed again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="364b7-122">См. также</span><span class="sxs-lookup"><span data-stu-id="364b7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="364b7-123">**Использование диспетчера загрузки**</span><span class="sxs-lookup"><span data-stu-id="364b7-123">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




