---
description: Алгоритмы могут поддерживаться поставщиком служб шифрования Microsoft RSA/SChannel.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: Алгоритмы поставщика RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9dc3293b0938e9c9e89e955b26eac2a40ac198b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662427"
---
# <a name="rsaschannel-provider-algorithms"></a><span data-ttu-id="017b3-103">Алгоритмы поставщика RSA/SChannel</span><span class="sxs-lookup"><span data-stu-id="017b3-103">RSA/Schannel Provider Algorithms</span></span>

<span data-ttu-id="017b3-104">[](../secgloss/r-gly.md) / Поставщик криптографии [*SChannel*](../secgloss/s-gly.md) для Microsoft RSA может поддерживать следующие алгоритмы.</span><span class="sxs-lookup"><span data-stu-id="017b3-104">The following algorithms might be supported by the Microsoft [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) Cryptographic Provider.</span></span>



| <span data-ttu-id="017b3-105">Идентификатор алгоритма</span><span class="sxs-lookup"><span data-stu-id="017b3-105">Algorithm ID</span></span>    | <span data-ttu-id="017b3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="017b3-106">Description</span></span>                                                                                                                         | <span data-ttu-id="017b3-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="017b3-107">Comments</span></span>                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="017b3-108">КАЛГ \_ RSA \_ KEYX</span><span class="sxs-lookup"><span data-stu-id="017b3-108">CALG\_RSA\_KEYX</span></span> | <span data-ttu-id="017b3-109">[ *Алгоритм обмена ключами* открытого ключа RSA](../secgloss/k-gly.md)</span><span class="sxs-lookup"><span data-stu-id="017b3-109">RSA public key [*key exchange algorithm*](../secgloss/k-gly.md)</span></span> | <span data-ttu-id="017b3-110">Длина ключа: может быть задано, 384 бит на 16 384 бит по 8 битам.</span><span class="sxs-lookup"><span data-stu-id="017b3-110">Key length: Can be set, 384 bits to 16,384 bits in 8 bit increments.</span></span> <span data-ttu-id="017b3-111">Длина ключа по умолчанию: 1 024 бит.</span><span class="sxs-lookup"><span data-stu-id="017b3-111">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="017b3-112">\_MD5 калг</span><span class="sxs-lookup"><span data-stu-id="017b3-112">CALG\_MD5</span></span>       | <span data-ttu-id="017b3-113">Алгоритм хэширования MD5.</span><span class="sxs-lookup"><span data-stu-id="017b3-113">MD5 hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="017b3-114">Предоставляется только для хэширования.</span><span class="sxs-lookup"><span data-stu-id="017b3-114">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="017b3-115">\_SHA калг</span><span class="sxs-lookup"><span data-stu-id="017b3-115">CALG\_SHA</span></span>       | <span data-ttu-id="017b3-116">Алгоритм хэширования SHA.</span><span class="sxs-lookup"><span data-stu-id="017b3-116">SHA hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="017b3-117">Необходимо использовать для подписей DSS.</span><span class="sxs-lookup"><span data-stu-id="017b3-117">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="017b3-118">КАЛГ \_ RC2</span><span class="sxs-lookup"><span data-stu-id="017b3-118">CALG\_RC2</span></span>       | <span data-ttu-id="017b3-119">Алгоритм шифрования блока RC2.</span><span class="sxs-lookup"><span data-stu-id="017b3-119">RC2 block encryption algorithm.</span></span>                                                                                                     | <span data-ttu-id="017b3-120">Длина ключа: 40 до 88 бит</span><span class="sxs-lookup"><span data-stu-id="017b3-120">Key length: 40 to 88 bits</span></span>                                                                                       |
| <span data-ttu-id="017b3-121">КАЛГ \_ RC4</span><span class="sxs-lookup"><span data-stu-id="017b3-121">CALG\_RC4</span></span>       | <span data-ttu-id="017b3-122">Алгоритм шифрования потока RC4.</span><span class="sxs-lookup"><span data-stu-id="017b3-122">RC4 stream encryption algorithm.</span></span>                                                                                                    | <span data-ttu-id="017b3-123">Длина ключа: 40 до 88 бит</span><span class="sxs-lookup"><span data-stu-id="017b3-123">Key length: 40 to 88 bits</span></span>                                                                                       |



 

 

 
