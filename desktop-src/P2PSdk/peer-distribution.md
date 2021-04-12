---
description: API однорангового распределения, поддерживающий функцию кэширования ветвей в Windows 7 и Windows Server 2008 R2, предлагает набор API-интерфейсов платформы, которые могут повысить скорость реагирования в сети централизованных приложений при доступе из удаленных офисов, предоставляя пользователям в этих офисах возможности работы в локальной сети. Возможности, предоставляемые этим набором API, также позволяют сократить общее использование глобальной сети (WAN).
ms.assetid: ad959586-7488-49ff-a237-4da409b81dd6
title: Одноранговое распределение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3382df432e8cedc40bf5679171563eb672a1a6a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080792"
---
# <a name="peer-distribution"></a><span data-ttu-id="3e6a9-104">Одноранговое распределение</span><span class="sxs-lookup"><span data-stu-id="3e6a9-104">Peer Distribution</span></span>

<span data-ttu-id="3e6a9-105">API однорангового распределения, поддерживающий функцию кэширования ветвей в Windows 7 и Windows Server 2008 R2, предлагает набор API-интерфейсов платформы, которые могут повысить скорость реагирования в сети централизованных приложений при доступе из удаленных офисов, предоставляя пользователям в этих офисах возможности работы в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="3e6a9-105">The Peer Distribution API, which supports the Branch Cache feature in Windows 7 and Windows Server 2008 R2, offers a set of platform APIs that can increase network responsiveness of centralized applications when accessed from remote offices, giving users in those offices the experience of working on your local area network.</span></span> <span data-ttu-id="3e6a9-106">Возможности, предоставляемые этим набором API, также позволяют сократить общее использование глобальной сети (WAN).</span><span class="sxs-lookup"><span data-stu-id="3e6a9-106">The capabilities offered by this set of APIs can also help in reducing overall wide area network (WAN) utilization.</span></span>

<span data-ttu-id="3e6a9-107">Для реализации этих функций не требуется ни одна существующая инфраструктура.</span><span class="sxs-lookup"><span data-stu-id="3e6a9-107">Implementing these features does not require any pre-existing infrastructure.</span></span> <span data-ttu-id="3e6a9-108">Повышение производительности удаленных сетей осуществляется просто путем развертывания Windows 7 на клиентских компьютерах, развертывания Windows Server 2008 R2 на серверных компьютерах и включения функции кэширования ветвей.</span><span class="sxs-lookup"><span data-stu-id="3e6a9-108">Making improvements to the performance of remote networks is accomplished simply by deploying Windows 7 to client computers, deploying Windows Server 2008 R2 to server computers, and enabling the Branch Cache feature.</span></span>

<span data-ttu-id="3e6a9-109">API-интерфейсы однорангового распространения тесно работают вместе с технологиями безопасности сети, включая SSL, подписывание SMB и сквозную IPsec.</span><span class="sxs-lookup"><span data-stu-id="3e6a9-109">The Peer Distribution APIs work seamlessly alongside network security technologies, including SSL, SMB Signing, and end-to-end IPsec.</span></span> <span data-ttu-id="3e6a9-110">Этот API можно использовать для уменьшения использования пропускной способности сети и повышения производительности приложений, даже если содержимое зашифровано.</span><span class="sxs-lookup"><span data-stu-id="3e6a9-110">You can use this API to reduce network bandwidth utilization and improve application performance even if the content is encrypted.</span></span>

## <a name="peer-distribution-api"></a><span data-ttu-id="3e6a9-111">API однорангового распространения</span><span class="sxs-lookup"><span data-stu-id="3e6a9-111">Peer Distribution API</span></span>



| <span data-ttu-id="3e6a9-112">Section</span><span class="sxs-lookup"><span data-stu-id="3e6a9-112">Section</span></span>                                                                | <span data-ttu-id="3e6a9-113">Описание</span><span class="sxs-lookup"><span data-stu-id="3e6a9-113">Description</span></span>                                                 |
|------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="3e6a9-114">О одноранговом распределении</span><span class="sxs-lookup"><span data-stu-id="3e6a9-114">About Peer Distribution</span></span>](about-peer-distribution.md)                 | <span data-ttu-id="3e6a9-115">Сведения о API распространения однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="3e6a9-115">Information about the Peer Distribution API.</span></span>                |
| [<span data-ttu-id="3e6a9-116">Справочник по API однорангового распространения</span><span class="sxs-lookup"><span data-stu-id="3e6a9-116">Peer Distribution API Reference</span></span>](peer-distribution-api-reference.md) | <span data-ttu-id="3e6a9-117">Обзор и справочные страницы для API однорангового распространения.</span><span class="sxs-lookup"><span data-stu-id="3e6a9-117">Overview and reference pages for the Peer Distribution API.</span></span> |



 

 

 



