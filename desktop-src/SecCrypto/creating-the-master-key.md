---
description: Главный ключ — это материал основных данных, из которого производятся другие ключи.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Создание главного ключа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541010"
---
# <a name="creating-the-master-key"></a><span data-ttu-id="6063b-103">Создание главного ключа</span><span class="sxs-lookup"><span data-stu-id="6063b-103">Creating the Master Key</span></span>

<span data-ttu-id="6063b-104">[*Главный ключ*](../secgloss/m-gly.md) — это материал основных данных, из которого производятся другие ключи.</span><span class="sxs-lookup"><span data-stu-id="6063b-104">A [*master key*](../secgloss/m-gly.md) is key data material from which other keys are derived.</span></span> <span data-ttu-id="6063b-105">В зависимости от используемого протокола и набора шифров главный ключ может иметь длину от 5 до 48 байт.</span><span class="sxs-lookup"><span data-stu-id="6063b-105">Depending on the protocol and cipher suite used, the master key can be from 5 to 48 bytes in length.</span></span> <span data-ttu-id="6063b-106">Для CSP [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) этот главный ключ создается на стороне клиента и передается на сервер на конверте RSA.</span><span class="sxs-lookup"><span data-stu-id="6063b-106">For the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) CSP, the master key is created by the client-side and transferred to the server in an RSA envelope.</span></span> <span data-ttu-id="6063b-107">Для CSP/Счаннел [*Диффи-Хелмана*](../secgloss/d-gly.md)главный ключ создается путем выполнения Diffie-Hellman обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="6063b-107">For a [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel CSP, the master key is created by performing a Diffie-Hellman key exchange.</span></span>

<span data-ttu-id="6063b-108">Код для создания и обмена главными ключами демонстрируется в:</span><span class="sxs-lookup"><span data-stu-id="6063b-108">Code for creating and exchanging master keys is demonstrated in:</span></span>

-   [<span data-ttu-id="6063b-109">Код клиента Диффи-Хелмана для создания главного ключа</span><span class="sxs-lookup"><span data-stu-id="6063b-109">Diffie-Hellman Client Code for Creating the Master Key</span></span>](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="6063b-110">Серверный код Диффи-Хелмана для создания главного ключа</span><span class="sxs-lookup"><span data-stu-id="6063b-110">Diffie-Hellman Server Code for Creating the Master Key</span></span>](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="6063b-111">Код клиента RSA для создания главного ключа</span><span class="sxs-lookup"><span data-stu-id="6063b-111">RSA Client Code for Creating the Master Key</span></span>](rsa-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="6063b-112">Код сервера RSA для создания главного ключа</span><span class="sxs-lookup"><span data-stu-id="6063b-112">RSA Server Code for Creating the Master Key</span></span>](rsa-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="6063b-113">Указание алгоритмов</span><span class="sxs-lookup"><span data-stu-id="6063b-113">Specifying the Algorithms</span></span>](specifying-the-algorithms.md)

 

 
