---
description: Все обычные операции RSA/SChannel и Диффи-Хелмана и SChannel используют \_ пару открытого и закрытого ключей в кэйексчанже.
ms.assetid: e12afdbb-7ba8-444e-a43f-e262b481a353
title: Использование пары открытого и закрытого ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dba78c487c433875ed23ce3f2f3c87a86b07c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683943"
---
# <a name="publicprivate-key-pair-usage"></a><span data-ttu-id="736e3-103">Использование пары открытого и закрытого ключей</span><span class="sxs-lookup"><span data-stu-id="736e3-103">Public/Private Key Pair Usage</span></span>

<span data-ttu-id="736e3-104">Все обычные операции [*RSA*](../secgloss/r-gly.md)/Счаннел и [*Диффи-Хелмана*](../secgloss/d-gly.md)/счаннел используют \_ пару из [*открытого и закрытого ключей*](../secgloss/p-gly.md)кэйексчанже.</span><span class="sxs-lookup"><span data-stu-id="736e3-104">All normal [*RSA*](../secgloss/r-gly.md)/Schannel and [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel operations use the AT\_KEYEXCHANGE [*public/private key pair*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="736e3-105">Чтобы обеспечить [*проверку подлинности*](../secgloss/a-gly.md)сервера, на стороне сервера операций SChannel должен быть доступ к сертификату [*X. 509*](../secgloss/x-gly.md) , содержащему открытый ключ, и доступу к соответствующему [*закрытому ключу*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="736e3-105">To provide server [*authentication*](../secgloss/a-gly.md), the server-side of Schannel operations must have access to its [*X.509*](../secgloss/x-gly.md) certificate containing its public key and access to the matching [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="736e3-106">Клиентская сторона [*SChannel*](../secgloss/s-gly.md) требует сертификат с открытым ключом и доступом к его закрытому ключу, если реализована проверка подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="736e3-106">The client-side of [*Schannel*](../secgloss/s-gly.md) needs its certificate with its public key and access to its private key if client authentication is implemented.</span></span>

<span data-ttu-id="736e3-107">Так как в механизмах протокола SChannel никогда не используется \_ пара открытого и закрытого ключей сигнатуры, эта пара ключей не должна поддерживаться новым CSP, поддерживающим только RSA, SChannel или Диффи-Хелмана и SChannel.</span><span class="sxs-lookup"><span data-stu-id="736e3-107">Since Schannel protocol engines never use the AT\_SIGNATURE public/private key pair, that key pair need not be supported by a new CSP supporting only RSA/Schannel or Diffie-Hellman/Schannel.</span></span>

<span data-ttu-id="736e3-108">Если подсистема протокола использует протокол экспорта SSL 3,0 с \_ парой ключей кэйексчанже, размер которых превышает 512 бит, сервер должен использовать дополнительную пару ключей RSA.</span><span class="sxs-lookup"><span data-stu-id="736e3-108">If a protocol engine uses an SSL 3.0 export cipher suite with an AT\_KEYEXCHANGE key pair larger than 512 bits, the server must use an additional RSA key pair.</span></span> <span data-ttu-id="736e3-109">Эта дополнительная пара ключей всегда имеет ровно 512 бит и может быть эфемерной.</span><span class="sxs-lookup"><span data-stu-id="736e3-109">This additional key pair is always exactly 512 bits and it can be ephemeral.</span></span> <span data-ttu-id="736e3-110">Пара сохраняется как \_ элемент at кэйексчанже в контейнере ключей, принадлежащих подсистеме протокола.</span><span class="sxs-lookup"><span data-stu-id="736e3-110">The pair is stored as an AT\_KEYEXCHANGE element in a key container owned by the protocol engine.</span></span> <span data-ttu-id="736e3-111">Маркер этого контейнера ключей обычно запрашивается при запуске механизма протокола.</span><span class="sxs-lookup"><span data-stu-id="736e3-111">A handle to this key container is typically acquired at protocol engine startup.</span></span>

<span data-ttu-id="736e3-112">Diffie-Hellman поддерживает только [*калг \_ DH \_ ефем*](../secgloss/c-gly.md) и использует обычные открытые ключи RSA или DSS.</span><span class="sxs-lookup"><span data-stu-id="736e3-112">Diffie-Hellman supports only [*CALG\_DH\_EPHEM*](../secgloss/c-gly.md) and uses normal RSA or DSS public keys.</span></span>

 

 
