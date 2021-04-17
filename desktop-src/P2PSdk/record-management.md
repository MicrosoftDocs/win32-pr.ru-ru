---
description: Для управления записями можно работать со сведениями, хранящимися в структурах одноранговых \_ записей.
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Управление записями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663833"
---
# <a name="record-management"></a><span data-ttu-id="31598-103">Управление записями</span><span class="sxs-lookup"><span data-stu-id="31598-103">Record Management</span></span>

<span data-ttu-id="31598-104">Для управления записями можно работать со сведениями, хранящимися в структурах [**одноранговых \_ записей**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="31598-104">To manage records, you can work with information that is stored in [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structures.</span></span> <span data-ttu-id="31598-105">При создании, обновлении или удалении записей изменения, внесенные в граф, реплицируются на все узлы.</span><span class="sxs-lookup"><span data-stu-id="31598-105">When records are created, updated, or deleted, the changes made to a graph are replicated to all nodes.</span></span> <span data-ttu-id="31598-106">В следующей таблице приведены правила обновления и автоматического обновления записей.</span><span class="sxs-lookup"><span data-stu-id="31598-106">The following table identifies the rules for updating and automatically refreshing records.</span></span>



| <span data-ttu-id="31598-107">Задача управления</span><span class="sxs-lookup"><span data-stu-id="31598-107">Management Task</span></span>     | <span data-ttu-id="31598-108">Правило</span><span class="sxs-lookup"><span data-stu-id="31598-108">Rule</span></span>                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31598-109">Обновление записи</span><span class="sxs-lookup"><span data-stu-id="31598-109">Updating a record</span></span>   | <span data-ttu-id="31598-110">Не изменяйте время истечения срока действия или увеличьте его.</span><span class="sxs-lookup"><span data-stu-id="31598-110">Keep the expiration time the same or increase it.</span></span> <span data-ttu-id="31598-111">Нельзя уменьшить срок действия.</span><span class="sxs-lookup"><span data-stu-id="31598-111">You cannot decrease the expiration time.</span></span>                                                                                                                      |
| <span data-ttu-id="31598-112">Обновление записи</span><span class="sxs-lookup"><span data-stu-id="31598-112">Refreshing a record</span></span> | <span data-ttu-id="31598-113">Используйте флаг [**\_ \_ \_ автообновления флага одноранговой записи**](/windows/desktop/api/P2P/ns-p2p-peer_record) для автоматического обновления записи.</span><span class="sxs-lookup"><span data-stu-id="31598-113">Use the [**PEER\_RECORD\_FLAG\_AUTOREFRESH**](/windows/desktop/api/P2P/ns-p2p-peer_record) flag to automatically refresh a record.</span></span> <span data-ttu-id="31598-114">Этот флаг следует использовать только в том случае, если узел, публикующий запись, находится в режиме «в сети».</span><span class="sxs-lookup"><span data-stu-id="31598-114">Only use this flag when the node that is publishing a record is online.</span></span> <span data-ttu-id="31598-115">В противном случае не используйте этот флаг.</span><span class="sxs-lookup"><span data-stu-id="31598-115">Otherwise, do not use this flag.</span></span> |



 

 

 



