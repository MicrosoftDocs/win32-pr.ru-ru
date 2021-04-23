---
description: Объясняется, как проверить учетные данные SChannel вручную.
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: Проверка учетных данных SChannel вручную
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ec87b662cf9d3711c1ae729d2dd3b14ac5f79e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651023"
---
# <a name="manually-validating-schannel-credentials"></a><span data-ttu-id="b673b-103">Проверка учетных данных SChannel вручную</span><span class="sxs-lookup"><span data-stu-id="b673b-103">Manually Validating Schannel Credentials</span></span>

<span data-ttu-id="b673b-104">По умолчанию SChannel проверяет [*сертификат сервера*](../secgloss/s-gly.md) , вызывая функцию [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) . Однако если вы отключили эту функцию с помощью \_ \_ \_ \_ флага проверки ручного удостоверения ISC, необходимо проверить сертификат, предоставленный сервером, который пытается установить его удостоверение.</span><span class="sxs-lookup"><span data-stu-id="b673b-104">By default, Schannel validates the [*server certificate*](../secgloss/s-gly.md) by calling the [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) function; however, if you have disabled this feature using the ISC\_REQ\_MANUAL\_CRED\_VALIDATION flag, you must validate the certificate provided by the server that is attempting to establish its identity.</span></span>

<span data-ttu-id="b673b-105">Чтобы вручную проверить сертификат сервера, необходимо сначала получить его.</span><span class="sxs-lookup"><span data-stu-id="b673b-105">To manually validate the server certificate, you must first get it.</span></span> <span data-ttu-id="b673b-106">Используйте функцию [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) и укажите \_ \_ \_ значение атрибута контекста удаленного сертификата SECPKG attr \_ .</span><span class="sxs-lookup"><span data-stu-id="b673b-106">Use the [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) function and specify the SECPKG\_ATTR\_REMOTE\_CERT\_CONTEXT attribute value.</span></span> <span data-ttu-id="b673b-107">Этот атрибут возвращает структуру [**\_ контекста сертификата**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) , содержащую сертификат, предоставленный сервером.</span><span class="sxs-lookup"><span data-stu-id="b673b-107">This attribute returns a [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure containing the certificate supplied by the server.</span></span> <span data-ttu-id="b673b-108">Этот сертификат называется конечным сертификатом, так как он является последним сертификатом в цепочке сертификатов и находится дальше от [*корневого сертификата*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b673b-108">This certificate is called the leaf certificate because it is the last certificate in the certificate chain and is farthest away from the [*root certificate*](../secgloss/r-gly.md).</span></span>

<span data-ttu-id="b673b-109">С помощью конечного сертификата необходимо проверить следующее:</span><span class="sxs-lookup"><span data-stu-id="b673b-109">Using the leaf certificate you must verify the following:</span></span>

-   <span data-ttu-id="b673b-110">Цепочка сертификатов завершена, а корень — сертификат из доверенного [*центра сертификации*](../secgloss/c-gly.md) (ЦС).</span><span class="sxs-lookup"><span data-stu-id="b673b-110">The certificate chain is complete and the root is a certificate from a trusted [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>
-   <span data-ttu-id="b673b-111">Текущее время не превышает даты начала и окончания для каждого из сертификатов в цепочке сертификатов.</span><span class="sxs-lookup"><span data-stu-id="b673b-111">The current time is not beyond the begin and end dates for each of the certificates in the certificate chain.</span></span>
-   <span data-ttu-id="b673b-112">Ни один из сертификатов в цепочке сертификатов не был отозван.</span><span class="sxs-lookup"><span data-stu-id="b673b-112">None of the certificates in the certificate chain have been revoked.</span></span>
-   <span data-ttu-id="b673b-113">Глубина конечного сертификата не превышает максимально допустимую глубину, указанную в расширении сертификата.</span><span class="sxs-lookup"><span data-stu-id="b673b-113">The depth of the leaf certificate is not deeper than the maximum allowable depth specified in the certificate extension.</span></span> <span data-ttu-id="b673b-114">Эта проверка необходима, только если указана глубина.</span><span class="sxs-lookup"><span data-stu-id="b673b-114">This check is only necessary if there is a depth specified.</span></span>
-   <span data-ttu-id="b673b-115">Использование сертификата является правильным, например, [*сертификат клиента*](../secgloss/c-gly.md) не следует использовать для проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="b673b-115">The usage of the certificate is correct, for example, a [*client certificate*](../secgloss/c-gly.md) should not be used to authenticate a server.</span></span>
-   <span data-ttu-id="b673b-116">Для проверки подлинности сервера удостоверение сервера, содержащееся в конечном сертификате сервера, соответствует серверу, к которому пытается связаться клиент.</span><span class="sxs-lookup"><span data-stu-id="b673b-116">For server authentication, the server identity contained in the server's leaf certificate matches the server that the client is attempting to contact.</span></span> <span data-ttu-id="b673b-117">Как правило, клиент будет сопоставлять некоторые элементы в поле имени субъекта сертификата с IP-адресом или DNS-именем сервера.</span><span class="sxs-lookup"><span data-stu-id="b673b-117">Typically, the client will match some item in the certificate's Subject Name field to the server's IP address or DNS name.</span></span>

 

 
