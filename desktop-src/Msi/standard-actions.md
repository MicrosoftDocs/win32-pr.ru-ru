---
description: Действие инкапсулирует типичную функцию, выполняемую во время установки или обслуживания приложения. Установщик Windows имеет множество встроенных стандартных действий. Разработчики пакетов установки могут также создавать собственные пользовательские действия.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Стандартные действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264041"
---
# <a name="standard-actions"></a><span data-ttu-id="a255a-105">Стандартные действия</span><span class="sxs-lookup"><span data-stu-id="a255a-105">Standard Actions</span></span>

<span data-ttu-id="a255a-106">Действие инкапсулирует типичную функцию, выполняемую во время установки или обслуживания приложения.</span><span class="sxs-lookup"><span data-stu-id="a255a-106">An action encapsulates a typical function performed during the installation or maintenance of an application.</span></span> <span data-ttu-id="a255a-107">Установщик Windows имеет множество встроенных стандартных действий.</span><span class="sxs-lookup"><span data-stu-id="a255a-107">Windows Installer has many built-in standard actions.</span></span> <span data-ttu-id="a255a-108">Разработчики пакетов установки могут также создавать собственные [пользовательские действия](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="a255a-108">Developers of installation packages can also author their own [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="a255a-109">Примеры стандартных действий установщика включают следующие.</span><span class="sxs-lookup"><span data-stu-id="a255a-109">Examples of installer standard actions include:</span></span>

-   <span data-ttu-id="a255a-110">[Действие креатешорткутс](createshortcuts-action.md): управляет созданием ярлыков для файлов, установленных с текущим приложением.</span><span class="sxs-lookup"><span data-stu-id="a255a-110">[CreateShortcuts action](createshortcuts-action.md): Manages the creation of shortcuts to files installed with the current application.</span></span> <span data-ttu-id="a255a-111">Это действие использует [таблицу ярлыков](shortcut-table.md) для своих данных.</span><span class="sxs-lookup"><span data-stu-id="a255a-111">This action uses the [Shortcut table](shortcut-table.md) for its data.</span></span>
-   <span data-ttu-id="a255a-112">[Действие инсталлфилес](installfiles-action.md): копирует выбранные файлы из исходного каталога в целевой каталог.</span><span class="sxs-lookup"><span data-stu-id="a255a-112">[InstallFiles action](installfiles-action.md): Copies selected files from the source directory to the destination directory.</span></span> <span data-ttu-id="a255a-113">Это действие использует [таблицу File](file-table.md) для своих данных.</span><span class="sxs-lookup"><span data-stu-id="a255a-113">This action uses the [File table](file-table.md) for its data.</span></span>
-   <span data-ttu-id="a255a-114">[Действие вритерегистривалуес](writeregistryvalues-action.md): настраивает сведения реестра, необходимые приложению в реестре.</span><span class="sxs-lookup"><span data-stu-id="a255a-114">[WriteRegistryValues action](writeregistryvalues-action.md): Sets up registry information the application requires in the registry.</span></span> <span data-ttu-id="a255a-115">Это действие использует [таблицу реестра](registry-table.md) для своих данных.</span><span class="sxs-lookup"><span data-stu-id="a255a-115">This action uses the [Registry table](registry-table.md) for its data.</span></span>

<span data-ttu-id="a255a-116">В следующих разделах рассматриваются стандартные действия.</span><span class="sxs-lookup"><span data-stu-id="a255a-116">The following sections discuss standard actions.</span></span>

-   [<span data-ttu-id="a255a-117">О стандартных действиях</span><span class="sxs-lookup"><span data-stu-id="a255a-117">About Standard Actions</span></span>](about-standard-actions.md)
-   [<span data-ttu-id="a255a-118">Использование стандартных действий</span><span class="sxs-lookup"><span data-stu-id="a255a-118">Using Standard Actions</span></span>](using-standard-actions.md)
-   [<span data-ttu-id="a255a-119">Справочник по стандартным действиям</span><span class="sxs-lookup"><span data-stu-id="a255a-119">Standard Actions Reference</span></span>](standard-actions-reference.md)

 

 



