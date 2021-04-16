---
description: Аннотация абстрактного синтаксиса One (ASN. 1) определяет следующие наборы правил, которые управляют кодированием и декодированием структур данных, передаваемых между компьютерами.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: Distinguished Encoding Rules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542695"
---
# <a name="distinguished-encoding-rules"></a><span data-ttu-id="cf6e0-103">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="cf6e0-103">Distinguished Encoding Rules</span></span>

<span data-ttu-id="cf6e0-104">Аннотация абстрактного синтаксиса One (ASN. 1) определяет следующие наборы правил, которые управляют кодированием и декодированием структур данных, передаваемых между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="cf6e0-104">Abstract Syntax Notation One (ASN.1) defines the following rule sets that govern how data structures that are being sent between computers are encoded and decoded.</span></span>

-   <span data-ttu-id="cf6e0-105">Базовые правила кодирования (ЛИЧЕСТВО)</span><span class="sxs-lookup"><span data-stu-id="cf6e0-105">Basic Encoding Rules (BER)</span></span>
-   <span data-ttu-id="cf6e0-106">Правила канонической кодировки (CER)</span><span class="sxs-lookup"><span data-stu-id="cf6e0-106">Canonical Encoding Rules (CER)</span></span>
-   <span data-ttu-id="cf6e0-107">Distinguished Encoding Rules (DER)</span><span class="sxs-lookup"><span data-stu-id="cf6e0-107">Distinguished Encoding Rules (DER)</span></span>
-   <span data-ttu-id="cf6e0-108">Правила упакованной кодировки (на)</span><span class="sxs-lookup"><span data-stu-id="cf6e0-108">Packed Encoding Rules (PER)</span></span>

<span data-ttu-id="cf6e0-109">Исходный набор правил был определен спецификацией ЛИЧЕСТВО.</span><span class="sxs-lookup"><span data-stu-id="cf6e0-109">The original rule set was defined by the BER specification.</span></span> <span data-ttu-id="cf6e0-110">CER и DER были разработаны позже как специализированные подмножества ЛИЧЕСТВО.</span><span class="sxs-lookup"><span data-stu-id="cf6e0-110">CER and DER were developed later as specialized subsets of BER.</span></span> <span data-ttu-id="cf6e0-111">В было создано в ответ на критику о объеме пропускной способности, необходимой для передачи данных с помощью ЛИЧЕСТВО или его разновидностей.</span><span class="sxs-lookup"><span data-stu-id="cf6e0-111">PER was developed in response to criticisms about the amount of bandwidth required to transmit data using BER or its variants.</span></span> <span data-ttu-id="cf6e0-112">ДЛЯ обеспечивает значительную экономию.</span><span class="sxs-lookup"><span data-stu-id="cf6e0-112">PER provides a significant savings.</span></span>

<span data-ttu-id="cf6e0-113">Протокол DER был создан для удовлетворения требований спецификации X. 509 для безопасной пересылки данных.</span><span class="sxs-lookup"><span data-stu-id="cf6e0-113">DER was created to satisfy the requirements of the X.509 specification for secure data transfer.</span></span> <span data-ttu-id="cf6e0-114">API регистрации сертификатов использует исключительно DER.</span><span class="sxs-lookup"><span data-stu-id="cf6e0-114">The Certificate Enrollment API uses DER exclusively.</span></span> <span data-ttu-id="cf6e0-115">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="cf6e0-115">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="cf6e0-116">Синтаксис преобразования DER</span><span class="sxs-lookup"><span data-stu-id="cf6e0-116">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
-   [<span data-ttu-id="cf6e0-117">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="cf6e0-117">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a><span data-ttu-id="cf6e0-118">См. также</span><span class="sxs-lookup"><span data-stu-id="cf6e0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf6e0-119">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="cf6e0-119">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="cf6e0-120">Кодирование запроса сертификата</span><span class="sxs-lookup"><span data-stu-id="cf6e0-120">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="cf6e0-121">Общие сведения о синтаксисе и кодировке ASN. 1</span><span class="sxs-lookup"><span data-stu-id="cf6e0-121">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



