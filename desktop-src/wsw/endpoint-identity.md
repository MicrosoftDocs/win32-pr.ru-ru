---
title: Удостоверение конечной точки
description: Типы, определенные в этом разделе, используются для определения идентификатора безопасности адреса конечной точки.
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Веб-службы удостоверения конечной точки для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7a3f7b95d5fc1b926d8bafb49b06f96c7d68fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410643"
---
# <a name="endpoint-identity"></a><span data-ttu-id="36bec-106">Удостоверение конечной точки</span><span class="sxs-lookup"><span data-stu-id="36bec-106">Endpoint Identity</span></span>

<span data-ttu-id="36bec-107">Типы, определенные в этом разделе, используются для определения идентификатора безопасности адреса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="36bec-107">The types defined in this section are used to define the security identity of an endpoint address.</span></span>

<span data-ttu-id="36bec-108">Следующие элементы API являются частью отступов конечной точки:</span><span class="sxs-lookup"><span data-stu-id="36bec-108">The following API elements are part of endpoint indentity:</span></span>



| <span data-ttu-id="36bec-109">Перечисление</span><span class="sxs-lookup"><span data-stu-id="36bec-109">Enumeration</span></span>                                                       | <span data-ttu-id="36bec-110">Описание</span><span class="sxs-lookup"><span data-stu-id="36bec-110">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36bec-111">**\_тип удостоверения конечной точки WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="36bec-111">**WS\_ENDPOINT\_IDENTITY\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | <span data-ttu-id="36bec-112">Тип удостоверения конечной точки, используемый в качестве селектора для подтипов [**\_ \_ удостоверения конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span><span class="sxs-lookup"><span data-stu-id="36bec-112">The type of the endpoint identity, used as a selector for subtypes of [**WS\_ENDPOINT\_IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span></span> |



 



| <span data-ttu-id="36bec-113">Структура</span><span class="sxs-lookup"><span data-stu-id="36bec-113">Structure</span></span>                                                               | <span data-ttu-id="36bec-114">Описание</span><span class="sxs-lookup"><span data-stu-id="36bec-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36bec-115">**\_ \_ удостоверение КОНЕЧНОЙ точки WS CERT \_**</span><span class="sxs-lookup"><span data-stu-id="36bec-115">**WS\_CERT\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | <span data-ttu-id="36bec-116">Тип удостоверения конечной точки сертификата.</span><span class="sxs-lookup"><span data-stu-id="36bec-116">The type for certificate endpoint identity .</span></span>                                                 |
| [<span data-ttu-id="36bec-117">**\_ \_ удостоверение конечной точки DNS WS \_**</span><span class="sxs-lookup"><span data-stu-id="36bec-117">**WS\_DNS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | <span data-ttu-id="36bec-118">Тип для указания удостоверения конечной точки, представленного DNS-именем.</span><span class="sxs-lookup"><span data-stu-id="36bec-118">The type for specifying an endpoint identity represented by a DNS name.</span></span>                      |
| [<span data-ttu-id="36bec-119">**\_удостоверение конечной точки WS \_**</span><span class="sxs-lookup"><span data-stu-id="36bec-119">**WS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | <span data-ttu-id="36bec-120">Базовый тип для всех идентификаторов конечных точек.</span><span class="sxs-lookup"><span data-stu-id="36bec-120">The base type for all endpoint identities.</span></span>                                                   |
| [<span data-ttu-id="36bec-121">**\_ \_ удостоверение КОНЕЧНОЙ точки WS RSA \_**</span><span class="sxs-lookup"><span data-stu-id="36bec-121">**WS\_RSA\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | <span data-ttu-id="36bec-122">Введите идентификатор конечной точки RSA.</span><span class="sxs-lookup"><span data-stu-id="36bec-122">Type for RSA endpoint identity.</span></span>                                                              |
| [<span data-ttu-id="36bec-123">**\_ \_ удостоверение конечной точки имени участника-службы WS \_**</span><span class="sxs-lookup"><span data-stu-id="36bec-123">**WS\_SPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | <span data-ttu-id="36bec-124">Тип для указания удостоверения конечной точки, представленного именем участника-службы (SPN).</span><span class="sxs-lookup"><span data-stu-id="36bec-124">The type for specifying an endpoint identity represented by an SPN (service principal name).</span></span> |
| [<span data-ttu-id="36bec-125">**WS — \_ неизвестное \_ \_ удостоверение конечной точки**</span><span class="sxs-lookup"><span data-stu-id="36bec-125">**WS\_UNKNOWN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | <span data-ttu-id="36bec-126">Тип для идентификатора неизвестной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="36bec-126">The type for an unknown endpoint identity.</span></span>                                                   |
| [<span data-ttu-id="36bec-127">**\_ \_ удостоверение конечной точки имени участника-пользователя \_**</span><span class="sxs-lookup"><span data-stu-id="36bec-127">**WS\_UPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | <span data-ttu-id="36bec-128">Тип для указания удостоверения конечной точки, представленного именем участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="36bec-128">The type for specifying an endpoint identity represented by a UPN (user principal name).</span></span>     |



 

 

 




