---
title: Переход к другим Интернет-магазинам
description: Переход к другим Интернет-магазинам
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Интернет-магазины проигрывателя Windows Media, Навигация
- Интернет-магазины, Навигация
- Тип 2 Интернет-магазинов, Навигация
- Навигация по типу 2 Интернет-магазинов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8456954d5a7197a054098320b35fb38409ba62
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328291"
---
# <a name="navigating-to-other-online-stores"></a><span data-ttu-id="4a452-107">Переход к другим Интернет-магазинам</span><span class="sxs-lookup"><span data-stu-id="4a452-107">Navigating to Other Online Stores</span></span>

<span data-ttu-id="4a452-108">Вы можете создавать ссылки на другие Интернет-магазины, которыми вы владеете или перекрестными ссылками на Интернет-магазины, предоставляемые другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="4a452-108">You can create links to other online stores you own or cross-link to online stores provided by others.</span></span> <span data-ttu-id="4a452-109">Для этого необходимо знать имя ключа для Интернет-магазина, к которому необходимо выполнить переход.</span><span class="sxs-lookup"><span data-stu-id="4a452-109">To do this, you need to know the key name for the online store to which you want to navigate.</span></span>

<span data-ttu-id="4a452-110">В следующем примере кода показан HTML-код, который создает ссылку для переключения из Интернет-магазина Proseware в функцию "ServiceTask2" в магазине Саусридже Video online.</span><span class="sxs-lookup"><span data-stu-id="4a452-110">The following example code shows HTML that creates a link to switch from the Proseware online store to the "ServiceTask2" feature of the Southridge Video online store:</span></span>


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



<span data-ttu-id="4a452-111">Когда пользователь щелкнет ссылку, проигрыватель Windows Media предлагает пользователю переключиться в хранилище видео Саусридже.</span><span class="sxs-lookup"><span data-stu-id="4a452-111">When the user clicks the link, Windows Media Player prompts the user to switch to the Southridge Video store.</span></span> <span data-ttu-id="4a452-112">Если пользователь разрешает эту задачу, проигрыватель переключает хранилища и переходит в указанную область задач, добавляя параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="4a452-112">If the user permits it, the Player then switches stores and navigates to the specified task pane, appending the query string parameters.</span></span> <span data-ttu-id="4a452-113">Параметры строки запроса, приведенные в предыдущем примере, являются пользовательскими параметрами.</span><span class="sxs-lookup"><span data-stu-id="4a452-113">The query string parameters shown in the preceding example are custom parameters.</span></span> <span data-ttu-id="4a452-114">Это означает, что Интернет-магазин, на который вы переключиться, должен рассчитывать эти значения и их обработку.</span><span class="sxs-lookup"><span data-stu-id="4a452-114">This means that the online store you switch to must expect these values and handle them.</span></span> <span data-ttu-id="4a452-115">Ваш Интернет-магазин (а также любое хранилище, к которому вы переключается) может использовать параметры строки запроса любым способом.</span><span class="sxs-lookup"><span data-stu-id="4a452-115">Your online store (and any store you switch to) can use query string parameters any way you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a452-116">См. также</span><span class="sxs-lookup"><span data-stu-id="4a452-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a452-117">**Переход между областями задач службы**</span><span class="sxs-lookup"><span data-stu-id="4a452-117">**Navigating between Service Task Panes**</span></span>](navigating-between-service-task-panes.md)
</dt> <dt>

[<span data-ttu-id="4a452-118">**Навигация для Интернет-магазинов типа 2**</span><span class="sxs-lookup"><span data-stu-id="4a452-118">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




