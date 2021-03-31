---
title: Иажентнотифисинк закладка
description: Иажентнотифисинк закладка
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1febedfc962904544a49b8621812d0518026b459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774846"
---
# <a name="iagentnotifysinkbookmark"></a><span data-ttu-id="f9edc-103">Иажентнотифисинк:: Bookmark</span><span class="sxs-lookup"><span data-stu-id="f9edc-103">IAgentNotifySink::Bookmark</span></span>

<span data-ttu-id="f9edc-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f9edc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

<span data-ttu-id="f9edc-105">Уведомляет клиентское приложение о завершении заданной закладки.</span><span class="sxs-lookup"><span data-stu-id="f9edc-105">Notifies a client application when its bookmark completes.</span></span>

-   <span data-ttu-id="f9edc-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f9edc-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="f9edc-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*двбукмаркид*</span><span class="sxs-lookup"><span data-stu-id="f9edc-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span></span>
</dt> <dd>

<span data-ttu-id="f9edc-108">Идентификатор закладки, которая привела к срабатыванию события.</span><span class="sxs-lookup"><span data-stu-id="f9edc-108">Identifier of the bookmark that resulted in triggering the event.</span></span>

</dd> </dl>

<span data-ttu-id="f9edc-109">При включении тегов закладок в метод [**говорите**](speak-method.md) можно отнестись к возникновению этого события.</span><span class="sxs-lookup"><span data-stu-id="f9edc-109">When you include bookmark tags in a [**Speak**](speak-method.md) method, you can track when they occur with this event.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9edc-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="f9edc-110">See Also</span></span>

<span data-ttu-id="f9edc-111">[**Иажентчарактер:: говорите**](iagentcharacter--speak.md), [теги выходных данных агента Microsoft Agent](microsoft-agent-speech-output-tags.md)</span><span class="sxs-lookup"><span data-stu-id="f9edc-111">[**IAgentCharacter::Speak**](iagentcharacter--speak.md), [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md)</span></span>


 

 




