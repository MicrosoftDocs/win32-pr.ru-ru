---
title: Расширение пользовательского интерфейса для объектов каталога
description: В Microsoft Windows 2000 и более поздних версиях оснастки консоли управления (MMC), такие как Active Directory пользователи и компьютеры, доступны для администрирования домен Active Directory служб.
ms.assetid: 758ec25d-42ab-46ba-aa58-416d7ac8fd68
ms.tgt_platform: multiple
keywords:
- Active Directory, использование, расширение пользовательского интерфейса
- объекты Active Directory, расширение пользовательского интерфейса для объектов каталога
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d635132a26e80a63fddb35f779211308779f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773157"
---
# <a name="extending-the-user-interface-for-directory-objects"></a><span data-ttu-id="b4899-105">Расширение пользовательского интерфейса для объектов каталога</span><span class="sxs-lookup"><span data-stu-id="b4899-105">Extending the User Interface for Directory Objects</span></span>

<span data-ttu-id="b4899-106">В Microsoft Windows 2000 и более поздних версиях оснастки консоли управления (MMC), такие как Active Directory пользователи и компьютеры, доступны для администрирования домен Active Directory служб.</span><span class="sxs-lookup"><span data-stu-id="b4899-106">With Microsoft Windows 2000 and later, Microsoft Management Console (MMC) snap-ins, such as the Active Directory Users and Computers snap-in, for administration of Active Directory Domain Services, are available.</span></span> <span data-ttu-id="b4899-107">Кроме того, оболочка Windows 2000 включает пользовательские интерфейсы (UI) для поиска объектов, которые находятся в каталоге, а также для чтения и записи свойств.</span><span class="sxs-lookup"><span data-stu-id="b4899-107">In addition, the Windows 2000 shell includes user interfaces (UIs) for finding objects that reside in the directory and reading and writing properties.</span></span> <span data-ttu-id="b4899-108">В этом разделе объясняется, как расширить пользовательский интерфейс для просмотра объектов служб домен Active Directory Services и управления ими в оболочке Windows и Active Directory административных оснасток. В этом разделе также описывается, что необходимо для развертывания расширений пользовательского интерфейса на настольных компьютерах пользователей.</span><span class="sxs-lookup"><span data-stu-id="b4899-108">This section explains how to extend the UI for viewing and managing Active Directory Domain Services objects in the Windows shell and Active Directory administrative snap-ins. This section also covers what is required to deploy the UI extensions to the user's desktops.</span></span>

<span data-ttu-id="b4899-109">В частности, в этом разделе рассматриваются следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="b4899-109">Specifically, this section discusses the following:</span></span>

-   [<span data-ttu-id="b4899-110">Сведения о Active Directory пользовательских интерфейсах</span><span class="sxs-lookup"><span data-stu-id="b4899-110">About Active Directory User Interfaces</span></span>](about-the-user-interfaces-of-active-directory-domain-services.md)
-   [<span data-ttu-id="b4899-111">Описатели экрана</span><span class="sxs-lookup"><span data-stu-id="b4899-111">Display Specifiers</span></span>](display-specifiers.md)
-   [<span data-ttu-id="b4899-112">Отображаемые имена классов и атрибутов</span><span class="sxs-lookup"><span data-stu-id="b4899-112">Class and Attribute Display Names</span></span>](class-and-attribute-display-names.md)
-   [<span data-ttu-id="b4899-113">Значки классов</span><span class="sxs-lookup"><span data-stu-id="b4899-113">Class Icons</span></span>](class-icons.md)
-   [<span data-ttu-id="b4899-114">Просмотр контейнеров в виде конечных узлов</span><span class="sxs-lookup"><span data-stu-id="b4899-114">Viewing Containers as Leaf Nodes</span></span>](viewing-containers-as-leaf-nodes.md)
-   [<span data-ttu-id="b4899-115">Изменение существующих пользовательских интерфейсов</span><span class="sxs-lookup"><span data-stu-id="b4899-115">Modifying Existing User Interfaces</span></span>](modifying-existing-user-interfaces.md)
-   [<span data-ttu-id="b4899-116">Расширение пользовательского интерфейса для новых классов объектов</span><span class="sxs-lookup"><span data-stu-id="b4899-116">User Interface Extension for New Object Classes</span></span>](user-interface-extension-for-new-object-classes.md)
-   [<span data-ttu-id="b4899-117">Страницы свойств для использования с описателем экрана</span><span class="sxs-lookup"><span data-stu-id="b4899-117">Property Pages for Use with Display Specifiers</span></span>](property-pages-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="b4899-118">Контекстные меню для использования с описателем экрана</span><span class="sxs-lookup"><span data-stu-id="b4899-118">Context Menus for Use with Display Specifiers</span></span>](context-menus-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="b4899-119">Мастера создания объектов</span><span class="sxs-lookup"><span data-stu-id="b4899-119">Object Creation Wizards</span></span>](object-creation-wizards.md)
-   [<span data-ttu-id="b4899-120">Использование стандартных диалоговых окон для обработки объектов в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="b4899-120">Using Standard Dialog Boxes for Handling Objects in Active Directory Domain Services</span></span>](using-standard-dialog-boxes-to-handle-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="b4899-121">Административные обработчики уведомлений</span><span class="sxs-lookup"><span data-stu-id="b4899-121">Administrative Notification Handlers</span></span>](administrative-notification-handlers.md)
-   [<span data-ttu-id="b4899-122">Распространение компонентов пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="b4899-122">Distributing User Interface Components</span></span>](distributing-user-interface-components.md)
-   [<span data-ttu-id="b4899-123">Как приложения должны использовать описатели отображения</span><span class="sxs-lookup"><span data-stu-id="b4899-123">How Applications Should Use Display Specifiers</span></span>](how-applications-should-use-display-specifiers.md)
-   [<span data-ttu-id="b4899-124">Отладка расширения Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4899-124">Debugging an Active Directory Extension</span></span>](debugging-an-active-directory-extension.md)

 

 




