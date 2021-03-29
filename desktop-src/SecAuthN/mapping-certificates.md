---
description: Сопоставление сертификатов
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Сопоставление сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816033"
---
# <a name="mapping-certificates"></a><span data-ttu-id="363a0-103">Сопоставление сертификатов</span><span class="sxs-lookup"><span data-stu-id="363a0-103">Mapping Certificates</span></span>

> [!Note]  
> <span data-ttu-id="363a0-104">Сведения в этом разделе действительны только для серверов, которым требуется проверка подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="363a0-104">The information in this topic is valid only for servers that require client authentication.</span></span>

 

<span data-ttu-id="363a0-105">Если серверное приложение требует проверки подлинности клиента, Schannel автоматически пытается сопоставить сертификат, предоставленный клиентом, с учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="363a0-105">When a server application requires client authentication, Schannel automatically attempts to map the certificate supplied by the client to a user account.</span></span>

<span data-ttu-id="363a0-106">После установки [*контекста безопасности*](../secgloss/s-gly.md) серверное приложение может использовать функцию [**куерисекуритиконтексттокен**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) для получения [*маркера доступа*](../secgloss/a-gly.md) для учетной записи пользователя, с которой был сопоставлен [*сертификат клиента*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="363a0-106">After the [*security context*](../secgloss/s-gly.md) has been established, the server application can use the [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) function to obtain an [*access token*](../secgloss/a-gly.md) for the user account to which the [*client certificate*](../secgloss/c-gly.md) was mapped.</span></span> <span data-ttu-id="363a0-107">Кроме того, сервер может использовать функцию [**имперсонатесекуритиконтекст**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) для олицетворения клиента.</span><span class="sxs-lookup"><span data-stu-id="363a0-107">Also, the server can use the [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) function to impersonate the client.</span></span>

<span data-ttu-id="363a0-108">Дополнительные сведения о проверке подлинности см. в разделе [выполнение проверки подлинности с помощью канала Schannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="363a0-108">For more information on authentication, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
