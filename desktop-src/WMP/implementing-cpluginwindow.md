---
title: Реализация Кплугинвиндов
description: Реализация Кплугинвиндов
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Подключаемые модули проигрывателя Windows Media, класс Кплугинвиндов
- подключаемые модули, класс Кплугинвиндов
- подключаемые модули пользовательского интерфейса, класс Кплугинвиндов
- Подключаемые модули пользовательского интерфейса, класс Кплугинвиндов
- Класс Кплугинвиндов
- инструкции по программированию, подключаемые модули пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774609"
---
# <a name="implementing-cpluginwindow"></a><span data-ttu-id="830f2-109">Реализация Кплугинвиндов</span><span class="sxs-lookup"><span data-stu-id="830f2-109">Implementing CPluginWindow</span></span>

<span data-ttu-id="830f2-110">Класс Кплугинвиндов предоставляет пользовательский интерфейс для подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="830f2-110">The CPluginWindow class provides the UI to the plug-in.</span></span> <span data-ttu-id="830f2-111">В случае подключаемого модуля пользовательского интерфейса поиска этот класс содержит код для кнопки **поиска** и код, запускающий страницу поиска при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="830f2-111">In the case of the Search UI plug-in, this class contains the code for the **Search** button and the code that launches the search page when the button is clicked.</span></span>

<span data-ttu-id="830f2-112">Мастер предоставляет базовую реализацию Кплугинвиндов в файле заголовка Кплугинвиндов. h.</span><span class="sxs-lookup"><span data-stu-id="830f2-112">The wizard provides a basic implementation of CPluginWindow in the CPluginWindow.h header file.</span></span> <span data-ttu-id="830f2-113">Чтобы упростить работу, подключаемый модуль пользовательского интерфейса поиска изменит этот файл напрямую, хотя расширенные добавления обычно помещаются в отдельный файл Кплугинвиндов. cpp.</span><span class="sxs-lookup"><span data-stu-id="830f2-113">To keep things simple, the Search UI plug-in will modify this file directly, although extensive additions would normally be placed in a separate CPluginWindow.cpp file.</span></span>

<span data-ttu-id="830f2-114">В следующих разделах описаны действия, которые необходимо выполнить для реализации Кплугинвиндов:</span><span class="sxs-lookup"><span data-stu-id="830f2-114">The following sections describe what you need to do to implement CPluginWindow:</span></span>

-   [<span data-ttu-id="830f2-115">Схема сообщений</span><span class="sxs-lookup"><span data-stu-id="830f2-115">The Message Map</span></span>](the-message-map.md)
-   [<span data-ttu-id="830f2-116">Конструктор</span><span class="sxs-lookup"><span data-stu-id="830f2-116">The Constructor</span></span>](the-constructor.md)
-   [<span data-ttu-id="830f2-117">Метод onpain</span><span class="sxs-lookup"><span data-stu-id="830f2-117">The OnPaint Method</span></span>](the-onpaint-method.md)
-   [<span data-ttu-id="830f2-118">Метод onCreate</span><span class="sxs-lookup"><span data-stu-id="830f2-118">The OnCreate Method</span></span>](the-oncreate-method.md)
-   [<span data-ttu-id="830f2-119">Метод onSearch</span><span class="sxs-lookup"><span data-stu-id="830f2-119">The OnSearch Method</span></span>](the-onsearch-method.md)
-   [<span data-ttu-id="830f2-120">Метод Лаунчпаже</span><span class="sxs-lookup"><span data-stu-id="830f2-120">The LaunchPage Method</span></span>](the-launchpage-method.md)

## <a name="related-topics"></a><span data-ttu-id="830f2-121">См. также</span><span class="sxs-lookup"><span data-stu-id="830f2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="830f2-122">**Программное руководством по программированию подключаемых модулей пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="830f2-122">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




