---
description: В следующей таблице перечислены алгоритмы, поддерживаемые поставщиком служб шифрования Microsoft DSS.
ms.assetid: 2a7aecf8-e242-4087-83ee-aaa637a9ec71
title: Алгоритмы поставщика DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0bd9346da7a9ab1490e2646d9d2559c07359b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647355"
---
# <a name="dss-provider-algorithms"></a><span data-ttu-id="df46b-103">Алгоритмы поставщика DSS</span><span class="sxs-lookup"><span data-stu-id="df46b-103">DSS Provider Algorithms</span></span>

<span data-ttu-id="df46b-104">В следующей таблице перечислены алгоритмы, поддерживаемые поставщиком служб шифрования Microsoft DSS.</span><span class="sxs-lookup"><span data-stu-id="df46b-104">The following table lists the algorithms supported by the Microsoft DSS Cryptographic Provider.</span></span>



| <span data-ttu-id="df46b-105">Идентификатор алгоритма</span><span class="sxs-lookup"><span data-stu-id="df46b-105">Algorithm ID</span></span>    | <span data-ttu-id="df46b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="df46b-106">Description</span></span>                                 | <span data-ttu-id="df46b-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df46b-107">Comments</span></span>                                                                                                        |
|-----------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df46b-108">\_MD5 калг</span><span class="sxs-lookup"><span data-stu-id="df46b-108">CALG\_MD5</span></span>       | <span data-ttu-id="df46b-109">Алгоритм хэширования MD5.</span><span class="sxs-lookup"><span data-stu-id="df46b-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="df46b-110">Предоставляется только для хэширования.</span><span class="sxs-lookup"><span data-stu-id="df46b-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="df46b-111">\_SHA калг</span><span class="sxs-lookup"><span data-stu-id="df46b-111">CALG\_SHA</span></span>       | <span data-ttu-id="df46b-112">Алгоритм хэширования SHA.</span><span class="sxs-lookup"><span data-stu-id="df46b-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="df46b-113">Необходимо использовать для подписей DSS.</span><span class="sxs-lookup"><span data-stu-id="df46b-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="df46b-114">КАЛГ \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="df46b-114">CALG\_SHA1</span></span>      | <span data-ttu-id="df46b-115">То же, что и КАЛГ \_ SHA.</span><span class="sxs-lookup"><span data-stu-id="df46b-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="df46b-116">Без комментариев.</span><span class="sxs-lookup"><span data-stu-id="df46b-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="df46b-117">\_знак DSS \_ калг</span><span class="sxs-lookup"><span data-stu-id="df46b-117">CALG\_DSS\_SIGN</span></span> | <span data-ttu-id="df46b-118">Алгоритм подписи открытого и закрытого ключей DSS.</span><span class="sxs-lookup"><span data-stu-id="df46b-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="df46b-119">Длина ключа: может быть задано, 512 бит на 1 024 бит в 64 бит.</span><span class="sxs-lookup"><span data-stu-id="df46b-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="df46b-120">Длина ключа по умолчанию: 1 024 бит.</span><span class="sxs-lookup"><span data-stu-id="df46b-120">Default key length: 1,024 bits.</span></span><br/> |



 

 

 




