---
description: В следующем списке содержатся элементы адреса КМСП.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Элементы Кмспаддресс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913819"
---
# <a name="cmspaddress-members"></a><span data-ttu-id="c7b5d-103">Элементы Кмспаддресс</span><span class="sxs-lookup"><span data-stu-id="c7b5d-103">CMSPAddress Members</span></span>



| <span data-ttu-id="c7b5d-104">Типы элементов</span><span class="sxs-lookup"><span data-stu-id="c7b5d-104">Member types</span></span>                    | <span data-ttu-id="c7b5d-105">Имя</span><span class="sxs-lookup"><span data-stu-id="c7b5d-105">Name</span></span>                    | <span data-ttu-id="c7b5d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c7b5d-106">Description</span></span>                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b5d-107">Iunknown</span><span class="sxs-lookup"><span data-stu-id="c7b5d-107">Iunknown</span></span>                        | <span data-ttu-id="c7b5d-108">\*m \_ пфтм</span><span class="sxs-lookup"><span data-stu-id="c7b5d-108">\*m\_pFTM</span></span>               | <span data-ttu-id="c7b5d-109">Указатель на свободный потоковый маршалинг.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-109">Pointer to the free threaded marshaller.</span></span>                                                         |
| <span data-ttu-id="c7b5d-110">HANDLE</span><span class="sxs-lookup"><span data-stu-id="c7b5d-110">HANDLE</span></span>                          | <span data-ttu-id="c7b5d-111">m \_ хтевент</span><span class="sxs-lookup"><span data-stu-id="c7b5d-111">m\_htEvent</span></span>              | <span data-ttu-id="c7b5d-112">Обработчик события Tapi3.dll, который используется для уведомления TAPI о том, что MSP хочет отправить данные в него.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-112">Handle to Tapi3.dll's event, which is used to notify TAPI that the MSP wants to send data to it.</span></span> |
| <span data-ttu-id="c7b5d-113">\_запись списка</span><span class="sxs-lookup"><span data-stu-id="c7b5d-113">LIST\_ENTRY</span></span>                     | <span data-ttu-id="c7b5d-114">m \_ евентлист</span><span class="sxs-lookup"><span data-stu-id="c7b5d-114">m\_EventList</span></span>            | <span data-ttu-id="c7b5d-115">Список событий.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-115">List of events.</span></span>                                                                                  |
| <span data-ttu-id="c7b5d-116">кмспкритсектион</span><span class="sxs-lookup"><span data-stu-id="c7b5d-116">CMSPCritSection</span></span>                 | <span data-ttu-id="c7b5d-117">m \_ евентдаталокк</span><span class="sxs-lookup"><span data-stu-id="c7b5d-117">m\_EventDataLock</span></span>        | <span data-ttu-id="c7b5d-118">Блокировка, защищающая данные, связанные с обработкой событий, с помощью TAPI.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-118">The lock that protects the data related to event handling with TAPI.</span></span>                             |
| <span data-ttu-id="c7b5d-119">иттерминалманажер</span><span class="sxs-lookup"><span data-stu-id="c7b5d-119">ITTerminalManager</span></span>               | <span data-ttu-id="c7b5d-120">\*m \_ питтерминалманажер</span><span class="sxs-lookup"><span data-stu-id="c7b5d-120">\*m\_pITTerminalManager</span></span> | <span data-ttu-id="c7b5d-121">Указатель на объект диспетчера терминалов.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-121">The pointer to the Terminal Manager object.</span></span>                                                      |
| <span data-ttu-id="c7b5d-122">Кмспаррай <Иттерминал \*></span><span class="sxs-lookup"><span data-stu-id="c7b5d-122">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="c7b5d-123">m \_ терминалов</span><span class="sxs-lookup"><span data-stu-id="c7b5d-123">m\_Terminals</span></span>            | <span data-ttu-id="c7b5d-124">Список статических терминалов, которые могут использоваться в адресе.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-124">The list of static terminals that can be used on the address.</span></span>                                    |
| <span data-ttu-id="c7b5d-125">BOOL</span><span class="sxs-lookup"><span data-stu-id="c7b5d-125">BOOL</span></span>                            | <span data-ttu-id="c7b5d-126">m \_ фтерминалсуптодате</span><span class="sxs-lookup"><span data-stu-id="c7b5d-126">m\_fTerminalsUpToDate</span></span>   | <span data-ttu-id="c7b5d-127">Этот флаг имеет **значение true** , если список терминалов находится в актуальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-127">This flag is **TRUE** if the terminal list is up to date.</span></span>                                        |
| <span data-ttu-id="c7b5d-128">кмспкритсектион</span><span class="sxs-lookup"><span data-stu-id="c7b5d-128">CMSPCritSection</span></span>                 | <span data-ttu-id="c7b5d-129">m \_ терминалдаталокк</span><span class="sxs-lookup"><span data-stu-id="c7b5d-129">m\_TerminalDataLock</span></span>     | <span data-ttu-id="c7b5d-130">Блокировка, защищающая элементы данных, связанные с терминалом.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-130">The lock that protects the terminal-related data members.</span></span>                                        |



 

 

 



