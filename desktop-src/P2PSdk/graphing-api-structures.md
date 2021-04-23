---
description: 'API-интерфейс для построения диаграмм использует следующие структуры:'
ms.assetid: 6bf06e90-5a1c-461c-8053-93cf4d4bfc95
title: Построение диаграмм по структурам API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b4c4f5da5a89a821e1abbf669d5eae0c6cb1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663341"
---
# <a name="graphing-api-structures"></a><span data-ttu-id="028e0-103">Построение диаграмм по структурам API</span><span class="sxs-lookup"><span data-stu-id="028e0-103">Graphing API Structures</span></span>

<span data-ttu-id="028e0-104">API-интерфейс для построения диаграмм использует следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="028e0-104">The Graphing API uses the following structures:</span></span>



| <span data-ttu-id="028e0-105">Структура</span><span class="sxs-lookup"><span data-stu-id="028e0-105">Structure</span></span>                                                                 | <span data-ttu-id="028e0-106">Описание</span><span class="sxs-lookup"><span data-stu-id="028e0-106">Description</span></span>                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="028e0-107">**\_ \_ \_ данные изменения узла событий \_ в одноранговых узлах**</span><span class="sxs-lookup"><span data-stu-id="028e0-107">**PEER\_EVENT\_NODE\_CHANGE\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_node_change_data)    | <span data-ttu-id="028e0-108">Содержит указатель на данные при запуске события **\_ \_ \_ \_ изменения узла однорангового графа** .</span><span class="sxs-lookup"><span data-stu-id="028e0-108">Contains a pointer to the data if a **PEER\_GRAPH\_EVENT\_NODE\_CHANGE** event is triggered.</span></span>                  |
| [<span data-ttu-id="028e0-109">**\_ \_ синхронизированные данные события однорангового узла \_**</span><span class="sxs-lookup"><span data-stu-id="028e0-109">**PEER\_EVENT\_SYNCHRONIZED\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_synchronized_data)   | <span data-ttu-id="028e0-110">Указывает тип синхронизированной записи.</span><span class="sxs-lookup"><span data-stu-id="028e0-110">Indicates the type of record that has been synchronized.</span></span>                                                      |
| [<span data-ttu-id="028e0-111">**данные события однорангового \_ графа \_ \_**</span><span class="sxs-lookup"><span data-stu-id="028e0-111">**PEER\_GRAPH\_EVENT\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data)                 | <span data-ttu-id="028e0-112">Содержит данные, связанные с одноранговым событием.</span><span class="sxs-lookup"><span data-stu-id="028e0-112">Contains data associated with a peer event.</span></span>                                                                   |
| [<span data-ttu-id="028e0-113">**\_ \_ Регистрация события одноранговой диаграммы \_**</span><span class="sxs-lookup"><span data-stu-id="028e0-113">**PEER\_GRAPH\_EVENT\_REGISTRATION**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) | <span data-ttu-id="028e0-114">Указывает события однорангового узла, для которых приложению требуются уведомления.</span><span class="sxs-lookup"><span data-stu-id="028e0-114">Specifies which peer events an application requires notifications for.</span></span>                                        |
| [<span data-ttu-id="028e0-115">**свойства однорангового \_ графа \_**</span><span class="sxs-lookup"><span data-stu-id="028e0-115">**PEER\_GRAPH\_PROPERTIES**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_graph_properties)                  | <span data-ttu-id="028e0-116">Содержит данные о политике однорангового графа, идентификатора, области и других сведений.</span><span class="sxs-lookup"><span data-stu-id="028e0-116">Contains data about the policy of a peer graph, ID, scope, and other information.</span></span>                             |
| [<span data-ttu-id="028e0-117">**\_ \_ сведения о одноранговом узле**</span><span class="sxs-lookup"><span data-stu-id="028e0-117">**PEER\_NODE\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_node_info)                                | <span data-ttu-id="028e0-118">Содержит сведения, относящиеся к определенному узлу в одноранговой диаграмме.</span><span class="sxs-lookup"><span data-stu-id="028e0-118">Contains information that is specific to a particular node in a peer graph.</span></span>                                   |
| [<span data-ttu-id="028e0-119">**\_интерфейс безопасности \_ узла**</span><span class="sxs-lookup"><span data-stu-id="028e0-119">**PEER\_SECURITY\_INTERFACE**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_security_interface)              | <span data-ttu-id="028e0-120">Указывает интерфейсы безопасности, которые вызывают API-интерфейсы одноранговой диаграммы, используемые для проверки, защиты и освобождения записей.</span><span class="sxs-lookup"><span data-stu-id="028e0-120">Specifies the security interfaces that calls to Peer Graphing APIs use to validate, secure, and free records.</span></span> |



 

 

 



