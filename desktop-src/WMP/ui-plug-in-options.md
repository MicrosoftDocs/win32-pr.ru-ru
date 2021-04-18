---
title: Параметры подключаемого модуля пользовательского интерфейса
description: Параметры подключаемого модуля пользовательского интерфейса
ms.assetid: 3c188506-865c-4e0c-965d-1429eafd01ef
keywords:
- Подключаемые модули проигрывателя Windows Media, параметры
- подключаемые модули, параметры
- подключаемые модули пользовательского интерфейса, параметры
- Подключаемые модули пользовательского интерфейса, параметры
- подключаемые модули области параметров
- фоновые подключаемые модули
- отдельные подключаемые модули окна
- подключаемые модули области метаданных
- подключаемые модули области дисплея
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281dd0679e6a975b1c867624f2f652f2b3e6b9ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700505"
---
# <a name="ui-plug-in-options"></a><span data-ttu-id="e2115-112">Параметры подключаемого модуля пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="e2115-112">UI Plug-in Options</span></span>

<span data-ttu-id="e2115-113">Любой из пяти типов подключаемых модулей пользовательского интерфейса может иметь страницу свойств, где пользователь может изменять параметры подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="e2115-113">Any of the five UI plug-in types can have a property page where the user can modify plug-in settings.</span></span> <span data-ttu-id="e2115-114">Эта страница свойств может быть настроена на автоматическое отображение при первой загрузке подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="e2115-114">This property page can be set to display automatically when a plug-in is loaded for the first time.</span></span> <span data-ttu-id="e2115-115">Доступ к нему можно также получить на вкладке подключаемые модули диалогового окна Параметры.</span><span class="sxs-lookup"><span data-stu-id="e2115-115">It can also be accessed from the Plug-ins tab of the Options dialog box.</span></span>

<span data-ttu-id="e2115-116">Подключаемый модуль пользовательского интерфейса может быть настроен на автоматическую загрузку после установки при запуске проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e2115-116">A UI plug-in can be set to load automatically after installation when Windows Media Player is started.</span></span> <span data-ttu-id="e2115-117">Если он не запускается автоматически, пользователь может загрузить его, выбрав его из списка **подключаемые модули** в меню **Сервис** .</span><span class="sxs-lookup"><span data-stu-id="e2115-117">If it is not started automatically, the user can load it by selecting it from the **Plug-ins** list on the **Tools** menu.</span></span>

<span data-ttu-id="e2115-118">Подключаемый модуль области отображения может иметь несколько предустановок, которые являются разными представлениями, которые подключаемый модуль может сделать доступным для пользователя.</span><span class="sxs-lookup"><span data-stu-id="e2115-118">A display area plug-in can have multiple presets, which are different views that the plug-in can make available to the user.</span></span> <span data-ttu-id="e2115-119">Пользователь может изменить предустановку, выбрав другую запись в списке " **визуализации и представления** " в меню " **вид** " или используя кнопки со стрелками, расположенные в нижней части области " **Воспроизведение** ", непосредственно над сообщением о состоянии и элементами управления передачей.</span><span class="sxs-lookup"><span data-stu-id="e2115-119">The user can change the preset by selecting a different entry from the **Visualizations and Views** list on the **View** menu, or by using the arrow buttons provided at the bottom of the **Now Playing** pane just above the status message and transport controls.</span></span>

<span data-ttu-id="e2115-120">Фоновые и отдельные подключаемые модули пользовательского интерфейса окна могут быть запрограммированы для принятия элемента мультимедиа или списка воспроизведения, отправляемого пользователем.</span><span class="sxs-lookup"><span data-stu-id="e2115-120">Background and separate window UI plug-ins can be programmed to accept a media item or playlist that the user sends to it.</span></span> <span data-ttu-id="e2115-121">Если подключаемый модуль поддерживает эту функцию, его имя появится в списке **Отправить** в, доступном в контекстном меню элемента управления списка воспроизведения или библиотеки.</span><span class="sxs-lookup"><span data-stu-id="e2115-121">If a plug-in supports this feature, its name will appear on the **Send to** list available from the shortcut menu of the playlist control or the library.</span></span>

<span data-ttu-id="e2115-122">Подключаемый модуль пользовательского интерфейса может быть запрограммирован на перехват сочетаний клавиш при наличии фокуса клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="e2115-122">A UI plug-in can be programmed to intercept keyboard shortcuts when it has the keyboard focus.</span></span> <span data-ttu-id="e2115-123">Фокус клавиатуры необходим для предотвращения конфликтов при загрузке нескольких подключаемых модулей пользовательского интерфейса, которые перехватывают одно и то же сочетание клавиш.</span><span class="sxs-lookup"><span data-stu-id="e2115-123">Keyboard focus is required to prevent conflicts when multiple UI plug-ins that intercept the same keyboard shortcut are loaded.</span></span> <span data-ttu-id="e2115-124">Хотя это предотвращает конфликты, это также может привести к путанице конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="e2115-124">Although this prevents conflicts, it can also cause confusion to end users.</span></span> <span data-ttu-id="e2115-125">По этой причине не рекомендуется использовать сочетания клавиш с подключаемыми модулями пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e2115-125">For this reason, the use of keyboard shortcuts with UI plug-ins is not recommended.</span></span> <span data-ttu-id="e2115-126">Однако если они используются, они не должны перехватывать сочетания клавиш, используемые проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e2115-126">When they are used, however, they should not intercept any keyboard shortcuts that are used by Windows Media Player.</span></span> <span data-ttu-id="e2115-127">Полный список сочетаний клавиш, используемых проигрывателем, см. в справке проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e2115-127">For a complete list of keyboard shortcuts used by the Player, see Windows Media Player Help.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2115-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e2115-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2115-129">**Общие сведения о подключаемом модуле пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="e2115-129">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




