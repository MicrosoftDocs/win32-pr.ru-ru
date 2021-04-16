---
description: Интерфейс Иупдатесервицеманажер определяет следующие методы.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Методы Иупдатесервицеманажер
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464b0b6e48d074dbc43f370f267fe7a526e8269b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540138"
---
# <a name="iupdateservicemanager-methods"></a><span data-ttu-id="26bcf-103">Методы Иупдатесервицеманажер</span><span class="sxs-lookup"><span data-stu-id="26bcf-103">IUpdateServiceManager Methods</span></span>

<span data-ttu-id="26bcf-104">Интерфейс [**иупдатесервицеманажер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) определяет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="26bcf-104">The [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) interface defines the following methods.</span></span>



| <span data-ttu-id="26bcf-105">Метод</span><span class="sxs-lookup"><span data-stu-id="26bcf-105">Method</span></span>                                                                           | <span data-ttu-id="26bcf-106">Описание</span><span class="sxs-lookup"><span data-stu-id="26bcf-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26bcf-107">**аддсканпаккажесервице**</span><span class="sxs-lookup"><span data-stu-id="26bcf-107">**AddScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | <span data-ttu-id="26bcf-108">Регистрирует пакет сканирования как службу с помощью агента Центр обновления Windows Agent (WUA), а затем возвращает интерфейс [**иупдатесервице**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) .</span><span class="sxs-lookup"><span data-stu-id="26bcf-108">Registers a scan package as a service with Windows Update Agent (WUA) and then returns an [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface.</span></span>    |
| [<span data-ttu-id="26bcf-109">**AddService**</span><span class="sxs-lookup"><span data-stu-id="26bcf-109">**AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | <span data-ttu-id="26bcf-110">Регистрирует службу с помощью WUA.</span><span class="sxs-lookup"><span data-stu-id="26bcf-110">Registers a service with WUA.</span></span>                                                                                                                    |
| [<span data-ttu-id="26bcf-111">**регистерсервицевисау**</span><span class="sxs-lookup"><span data-stu-id="26bcf-111">**RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | <span data-ttu-id="26bcf-112">Регистрирует службу с автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="26bcf-112">Registers a service with Automatic Updates.</span></span>                                                                                                      |
| [<span data-ttu-id="26bcf-113">**ремовесервице**</span><span class="sxs-lookup"><span data-stu-id="26bcf-113">**RemoveService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | <span data-ttu-id="26bcf-114">Удаляет регистрацию службы из WUA.</span><span class="sxs-lookup"><span data-stu-id="26bcf-114">Removes a service registration from WUA.</span></span>                                                                                                         |
| [<span data-ttu-id="26bcf-115">**SetOption**</span><span class="sxs-lookup"><span data-stu-id="26bcf-115">**SetOption**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | <span data-ttu-id="26bcf-116">Задает параметры для объекта, указывающего идентификатор службы, и указывает, следует ли отображать предупреждение при изменении регистрации автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="26bcf-116">Sets options for the object that specifies the service ID, and whether to display a warning when changing the registration of Automatic Updates.</span></span> |
| [<span data-ttu-id="26bcf-117">**унрегистерсервицевисау**</span><span class="sxs-lookup"><span data-stu-id="26bcf-117">**UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | <span data-ttu-id="26bcf-118">Отменяет регистрацию службы с автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="26bcf-118">Unregisters a service with Automatic Updates.</span></span>                                                                                                    |



 

 

 



