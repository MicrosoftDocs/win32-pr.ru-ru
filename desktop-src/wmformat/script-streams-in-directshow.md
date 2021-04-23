---
title: Создание скриптов для потоков в DirectShow
description: Создание скриптов для потоков в DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Пакет SDK для Windows Media Format, DirectShow
- Пакет Windows Media Format SDK, скриптовые потоки
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный системный формат (ASF), скриптовые потоки
- ASF (Расширенный системный формат), скриптовые потоки
- DirectShow, скриптовые потоки
- Создание скриптов для потоков, DirectShow
- потоки, скриптовые потоки в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332171"
---
# <a name="script-streams-in-directshow"></a><span data-ttu-id="6eee0-112">Создание скриптов для потоков в DirectShow</span><span class="sxs-lookup"><span data-stu-id="6eee0-112">Script Streams in DirectShow</span></span>

<span data-ttu-id="6eee0-113">Когда фильтр чтения WM ASF получает файл, содержащий поток типа ВММЕДИАТИПЕ \_ script, он создает для него закрепление вывода, которое может быть подключено к фильтру модуля подготовки отчетов для внутреннего выполнения DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6eee0-113">When the WM ASF Reader filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the DirectShow Internal Script Command Renderer filter.</span></span> <span data-ttu-id="6eee0-114">При вызове **играфбуилдер:: renderFile** этот фильтр автоматически добавляется в граф и подключается к нему.</span><span class="sxs-lookup"><span data-stu-id="6eee0-114">When you call **IGraphBuilder::RenderFile**, that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="6eee0-115">Когда модуль подготовки отчетов команды внутреннего скрипта получает пример, содержащий команду сценария, он запускает **событие EC \_ OLE \_** **, которое содержит скрипт** .</span><span class="sxs-lookup"><span data-stu-id="6eee0-115">When the Internal Script Command Renderer receives a sample containing a script command, it fires an **EC\_OLE\_EVENT** whose **lParam** contains the script.</span></span> <span data-ttu-id="6eee0-116">Приложение полностью отвечает за обработку этого события.</span><span class="sxs-lookup"><span data-stu-id="6eee0-116">The application is entirely responsible for handling this event.</span></span> <span data-ttu-id="6eee0-117">Дополнительные сведения о **\_ \_ событии EC OLE** см. в документации по пакету SDK для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6eee0-117">For more information on **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

 

 




