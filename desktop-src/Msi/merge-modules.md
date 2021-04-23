---
description: Модули слияния предоставляют стандартный метод, с помощью которого разработчики предоставляют приложениям общие установщик Windows и логику установки.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Модули слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272608"
---
# <a name="merge-modules"></a><span data-ttu-id="73777-103">Модули слияния</span><span class="sxs-lookup"><span data-stu-id="73777-103">Merge Modules</span></span>

<span data-ttu-id="73777-104">Модули слияния предоставляют стандартный метод, с помощью которого разработчики предоставляют приложениям [*общие установщик Windows и*](c-gly.md) логику установки.</span><span class="sxs-lookup"><span data-stu-id="73777-104">Merge modules provide a standard method by which developers deliver shared Windows Installer [*components*](c-gly.md) and setup logic to their applications.</span></span> <span data-ttu-id="73777-105">Модули слияния используются для предоставления общего кода, файлов, ресурсов, записей реестра и логики установки в приложениях в виде одного составного файла.</span><span class="sxs-lookup"><span data-stu-id="73777-105">Merge modules are used to deliver shared code, files, resources, registry entries, and setup logic to applications as a single compound file.</span></span> <span data-ttu-id="73777-106">Разработчики, разработав новые модули слияния или использующие существующие модули слияния, должны следовать стандарту, описанному в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="73777-106">Developers authoring new merge modules or using existing merge modules should follow the standard outlined in this section.</span></span>

<span data-ttu-id="73777-107">Модуль слияния похож на структуру для упрощенного [*файла установщик Windows. msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="73777-107">A merge module is similar in structure to a simplified Windows Installer [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="73777-108">Однако модуль слияния не может быть установлен отдельно, его необходимо объединить с установочным пакетом с помощью средства слияния.</span><span class="sxs-lookup"><span data-stu-id="73777-108">However, a merge module cannot be installed alone, it must be merged into an installation package using a merge tool.</span></span> <span data-ttu-id="73777-109">Разработчики, желающие использовать модули слияния, должны получить один из свободно распределенных средств слияния, таких как Mergemod.dll, или приобрести средство слияния от независимого поставщика программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="73777-109">Developers wanting to use merge modules must obtain one of the freely distributed merge tools, such as Mergemod.dll, or purchase a merge tool from an independent software vendor.</span></span> <span data-ttu-id="73777-110">Разработчики могут создавать новые модули слияния с помощью многих тех же программных средств, которые используются для создания пакета установки установщик Windows, например редактора таблиц базы данных Orca, поставляемого с пакетом SDK для установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="73777-110">Developers can create new merge modules by using many of the same software tools used to create a Windows Installer installation package, such as the database table editor Orca provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="73777-111">При слиянии модуля слияния в MSI-файл приложения вся информация и ресурсы, необходимые для установки компонентов, поставляемых модулем слияния, включаются в MSI-файл приложения.</span><span class="sxs-lookup"><span data-stu-id="73777-111">When a merge module is merged into the .msi file of an application, all the information and resources required to install the components delivered by the merge module are incorporated into the application's .msi file.</span></span> <span data-ttu-id="73777-112">Модуль слияния больше не требуется для установки этих компонентов, и модуль слияния не должен быть доступен пользователю.</span><span class="sxs-lookup"><span data-stu-id="73777-112">The merge module is then no longer required to install these components and the merge module does not need to be accessible to a user.</span></span> <span data-ttu-id="73777-113">Поскольку все сведения, необходимые для установки компонентов, доставляются в виде одного файла, использование модулей слияния может устранить многие экземпляры конфликтов версий, отсутствующие записи реестра и неправильно установленные файлы.</span><span class="sxs-lookup"><span data-stu-id="73777-113">Because all the information needed to install the components is delivered as a single file, the use of merge modules can eliminate many instances of version conflicts, missing registry entries, and improperly installed files.</span></span>

<span data-ttu-id="73777-114">Дополнительные сведения о модулях слияния см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="73777-114">For more information about merge modules, see:</span></span>

-   [<span data-ttu-id="73777-115">О модулях слияния</span><span class="sxs-lookup"><span data-stu-id="73777-115">About Merge Modules</span></span>](about-merge-modules.md)
-   [<span data-ttu-id="73777-116">Использование модулей слияния</span><span class="sxs-lookup"><span data-stu-id="73777-116">Using Merge Modules</span></span>](using-merge-modules.md)
-   [<span data-ttu-id="73777-117">Ссылка на модуль слияния</span><span class="sxs-lookup"><span data-stu-id="73777-117">Merge Module Reference</span></span>](merge-module-reference.md)

 

 



