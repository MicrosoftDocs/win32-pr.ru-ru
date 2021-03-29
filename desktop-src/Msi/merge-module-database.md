---
description: База данных модуля слияния содержит все свойства установки и логику установки для модуля.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: База данных модуля слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347155"
---
# <a name="merge-module-database"></a><span data-ttu-id="3a43a-103">База данных модуля слияния</span><span class="sxs-lookup"><span data-stu-id="3a43a-103">Merge Module Database</span></span>

<span data-ttu-id="3a43a-104">База данных модуля слияния содержит все свойства установки и логику установки для модуля.</span><span class="sxs-lookup"><span data-stu-id="3a43a-104">The database of a merge module contains all the installation properties and setup logic for the module.</span></span> <span data-ttu-id="3a43a-105">По сути, это упрощенная [база данных установщика](installer-database.md) или MSI-файл.</span><span class="sxs-lookup"><span data-stu-id="3a43a-105">It is essentially a simplified [installer database](installer-database.md) or .msi file.</span></span> <span data-ttu-id="3a43a-106">Файлы базы данных стандартных модулей слияния обозначаются расширением MSM.</span><span class="sxs-lookup"><span data-stu-id="3a43a-106">Standard merge module database files are indicated by an .msm extension.</span></span> <span data-ttu-id="3a43a-107">Список всех таблиц базы данных, которые могут существовать в модулях слияния, см. в разделе [таблицы базы данных модуля слияния](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3a43a-107">For a list of all database tables that can exist in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span> <span data-ttu-id="3a43a-108">В базе данных каждого файла. MSM необходимы следующие таблицы:</span><span class="sxs-lookup"><span data-stu-id="3a43a-108">The following tables are required in the database of every .msm file:</span></span>

[<span data-ttu-id="3a43a-109">Компонент</span><span class="sxs-lookup"><span data-stu-id="3a43a-109">Component</span></span>](component-table.md)

[<span data-ttu-id="3a43a-110">Каталог</span><span class="sxs-lookup"><span data-stu-id="3a43a-110">Directory</span></span>](directory-table.md)

[<span data-ttu-id="3a43a-111">феатурекомпонентс</span><span class="sxs-lookup"><span data-stu-id="3a43a-111">FeatureComponents</span></span>](featurecomponents-table.md)

[<span data-ttu-id="3a43a-112">Файл</span><span class="sxs-lookup"><span data-stu-id="3a43a-112">File</span></span>](file-table.md)

[<span data-ttu-id="3a43a-113">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="3a43a-113">ModuleSignature</span></span>](modulesignature-table.md)

[<span data-ttu-id="3a43a-114">модулекомпонентс</span><span class="sxs-lookup"><span data-stu-id="3a43a-114">ModuleComponents</span></span>](modulecomponents-table.md)

<span data-ttu-id="3a43a-115">Обратите внимание, что таблицы Component, Directory, Феатурекомпонентс и File также имеются во всех файлах MSI.</span><span class="sxs-lookup"><span data-stu-id="3a43a-115">Note that the Component, Directory, FeatureComponents, and File tables are also present in all .msi files.</span></span> <span data-ttu-id="3a43a-116">База данных модуля слияния не содержит [таблицу функций](feature-table.md) , поэтому MSM-файл невозможно установить отдельно.</span><span class="sxs-lookup"><span data-stu-id="3a43a-116">A merge module database does not contain a [Feature table](feature-table.md) and so the .msm file cannot be installed alone.</span></span> <span data-ttu-id="3a43a-117">Чтобы установить модуль слияния, сначала необходимо выполнить слияние с помощью средства слияния в MSI-файл.</span><span class="sxs-lookup"><span data-stu-id="3a43a-117">To install a merge module, it must first be merged by using a merge tool into an .msi file.</span></span>

<span data-ttu-id="3a43a-118">[Таблица ModuleSignature](modulesignature-table.md) имеется только в MSI-файлах, которые были объединены по крайней мере с одним файлом MSM.</span><span class="sxs-lookup"><span data-stu-id="3a43a-118">The [ModuleSignature Table](modulesignature-table.md) is only present in .msi files that has been merged with at least one .msm file.</span></span> <span data-ttu-id="3a43a-119">Если эта таблица содержится в MSI-файле, она содержит по одной записи для каждого модуля слияния, который ранее был объединен с базой данных установки.</span><span class="sxs-lookup"><span data-stu-id="3a43a-119">If this table is present in an .msi file, it contains one record for each merge module that has been previously merged into the installation database.</span></span>

<span data-ttu-id="3a43a-120">Модули слияния могут содержать необязательные таблицы последовательностей установочного модуля.</span><span class="sxs-lookup"><span data-stu-id="3a43a-120">Merge modules may contain optional MergeModule Sequence tables.</span></span> <span data-ttu-id="3a43a-121">Эти таблицы происходят только в файлах MSM.</span><span class="sxs-lookup"><span data-stu-id="3a43a-121">These tables occur only in .msm files.</span></span> <span data-ttu-id="3a43a-122">Когда файлы MSM объединяются в MSI, эти таблицы изменяют [*таблицы последовательности*](s-gly.md) действий MSI файла.</span><span class="sxs-lookup"><span data-stu-id="3a43a-122">When the .msm files are merged into an .msi file, these tables modify the action [*sequence tables*](s-gly.md) of the .msi file.</span></span>

<span data-ttu-id="3a43a-123">Модули слияния могут содержать пользовательские таблицы.</span><span class="sxs-lookup"><span data-stu-id="3a43a-123">Merge modules may contain custom tables.</span></span> <span data-ttu-id="3a43a-124">Эти таблицы используются [пользовательскими действиями](custom-actions.md) , определенными в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="3a43a-124">These tables are used by [custom actions](custom-actions.md) defined in the merge module.</span></span>

<span data-ttu-id="3a43a-125">Для модулей слияния редко требуются таблицы пользовательских интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="3a43a-125">Merge modules rarely require user interface tables.</span></span> <span data-ttu-id="3a43a-126">Эти таблицы должны быть представлены только в редких случаях, когда модулю слияния требуются входные данные пользователя во время установки.</span><span class="sxs-lookup"><span data-stu-id="3a43a-126">These tables need to be present only in rare cases where the merge module requires input from the user during installation.</span></span> <span data-ttu-id="3a43a-127">Дополнительные сведения см. [в разделе Создание пользовательских интерфейсов в модулях слияния](authoring-user-interfaces-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="3a43a-127">For more information, see [Authoring User Interfaces in Merge Modules](authoring-user-interfaces-in-merge-modules.md).</span></span>

 

 



