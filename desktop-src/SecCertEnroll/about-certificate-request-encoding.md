---
description: В PKI Майкрософт запросы на сертификаты отправляются с клиентских компьютеров в центры сертификации (CAs) в виде двоичной строки, содержащей последовательность закодированных структур данных.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Кодирование запроса сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd9dfedede4c7b10d4968242b1d27ad11e2b6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813752"
---
# <a name="certificate-request-encoding"></a><span data-ttu-id="a4107-103">Кодирование запроса сертификата</span><span class="sxs-lookup"><span data-stu-id="a4107-103">Certificate Request Encoding</span></span>

<span data-ttu-id="a4107-104">В PKI Майкрософт запросы на сертификаты отправляются с клиентских компьютеров в центры сертификации (CAs) в виде двоичной строки, содержащей последовательность закодированных структур данных.</span><span class="sxs-lookup"><span data-stu-id="a4107-104">In a Microsoft PKI, certificate requests are sent from client computers to certification authorities (CAs) as a binary string that contains a sequence of encoded data structures.</span></span> <span data-ttu-id="a4107-105">API регистрации сертификатов использует синтаксическую нотацию (ASN. 1) для описания и кодирования этих структур.</span><span class="sxs-lookup"><span data-stu-id="a4107-105">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to describe and encode these structures.</span></span> <span data-ttu-id="a4107-106">Для целей этой документации ASN. 1 можно разделить на синтаксические правила (ISO 8824), описывающие структуры данных, и правила кодирования (ISO 8825), которые определяют способ кодирования данных для передачи по сети.</span><span class="sxs-lookup"><span data-stu-id="a4107-106">For the purposes of this documentation, ASN.1 can be conceptually divided into the syntax rules (ISO 8824) that describe the data structures and the encoding rules (ISO 8825) that specify how the data is to be encoded for network transmission.</span></span> <span data-ttu-id="a4107-107">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a4107-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a4107-108">Общие сведения о синтаксисе и кодировке ASN. 1</span><span class="sxs-lookup"><span data-stu-id="a4107-108">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [<span data-ttu-id="a4107-109">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="a4107-109">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
-   [<span data-ttu-id="a4107-110">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="a4107-110">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)

## <a name="related-topics"></a><span data-ttu-id="a4107-111">См. также</span><span class="sxs-lookup"><span data-stu-id="a4107-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4107-112">Сведения об API регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="a4107-112">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



