---
description: Каталог Windows — это каталог, содержащий приложения на основе Windows, файлы инициализации и файлы справки. Функция Жетвиндовсдиректори извлекает путь к этому каталогу.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Конфигурация операционной системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38aa2c2b6b4f6b3ac5caac78a89ad980a9bd074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265625"
---
# <a name="operating-system-configuration"></a><span data-ttu-id="a8a18-104">Конфигурация операционной системы</span><span class="sxs-lookup"><span data-stu-id="a8a18-104">Operating System Configuration</span></span>

<span data-ttu-id="a8a18-105">*Каталог Windows* — это каталог, содержащий приложения на основе Windows, файлы инициализации и файлы справки.</span><span class="sxs-lookup"><span data-stu-id="a8a18-105">The *Windows directory* is the directory that contains Windows-based applications, initialization files, and help files.</span></span> <span data-ttu-id="a8a18-106">Функция [**жетвиндовсдиректори**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) извлекает путь к этому каталогу.</span><span class="sxs-lookup"><span data-stu-id="a8a18-106">The [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="a8a18-107">*Системный каталог* — это каталог, содержащий библиотеки динамической компоновки, драйверы и файлы шрифтов.</span><span class="sxs-lookup"><span data-stu-id="a8a18-107">The *system directory* is the directory that contains dynamic-link libraries, drivers, and font files.</span></span> <span data-ttu-id="a8a18-108">Функция [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) извлекает путь к этому каталогу.</span><span class="sxs-lookup"><span data-stu-id="a8a18-108">The [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="a8a18-109">Функция [**суперпользователя**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) извлекает имя пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="a8a18-109">The [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) function retrieves the name of the user currently logged onto the system.</span></span> <span data-ttu-id="a8a18-110">Имя пользователя — это либо имя входа, либо полное имя пользователя, если Последнее включено в реестр.</span><span class="sxs-lookup"><span data-stu-id="a8a18-110">The user name is either the logon name or the user's full name, if the latter is included in the registry.</span></span>

<span data-ttu-id="a8a18-111">*Переменная среды* — это символьная переменная, представляющая некоторый элемент системы, например путь, имя файла или другие литеральные данные.</span><span class="sxs-lookup"><span data-stu-id="a8a18-111">An *environment variable* is a symbolic variable that represents some element of the system, such as a path, a file name, or other literal data.</span></span> <span data-ttu-id="a8a18-112">Например, переменная среды PATH представляет каталоги, в которых выполняется поиск исполняемых файлов.</span><span class="sxs-lookup"><span data-stu-id="a8a18-112">For example, the environment variable PATH represents the directories in which to search for executable files.</span></span> <span data-ttu-id="a8a18-113">Когда пользователь входит в систему, система инициализирует переменные среды на основе раздела Environment в реестре.</span><span class="sxs-lookup"><span data-stu-id="a8a18-113">When a user logs on, the system initializes environment variables based on the environment section of the registry.</span></span> <span data-ttu-id="a8a18-114">Функция [**експанденвиронментстрингс**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) извлекает значения указанных переменных среды.</span><span class="sxs-lookup"><span data-stu-id="a8a18-114">The [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) function retrieves the values of specified environment variables.</span></span>

<span data-ttu-id="a8a18-115">Дополнительные сведения предоставляются интерфейсом [**иадсадсистеминфо**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) .</span><span class="sxs-lookup"><span data-stu-id="a8a18-115">Additional information is provided by the [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) interface.</span></span>

 

 
