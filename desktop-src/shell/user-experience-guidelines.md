---
description: Основной обязанностью любого элемента панели управления является отображение окна, позволяющего пользователю просматривать параметры и управлять ими.
title: Руководство по работе пользователей
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997918"
---
# <a name="user-experience-guidelines"></a><span data-ttu-id="1706f-103">Руководство по работе пользователей</span><span class="sxs-lookup"><span data-stu-id="1706f-103">User Experience Guidelines</span></span>

<span data-ttu-id="1706f-104">Основной обязанностью любого элемента панели управления является отображение окна, позволяющего пользователю просматривать параметры и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="1706f-104">The primary responsibility of any Control Panel item is to display a window that allows the user to view and manipulate settings.</span></span> <span data-ttu-id="1706f-105">Сведения о поведении и проектировании элементов панели управления см. в [руководстве по пользовательскому интерфейсу панели управления](../uxguide/winenv-ctrl-panels.md) .</span><span class="sxs-lookup"><span data-stu-id="1706f-105">See the [Control Panels user experience (UX) guidelines](../uxguide/winenv-ctrl-panels.md) for the behavior and design of Control Panel items.</span></span> <span data-ttu-id="1706f-106">В рекомендациях, описанных в этом разделе, показан способ организации элемента панели управления с помощью потока задач.</span><span class="sxs-lookup"><span data-stu-id="1706f-106">The guidelines discussed in that topic show a task flow method of organizing a Control Panel item.</span></span> <span data-ttu-id="1706f-107">Это помещает наиболее важные параметры на домашнюю страницу.</span><span class="sxs-lookup"><span data-stu-id="1706f-107">This places the most important settings on a home page.</span></span> <span data-ttu-id="1706f-108">Менее часто используемые параметры помещаются на периферийные страницы или доступны из ссылок в боковой области.</span><span class="sxs-lookup"><span data-stu-id="1706f-108">Less frequently used settings are placed on spoke pages or accessed from links in a side pane.</span></span>

<span data-ttu-id="1706f-109">Панель управления содержит множество элементов, которые следуют этим рекомендациям, например центр доступа и центр управления сетями и общим доступом.</span><span class="sxs-lookup"><span data-stu-id="1706f-109">The Control Panel includes many items that follow these guidelines, such as Ease of Access Center and Network and Sharing Center.</span></span> <span data-ttu-id="1706f-110">Другие элементы панели управления используют формат вкладки диалогового окна с вкладками, как в предыдущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="1706f-110">Other Control Panel items use the tabbed dialog property sheet format as in earlier versions of Windows.</span></span> <span data-ttu-id="1706f-111">К примерам относятся элемент мыши и свойства браузера.</span><span class="sxs-lookup"><span data-stu-id="1706f-111">Examples include the Mouse item and Internet Options.</span></span> <span data-ttu-id="1706f-112">Использование формата листа свойств должно быть прекращено.</span><span class="sxs-lookup"><span data-stu-id="1706f-112">Use of the property sheet format should be discontinued.</span></span> <span data-ttu-id="1706f-113">При создании новых элементов панели управления следует следовать рекомендациям потока задач.</span><span class="sxs-lookup"><span data-stu-id="1706f-113">If you create new Control Panel items, you should follow the task flow guidelines.</span></span>

<span data-ttu-id="1706f-114">В прошлом элементы панели управления были упакованы как файлы. cpl.</span><span class="sxs-lookup"><span data-stu-id="1706f-114">In the past, Control Panel items were packaged as .cpl files.</span></span> <span data-ttu-id="1706f-115">Это больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="1706f-115">That is no longer necessary.</span></span> <span data-ttu-id="1706f-116">Новые элементы панели управления должны быть реализованы в виде автономного exe-файла или в качестве параметра флага командной строки для основного исполняемого файла приложения.</span><span class="sxs-lookup"><span data-stu-id="1706f-116">New Control Panel items should be implemented as a standalone .exe file or as a command-line flag option for the application's main executable file.</span></span>

> [!Note]  
> <span data-ttu-id="1706f-117">В 64-разрядных системах, 32-разрядные элементы панели управления отображаются на панели управления, когда выбран параметр **Папка "представление элементов панели управления" представления 32-bit** .</span><span class="sxs-lookup"><span data-stu-id="1706f-117">On 64-bit systems, 32-bit Control Panel items are displayed in the Control Panel when the **View 32-bit Control Panel Items folder** option is selected.</span></span> <span data-ttu-id="1706f-118">32-разрядные элементы должны находиться в папке% SystemRoot% \\ SysWOW64 для отображения.</span><span class="sxs-lookup"><span data-stu-id="1706f-118">The 32-bit items must be located in the %SystemRoot%\\SysWOW64 folder to be displayed.</span></span> <span data-ttu-id="1706f-119">Для них не требуется дальнейшая регистрация.</span><span class="sxs-lookup"><span data-stu-id="1706f-119">They do not require any further registration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1706f-120">См. также</span><span class="sxs-lookup"><span data-stu-id="1706f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1706f-121">Элементы панели управления</span><span class="sxs-lookup"><span data-stu-id="1706f-121">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="1706f-122">Регистрация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="1706f-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="1706f-123">Использование Кплапплет</span><span class="sxs-lookup"><span data-stu-id="1706f-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="1706f-124">Обработка сообщений в панели управления</span><span class="sxs-lookup"><span data-stu-id="1706f-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="1706f-125">Исполнение элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="1706f-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="1706f-126">Расширение элементов панели управления "система"</span><span class="sxs-lookup"><span data-stu-id="1706f-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="1706f-127">Назначение категорий панели управления</span><span class="sxs-lookup"><span data-stu-id="1706f-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="1706f-128">Создание ссылок на задачи с возможностью поиска для элемента панели управления</span><span class="sxs-lookup"><span data-stu-id="1706f-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="1706f-129">Доступ к панели управления в защищенном режиме</span><span class="sxs-lookup"><span data-stu-id="1706f-129">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



