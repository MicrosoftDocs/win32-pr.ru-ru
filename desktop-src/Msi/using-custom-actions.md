---
description: В следующих разделах описывается использование настраиваемых действий.
ms.assetid: dd2a0681-f50d-4232-bdcc-8aee6bb121a1
title: Использование настраиваемых действий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1937adbf64b94667fc3e7c44d82843b561dfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263427"
---
# <a name="using-custom-actions"></a><span data-ttu-id="2086c-103">Использование настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="2086c-103">Using Custom Actions</span></span>

<span data-ttu-id="2086c-104">В следующих разделах описывается использование настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="2086c-104">The following sections describe using custom actions.</span></span>

-   [<span data-ttu-id="2086c-105">Вызов настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="2086c-105">Invoking Custom Actions</span></span>](invoking-custom-actions.md)
-   [<span data-ttu-id="2086c-106">Виртуализация настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="2086c-106">Sequencing Custom Actions</span></span>](sequencing-custom-actions.md)
-   [<span data-ttu-id="2086c-107">Получение сведений о контексте для отложенных настраиваемых действий выполнения</span><span class="sxs-lookup"><span data-stu-id="2086c-107">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
-   [<span data-ttu-id="2086c-108">Добавление настраиваемых действий в ProgressBar</span><span class="sxs-lookup"><span data-stu-id="2086c-108">Adding Custom Actions to the ProgressBar</span></span>](adding-custom-actions-to-the-progressbar.md)
-   [<span data-ttu-id="2086c-109">Отладка настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="2086c-109">Debugging Custom Actions</span></span>](debugging-custom-actions.md)
-   [<span data-ttu-id="2086c-110">Определение уровня пользовательского интерфейса на основе настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="2086c-110">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
-   [<span data-ttu-id="2086c-111">Удаление настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="2086c-111">Uninstalling Custom Actions</span></span>](uninstalling-custom-actions.md)
-   [<span data-ttu-id="2086c-112">Возвращение сообщений об ошибках из настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="2086c-112">Returning Error Messages from Custom Actions</span></span>](returning-error-messages-from-custom-actions.md)
-   [<span data-ttu-id="2086c-113">Настройка точки восстановления из настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="2086c-113">Setting a restore point from a Custom Action</span></span>](setting-a-restore-point-from-a-custom-action.md)
-   [<span data-ttu-id="2086c-114">Функции, не предназначенные для использования в настраиваемых действиях</span><span class="sxs-lookup"><span data-stu-id="2086c-114">Functions Not for Use in Custom Actions</span></span>](functions-not-for-use-in-custom-actions.md)
-   [<span data-ttu-id="2086c-115">Изменение состояния системы с помощью настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="2086c-115">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)
-   [<span data-ttu-id="2086c-116">Доступ к текущему сеансу установщика из пользовательского действия</span><span class="sxs-lookup"><span data-stu-id="2086c-116">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
-   [<span data-ttu-id="2086c-117">Доступ к базе данных или сеансу из настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="2086c-117">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
-   [<span data-ttu-id="2086c-118">Использование настраиваемого действия для запуска установленного файла в конце установки</span><span class="sxs-lookup"><span data-stu-id="2086c-118">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
-   [<span data-ttu-id="2086c-119">Использование настраиваемого действия для создания учетных записей пользователей на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="2086c-119">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
-   [<span data-ttu-id="2086c-120">Использование 64-разрядных настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="2086c-120">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)

<span data-ttu-id="2086c-121">Общие сведения о настраиваемых действиях см. в разделе [о настраиваемых действиях](about-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="2086c-121">For an overview of custom actions, see [About Custom Actions](about-custom-actions.md).</span></span>

<span data-ttu-id="2086c-122">Дополнительные сведения о кодировании настраиваемых действий в [таблицу CustomAction](customaction-table.md)см. в разделе [ссылка на настраиваемое действие](custom-action-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2086c-122">For more information about encoding custom actions into the [CustomAction table](customaction-table.md), see [Custom Action Reference](custom-action-reference.md).</span></span>

<span data-ttu-id="2086c-123">Сводные сведения о пользовательских действиях и их кодировании в таблице CustomAction см. в разделе [сводный список всех типов настраиваемых действий](summary-list-of-all-custom-action-types.md).</span><span class="sxs-lookup"><span data-stu-id="2086c-123">For a summary of custom actions and how they are encoded into the CustomAction table, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span>

 

 



