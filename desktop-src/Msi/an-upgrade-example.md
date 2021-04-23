---
description: В следующих разделах представлен пример создания пакета обновления для приложения, описанного в примере установки.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Пример обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662951"
---
# <a name="an-upgrade-example"></a><span data-ttu-id="9b790-103">Пример обновления</span><span class="sxs-lookup"><span data-stu-id="9b790-103">An Upgrade Example</span></span>

<span data-ttu-id="9b790-104">В следующих разделах представлен пример создания пакета обновления для приложения, описанного в [примере установки](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="9b790-104">The following sections present an example of authoring an upgrade package for the application described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="9b790-105">Пример минимального пользовательского интерфейса для этого примера приведен в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md) в качестве Uisample.msi файлов.</span><span class="sxs-lookup"><span data-stu-id="9b790-105">An example of a minimal user interface for this sample is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) as the file Uisample.msi.</span></span> <span data-ttu-id="9b790-106">Если у вас есть пакет SDK, у вас есть доступ ко всем средствам и данным, необходимым для воспроизведения примера установочного пакета, пользовательского интерфейса и примера пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="9b790-106">If you have the SDK, you have access to all the tools and data necessary to reproduce the sample installation package, user interface, and sample upgrade package.</span></span>

<span data-ttu-id="9b790-107">В этом примере показано, как создать пакет установщик Windows, который обновляет гипотетический продукт MNP2000 до нового продукта с именем MNP2001.</span><span class="sxs-lookup"><span data-stu-id="9b790-107">This example illustrates how to create a Windows Installer package that upgrades the hypothetical product MNP2000 to a new product called MNP2001.</span></span> <span data-ttu-id="9b790-108">В примере пакета обновления применяется крупное обновление продукта, требующее изменения кода продукта.</span><span class="sxs-lookup"><span data-stu-id="9b790-108">The example upgrade package applies a major upgrade to the product which requires changing the product code.</span></span> <span data-ttu-id="9b790-109">Дополнительные сведения о основных обновлениях см. в разделе [основные обновления](major-upgrades.md) в разделе об [исправлениях и обновлениях](patching-and-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="9b790-109">For more information about major upgrades, see the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section.</span></span>

<span data-ttu-id="9b790-110">Образец пакета обновления имеет следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="9b790-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="9b790-111">Чтобы вы могли получить это обновление до MNP2001, пользователь должен был установить ранее 1,0-1,4 (включительно) версии английского языка MNP2000 с помощью установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="9b790-111">To qualify to receive this upgrade to MNP2001, a user must have previously installed the 1.0 to 1.4 (inclusive) versions of English language MNP2000 using Windows Installer.</span></span>
-   <span data-ttu-id="9b790-112">Когда пользователь пытается установить пакет обновления, функция обновления установщик Windows выполняет поиск всех продуктов, соответствующих обновлению, на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b790-112">When a user attempts to install the upgrade package, the upgrade functionality of Windows Installer searches the user's computer for any products that qualify for the upgrade.</span></span>
-   <span data-ttu-id="9b790-113">Установщик Windows переносит все настройки компонентов исходного продукта в обновленный продукт.</span><span class="sxs-lookup"><span data-stu-id="9b790-113">Windows Installer migrates all the of the original product's feature settings to the upgraded product.</span></span>
-   <span data-ttu-id="9b790-114">Установщик удаляет все устаревшие компоненты с компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b790-114">The installer removes all obsolete features from the user's computer.</span></span>
-   <span data-ttu-id="9b790-115">Установщик устанавливает все новые компоненты, относящиеся к обновлению.</span><span class="sxs-lookup"><span data-stu-id="9b790-115">The installer installs all new features belonging to the upgrade.</span></span>
-   <span data-ttu-id="9b790-116">Удаление пакета обновления удаляет продукт с компьютера пользователя и не восстанавливает более раннюю версию продукта.</span><span class="sxs-lookup"><span data-stu-id="9b790-116">An uninstall of the upgrade package removes the product from the user's computer, and does not restore the earlier version of the product.</span></span>
-   <span data-ttu-id="9b790-117">В примере обновления обновляются ярлыки для новых файлов и компонентов.</span><span class="sxs-lookup"><span data-stu-id="9b790-117">The sample upgrade updates shortcuts to new files and features.</span></span>

    [<span data-ttu-id="9b790-118">Планирование основного обновления</span><span class="sxs-lookup"><span data-stu-id="9b790-118">Planning a Major Upgrade</span></span>](planning-a-major-upgrade.md)

    [<span data-ttu-id="9b790-119">Импорт исходной базы данных установки</span><span class="sxs-lookup"><span data-stu-id="9b790-119">Importing Original Installation Database</span></span>](importing-original-installation-database.md)

    [<span data-ttu-id="9b790-120">Обновление структуры каталогов для обновления</span><span class="sxs-lookup"><span data-stu-id="9b790-120">Updating Directory Structure for an Upgrade</span></span>](updating-directory-structure-for-an-upgrade.md)

    [<span data-ttu-id="9b790-121">Обновление файлов и атрибутов файлов для обновления</span><span class="sxs-lookup"><span data-stu-id="9b790-121">Updating Files and File Attributes for an Upgrade</span></span>](updating-files-and-file-attributes-for-an-upgrade.md)

    [<span data-ttu-id="9b790-122">Обновление компонентов для обновления</span><span class="sxs-lookup"><span data-stu-id="9b790-122">Updating Components for an Upgrade</span></span>](updating-components-for-an-upgrade.md)

    [<span data-ttu-id="9b790-123">Обновление компонентов для обновления</span><span class="sxs-lookup"><span data-stu-id="9b790-123">Updating Features for an Upgrade</span></span>](updating-features-for-an-upgrade.md)

    [<span data-ttu-id="9b790-124">Обновление ярлыков для обновления</span><span class="sxs-lookup"><span data-stu-id="9b790-124">Updating Shortcuts for an Upgrade</span></span>](updating-shortcuts-for-an-upgrade.md)

    [<span data-ttu-id="9b790-125">Обновление таблицы обновления для обновления</span><span class="sxs-lookup"><span data-stu-id="9b790-125">Updating Upgrade Table for an Upgrade</span></span>](updating-upgrade-table-for-an-upgrade.md)

    [<span data-ttu-id="9b790-126">Обновление свойств для обновления</span><span class="sxs-lookup"><span data-stu-id="9b790-126">Updating Properties for an Upgrade</span></span>](updating-properties-for-an-upgrade.md)

    [<span data-ttu-id="9b790-127">Обновление таблиц последовательностей для обновления</span><span class="sxs-lookup"><span data-stu-id="9b790-127">Updating Sequence Tables for an Upgrade</span></span>](updating-sequence-tables-for-an-upgrade.md)

    [<span data-ttu-id="9b790-128">Обновление сводных данных для обновления</span><span class="sxs-lookup"><span data-stu-id="9b790-128">Updating Summary Information for an Upgrade</span></span>](updating-summary-information-for-an-upgrade.md)

    [<span data-ttu-id="9b790-129">Проверка обновления установки</span><span class="sxs-lookup"><span data-stu-id="9b790-129">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)

 

 



