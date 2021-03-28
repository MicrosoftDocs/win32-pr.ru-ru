---
description: Показывает, какой раздел реестра должен быть настроен для предотвращения автозапуска.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Как предотвратить автозапуск для компонента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebe03473ce7c5eb441ec428cbe4d060dc62f042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985425"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a><span data-ttu-id="46017-103">Как предотвратить автозапуск для компонента</span><span class="sxs-lookup"><span data-stu-id="46017-103">How to Prevent AutoPlay for a Component</span></span>

<span data-ttu-id="46017-104">Показывает, какой раздел реестра должен быть настроен для предотвращения автозапуска.</span><span class="sxs-lookup"><span data-stu-id="46017-104">Illustrates which registry key must be set to prevent AutoPlay.</span></span>

## <a name="instructions"></a><span data-ttu-id="46017-105">Инструкции</span><span class="sxs-lookup"><span data-stu-id="46017-105">Instructions</span></span>


<span data-ttu-id="46017-106">Чтобы предотвратить запуск автозапуска в ответ на событие, добавьте следующее значение **reg \_ SZ** , как показано в этом примере.</span><span class="sxs-lookup"><span data-stu-id="46017-106">To prevent AutoPlay from launching in response to an event, add the following **REG\_SZ** value, as shown in this example.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="46017-107">Значение является идентификатором класса (CLSID), который компонент, создающий событие, известен в таблице текущих объектов (ROT).</span><span class="sxs-lookup"><span data-stu-id="46017-107">The value is the class identifier (CLSID) that the component that is generating the event is known by in the running object table (ROT).</span></span> <span data-ttu-id="46017-108">Значение не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="46017-108">The value has no data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46017-109">В этом ключе идентификаторы CLSID не заключаются в фигурные скобки ( {} ).</span><span class="sxs-lookup"><span data-stu-id="46017-109">Under this key, the CLSIDs are not enclosed in braces ( {} ).</span></span>

 

 

 



