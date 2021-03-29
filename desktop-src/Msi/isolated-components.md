---
description: Авторы пакетов установки могут указать, что установщик копирует общие файлы (обычно общие библиотеки DLL) приложения в папку этого приложения, а не в общее расположение.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Изолированные компоненты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f29f614dfd819e093c5729a9a97a076247d281d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808740"
---
# <a name="isolated-components"></a><span data-ttu-id="ef7ff-103">Изолированные компоненты</span><span class="sxs-lookup"><span data-stu-id="ef7ff-103">Isolated Components</span></span>

<span data-ttu-id="ef7ff-104">Авторы пакетов установки могут указать, что установщик копирует общие файлы (обычно общие библиотеки DLL) приложения в папку этого приложения, а не в общее расположение.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-104">Authors of installation packages can specify that the installer copy the shared files (commonly shared DLLs) of an application into that application's folder rather than to a shared location.</span></span> <span data-ttu-id="ef7ff-105">Этот частный набор файлов (DLL) используется только приложением.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-105">This private set of files (DLLs) are then used only by the application.</span></span> <span data-ttu-id="ef7ff-106">Таким образом изоляция приложения вместе с его общими компонентами имеет следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-106">Isolating the application together with its shared components in this manner has the following advantages:</span></span>

-   <span data-ttu-id="ef7ff-107">Приложение всегда использует версии общих файлов, с которыми он был развернут.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-107">The application always uses the versions of the shared files with which it was deployed.</span></span>
-   <span data-ttu-id="ef7ff-108">При установке приложения другие версии общих файлов не перезаписываются другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-108">Installing the application does not overwrite other versions of the shared files by other applications.</span></span>
-   <span data-ttu-id="ef7ff-109">Последующие установки других приложений, использующих разные версии общих файлов, не могут перезаписывать файлы, используемые этим приложением.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-109">Subsequent installations of other applications using different versions of the shared files cannot overwrite the files used by this application.</span></span>

<span data-ttu-id="ef7ff-110">Поскольку текущая реализация COM хранит один полный путь в реестре для каждой пары CLSID/Context, она заставляет все приложения использовать одну и ту же версию общей библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-110">Because the current implementation of COM keeps a single full path in the registry for each CLSID/Context pair, it forces all applications to use the same version of a shared DLL.</span></span> <span data-ttu-id="ef7ff-111">Чтобы приложение оставало защищенной копии COM-сервера, системный загрузчик в Windows 2000 проверяет наличие. ЛОКАЛЬНЫЙ файл в папке приложения.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-111">To enable an application to keep a private copy of a COM server, the system loader in Windows 2000 checks for the presence of a .LOCAL file in the application's folder.</span></span> <span data-ttu-id="ef7ff-112">Значение, если системный загрузчик обнаруживает. ЛОКАЛЬНЫЙ файл, он изменяет логику поиска, чтобы предпочитать библиотеки DLL, расположенные в той же папке, что и приложение.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-112">If the system loader detects a .LOCAL file, it alters its search logic to prefer DLLs located in the same folder as the application.</span></span>

<span data-ttu-id="ef7ff-113">Когда установщик Windows выполняет [действие исолатекомпонентс](isolatecomponents-action.md) , они копируют файлы компонента (обычно это общая библиотека DLL), указанные в \_ общем столбце Component [таблицы исолатедкомпонент](isolatedcomponent-table.md) , в ту же папку, что и компонент (обычно exe-файл), указанный в \_ столбце приложение компонента.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-113">When Windows Installer runs the [IsolateComponents action](isolatecomponents-action.md) they copy the files of the component (commonly a shared DLL) specified in the Component\_Shared column of the [IsolatedComponent table](isolatedcomponent-table.md) into the same folder as the component (commonly an .exe file) specified in the Component\_Application column.</span></span> <span data-ttu-id="ef7ff-114">Установщик создает в этом каталоге файл с нулевым количеством байт, а также имеет короткое имя файла ключа для \_ приложения-компонента (обычно имя совпадает с именем exe приложения), добавленным в. Языковые.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-114">The installer creates a file in this directory, zero bytes in length, having the short file name of the key file for Component\_Application (typically the name is the same as the application's .exe) appended with .LOCAL.</span></span> <span data-ttu-id="ef7ff-115">Установщик использует регистрацию для компонента в его общем расположении и не записывает сведения о регистрации для копии компонента в частном расположении.</span><span class="sxs-lookup"><span data-stu-id="ef7ff-115">The installer uses the registration for the component in its shared location and does not write any registration information for the copy of the component in the private location.</span></span>

<span data-ttu-id="ef7ff-116">Дополнительные сведения можно найти в разделе</span><span class="sxs-lookup"><span data-stu-id="ef7ff-116">For more information, see:</span></span>

-   [<span data-ttu-id="ef7ff-117">Установка изолированных компонентов</span><span class="sxs-lookup"><span data-stu-id="ef7ff-117">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
-   [<span data-ttu-id="ef7ff-118">Повторная установка изолированных компонентов</span><span class="sxs-lookup"><span data-stu-id="ef7ff-118">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
-   [<span data-ttu-id="ef7ff-119">Удаление изолированных компонентов</span><span class="sxs-lookup"><span data-stu-id="ef7ff-119">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
-   [<span data-ttu-id="ef7ff-120">Использование изолированных компонентов</span><span class="sxs-lookup"><span data-stu-id="ef7ff-120">Using Isolated Components</span></span>](using-isolated-components.md)

 

 



