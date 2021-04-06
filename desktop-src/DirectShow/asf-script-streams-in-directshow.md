---
description: Потоки скриптов ASF в DirectShow
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: Потоки скриптов ASF в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990204"
---
# <a name="asf-script-streams-in-directshow"></a><span data-ttu-id="2c7e7-103">Потоки скриптов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="2c7e7-103">ASF Script Streams in DirectShow</span></span>

<span data-ttu-id="2c7e7-104">Когда фильтру [чтения WM ASF](wm-asf-reader-filter.md) присваивается файл, содержащий поток типа вммедиатипе \_ script, он создает для него закрепление вывода, которое можно подключить к фильтру модуля подготовки к [просмотру команды скрипта](internal-script-command-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="2c7e7-104">When the [WM ASF Reader](wm-asf-reader-filter.md) filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="2c7e7-105">При вызове [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)этот фильтр автоматически добавляется в граф и подключается к нему.</span><span class="sxs-lookup"><span data-stu-id="2c7e7-105">When you call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="2c7e7-106">Когда модуль подготовки отчетов команды скрипта получает пример, содержащий команду сценария, он запускает событие [**события EC \_ OLE \_**](ec-ole-event.md) *, которое содержит скрипт* .</span><span class="sxs-lookup"><span data-stu-id="2c7e7-106">When the Internal Script Command Renderer receives a sample containing a script command, it fires an [**EC\_OLE\_EVENT**](ec-ole-event.md) event whose *lParam* contains the script.</span></span> <span data-ttu-id="2c7e7-107">Приложение полностью отвечает за обработку этого события.</span><span class="sxs-lookup"><span data-stu-id="2c7e7-107">The application is entirely responsible for handling this event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c7e7-108">См. также</span><span class="sxs-lookup"><span data-stu-id="2c7e7-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c7e7-109">Чтение файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="2c7e7-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



