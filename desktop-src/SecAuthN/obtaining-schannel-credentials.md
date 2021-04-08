---
description: В процессе проверки подлинности Schannel требуются учетные данные. Клиент и сервер должны получить действительные учетные данные, чтобы установить контекст безопасности для обмена сообщениями. Пример, демонстрирующий эту процедуру, см. в разделе Получение учетных данных.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Получение учетных данных SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813608"
---
# <a name="obtaining-schannel-credentials"></a><span data-ttu-id="09129-104">Получение учетных данных SChannel</span><span class="sxs-lookup"><span data-stu-id="09129-104">Obtaining Schannel Credentials</span></span>

<span data-ttu-id="09129-105">В процессе проверки подлинности Schannel требуются учетные данные. Клиент и сервер должны получить действительные учетные данные, чтобы установить [*контекст безопасности*](../secgloss/s-gly.md) для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="09129-105">Credentials are required by the Schannel authentication process; both client and server must obtain valid credentials to establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="09129-106">Пример, демонстрирующий эту процедуру, см. в разделе [Получение учетных данных](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="09129-106">For an example that demonstrates this procedure, see [Getting credentials](getting-a-certificate-for-schannel.md).</span></span>

<span data-ttu-id="09129-107">Приложение получает учетные данные путем вызова функции [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , которая возвращает маркер запрошенным учетным данным.</span><span class="sxs-lookup"><span data-stu-id="09129-107">Your application obtains credentials by calling the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, which returns a handle to the requested credentials.</span></span> <span data-ttu-id="09129-108">Так как дескрипторы учетных данных используются для хранения сведений о конфигурации, один и тот же дескриптор не может использоваться как для операций на стороне клиента, так и для операции на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="09129-108">Because credentials handles are used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="09129-109">Это означает, что приложения, поддерживающие как клиентские, так и серверные соединения, должны получить как минимум два дескриптора учетных данных.</span><span class="sxs-lookup"><span data-stu-id="09129-109">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="09129-110">В Windows XP структура учетного записи [**SChannel \_**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) содержит следующие указания:</span><span class="sxs-lookup"><span data-stu-id="09129-110">In Windows XP, an [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure specifies the following:</span></span>

-   <span data-ttu-id="09129-111">Протокол безопасности</span><span class="sxs-lookup"><span data-stu-id="09129-111">A security protocol</span></span>
-   <span data-ttu-id="09129-112">Допустимые шифры</span><span class="sxs-lookup"><span data-stu-id="09129-112">The allowable ciphers</span></span>
-   <span data-ttu-id="09129-113">Минимальная и максимальная стойкости шифра</span><span class="sxs-lookup"><span data-stu-id="09129-113">Minimum and maximum cipher strengths</span></span>
-   <span data-ttu-id="09129-114">Сертификат [*X. 509*](../secgloss/x-gly.md) , используемый для проверки подлинности — требуется для сервера, необязательно для клиента, если сервер не запрашивает проверку подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="09129-114">An [*X.509*](../secgloss/x-gly.md) certificate used for authentication — Required for server, optional for client unless server requests client authentication.</span></span>

<span data-ttu-id="09129-115">Передайте в функцию [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) структуру [**\_ cred**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (с помощью параметра *паусдата* ).</span><span class="sxs-lookup"><span data-stu-id="09129-115">Pass the [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure (via the *pAuthData* parameter) to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span> <span data-ttu-id="09129-116">Эта функция возвращает маркер учетных данных, необходимый для установки [*контекста безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="09129-116">This function returns the credentials handle required to establish a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="09129-117">Подробные сведения о настройке шифров, используемых с SChannel, см. в разделе [Указание шифров SChannel и стойкости шифра](specifying-schannel-ciphers-and-cipher-strengths.md).</span><span class="sxs-lookup"><span data-stu-id="09129-117">For detailed information on setting the ciphers used with Schannel, see [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).</span></span>

<span data-ttu-id="09129-118">Сведения о сертификатах см. в статье [функции хранилища сертификатов и](../seccrypto/cryptography-functions.md)сертификатов.</span><span class="sxs-lookup"><span data-stu-id="09129-118">For information about certificates, see [Certificate and Certificate Store Functions](../seccrypto/cryptography-functions.md).</span></span>

<span data-ttu-id="09129-119">Пример, демонстрирующий открытие [*хранилища сертификатов*](../secgloss/c-gly.md) и поиск сертификата, используемого для проверки подлинности Schannel, см. в разделе [Получение сертификата](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="09129-119">For an example that demonstrates opening a [*certificate store*](../secgloss/c-gly.md) and locating a certificate to use for Schannel authentication, see [Getting a Certificate](getting-a-certificate-for-schannel.md).</span></span>

 

 
