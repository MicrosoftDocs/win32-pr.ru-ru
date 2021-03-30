---
description: Интерфейс Иинсталлатионжоб определяет следующие методы.
ms.assetid: 4990ef7c-b6cd-46fc-9e7d-8d1d78edc9f2
title: Методы Иинсталлатионжоб
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0c1a5850f3d71ad1a6a51046fe890ea9bc7426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145754"
---
# <a name="iinstallationjob-methods"></a><span data-ttu-id="8bb59-103">Методы Иинсталлатионжоб</span><span class="sxs-lookup"><span data-stu-id="8bb59-103">IInstallationJob Methods</span></span>

<span data-ttu-id="8bb59-104">Интерфейс [**иинсталлатионжоб**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) определяет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8bb59-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following methods.</span></span>



| <span data-ttu-id="8bb59-105">Метод</span><span class="sxs-lookup"><span data-stu-id="8bb59-105">Method</span></span>                                                | <span data-ttu-id="8bb59-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8bb59-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bb59-107">**Чистку**</span><span class="sxs-lookup"><span data-stu-id="8bb59-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)           | <span data-ttu-id="8bb59-108">Ожидает завершения асинхронной операции, а затем освобождает все обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="8bb59-108">Waits for an asynchronous operation to be completed and then releases all the callbacks.</span></span>                                                              |
| [<span data-ttu-id="8bb59-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="8bb59-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-getprogress)   | <span data-ttu-id="8bb59-110">Возвращает интерфейс [**иинсталлатионпрогресс**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) , описывающий текущий ход выполнения установки или удаления.</span><span class="sxs-lookup"><span data-stu-id="8bb59-110">Returns an [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface that describes the current progress of an installation or uninstallation.</span></span> |
| [<span data-ttu-id="8bb59-111">**рекуестаборт**</span><span class="sxs-lookup"><span data-stu-id="8bb59-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-requestabort) | <span data-ttu-id="8bb59-112">Выполняет запрос на отмену установки или удаления.</span><span class="sxs-lookup"><span data-stu-id="8bb59-112">Makes a request to cancel the installation or uninstallation.</span></span>                                                                                         |



 

 

 



