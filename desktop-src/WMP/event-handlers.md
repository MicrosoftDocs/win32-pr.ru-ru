---
title: Обработчики событий
description: Обработчики событий
ms.assetid: abb5f123-b838-46fb-ab11-cee70cc76a38
keywords:
- Обложки проигрывателя Windows Media, обработчики событий в JScript
- обложки, обработчики событий в JScript
- события, JScript
- Файлы JScript для обложек, обработчики событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec4413ae3a2358b01685cd0edfe66de92810a64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691134"
---
# <a name="event-handlers"></a><span data-ttu-id="60e9f-107">Обработчики событий</span><span class="sxs-lookup"><span data-stu-id="60e9f-107">Event Handlers</span></span>

<span data-ttu-id="60e9f-108">Microsoft JScript используется для обработки событий в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="60e9f-108">Microsoft JScript is used to process events in the skin definition file.</span></span> <span data-ttu-id="60e9f-109">Дополнительные сведения о обработчиках событий см. в разделе [Обработка событий](handling-events.md) .</span><span class="sxs-lookup"><span data-stu-id="60e9f-109">See [Handling Events](handling-events.md) for more information about event handlers.</span></span>

<span data-ttu-id="60e9f-110">В обработчике событий может быть несколько строк кода, но необходимо соблюдать осторожность, чтобы не превысить длину строки, которую разрешает JScript.</span><span class="sxs-lookup"><span data-stu-id="60e9f-110">You can have more than one line of code in an event handler, but care must be taken not to exceed the line length that JScript permits.</span></span> <span data-ttu-id="60e9f-111">Разделяйте строки точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="60e9f-111">Separate the lines by semicolons.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a><span data-ttu-id="60e9f-112">См. также</span><span class="sxs-lookup"><span data-stu-id="60e9f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60e9f-113">**Использование JScript**</span><span class="sxs-lookup"><span data-stu-id="60e9f-113">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




