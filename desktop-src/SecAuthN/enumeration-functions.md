---
description: Если поставщик сети должен поддерживать просмотр сетевых ресурсов, он должен реализовать следующие функции. Многопротокольное обращение вызывает эти функции для перечисления ресурсов.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Функции перечисления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2670424be1540aad3e46e32c5b0606eb02e04bdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072686"
---
# <a name="enumeration-functions"></a><span data-ttu-id="be513-104">Функции перечисления</span><span class="sxs-lookup"><span data-stu-id="be513-104">Enumeration Functions</span></span>

<span data-ttu-id="be513-105">Если поставщик сети должен поддерживать просмотр сетевых ресурсов, он должен реализовать следующие функции.</span><span class="sxs-lookup"><span data-stu-id="be513-105">If your network provider needs to support browsing of its network resources, it should implement the following functions.</span></span> <span data-ttu-id="be513-106">Многопротокольное обращение вызывает эти функции для перечисления ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be513-106">MPR calls these functions to enumerate the resources.</span></span>

<span data-ttu-id="be513-107">Поставщик сети не требуется для реализации каких-либо функций перечисления.</span><span class="sxs-lookup"><span data-stu-id="be513-107">A network provider is not required to implement any of the enumeration functions.</span></span> <span data-ttu-id="be513-108">Однако если поставщик сети реализует либо [**нпопененум**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**Нпенумресаурце**](/windows/desktop/api/Npapi/nf-npapi-npenumresource), либо [**нпклосинум**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), он также должен реализовывать другие две функции перечисления.</span><span class="sxs-lookup"><span data-stu-id="be513-108">If, however, a network provider implements either [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource), or [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), it must also implement the other two enumeration functions.</span></span>



| <span data-ttu-id="be513-109">Функция</span><span class="sxs-lookup"><span data-stu-id="be513-109">Function</span></span>                                                     | <span data-ttu-id="be513-110">Описание</span><span class="sxs-lookup"><span data-stu-id="be513-110">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be513-111">**нпопененум**</span><span class="sxs-lookup"><span data-stu-id="be513-111">**NPOpenEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | <span data-ttu-id="be513-112">Открывает перечисление сетевых ресурсов или существующих подключений.</span><span class="sxs-lookup"><span data-stu-id="be513-112">Opens an enumeration of network resources or existing connections.</span></span>                                                                                                  |
| [<span data-ttu-id="be513-113">**нпенумресаурце**</span><span class="sxs-lookup"><span data-stu-id="be513-113">**NPEnumResource**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | <span data-ttu-id="be513-114">Выполняет перечисление для маркера, возвращаемого функцией [**нпопененум**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span><span class="sxs-lookup"><span data-stu-id="be513-114">Performs an enumeration on a handle returned by [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span></span>                                                                                   |
| [<span data-ttu-id="be513-115">**нпклосинум**</span><span class="sxs-lookup"><span data-stu-id="be513-115">**NPCloseEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | <span data-ttu-id="be513-116">Закрывает перечисление.</span><span class="sxs-lookup"><span data-stu-id="be513-116">Closes an enumeration.</span></span>                                                                                                                                              |
| [<span data-ttu-id="be513-117">**нпжетресаурцеинформатион**</span><span class="sxs-lookup"><span data-stu-id="be513-117">**NPGetResourceInformation**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | <span data-ttu-id="be513-118">Определяет, является ли поставщик правильным поставщиком для ответа на запрос указанного сетевого ресурса и возвращает сведения о типе ресурса.</span><span class="sxs-lookup"><span data-stu-id="be513-118">Determines whether the provider is the correct provider to respond to a request for a specified network resource and returns information about the resource's type.</span></span> |
| [<span data-ttu-id="be513-119">**нпжетресаурцепарент**</span><span class="sxs-lookup"><span data-stu-id="be513-119">**NPGetResourceParent**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | <span data-ttu-id="be513-120">Возвращает родителя указанного сетевого ресурса в иерархии обзора.</span><span class="sxs-lookup"><span data-stu-id="be513-120">Returns the parent of a specified network resource in the browse hierarchy.</span></span>                                                                                         |



 

 

 



