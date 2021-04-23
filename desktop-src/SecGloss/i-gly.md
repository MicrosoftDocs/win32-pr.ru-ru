---
description: Содержит определения терминов безопасности, начинающихся с буквы I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: af511aed-88f5-4b12-ad44-317925297f70
title: I (глоссарий по безопасности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d3e727128c2494f313bdffc879b5c5e47a28ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081128"
---
# <a name="i-security-glossary"></a><span data-ttu-id="f129d-103">I (глоссарий по безопасности)</span><span class="sxs-lookup"><span data-stu-id="f129d-103">I (Security Glossary)</span></span>

<span data-ttu-id="f129d-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [р](h-gly.md) . J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="f129d-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="f129d-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**</span><span class="sxs-lookup"><span data-stu-id="f129d-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**</span></span>
</dt> <dd>

<span data-ttu-id="f129d-106">Программные службы, поддерживающие создание, настройку и управление веб-сайтом, а также другие функции Интернета.</span><span class="sxs-lookup"><span data-stu-id="f129d-106">Software services that support website creation, configuration, and management, along with other Internet functions.</span></span> <span data-ttu-id="f129d-107">Службы IIS включают протокол NNTP, протокол FTP (FTP) и протокол SMTP (Simple Mail).</span><span class="sxs-lookup"><span data-stu-id="f129d-107">Internet Information Services include Network News Transfer Protocol (NNTP), File Transfer Protocol (FTP), and Simple Mail Transfer Protocol (SMTP).</span></span> <span data-ttu-id="f129d-108">Службы IIS содержат различные функции для обеспечения безопасности, позволяют приложениям CGI и обеспечивают поддержку серверов gopher и FTP.</span><span class="sxs-lookup"><span data-stu-id="f129d-108">IIS incorporates various functions for security, allows for CGI applications, and provides for Gopher and FTP servers.</span></span>

</dd> <dt>

<span data-ttu-id="f129d-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**олицетворения**</span><span class="sxs-lookup"><span data-stu-id="f129d-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="f129d-110">Механизм, позволяющий серверному процессу запускаться с использованием учетных данных безопасности клиента или другого пользователя, использующего учетные данные.</span><span class="sxs-lookup"><span data-stu-id="f129d-110">A mechanism that allows a server process to run by using the security credentials of the client or some other user using the credentials.</span></span> <span data-ttu-id="f129d-111">Когда сервер олицетворяет клиента, любые операции, выполняемые сервером, выполняются с использованием учетных данных клиента (олицетворенного пользователя).</span><span class="sxs-lookup"><span data-stu-id="f129d-111">When the server is impersonating the client, any operations performed by the server are performed by using the client's (impersonating user's) credentials.</span></span> <span data-ttu-id="f129d-112">Олицетворение не позволяет серверу получать доступ к удаленным ресурсам от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="f129d-112">Impersonation does not allow the server to access remote resources on behalf of the client.</span></span> <span data-ttu-id="f129d-113">Для этого требуется делегирование.</span><span class="sxs-lookup"><span data-stu-id="f129d-113">This requires delegation.</span></span>

</dd> <dt>

<span data-ttu-id="f129d-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**токен олицетворения**</span><span class="sxs-lookup"><span data-stu-id="f129d-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**impersonation token**</span></span>
</dt> <dd>

<span data-ttu-id="f129d-115">Маркер доступа, созданный для записи сведений о безопасности клиентского процесса, позволяющий серверу «олицетворять» клиентский процесс в операциях безопасности.</span><span class="sxs-lookup"><span data-stu-id="f129d-115">An access token that has been created to capture the security information of a client process, allowing a server to "impersonate" the client process in security operations.</span></span>

