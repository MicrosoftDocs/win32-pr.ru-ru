---
description: Элементы панели управления должны быть зарегистрированы, чтобы они отображались в окне панели управления.
title: Регистрация элементов панели управления
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156690"
---
# <a name="registering-control-panel-items"></a><span data-ttu-id="db9f0-103">Регистрация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="db9f0-103">Registering Control Panel Items</span></span>

<span data-ttu-id="db9f0-104">Элементы панели управления должны быть зарегистрированы, чтобы они отображались в окне панели управления.</span><span class="sxs-lookup"><span data-stu-id="db9f0-104">Control Panel items must be registered in order to appear in the Control Panel window.</span></span> <span data-ttu-id="db9f0-105">Если элемент панели управления реализуется как часть exe-файла, то он регистрируется как объект команды.</span><span class="sxs-lookup"><span data-stu-id="db9f0-105">If the Control Panel item is implemented as part of a .exe file then it is registered as a command object.</span></span> <span data-ttu-id="db9f0-106">Регистрация различается, если элемент реализован как DLL-файл, который экспортирует функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) .</span><span class="sxs-lookup"><span data-stu-id="db9f0-106">Registration differs if the item is implemented as a .dll file that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function.</span></span>

<span data-ttu-id="db9f0-107">Конкретные требования обсуждаются в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="db9f0-107">Specific requirements are discussed in these topics:</span></span>

-   [<span data-ttu-id="db9f0-108">Регистрация исполняемых элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="db9f0-108">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="db9f0-109">Регистрация элементов панели управления DLL</span><span class="sxs-lookup"><span data-stu-id="db9f0-109">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a><span data-ttu-id="db9f0-110">См. также</span><span class="sxs-lookup"><span data-stu-id="db9f0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db9f0-111">Элементы панели управления</span><span class="sxs-lookup"><span data-stu-id="db9f0-111">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="db9f0-112">Руководство по работе пользователей</span><span class="sxs-lookup"><span data-stu-id="db9f0-112">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="db9f0-113">Использование Кплапплет</span><span class="sxs-lookup"><span data-stu-id="db9f0-113">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="db9f0-114">Обработка сообщений в панели управления</span><span class="sxs-lookup"><span data-stu-id="db9f0-114">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="db9f0-115">Исполнение элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="db9f0-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="db9f0-116">Расширение элементов панели управления "система"</span><span class="sxs-lookup"><span data-stu-id="db9f0-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="db9f0-117">Назначение категорий панели управления</span><span class="sxs-lookup"><span data-stu-id="db9f0-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="db9f0-118">Создание ссылок на задачи с возможностью поиска для элемента панели управления</span><span class="sxs-lookup"><span data-stu-id="db9f0-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="db9f0-119">Доступ к панели управления в защищенном режиме в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db9f0-119">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
