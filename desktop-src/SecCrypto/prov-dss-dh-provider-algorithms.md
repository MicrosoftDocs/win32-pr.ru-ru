---
description: Алгоритмы, поддерживаемые поставщиком служб Microsoft Base DSS и Diffie-Hellman.
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: Алгоритмы поставщика PROV_DSS_DH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647721"
---
# <a name="prov_dss_dh-provider-algorithms"></a><span data-ttu-id="c5288-103">\_ \_ Алгоритмы поставщика DH Prov DSS</span><span class="sxs-lookup"><span data-stu-id="c5288-103">PROV\_DSS\_DH Provider Algorithms</span></span>

<span data-ttu-id="c5288-104">В следующей таблице перечислены алгоритмы, поддерживаемые поставщиком служб Microsoft Base DSS и Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="c5288-104">The following table lists the algorithms supported by the Microsoft Base DSS and Diffie-Hellman Cryptographic Provider.</span></span>



| <span data-ttu-id="c5288-105">Идентификатор алгоритма</span><span class="sxs-lookup"><span data-stu-id="c5288-105">Algorithm ID</span></span>      | <span data-ttu-id="c5288-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c5288-106">Description</span></span>                                 | <span data-ttu-id="c5288-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5288-107">Comments</span></span>                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5288-108">\_MD5 калг</span><span class="sxs-lookup"><span data-stu-id="c5288-108">CALG\_MD5</span></span>         | <span data-ttu-id="c5288-109">Алгоритм хэширования MD5.</span><span class="sxs-lookup"><span data-stu-id="c5288-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="c5288-110">Предоставляется только для хэширования.</span><span class="sxs-lookup"><span data-stu-id="c5288-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="c5288-111">\_SHA калг</span><span class="sxs-lookup"><span data-stu-id="c5288-111">CALG\_SHA</span></span>         | <span data-ttu-id="c5288-112">Алгоритм хэширования SHA.</span><span class="sxs-lookup"><span data-stu-id="c5288-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="c5288-113">Необходимо использовать для подписей DSS.</span><span class="sxs-lookup"><span data-stu-id="c5288-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="c5288-114">КАЛГ \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="c5288-114">CALG\_SHA1</span></span>        | <span data-ttu-id="c5288-115">То же, что и КАЛГ \_ SHA.</span><span class="sxs-lookup"><span data-stu-id="c5288-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="c5288-116">Без комментариев.</span><span class="sxs-lookup"><span data-stu-id="c5288-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="c5288-117">\_знак DSS \_ калг</span><span class="sxs-lookup"><span data-stu-id="c5288-117">CALG\_DSS\_SIGN</span></span>   | <span data-ttu-id="c5288-118">Алгоритм подписи открытого и закрытого ключей DSS.</span><span class="sxs-lookup"><span data-stu-id="c5288-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="c5288-119">Длина ключа: может быть задано, 512 бит на 1 024 бит в 64 бит.</span><span class="sxs-lookup"><span data-stu-id="c5288-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="c5288-120">Длина ключа по умолчанию: 1 024 бит.</span><span class="sxs-lookup"><span data-stu-id="c5288-120">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="c5288-121">КАЛГ \_ DH \_ SF</span><span class="sxs-lookup"><span data-stu-id="c5288-121">CALG\_DH\_SF</span></span>      | <span data-ttu-id="c5288-122">Обмен ключами хранения и пересылки D-H.</span><span class="sxs-lookup"><span data-stu-id="c5288-122">Store and Forward D-H key exchange.</span></span>         | <span data-ttu-id="c5288-123">Длина ключа: может быть задано, 384 бит на 512 бит по 8 битам.</span><span class="sxs-lookup"><span data-stu-id="c5288-123">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="c5288-124">Длина ключа по умолчанию: 512 бит.</span><span class="sxs-lookup"><span data-stu-id="c5288-124">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="c5288-125">КАЛГ \_ DH \_ ефем</span><span class="sxs-lookup"><span data-stu-id="c5288-125">CALG\_DH\_EPHEM</span></span>   | <span data-ttu-id="c5288-126">Обмен ключами эфемерного D-H.</span><span class="sxs-lookup"><span data-stu-id="c5288-126">Ephemeral D-H key exchange.</span></span>                 | <span data-ttu-id="c5288-127">Длина ключа: может быть задано, 384 бит на 512 бит по 8 битам.</span><span class="sxs-lookup"><span data-stu-id="c5288-127">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="c5288-128">Длина ключа по умолчанию: 512 бит.</span><span class="sxs-lookup"><span data-stu-id="c5288-128">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="c5288-129">КАЛГ \_ цилинк \_ главный ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="c5288-129">CALG\_CYLINK\_MEK</span></span> | <span data-ttu-id="c5288-130">40-разрядный вариант ключа DES.</span><span class="sxs-lookup"><span data-stu-id="c5288-130">A 40-bit variant of a DES key.</span></span>              | <span data-ttu-id="c5288-131">Длина ключа: 40 бит.</span><span class="sxs-lookup"><span data-stu-id="c5288-131">Key Length: 40 bits.</span></span>                                                                                            |



 

 

 




