---
title: Восстановление системы
description: Так как компьютер используется с течением времени, точки восстановления собираются в архиве данных без вмешательства пользователя или управления им.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c5ff4aef88ec9eca591ee3c1afb1ad570689a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691224"
---
# <a name="restoring-the-system"></a><span data-ttu-id="75102-103">Восстановление системы</span><span class="sxs-lookup"><span data-stu-id="75102-103">Restoring the System</span></span>

<span data-ttu-id="75102-104">Так как компьютер используется с течением времени, точки восстановления собираются в архиве данных без вмешательства пользователя или управления им.</span><span class="sxs-lookup"><span data-stu-id="75102-104">As the computer is used over time, restore points are collected in the data archive without any management or intervention required by the user.</span></span> <span data-ttu-id="75102-105">Если пользователю когда-либо нужно восстановить систему в предыдущее состояние, доступные точки восстановления становятся видимыми пользователю через пользовательский интерфейс восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="75102-105">If the user ever needs to restore the system to a previous state, the available restore points are made visible to the user through the System Restore user interface.</span></span> <span data-ttu-id="75102-106">Пользователь может выбрать любую из этих точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="75102-106">The user can choose any of these restore points.</span></span> <span data-ttu-id="75102-107">Единственным способом доступа к этому архиву точек восстановления является Пользовательский интерфейс восстановления системы и API восстановления системы. Это позволяет защитить целостность данных и предотвратить случайные изменения, внесенные пользователем, приложениями или другими агентами.</span><span class="sxs-lookup"><span data-stu-id="75102-107">The only way to access this archive of restore points is through the System Restore user interface and the System Restore API; this is to protect data integrity and prevent accidental changes made by the user, applications, or other agents.</span></span>

<span data-ttu-id="75102-108">Для восстановления системы восстановление системы отменяет изменения файлов, внесенные в отслеживаемые файлы, повторно записывая состояние файла во время выбранной точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="75102-108">To restore a system, System Restore undoes file changes made to monitored files, recapturing the file state at the time of the selected restore point.</span></span> <span data-ttu-id="75102-109">Затем он заменяет текущий реестр на тот, который был сохранен для выбранной точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="75102-109">It then replaces the current registry with the one saved for the selected restore point.</span></span>

<span data-ttu-id="75102-110">Чтобы обеспечить требуемое поведение приложения после восстановления, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="75102-110">To ensure that your application has the desired behavior after a restore, do the following:</span></span>

-   <span data-ttu-id="75102-111">Не храните в реестре сведения, которые предотвращают доступ пользователей к личным файлам данных или приложениям при восстановлении системы.</span><span class="sxs-lookup"><span data-stu-id="75102-111">Do not store information in the registry that prevents user access to personal data files or applications on system restore.</span></span> <span data-ttu-id="75102-112">В противном случае необходимо предоставить механизм, с помощью которого пользователь может загружать и переустанавливать приложения без необходимости платить за них.</span><span class="sxs-lookup"><span data-stu-id="75102-112">Otherwise, you must provide a mechanism by which the user can download and reinstall the applications without having to pay for them again.</span></span>
-   <span data-ttu-id="75102-113">Используйте [API восстановления системы](system-restore-api.md) для создания осмысленных точек восстановления при установке и удалении.</span><span class="sxs-lookup"><span data-stu-id="75102-113">Use the [System Restore API](system-restore-api.md) to create meaningful restore points at install and uninstall.</span></span>
-   <span data-ttu-id="75102-114">В Windows XP ключевые двоичные файлы приложения, подходящие для защиты, должны использовать расширения, соответствующие используемым в Filelist.xml.</span><span class="sxs-lookup"><span data-stu-id="75102-114">In Windows XP, the key application binaries to be protected must use extensions consistent with those used in Filelist.xml.</span></span> <span data-ttu-id="75102-115">Дополнительные сведения см. в разделе [отслеживаемые расширения имен файлов](monitored-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="75102-115">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span> <span data-ttu-id="75102-116">Этот файл не используется в Windows 7 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="75102-116">This file is not used by Windows 7 and Windows Vista.</span></span> <span data-ttu-id="75102-117">Не используйте отслеживаемые типы расширений для файлов, изменяемых пользователем.</span><span class="sxs-lookup"><span data-stu-id="75102-117">Do not use monitored extension types for user-editable files.</span></span> <span data-ttu-id="75102-118">Например, если вы назначите имя личного файла данных пользователя с помощью расширения. ini, пользователь может потерять работу в результате восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="75102-118">For example, if you name a user's personal data file using the extension .ini, the user may lose work as a result of a system restore.</span></span>

 

 




