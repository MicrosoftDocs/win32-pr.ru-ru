---
description: Службы сертификатов поддерживают запросы сертификатов на основе формата PKCS \# 10 и формата Keygen (Netscape). Службы сертификатов также поддерживают \# запросы на обновление PKCS 7 и запросы синтаксиса сообщений (CMS).
ms.assetid: 6321ce99-f5d1-4d72-a062-99cffb543731
title: Requests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7870e09d930fb06d50f0cc8acfff1270db1c92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683816"
---
# <a name="requests"></a><span data-ttu-id="6f614-104">Requests</span><span class="sxs-lookup"><span data-stu-id="6f614-104">Requests</span></span>

<span data-ttu-id="6f614-105">Службы сертификатов поддерживают [*запросы сертификатов*](../secgloss/c-gly.md) на основе формата PKCS \# 10 и формата Keygen (Netscape).</span><span class="sxs-lookup"><span data-stu-id="6f614-105">Certificate Services supports [*certificate requests*](../secgloss/c-gly.md) based on the PKCS \#10 format and the Keygen (Netscape) format.</span></span> <span data-ttu-id="6f614-106">Службы сертификатов также поддерживают \# запросы на обновление PKCS 7 и запросы синтаксиса сообщений (CMS).</span><span class="sxs-lookup"><span data-stu-id="6f614-106">Certificate Services also supports PKCS \#7 renewal requests and Cryptographic Message Syntax (CMS) requests.</span></span>

<span data-ttu-id="6f614-107">Службы сертификатов также предоставляют интерфейс [интерфейса ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) , который содержит методы для отправки запроса на сертификат и (если запрос утвержден) для получения полученного сертификата.</span><span class="sxs-lookup"><span data-stu-id="6f614-107">Certificate Services also provides an [ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) interface, which contains methods for submitting a certificate request and (if the request is approved) for receiving the resulting issued certificate.</span></span>

<span data-ttu-id="6f614-108">Дополнительные интерфейсы, связанные с безопасностью, доступны в [элементе управления регистрации сертификатов](certificate-enrollment-control.md).</span><span class="sxs-lookup"><span data-stu-id="6f614-108">Additional security-related interfaces are available in the [Certificate Enrollment Control](certificate-enrollment-control.md).</span></span>

 

 
