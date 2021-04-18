---
description: 'API поставщика пространства имен PNRP использует следующие структуры:'
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Структуры PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663292"
---
# <a name="pnrp-structures"></a><span data-ttu-id="535b1-103">Структуры PNRP</span><span class="sxs-lookup"><span data-stu-id="535b1-103">PNRP Structures</span></span>

<span data-ttu-id="535b1-104">API поставщика пространства имен PNRP использует следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="535b1-104">The PNRP Namespace Provider API uses the following structures:</span></span>



| <span data-ttu-id="535b1-105">Структура</span><span class="sxs-lookup"><span data-stu-id="535b1-105">Structure</span></span>                                                             | <span data-ttu-id="535b1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="535b1-106">Description</span></span>                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="535b1-107">**\_ \_ сведения о конечной точке PNRP Peer \_**</span><span class="sxs-lookup"><span data-stu-id="535b1-107">**PEER\_PNRP\_ENDPOINT\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | <span data-ttu-id="535b1-108">Содержит IP-адреса и данные, связанные с конечной точкой одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="535b1-108">Contains the IP addresses and data associated with a peer endpoint.</span></span>                                                                                                 |
| [<span data-ttu-id="535b1-109">**\_сведения о одноранговом \_ облаке PNRP \_**</span><span class="sxs-lookup"><span data-stu-id="535b1-109">**PEER\_PNRP\_CLOUD\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | <span data-ttu-id="535b1-110">Содержит сведения о облаке протокола PNRP.</span><span class="sxs-lookup"><span data-stu-id="535b1-110">Contains information about a Peer Name Resolution Protocol (PNRP) cloud.</span></span>                                                                                            |
| [<span data-ttu-id="535b1-111">**\_ \_ сведения о регистрации однорангового PNRP \_**</span><span class="sxs-lookup"><span data-stu-id="535b1-111">**PEER\_PNRP\_REGISTRATION\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | <span data-ttu-id="535b1-112">Содержит сведения, предоставленные одноранговым удостоверением при регистрации в облаке PNRP.</span><span class="sxs-lookup"><span data-stu-id="535b1-112">Contains the information provided by a peer identity when it registers with a PNRP cloud.</span></span>                                                                           |
| [<span data-ttu-id="535b1-113">PNRP и BLOB-объект</span><span class="sxs-lookup"><span data-stu-id="535b1-113">PNRP and BLOB</span></span>](pnrp-and-blob.md)                                    | <span data-ttu-id="535b1-114">Передает данные в структуру [**всакуерисет**](winsock-nsp-reference-links.md) во время вызовов нескольких функций.</span><span class="sxs-lookup"><span data-stu-id="535b1-114">Passes data to the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure during calls to several functions.</span></span>                                                  |
| [<span data-ttu-id="535b1-115">PNRP и ВСАКУЕРИСЕТ</span><span class="sxs-lookup"><span data-stu-id="535b1-115">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)                      | <span data-ttu-id="535b1-116">Облегчает разрешение имен и перечисление имен и облаков.</span><span class="sxs-lookup"><span data-stu-id="535b1-116">Facilitates the resolving of names and the enumeration of names and clouds.</span></span>                                                                                         |
| [<span data-ttu-id="535b1-117">**\_ИД облака \_ PNRP**</span><span class="sxs-lookup"><span data-stu-id="535b1-117">**PNRP\_CLOUD\_ID**</span></span>](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | <span data-ttu-id="535b1-118">Содержит значения, определяющие сетевое облако.</span><span class="sxs-lookup"><span data-stu-id="535b1-118">Contains the values that define a network cloud.</span></span>                                                                                                                    |
| [<span data-ttu-id="535b1-119">**пнрпклаудинфо**</span><span class="sxs-lookup"><span data-stu-id="535b1-119">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | <span data-ttu-id="535b1-120">На который указывает элемент **лпблоб** структуры [**всакуерисет**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="535b1-120">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure.</span></span>                                                            |
| [<span data-ttu-id="535b1-121">**ПНРПИНФО \_ v1**</span><span class="sxs-lookup"><span data-stu-id="535b1-121">**PNRPINFO\_V1**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | <span data-ttu-id="535b1-122">Указывает элемент **лпблоб** структуры [**всакуерисет**](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="535b1-122">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure</span></span>                                                             |
| <span data-ttu-id="535b1-123">[**ПНРПИНФО \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="535b1-123">[**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span></span>                                   | <span data-ttu-id="535b1-124">На который указывает элемент **лпблоб** структуры [**всакуерисет**](winsock-nsp-reference-links.md) , и обеспечивает поддержку непрозрачных данных, зависящих от приложения.</span><span class="sxs-lookup"><span data-stu-id="535b1-124">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure, and provides support for application-specific opaque data.</span></span> |



 

 

 
