---
description: Интерфейс IUpdateSession3 определяет следующие методы.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Методы IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143690"
---
# <a name="iupdatesession3-methods"></a><span data-ttu-id="96610-103">Методы IUpdateSession3</span><span class="sxs-lookup"><span data-stu-id="96610-103">IUpdateSession3 Methods</span></span>

<span data-ttu-id="96610-104">Интерфейс [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) определяет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="96610-104">The [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) interface defines the following methods.</span></span>



| <span data-ttu-id="96610-105">Метод</span><span class="sxs-lookup"><span data-stu-id="96610-105">Method</span></span>                                                                           | <span data-ttu-id="96610-106">Описание</span><span class="sxs-lookup"><span data-stu-id="96610-106">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96610-107">**креатеупдатесервицеманажер**</span><span class="sxs-lookup"><span data-stu-id="96610-107">**CreateUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | <span data-ttu-id="96610-108">Возвращает указатель на интерфейс [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) для сеанса.</span><span class="sxs-lookup"><span data-stu-id="96610-108">Returns a pointer to an [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) interface for the session.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="96610-109">**куерихистори**</span><span class="sxs-lookup"><span data-stu-id="96610-109">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | <span data-ttu-id="96610-110">Возвращает указатель на интерфейс [**иупдатехисторентриколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) .</span><span class="sxs-lookup"><span data-stu-id="96610-110">Returns a pointer to an [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) interface.</span></span> <span data-ttu-id="96610-111">Интерфейс содержит совпадающие записи событий на компьютере.</span><span class="sxs-lookup"><span data-stu-id="96610-111">The interface contains matching event records on the computer.</span></span> <span data-ttu-id="96610-112">Это приводит к тому, что метод [**куерихистори**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) синхронно запрашивает на компьютере журнал событий обновления.</span><span class="sxs-lookup"><span data-stu-id="96610-112">This causes the [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) method to synchronously query the computer for the history of update events.</span></span> |



 

<span data-ttu-id="96610-113">Сведения о членах, наследуемых этим интерфейсом, см. в следующих интерфейсах:</span><span class="sxs-lookup"><span data-stu-id="96610-113">For information about the members inherited by this interface, see the following interfaces:</span></span>

-   [<span data-ttu-id="96610-114">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="96610-114">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="96610-115">**иупдатесессион**</span><span class="sxs-lookup"><span data-stu-id="96610-115">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



