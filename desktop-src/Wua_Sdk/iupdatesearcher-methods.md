---
description: Интерфейс Иупдатесеарчер определяет следующие методы.
ms.assetid: 82735555-b23a-43b0-bf5b-a8cf72dc40d4
title: Методы Иупдатесеарчер
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462cbd371546743bab836ed1cdc2479e30f13612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662418"
---
# <a name="iupdatesearcher-methods"></a><span data-ttu-id="e7946-103">Методы Иупдатесеарчер</span><span class="sxs-lookup"><span data-stu-id="e7946-103">IUpdateSearcher Methods</span></span>

<span data-ttu-id="e7946-104">Интерфейс [**иупдатесеарчер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) определяет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e7946-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following methods.</span></span>



| <span data-ttu-id="e7946-105">Метод</span><span class="sxs-lookup"><span data-stu-id="e7946-105">Method</span></span>                                                              | <span data-ttu-id="e7946-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e7946-106">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7946-107">**бегинсеарч**</span><span class="sxs-lookup"><span data-stu-id="e7946-107">**BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)                   | <span data-ttu-id="e7946-108">Начинает выполнение асинхронного поиска обновлений.</span><span class="sxs-lookup"><span data-stu-id="e7946-108">Begins execution of an asynchronous search for updates.</span></span> <span data-ttu-id="e7946-109">Поиск использует параметры поиска, настроенные в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="e7946-109">The search uses the search options that are currently configured.</span></span> |
| [<span data-ttu-id="e7946-110">**ендсеарч**</span><span class="sxs-lookup"><span data-stu-id="e7946-110">**EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)                       | <span data-ttu-id="e7946-111">Завершает асинхронный поиск обновлений.</span><span class="sxs-lookup"><span data-stu-id="e7946-111">Completes an asynchronous search for updates.</span></span>                                                                             |
| [<span data-ttu-id="e7946-112">**EscapeString**</span><span class="sxs-lookup"><span data-stu-id="e7946-112">**EscapeString**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-escapestring)                 | <span data-ttu-id="e7946-113">Преобразует строку в строку, которая может использоваться как литеральное значение в строке условий поиска.</span><span class="sxs-lookup"><span data-stu-id="e7946-113">Converts a string into a string that can be used as a literal value in a search criteria string.</span></span>                          |
| [<span data-ttu-id="e7946-114">**жеттоталхисторикаунт**</span><span class="sxs-lookup"><span data-stu-id="e7946-114">**GetTotalHistoryCount**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-gettotalhistorycount) | <span data-ttu-id="e7946-115">Возвращает число событий обновления на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e7946-115">Returns the number of update events on the computer.</span></span>                                                                      |
| [<span data-ttu-id="e7946-116">**куерихистори**</span><span class="sxs-lookup"><span data-stu-id="e7946-116">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-queryhistory)                | <span data-ttu-id="e7946-117">Синхронно запрашивает у компьютера журнал событий обновления.</span><span class="sxs-lookup"><span data-stu-id="e7946-117">Synchronously queries the computer for the history of update events.</span></span>                                                      |
| [<span data-ttu-id="e7946-118">**Поиск**</span><span class="sxs-lookup"><span data-stu-id="e7946-118">**Search**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search)                             | <span data-ttu-id="e7946-119">Выполняет синхронный поиск обновлений.</span><span class="sxs-lookup"><span data-stu-id="e7946-119">Performs a synchronous search for updates.</span></span> <span data-ttu-id="e7946-120">Поиск использует параметры поиска, настроенные в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="e7946-120">The search uses the search options that are currently configured.</span></span>              |



 

 

 



