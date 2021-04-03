---
description: Чтобы использовать API агента Центр обновления Windows (WUA), сначала создайте экземпляр одного из интерфейсов, создав объект из соответствующего компонентного класса.
ms.assetid: b304971d-584a-4d0f-be5b-26f0ab315ec9
title: Использование API агента Центр обновления Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b5d155a2354b68135d0742f765dffb01e7235f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810199"
---
# <a name="using-the-windows-update-agent-api"></a><span data-ttu-id="3641a-103">Использование API агента Центр обновления Windows</span><span class="sxs-lookup"><span data-stu-id="3641a-103">Using the Windows Update Agent API</span></span>

<span data-ttu-id="3641a-104">Чтобы использовать API агента Центр обновления Windows (WUA), сначала создайте экземпляр одного из интерфейсов, создав объект из соответствующего компонентного класса.</span><span class="sxs-lookup"><span data-stu-id="3641a-104">To use the Windows Update Agent (WUA) API, first create an instance of one of the interfaces by creating the object from the appropriate coclass.</span></span>

<span data-ttu-id="3641a-105">В следующих разделах описывается, как можно использовать API WUA.</span><span class="sxs-lookup"><span data-stu-id="3641a-105">The following topics describe how you can use the WUA API:</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="3641a-106">Эти сценарии предназначены для демонстрации использования API-интерфейсов агента Центр обновления Windows и предоставляют примеры того, как разработчики могут использовать эти API для решения проблем.</span><span class="sxs-lookup"><span data-stu-id="3641a-106">These scripts are intended to demonstrate the use of the Windows Update Agent APIs, and provide examples of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="3641a-107">Эти скрипты не предназначены для рабочего кода, и сами скрипты не поддерживаются корпорацией Майкрософт (хотя поддерживаются базовые API-интерфейсы Центр обновления Windows агента).</span><span class="sxs-lookup"><span data-stu-id="3641a-107">These scripts are not intended as production code, and the scripts themselves are not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 

-   [<span data-ttu-id="3641a-108">Объектная модель агента Центр обновления Windows</span><span class="sxs-lookup"><span data-stu-id="3641a-108">Windows Update Agent Object Model</span></span>](windows-update-agent-object-model.md)
-   [<span data-ttu-id="3641a-109">Определение текущей версии WUA</span><span class="sxs-lookup"><span data-stu-id="3641a-109">Determining the Current Version of WUA</span></span>](determining-the-current-version-of-wua.md)
-   [<span data-ttu-id="3641a-110">Обновление агента Центр обновления Windows</span><span class="sxs-lookup"><span data-stu-id="3641a-110">Updating the Windows Update Agent</span></span>](updating-the-windows-update-agent.md)
-   [<span data-ttu-id="3641a-111">Обновление файлов заголовков агента Центр обновления Windows</span><span class="sxs-lookup"><span data-stu-id="3641a-111">Updating Windows Update Agent Header Files</span></span>](updating-windows-update-agent-header-files.md)
-   [<span data-ttu-id="3641a-112">Использование агента WUA для проверки наличия обновлений в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="3641a-112">Using WUA to Scan for Updates Offline</span></span>](using-wua-to-scan-for-updates-offline.md)
-   [<span data-ttu-id="3641a-113">Защищенные методы и свойства в API WUA</span><span class="sxs-lookup"><span data-stu-id="3641a-113">Secured Methods and Properties in the WUA API</span></span>](secured-methods-and-properties-in-the-wua-api.md)
-   [<span data-ttu-id="3641a-114">Поиск, скачивание и установка обновлений</span><span class="sxs-lookup"><span data-stu-id="3641a-114">Searching, Downloading, and Installing Updates</span></span>](searching--downloading--and-installing-updates.md)
-   [<span data-ttu-id="3641a-115">Поиск, скачивание и установка конкретных обновлений</span><span class="sxs-lookup"><span data-stu-id="3641a-115">Searching, Downloading, and Installing Specific Updates</span></span>](searching--downloading--and-installing-specific-updates.md)
-   [<span data-ttu-id="3641a-116">Использование агента WUA с удаленного компьютера</span><span class="sxs-lookup"><span data-stu-id="3641a-116">Using WUA From a Remote Computer</span></span>](using-wua-from-a-remote-computer.md)
-   [<span data-ttu-id="3641a-117">Рекомендации по асинхронным операциям WUA</span><span class="sxs-lookup"><span data-stu-id="3641a-117">Guidelines for Asynchronous WUA Operations</span></span>](guidelines-for-asynchronous-wua-operations.md)
-   [<span data-ttu-id="3641a-118">Использование агента WUA из процесса вторичного входа в систему (Запуск от имени)</span><span class="sxs-lookup"><span data-stu-id="3641a-118">Using WUA from a Secondary Logon (Run As) Process</span></span>](using-wua-from-a-secondary-logon--run-as--process.md)
-   [<span data-ttu-id="3641a-119">Коды успешности и ошибок WUA</span><span class="sxs-lookup"><span data-stu-id="3641a-119">WUA Success and Error Codes</span></span>](wua-success-and-error-codes-.md)
-   [<span data-ttu-id="3641a-120">Коды ошибок сети WUA</span><span class="sxs-lookup"><span data-stu-id="3641a-120">WUA Networking Error Codes</span></span>](wua-networking-error-codes-.md)

 

 



