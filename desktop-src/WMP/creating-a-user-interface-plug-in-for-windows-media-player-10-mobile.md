---
title: Создание подключаемого модуля пользовательского интерфейса для проигрывателя Windows Media 10 Mobile
description: Создание подключаемого модуля пользовательского интерфейса для проигрывателя Windows Media 10 Mobile
ms.assetid: 050418b7-d99c-49ab-8ce6-6511b194ffe6
keywords:
- Проигрыватель Windows Media Mobile, подключаемые модули
- Проигрыватель Windows Media Mobile, подключаемые модули пользовательского интерфейса
- Подключаемые модули мобильных устройств проигрывателя Windows Media
- подключаемые модули, Пользовательский интерфейс
- подключаемые модули, проигрыватель Windows Media Mobile
- подключаемые модули пользовательского интерфейса, мобильные проигрыватели Windows Media
- Подключаемые модули пользовательского интерфейса, проигрыватель Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d649ef1d8ed1b8fb1e1b54dc7eed106f798b1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691256"
---
# <a name="creating-a-user-interface-plug-in-for-windows-media-player-10-mobile"></a><span data-ttu-id="38a67-110">Создание подключаемого модуля пользовательского интерфейса для проигрывателя Windows Media 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="38a67-110">Creating a User Interface Plug-in for Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="38a67-111">Проигрыватель Windows Media 10 Mobile использует ту же модель подключаемого модуля пользовательского интерфейса, что и классическое устройство Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="38a67-111">Windows Media Player 10 Mobile uses the same UI plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="38a67-112">Однако проигрыватель Windows Media 10 Mobile может взаимодействовать только с фоновыми подключаемыми модулями пользовательского интерфейса. Из-за аналогичных моделей подключаемых модулей те же вызовы API, которые применяются к фоновым подключаемым модулям пользовательского интерфейса на рабочем столе, также применяются к фоновым подключаемым модулям пользовательского интерфейса на устройстве Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="38a67-112">However, Windows Media Player 10 Mobile can only interact with background UI plug-ins. Because of the similar plug-in models, the same API calls that apply to background UI plug-ins on the desktop also apply to background UI plug-ins on a Windows Mobile device.</span></span>

<span data-ttu-id="38a67-113">В следующих разделах описывается создание подключаемого модуля фонового пользовательского интерфейса с помощью созданного мастером кода из мастера подключаемых модулей проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="38a67-113">The following sections describe how to create a background UI plug-in by using wizard-generated code from the Windows Media Player Plug-in Wizard.</span></span>



| <span data-ttu-id="38a67-114">Section</span><span class="sxs-lookup"><span data-stu-id="38a67-114">Section</span></span>                                                                | <span data-ttu-id="38a67-115">Описание</span><span class="sxs-lookup"><span data-stu-id="38a67-115">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38a67-116">Начало работы</span><span class="sxs-lookup"><span data-stu-id="38a67-116">Getting Started</span></span>](getting-started.md)                                 | <span data-ttu-id="38a67-117">Описывает, что необходимо установить, и использование мастера подключаемых модулей проигрывателя Windows Media для автоматизации создания фонового подключаемого модуля пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="38a67-117">Describes what you need to install and how to use the Windows Media Player Plug-in Wizard to help automate the creation of a background UI plug-in.</span></span>    |
| [<span data-ttu-id="38a67-118">Изменение кода, созданного мастером</span><span class="sxs-lookup"><span data-stu-id="38a67-118">Modifying Wizard-generated Code</span></span>](modifying-wizard-generated-code.md) | <span data-ttu-id="38a67-119">Описание того, что необходимо изменить из созданного мастером кода, созданного в предыдущем разделе, чтобы он работал с проигрывателем Windows Media 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="38a67-119">Describes what you need to modify from the wizard-generated code created in the previous section so that it works with Windows Media Player 10 Mobile.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="38a67-120">См. также</span><span class="sxs-lookup"><span data-stu-id="38a67-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38a67-121">**Программное руководством по программированию подключаемых модулей пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="38a67-121">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




