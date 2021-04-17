---
description: Начиная с Windows Vista, Текстинпутпанел заменяет Пенинпутпанел для управления внешним видом и поведением панели ввода планшета. в следующих разделах описывается программирование панели ввода с помощью интерфейсов программирования приложений на панели ввода текста. Текстинпутпанел для пользователей Пенинпутпанелусинг панели ввода Аутокомплетинаблинг текстовое исправление для пользовательского рукописного ввода Коллекторсноте панель ввода текста реализована в исполняемом файле с именем TabTip.exe. Выполнение TabTip.exe с параметром/Сикдесктоп пытается запустить ограниченную функциональную версию панели ввода на нестандартном интерактивном рабочем столе, созданном с помощью Креатедесктоп. Для большинства созданных настольных систем панель ввода будет автоматически запущена в этом режиме. Этот параметр предоставляет средства для запуска в необычных сценариях приложения, которые в противном случае препятствуют автоматическому запуску. Если панель ввода уже запущена на рабочем столе, этот параметр не будет действовать, а экземпляр TabTip.exe будет немедленно завершить работу.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Программирование панели ввода текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719716"
---
# <a name="programming-the-text-input-panel"></a><span data-ttu-id="6284c-107">Программирование панели ввода текста</span><span class="sxs-lookup"><span data-stu-id="6284c-107">Programming the Text Input Panel</span></span>

<span data-ttu-id="6284c-108">Начиная с Windows Vista, [**текстинпутпанел**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) заменяет [**пенинпутпанел**](peninputpanel-class.md) для управления внешним видом экрана и поведением панели ввода планшета.</span><span class="sxs-lookup"><span data-stu-id="6284c-108">Starting with Windows Vista, the [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) supersedes the [**PenInputPanel**](peninputpanel-class.md) for controlling the onscreen appearance and behavior of the Tablet Input Panel.</span></span>

<span data-ttu-id="6284c-109">В следующих разделах описывается программирование панели ввода с помощью интерфейсов программирования приложений для панели ввода текста.</span><span class="sxs-lookup"><span data-stu-id="6284c-109">The following sections describe programming the Input Panel using the Text Input Panel application programming interfaces.</span></span>

-   [<span data-ttu-id="6284c-110">Текстинпутпанел для пользователей Пенинпутпанел</span><span class="sxs-lookup"><span data-stu-id="6284c-110">TextInputPanel for Users of PenInputPanel</span></span>](textinputpanel-for-users-of-peninputpanel.md)
-   [<span data-ttu-id="6284c-111">Использование автозаполнения панели ввода</span><span class="sxs-lookup"><span data-stu-id="6284c-111">Using Input Panel AutoComplete</span></span>](using-input-panel-autocomplete.md)
-   [<span data-ttu-id="6284c-112">Включение исправления текста для пользовательских сборов рукописных данных</span><span class="sxs-lookup"><span data-stu-id="6284c-112">Enabling Text Correction for Custom Ink Collectors</span></span>](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> <span data-ttu-id="6284c-113">Панель ввода текста реализована в исполняемом файле с именем TabTip.exe.</span><span class="sxs-lookup"><span data-stu-id="6284c-113">The Text Input Panel is implemented in an executable file called TabTip.exe.</span></span> <span data-ttu-id="6284c-114">Выполнение TabTip.exe с параметром */сикдесктоп* пытается запустить ограниченную функциональную версию панели ввода на нестандартном интерактивном рабочем столе, созданном с помощью [**креатедесктоп**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span><span class="sxs-lookup"><span data-stu-id="6284c-114">Running TabTip.exe with the */SeekDesktop* parameter attempts to run a reduced functionality version of Input Panel on a nonstandard interactive desktop, as created with [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span> <span data-ttu-id="6284c-115">Для большинства созданных настольных систем панель ввода будет автоматически запущена в этом режиме.</span><span class="sxs-lookup"><span data-stu-id="6284c-115">For most created desktops, Input Panel will automatically run in this mode already.</span></span> <span data-ttu-id="6284c-116">Этот параметр предоставляет средства для запуска в необычных сценариях приложения, которые в противном случае препятствуют автоматическому запуску.</span><span class="sxs-lookup"><span data-stu-id="6284c-116">This parameter provides the means for launching it in unusual application scenarios that otherwise prevent the automatic launch.</span></span> <span data-ttu-id="6284c-117">Если панель ввода уже запущена на рабочем столе, этот параметр не будет действовать, а экземпляр TabTip.exe будет немедленно завершить работу.</span><span class="sxs-lookup"><span data-stu-id="6284c-117">If Input Panel is already running on the desktop, this parameter will have no effect and the instance of TabTip.exe will exit immediately.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6284c-118">См. также</span><span class="sxs-lookup"><span data-stu-id="6284c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6284c-119">Программирование панели ввода с помощью класса Пенинпутпанел</span><span class="sxs-lookup"><span data-stu-id="6284c-119">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
