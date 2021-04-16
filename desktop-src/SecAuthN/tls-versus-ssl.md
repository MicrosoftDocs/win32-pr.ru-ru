---
description: TLS — это стандарт, тесно связанный с SSL 3,0, который иногда называют &\# 0034; SSL 3,1&\# 0034;.
ms.assetid: 92b1b486-7e10-48a2-b1d2-56d4e472dbe4
title: TLS и SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac1a2e783b6f3355127a3148f1575f73119f6604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664152"
---
# <a name="tls-vs-ssl"></a><span data-ttu-id="aed72-103">TLS и SSL</span><span class="sxs-lookup"><span data-stu-id="aed72-103">TLS vs. SSL</span></span>

<span data-ttu-id="aed72-104">TLS — это стандарт, тесно связанный с SSL 3,0, который иногда называют "SSL 3,1".</span><span class="sxs-lookup"><span data-stu-id="aed72-104">TLS is a standard closely related to SSL 3.0, and is sometimes referred to as "SSL 3.1".</span></span> <span data-ttu-id="aed72-105">Протокол TLS заменяет SSL 2,0 и должен использоваться в новой разработке.</span><span class="sxs-lookup"><span data-stu-id="aed72-105">TLS supersedes SSL 2.0 and should be used in new development.</span></span> <span data-ttu-id="aed72-106">Начиная с Windows 10 версии 1607 и Windows Server 2016, протокол SSL 2,0 был удален и больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aed72-106">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

<span data-ttu-id="aed72-107">Приложения, которым требуется высокий уровень взаимодействия, должны поддерживать SSL 3,0 и TLS.</span><span class="sxs-lookup"><span data-stu-id="aed72-107">Applications that require a high level of interoperability should support SSL 3.0 and TLS.</span></span> <span data-ttu-id="aed72-108">Из-за сходства между этими двумя протоколами сведения SSL не включены в эту документацию, за исключением случаев, когда они отличаются от TLS.</span><span class="sxs-lookup"><span data-stu-id="aed72-108">Because of the similarities between these two protocols, SSL details are not included in this documentation, except where they differ from TLS.</span></span> <span data-ttu-id="aed72-109">Следующий пример относится к [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span><span class="sxs-lookup"><span data-stu-id="aed72-109">The following is from [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span></span>

<span data-ttu-id="aed72-110">«Различия между этим протоколом и SSL 3,0 не являются значительными, но они настолько важны, что TLS 1,0 и SSL 3,0 не взаимодействуют (хотя протокол TLS 1,0 включает механизм, с помощью которого реализация TLS может выполнять резервное копирование на SSL 3,0)».</span><span class="sxs-lookup"><span data-stu-id="aed72-110">"The differences between this protocol and SSL 3.0 are not dramatic, but they are significant enough that TLS 1.0 and SSL 3.0 do not interoperate (although TLS 1.0 does incorporate a mechanism by which a TLS implementation can back down to SSL 3.0)."</span></span>

 

 



