---
title: Общие сведения о подключаемом модуле пользовательского интерфейса
description: Общие сведения о подключаемом модуле пользовательского интерфейса
ms.assetid: 8c4feb56-31c0-4f69-98dd-3c203941bb4c
keywords:
- Проигрыватель Windows Media, подключаемые модули
- Проигрыватель Windows Media, подключаемые модули пользовательского интерфейса
- Подключаемые модули проигрывателя Windows Media, Пользовательский интерфейс
- подключаемые модули, Пользовательский интерфейс
- подключаемые модули пользовательского интерфейса, сведения
- Сведения о подключаемых модулях пользовательского интерфейса
- подключаемые модули пользовательского интерфейса, типы
- Подключаемые модули пользовательского интерфейса, типы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5228c9ab7ff97c9f0d03b1b8d1320d303b178e56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328987"
---
# <a name="ui-plug-in-overview"></a><span data-ttu-id="9ae15-111">Общие сведения о подключаемом модуле пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9ae15-111">UI Plug-in Overview</span></span>

<span data-ttu-id="9ae15-112">Подключаемые модули пользовательского интерфейса можно устанавливать, удалять и настраивать с помощью вкладки подключаемые модули диалогового окна Параметры в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9ae15-112">UI plug-ins can be installed, uninstalled, and configured using the Plug-ins tab of the Options dialog in Windows Media Player.</span></span>

<span data-ttu-id="9ae15-113">Существует пять типов подключаемых модулей пользовательского интерфейса, поддерживаемых проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9ae15-113">There are five types of UI plug-ins supported by Windows Media Player.</span></span> <span data-ttu-id="9ae15-114">Три из этих типов соответствуют разным областям **воспроизводимой** области в полном режиме проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="9ae15-114">Three of these types correspond to different areas of the **Now Playing** pane of the full mode of the player.</span></span> <span data-ttu-id="9ae15-115">Два других типа предназначены для подключаемых модулей, отображаемых в отдельном окне и для подключаемых модулей, которые не отображаются (за исключением страницы свойств).</span><span class="sxs-lookup"><span data-stu-id="9ae15-115">The other two types are for plug-ins that display in a separate window and for plug-ins that have no display (except perhaps a property page).</span></span>

<span data-ttu-id="9ae15-116">Подключаемые модули пользовательского интерфейса выгружаются, когда они закрываются или отключаются.</span><span class="sxs-lookup"><span data-stu-id="9ae15-116">UI plug-ins are unloaded when they are closed or disabled.</span></span> <span data-ttu-id="9ae15-117">Подключаемые модули пользовательского интерфейса, которые отображаются в области **Воспроизведение сейчас** , также выгружаются, когда пользователь выбирает другой подключаемый модуль того же типа или выходит из области **воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="9ae15-117">UI plug-ins that appear in the **Now Playing** pane are also unloaded when the user chooses another plug-in of the same type or switches out of the **Now Playing** pane.</span></span> <span data-ttu-id="9ae15-118">Когда пользователь переключается в режим обложки, все подключаемые модули остаются загруженными, но не отображаются.</span><span class="sxs-lookup"><span data-stu-id="9ae15-118">When the user switches to skin mode, all plug-ins remain loaded, but are not displayed.</span></span> <span data-ttu-id="9ae15-119">Если при закрытии проигрывателя Windows Media запущены отдельные подключаемые модули окна или фона, они будут автоматически перезагружены при следующем запуске проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="9ae15-119">If separate window or background plug-ins are running when Windows Media Player is closed, they will be automatically reloaded the next time the player is started.</span></span>

<span data-ttu-id="9ae15-120">В следующих разделах приведены общие сведения о подключаемых модулях пользовательского интерфейса проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9ae15-120">The following sections provide general information about Windows Media Player UI plug-ins:</span></span>

-   [<span data-ttu-id="9ae15-121">Отобразить подключаемые модули области (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="9ae15-121">Display Area Plug-ins (deprecated)</span></span>](display-area-plug-ins--deprecated.md)
-   [<span data-ttu-id="9ae15-122">Подключаемые модули области параметров</span><span class="sxs-lookup"><span data-stu-id="9ae15-122">Settings Area Plug-ins</span></span>](settings-area-plug-ins.md)
-   [<span data-ttu-id="9ae15-123">Подключаемые модули области метаданных (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="9ae15-123">Metadata Area Plug-ins (deprecated)</span></span>](metadata-area-plug-ins--deprecated.md)
-   [<span data-ttu-id="9ae15-124">Отдельные подключаемые модули окна</span><span class="sxs-lookup"><span data-stu-id="9ae15-124">Separate Window Plug-ins</span></span>](separate-window-plug-ins.md)
-   [<span data-ttu-id="9ae15-125">Фоновые подключаемые модули</span><span class="sxs-lookup"><span data-stu-id="9ae15-125">Background Plug-ins</span></span>](background-plug-ins.md)
-   [<span data-ttu-id="9ae15-126">Параметры подключаемого модуля пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9ae15-126">UI Plug-in Options</span></span>](ui-plug-in-options.md)
-   [<span data-ttu-id="9ae15-127">Отображение модальных пользовательских интерфейсов</span><span class="sxs-lookup"><span data-stu-id="9ae15-127">Displaying Modal User Interfaces</span></span>](displaying-modal-user-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="9ae15-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9ae15-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ae15-129">**О подключаемых модулях пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="9ae15-129">**About User Interface Plug-ins**</span></span>](about-user-interface-plug-ins.md)
</dt> </dl>

 

 




