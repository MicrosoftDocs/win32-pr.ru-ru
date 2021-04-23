---
description: В этом разделе обсуждается создание контекстных меню (контекстных) и реализация обработчиков контекстного меню (глагола).
title: Контекстное меню (контекст) и обработчики контекстного меню
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262916"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a><span data-ttu-id="a298b-103">Контекстное меню (контекст) и обработчики контекстного меню</span><span class="sxs-lookup"><span data-stu-id="a298b-103">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>

<span data-ttu-id="a298b-104">В этом разделе обсуждается создание контекстных меню (контекстных) и реализация обработчиков контекстного меню (глагола).</span><span class="sxs-lookup"><span data-stu-id="a298b-104">This section discusses the creation of shortcut (context) menus, and the implementation of shortcut menu (verb) handlers.</span></span>

<span data-ttu-id="a298b-105">Этот раздел по типам файлов и сопоставлению файлов организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a298b-105">This section on file types and file associations is organized as follows:</span></span>

-   [<span data-ttu-id="a298b-106">Команды и сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="a298b-106">Verbs and File Associations</span></span>](fa-verbs.md)
-   [<span data-ttu-id="a298b-107">Выбор метода статического или динамического контекстного меню</span><span class="sxs-lookup"><span data-stu-id="a298b-107">Choosing a Static or Dynamic Shortcut Menu Method</span></span>](shortcut-choose-method.md)
-   [<span data-ttu-id="a298b-108">Рекомендации по работе с обработчиками контекстного меню и несколькими командами</span><span class="sxs-lookup"><span data-stu-id="a298b-108">Best Practices for Shortcut Menu Handlers and Multiple Verbs</span></span>](verbs-best-practices.md)
-   [<span data-ttu-id="a298b-109">Создание обработчиков контекстного меню</span><span class="sxs-lookup"><span data-stu-id="a298b-109">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
-   [<span data-ttu-id="a298b-110">Создание статических каскадных меню</span><span class="sxs-lookup"><span data-stu-id="a298b-110">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
-   [<span data-ttu-id="a298b-111">Как подавлять и контролировать видимость команд</span><span class="sxs-lookup"><span data-stu-id="a298b-111">How to Suppress and Control Verb Visibility</span></span>](how-to-suppress-and-control-visibility.md)
-   [<span data-ttu-id="a298b-112">Как применить модель выбора глагола</span><span class="sxs-lookup"><span data-stu-id="a298b-112">How to Employ the Verb Selection Model</span></span>](how-to-employ-the-verb-selection-model.md)
-   [<span data-ttu-id="a298b-113">Использование атрибутов элементов</span><span class="sxs-lookup"><span data-stu-id="a298b-113">How to Use Item Attributes</span></span>](how-to-use-item-attributes.md)
-   [<span data-ttu-id="a298b-114">Реализация пользовательских команд для папок с помощью Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="a298b-114">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [<span data-ttu-id="a298b-115">Настройка контекстного меню с помощью динамических команд</span><span class="sxs-lookup"><span data-stu-id="a298b-115">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
-   [<span data-ttu-id="a298b-116">Реализация интерфейса IContextMenu</span><span class="sxs-lookup"><span data-stu-id="a298b-116">How to Implement the IContextMenu Interface</span></span>](how-to-implement-the-icontextmenu-interface.md)
-   [<span data-ttu-id="a298b-117">Справочник по контекстному меню</span><span class="sxs-lookup"><span data-stu-id="a298b-117">Shortcut Menu Reference</span></span>](context-menu-reference.md)

## <a name="additional-resources"></a><span data-ttu-id="a298b-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a298b-118">Additional Resources</span></span>

<span data-ttu-id="a298b-119">Дополнительные сведения о концептуальном плане см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a298b-119">For related conceptual background, see the following topics:</span></span>

-   <span data-ttu-id="a298b-120">[Общие сведения о сопоставлениях файлов](fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="a298b-120">[Introduction to File Associations](fa-intro.md).</span></span>
-   <span data-ttu-id="a298b-121">Сведения о расширении оболочки с помощью обработчиков типов файлов см. в разделе [Создание обработчиков расширений оболочки](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a298b-121">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>
-   <span data-ttu-id="a298b-122">Сведения о создании хранилища данных оболочки см. в разделе [реализация базовых интерфейсов объекта папки](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="a298b-122">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

<span data-ttu-id="a298b-123">Связанные справочные документации по см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a298b-123">For related reference documenation, see the following topics:</span></span>

-   <span data-ttu-id="a298b-124">Инструкции по выполнению команды для элемента оболочки см. в описании метода [**инвокеверб**](folderitem-invokeverb.md) .</span><span class="sxs-lookup"><span data-stu-id="a298b-124">To execute a verb on a Shell item, see the [**InvokeVerb**](folderitem-invokeverb.md) method.</span></span>
-   <span data-ttu-id="a298b-125">Чтобы получить коллекцию команд, которые могут быть выполнены в элементе оболочки, см. метод [**Verbs**](folderitem-verbs.md) .</span><span class="sxs-lookup"><span data-stu-id="a298b-125">To retrieve a collection of verbs that can be executed on a Shell item, see the [**Verbs**](folderitem-verbs.md) method.</span></span>
-   <span data-ttu-id="a298b-126">Сведения о выполнении операции с указанным файлом см. в разделе функции [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="a298b-126">To perform an operation on a specified file, see either the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) functions.</span></span>

 

 



