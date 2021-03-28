---
description: Элементы панели управления — это библиотеки DLL или исполняемые файлы (exe), позволяющие пользователям настраивать среду Windows. Доступ к ним обычно осуществляется щелчком значка на панели управления.
title: Реализация элементов панели управления
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2e61cbc0-fbb5-4680-8123-f8ffdcf98210
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 310d01f07d40cef69c6be30231bbf4780a1d8838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984344"
---
# <a name="implementing-control-panel-items"></a><span data-ttu-id="42419-104">Реализация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="42419-104">Implementing Control Panel Items</span></span>

<span data-ttu-id="42419-105">Элементы панели управления — это библиотеки DLL или исполняемые файлы (exe), позволяющие пользователям настраивать среду Windows.</span><span class="sxs-lookup"><span data-stu-id="42419-105">Control Panel items are DLLs or executable (.exe) files that let users configure the environment of Windows.</span></span> <span data-ttu-id="42419-106">Доступ к ним обычно осуществляется щелчком значка на панели управления.</span><span class="sxs-lookup"><span data-stu-id="42419-106">They are typically accessed by clicking an icon in the Control Panel.</span></span>

<span data-ttu-id="42419-107">В этом разделе описываются элементы панели управления и объясняется, как создавать и регистрировать их, чтобы они правильно отображались на панели управления.</span><span class="sxs-lookup"><span data-stu-id="42419-107">This section describes Control Panel items and explains how to create and register them so that they appear appropriately in the Control Panel.</span></span> <span data-ttu-id="42419-108">В Windows Vista содержатся сведения о том, как добавлять ссылки на задачи, которые отображаются в элементе панели управления и в результатах поиска панели управления.</span><span class="sxs-lookup"><span data-stu-id="42419-108">For Windows Vista, information is included that tells you how to add task links that appear under the Control Panel item and in Control Panel search results.</span></span>

-   [<span data-ttu-id="42419-109">Руководство по работе пользователей</span><span class="sxs-lookup"><span data-stu-id="42419-109">User Experience Guidelines</span></span>](user-experience-guidelines.md)
-   [<span data-ttu-id="42419-110">Регистрация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="42419-110">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
-   [<span data-ttu-id="42419-111">Регистрация исполняемых элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="42419-111">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="42419-112">Регистрация элементов панели управления DLL</span><span class="sxs-lookup"><span data-stu-id="42419-112">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
-   [<span data-ttu-id="42419-113">Использование Кплапплет</span><span class="sxs-lookup"><span data-stu-id="42419-113">Using CPLApplet</span></span>](using-cplapplet.md)
-   [<span data-ttu-id="42419-114">Обработка сообщений в панели управления</span><span class="sxs-lookup"><span data-stu-id="42419-114">Control Panel Message Processing</span></span>](message-processing.md)
-   [<span data-ttu-id="42419-115">Исполнение элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="42419-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
-   [<span data-ttu-id="42419-116">Расширение элементов панели управления "система"</span><span class="sxs-lookup"><span data-stu-id="42419-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
-   [<span data-ttu-id="42419-117">Назначение категорий панели управления</span><span class="sxs-lookup"><span data-stu-id="42419-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
-   [<span data-ttu-id="42419-118">Создание ссылок на задачи с возможностью поиска для элемента панели управления</span><span class="sxs-lookup"><span data-stu-id="42419-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
-   [<span data-ttu-id="42419-119">Доступ к панели управления в защищенном режиме</span><span class="sxs-lookup"><span data-stu-id="42419-119">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
-   [<span data-ttu-id="42419-120">Канонические имена элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="42419-120">Canonical Names of Control Panel Items</span></span>](controlpanel-canonical-names.md)

 

 



