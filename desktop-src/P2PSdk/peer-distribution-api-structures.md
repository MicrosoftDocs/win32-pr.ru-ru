---
description: Служба однорангового распространения (Майкрософт) поддерживает следующие структуры.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Структуры API однорангового распространения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663315"
---
# <a name="peer-distribution-api-structures"></a><span data-ttu-id="8e997-103">Структуры API однорангового распространения</span><span class="sxs-lookup"><span data-stu-id="8e997-103">Peer Distribution API Structures</span></span>

<span data-ttu-id="8e997-104">Служба однорангового распространения (Майкрософт) поддерживает следующие структуры.</span><span class="sxs-lookup"><span data-stu-id="8e997-104">The Microsoft Peer Distribution service supports the following structures.</span></span>



| <span data-ttu-id="8e997-105">Структура</span><span class="sxs-lookup"><span data-stu-id="8e997-105">Structure</span></span>                                                              | <span data-ttu-id="8e997-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8e997-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e997-107">**\_ \_ основные \_ сведения о клиенте WebClient**</span><span class="sxs-lookup"><span data-stu-id="8e997-107">**PEERDIST\_CLIENT\_BASIC\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | <span data-ttu-id="8e997-108">Указывает, существует ли несколько клиентов, одновременно загружая одно и то же содержимое.</span><span class="sxs-lookup"><span data-stu-id="8e997-108">Indicates whether or not there are many clients simultaneously downloading the same content.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="8e997-109">**\_тег содержимого для объекта, \_**</span><span class="sxs-lookup"><span data-stu-id="8e997-109">**PEERDIST\_CONTENT\_TAG**</span></span>](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | <span data-ttu-id="8e997-110">Содержит тег, предоставляемый клиентом, который является входным значением для [**пирдистклиентопенконтент**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span><span class="sxs-lookup"><span data-stu-id="8e997-110">Contains a client supplied tag which is an input value for [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span></span> <span data-ttu-id="8e997-111">Тег связан с сегментом содержимого и используется в API-интерфейсах управления содержимым, например [**пирдистклиентфлушконтент**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span><span class="sxs-lookup"><span data-stu-id="8e997-111">The tag is associated with the content segment and is used in content management APIs, like [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span></span> |
| [<span data-ttu-id="8e997-112">**\_Параметры публикации в \_ свойствах,**</span><span class="sxs-lookup"><span data-stu-id="8e997-112">**PEERDIST\_PUBLICATION\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | <span data-ttu-id="8e997-113">Содержит параметры публикации, включая сведения о версии API и возможные флаги параметров.</span><span class="sxs-lookup"><span data-stu-id="8e997-113">Contains publication options, including the API version information and possible option flags.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="8e997-114">**\_Параметры получения ОДНОранговых узлов \_**</span><span class="sxs-lookup"><span data-stu-id="8e997-114">**PEER\_RETRIEVAL\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | <span data-ttu-id="8e997-115">Содержит версию сведений о содержимом для извлечения.</span><span class="sxs-lookup"><span data-stu-id="8e997-115">Contains version of the content information to retrieve.</span></span>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="8e997-116">**\_сведения о состоянии сведений о том, \_**</span><span class="sxs-lookup"><span data-stu-id="8e997-116">**PEERDIST\_STATUS\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | <span data-ttu-id="8e997-117">Содержит сведения о текущем состоянии и возможностях службы BranchCache на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8e997-117">Contains information about the current status and capabilities of the BranchCache service on the local computer.</span></span>                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="8e997-118">См. также</span><span class="sxs-lookup"><span data-stu-id="8e997-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e997-119">Справочник по API однорангового распространения</span><span class="sxs-lookup"><span data-stu-id="8e997-119">Peer Distribution API Reference</span></span>](peer-distribution-api-reference.md)
</dt> </dl>

 

 



