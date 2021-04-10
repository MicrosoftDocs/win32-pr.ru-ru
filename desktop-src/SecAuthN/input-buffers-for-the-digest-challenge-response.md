---
description: Для проверки подлинности HTTP с помощью Microsoft Digest требуется три входных буфера для создания ответа на запрос. В следующей таблице перечислены эти буферы.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Входные буферы для ответа на запрос дайджеста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143735"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a><span data-ttu-id="7b378-104">Входные буферы для ответа на запрос дайджеста</span><span class="sxs-lookup"><span data-stu-id="7b378-104">Input Buffers for the Digest Challenge Response</span></span>

<span data-ttu-id="7b378-105">Для проверки подлинности HTTP с помощью Microsoft Digest требуется три входных буфера для создания ответа на запрос.</span><span class="sxs-lookup"><span data-stu-id="7b378-105">HTTP authentication using Microsoft Digest requires three input buffers to generate a challenge response.</span></span> <span data-ttu-id="7b378-106">В следующей таблице перечислены эти буферы.</span><span class="sxs-lookup"><span data-stu-id="7b378-106">The following table summarizes these buffers.</span></span>



| <span data-ttu-id="7b378-107">Номер буфера</span><span class="sxs-lookup"><span data-stu-id="7b378-107">Buffer number</span></span> | <span data-ttu-id="7b378-108">Содержит</span><span class="sxs-lookup"><span data-stu-id="7b378-108">Contains</span></span>                                                                                                                                             | <span data-ttu-id="7b378-109">Тип буфера</span><span class="sxs-lookup"><span data-stu-id="7b378-109">Buffer type</span></span>                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7b378-110">0</span><span class="sxs-lookup"><span data-stu-id="7b378-110">0</span></span>             | <span data-ttu-id="7b378-111">Запрос, полученный от сервера</span><span class="sxs-lookup"><span data-stu-id="7b378-111">Challenge received from the Server</span></span>                                                                                                                   | <span data-ttu-id="7b378-112">\_токен pvbuffer</span><span class="sxs-lookup"><span data-stu-id="7b378-112">SECBUFFER\_TOKEN</span></span>                                            |
| <span data-ttu-id="7b378-113">1</span><span class="sxs-lookup"><span data-stu-id="7b378-113">1</span></span>             | <span data-ttu-id="7b378-114">Метод HTTP</span><span class="sxs-lookup"><span data-stu-id="7b378-114">HTTP Method</span></span>                                                                                                                                          | <span data-ttu-id="7b378-115">\_Параметры pvbuffer</span><span class="sxs-lookup"><span data-stu-id="7b378-115">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="7b378-116">2</span><span class="sxs-lookup"><span data-stu-id="7b378-116">2</span></span>             | <span data-ttu-id="7b378-117">H (сущность)</span><span class="sxs-lookup"><span data-stu-id="7b378-117">H(Entity)</span></span>                                                                                                                                            | <span data-ttu-id="7b378-118">\_Параметры pvbuffer</span><span class="sxs-lookup"><span data-stu-id="7b378-118">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="7b378-119">3</span><span class="sxs-lookup"><span data-stu-id="7b378-119">3</span></span>             | <span data-ttu-id="7b378-120">[*Имя участника-службы*](../secgloss/s-gly.md) (SPN) целевого сервера.</span><span class="sxs-lookup"><span data-stu-id="7b378-120">The [*service principal name*](../secgloss/s-gly.md) (SPN) of the target server.</span></span> | <span data-ttu-id="7b378-121">**Pvbuffer \_ Целевой \_ узел** \| **pvbuffer \_ только для чтения**</span><span class="sxs-lookup"><span data-stu-id="7b378-121">**SECBUFFER\_TARGET\_HOST** \| **SECBUFFER\_READONLY**</span></span>      |
| <span data-ttu-id="7b378-122">4</span><span class="sxs-lookup"><span data-stu-id="7b378-122">4</span></span>             | <span data-ttu-id="7b378-123">Значения токенов привязок каналов</span><span class="sxs-lookup"><span data-stu-id="7b378-123">Channel bindings token values</span></span>                                                                                                                        | <span data-ttu-id="7b378-124">**Pvbuffer \_ \_привязки каналов** \| **pvbuffer \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="7b378-124">**SECBUFFER\_CHANNEL\_BINDINGS** \| **SECBUFFER\_READONLY**</span></span> |



 

<span data-ttu-id="7b378-125">Нулевой буфер содержит запрос дайджеста, полученный от сервера в ответ на первоначальный запрос ресурса, защищенного с помощью доступа.</span><span class="sxs-lookup"><span data-stu-id="7b378-125">Buffer zero contains the Digest challenge received from the server in response to the initial request for an access-protected resource.</span></span>

<span data-ttu-id="7b378-126">В буфере 1 содержится строковое представление метода, например GET или POST.</span><span class="sxs-lookup"><span data-stu-id="7b378-126">Buffer 1 contains the string representation of the method, such as "GET" or "POST".</span></span> <span data-ttu-id="7b378-127">Метод используется в вычислении a2, как описано в [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span><span class="sxs-lookup"><span data-stu-id="7b378-127">The method is used in the calculation of A2, as described in [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span></span>

<span data-ttu-id="7b378-128">Буфер 2 — это [*MD5*](../secgloss/m-gly.md) -хэш тела сообщения, как описано в RFC 2617.</span><span class="sxs-lookup"><span data-stu-id="7b378-128">Buffer 2 is the [*MD5*](../secgloss/m-gly.md) hash of the message's entity-body as described in RFC 2617.</span></span>

<span data-ttu-id="7b378-129">В буфере 3 содержится имя субъекта-службы целевого сервера в формате UTF-8, когда дайджест используется с привязками каналов.</span><span class="sxs-lookup"><span data-stu-id="7b378-129">Buffer 3 contains the SPN of the target server in UTF-8 formatting when Digest is used with channel bindings.</span></span>

<span data-ttu-id="7b378-130">В буфере 4 содержится значение маркера привязки канала, когда дайджест используется с привязками канала.</span><span class="sxs-lookup"><span data-stu-id="7b378-130">Buffer 4 contains the channel binding token value when Digest is used with channel bindings.</span></span>

## <a name="input-buffers-for-sasl"></a><span data-ttu-id="7b378-131">Входные буферы для SASL</span><span class="sxs-lookup"><span data-stu-id="7b378-131">Input Buffers for SASL</span></span>

<span data-ttu-id="7b378-132">Укажите только нулевой буфер.</span><span class="sxs-lookup"><span data-stu-id="7b378-132">Supply buffer zero only.</span></span> <span data-ttu-id="7b378-133">Для совместимости с другими SSP можно вызвать [**InitializeSecurityContext (дайджест)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) без допустимого запроса к серверу.</span><span class="sxs-lookup"><span data-stu-id="7b378-133">For compatibility with other SSPs, you may call [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) without a valid server challenge.</span></span> <span data-ttu-id="7b378-134">В этом случае параметру *пинпут* должно быть присвоено **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7b378-134">In this case the *pInput* parameter should be set to **NULL**.</span></span>

 

 