<span data-ttu-id="f129d-116">См. также [*маркер доступа*](a-gly.md) и [*основной маркер*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f129d-116">See also [*access token*](a-gly.md) and [*primary token*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f129d-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**вектор инициализации**</span><span class="sxs-lookup"><span data-stu-id="f129d-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**initialization vector**</span></span>
</dt> <dd>

<span data-ttu-id="f129d-118">(IV) последовательность случайных байтов, добавляемых перед открытым текстом перед шифрованием блочным шифром.</span><span class="sxs-lookup"><span data-stu-id="f129d-118">(IV) A sequence of random bytes appended to the front of the plaintext before encryption by a block cipher.</span></span> <span data-ttu-id="f129d-119">Добавление вектора инициализации в начало открытого текста избавляет от возможности наличия начального блока зашифрованных данных для любых двух сообщений.</span><span class="sxs-lookup"><span data-stu-id="f129d-119">Adding the initialization vector to the beginning of the plaintext eliminates the possibility of having the initial ciphertext block the same for any two messages.</span></span> <span data-ttu-id="f129d-120">Например, если сообщения всегда начинаются с общего заголовка (шапка или строка "от"), их первоначальный текст всегда будет одинаковым, предполагая, что использовался один и тот же криптографический алгоритм и симметричный ключ.</span><span class="sxs-lookup"><span data-stu-id="f129d-120">For example, if messages always start with a common header (a letterhead or "From" line) their initial ciphertext would always be the same, assuming that the same cryptographic algorithm and symmetric key was used.</span></span> <span data-ttu-id="f129d-121">Добавление случайного вектора инициализации исключает это из происходящих.</span><span class="sxs-lookup"><span data-stu-id="f129d-121">Adding a random initialization vector eliminates this from happening.</span></span>

</dd> <dt>

<span data-ttu-id="f129d-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**внутренние данные**</span><span class="sxs-lookup"><span data-stu-id="f129d-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**inner data**</span></span>
</dt> <dd>

<span data-ttu-id="f129d-123">Все закодированные данные, используемые в качестве сообщения для другого закодированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="f129d-123">Any encoded data used as the message for another encoded message.</span></span> <span data-ttu-id="f129d-124">Например, сообщение с оболочкой и его хэш-значение могут быть внутренними данными для второго сообщения.</span><span class="sxs-lookup"><span data-stu-id="f129d-124">For example, an enveloped message and its hash value may be the inner data for a second message.</span></span>

</dd> <dt>

<span data-ttu-id="f129d-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**внутреннее содержимое**</span><span class="sxs-lookup"><span data-stu-id="f129d-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**inner content**</span></span>
</dt> <dd>

<span data-ttu-id="f129d-126">Улучшенные данные, например с цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="f129d-126">Data that is enhanced, such as with a digital signature.</span></span> <span data-ttu-id="f129d-127">Этот термин используется в основном при обсуждении расширенных данных в \# сообщении PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="f129d-127">This term is used primarily when discussing enhanced data in a PKCS \#7 message.</span></span>

</dd> <dt>

<span data-ttu-id="f129d-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**контроля**</span><span class="sxs-lookup"><span data-stu-id="f129d-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**integrity**</span></span>
</dt> <dd>

<span data-ttu-id="f129d-129">Полнота и точность сообщения после его отправки или сохранения.</span><span class="sxs-lookup"><span data-stu-id="f129d-129">The completeness and accuracy of a message after it has been sent or stored.</span></span>

</dd> <dt>

<span data-ttu-id="f129d-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**SID целостности**</span><span class="sxs-lookup"><span data-stu-id="f129d-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**integrity SID**</span></span>
</dt> <dd>

<span data-ttu-id="f129d-131">[*Идентификатор безопасности*](s-gly.md) (SID), представляющий уровень целостности.</span><span class="sxs-lookup"><span data-stu-id="f129d-131">A [*security identifier*](s-gly.md) (SID) that represents an integrity level.</span></span> <span data-ttu-id="f129d-132">Идентификатор безопасности целостности в [*системном списке управления доступом*](s-gly.md) (SACL) дескриптора безопасности объекта задает уровень целостности объекта.</span><span class="sxs-lookup"><span data-stu-id="f129d-132">An integrity SID in the [*system access control list*](s-gly.md) (SACL) of an object's security descriptor specifies the integrity level of the object.</span></span> <span data-ttu-id="f129d-133">SID целостности в маркере доступа укажите уровень целостности токена.</span><span class="sxs-lookup"><span data-stu-id="f129d-133">Integrity SIDs in an access token specify the integrity level of the token.</span></span>

</dd> <dt>

<span data-ttu-id="f129d-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**УРОВЕНЬ**</span><span class="sxs-lookup"><span data-stu-id="f129d-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**</span></span>
</dt> <dd>

<span data-ttu-id="f129d-135">Уровень запросов прерывания (IRQL) определяет аппаратный приоритет, при котором процессор в любой момент времени работает.</span><span class="sxs-lookup"><span data-stu-id="f129d-135">An interrupt request level (IRQL) defines the hardware priority at which a processor operates at any given time.</span></span> <span data-ttu-id="f129d-136">В WDM поток, работающий на низком уровне IRQL, может быть прерван для выполнения кода на более высоком уровне IRQL.</span><span class="sxs-lookup"><span data-stu-id="f129d-136">In the Windows Driver Model, a thread running at a low IRQL can be interrupted to run code at a higher IRQL.</span></span>

</dd> <dt>

<span data-ttu-id="f129d-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="f129d-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**IV**</span></span>
</dt> <dd>

<span data-ttu-id="f129d-138">См. раздел *вектор инициализации*.</span><span class="sxs-lookup"><span data-stu-id="f129d-138">See *initialization vector*.</span></span>

</dd> </dl>

 

 



