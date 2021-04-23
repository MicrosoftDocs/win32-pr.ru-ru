---
description: Реализует протокол дайджест-доступа, протокол упрощенной проверки подлинности для использования с протоколом HTTP или простым уровнем безопасности проверки подлинности.
ms.assetid: 0b7d67c9-00ac-4b04-bf8e-97aaf1020108
title: Microsoft Digest SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d6ae88935e540a4969ee764fd26f8daba8686c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650514"
---
# <a name="microsoft-digest-ssp"></a><span data-ttu-id="e88c8-103">Microsoft Digest SSP</span><span class="sxs-lookup"><span data-stu-id="e88c8-103">Microsoft Digest SSP</span></span>

<span data-ttu-id="e88c8-104">Microsoft Digest — это [*поставщик услуг обеспечения безопасности*](../secgloss/s-gly.md) (SSP), который реализует протокол дайджест-доступа, протокол упрощенной проверки подлинности для сторон, участвующих в обмене данными по протоколу HTTP или на основе простой проверки подлинности на уровне безопасности (SASL).</span><span class="sxs-lookup"><span data-stu-id="e88c8-104">Microsoft Digest is a [*security support provider*](../secgloss/s-gly.md) (SSP) that implements the Digest Access protocol, a lightweight authentication protocol for parties involved in Hypertext Transfer Protocol (HTTP) or Simple Authentication Security Layer (SASL) based communications.</span></span>

<span data-ttu-id="e88c8-105">Microsoft Digest предоставляет простой механизм реагирования на запрос для проверки подлинности клиентов.</span><span class="sxs-lookup"><span data-stu-id="e88c8-105">Microsoft Digest provides a simple challenge response mechanism for authenticating clients.</span></span> <span data-ttu-id="e88c8-106">Этот поставщик общих служб предназначен для использования клиентскими и серверными приложениями с использованием протокола HTTP или связи на основе SASL.</span><span class="sxs-lookup"><span data-stu-id="e88c8-106">This SSP is intended for use by client/server applications using HTTP or SASL based communications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e88c8-107">Дайджест-проверка подлинности не поддерживается в лесах.</span><span class="sxs-lookup"><span data-stu-id="e88c8-107">Digest authentication is not supported across forests.</span></span>

 

<span data-ttu-id="e88c8-108">В следующих разделах приводятся сведения о дайджест-ПОСТАВЩИКе Microsoft Digest.</span><span class="sxs-lookup"><span data-stu-id="e88c8-108">The following sections provide information about Microsoft Digest SSP.</span></span>

-   [<span data-ttu-id="e88c8-109">Протокол дайджест-доступа</span><span class="sxs-lookup"><span data-stu-id="e88c8-109">The Digest Access Protocol</span></span>](the-digest-access-protocol.md)
-   [<span data-ttu-id="e88c8-110">Качество защиты и шифров</span><span class="sxs-lookup"><span data-stu-id="e88c8-110">Quality of Protection and Ciphers</span></span>](quality-of-protection-and-ciphers.md)
-   [<span data-ttu-id="e88c8-111">Дайджест-проверка подлинности Microsoft</span><span class="sxs-lookup"><span data-stu-id="e88c8-111">Microsoft Digest Authentication</span></span>](microsoft-digest-authentication.md)
-   [<span data-ttu-id="e88c8-112">Спецификации IETF для Microsoft Digest SSP</span><span class="sxs-lookup"><span data-stu-id="e88c8-112">IETF Specifications for Microsoft Digest SSP</span></span>](ietf-specifications-for-microsoft-digest-ssp.md)

 

 
