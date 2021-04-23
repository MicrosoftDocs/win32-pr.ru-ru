---
description: Ключи сеанса — это ключи, которые создаются для использования в одном сеансе связи.
ms.assetid: 18bf2023-084d-400d-b60d-1ba51ce6a2bc
title: Ключи сеанса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4089f9ab5a0ae6889463c1b24c2eecb376c7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684326"
---
# <a name="session-keys"></a><span data-ttu-id="09990-103">Ключи сеанса</span><span class="sxs-lookup"><span data-stu-id="09990-103">Session Keys</span></span>

<span data-ttu-id="09990-104">[*Ключи сеанса*](../secgloss/s-gly.md) — это ключи, которые создаются для использования в одном сеансе связи.</span><span class="sxs-lookup"><span data-stu-id="09990-104">[*Session keys*](../secgloss/s-gly.md) are keys that are generated to be used in a single communication session.</span></span> <span data-ttu-id="09990-105">Ключи сеанса часто изменяются и отбрасываются, когда они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="09990-105">Session keys are frequently changed and are discarded when they are no longer needed.</span></span> <span data-ttu-id="09990-106">Например, TLS использует отдельный ключ сеанса для каждого подключения, а S/MIME использует отдельный сеансовый ключ для каждого сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="09990-106">For example, TLS uses a separate session key for each connection and S/MIME uses a separate session key for each email message.</span></span> <span data-ttu-id="09990-107">Обычно в качестве ключа сеанса используется [*симметричный ключ*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="09990-107">Typically a [*symmetric key*](../secgloss/s-gly.md) is used as the session key.</span></span>

<span data-ttu-id="09990-108">Ключи сеанса являются временными.</span><span class="sxs-lookup"><span data-stu-id="09990-108">Session keys are volatile.</span></span> <span data-ttu-id="09990-109">Приложения могут сохранять эти ключи для последующего использования или для передачи другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="09990-109">Applications can save these keys for later use or for transmission to other users.</span></span> <span data-ttu-id="09990-110">Дополнительные сведения см. в статье [хранилище криптографических ключей и Exchange](cryptographic-key-storage-and-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="09990-110">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md).</span></span>

 

 
