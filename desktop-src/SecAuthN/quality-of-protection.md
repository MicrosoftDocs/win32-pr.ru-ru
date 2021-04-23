---
description: Качество защиты, определяемое директивой КОП, сначала определяется сервером в ходе дайджест-запроса, а затем подтверждается клиентом в ответе на запрос.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Качество защиты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4643c9e2de77647a3adf2cbf0441e31bcf5be5de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081326"
---
# <a name="quality-of-protection"></a><span data-ttu-id="c1f5e-103">Качество защиты</span><span class="sxs-lookup"><span data-stu-id="c1f5e-103">Quality of Protection</span></span>

<span data-ttu-id="c1f5e-104">Качество защиты, определяемое директивой КОП, сначала определяется сервером в ходе дайджест-запроса, а затем подтверждается клиентом в ответе на запрос.</span><span class="sxs-lookup"><span data-stu-id="c1f5e-104">The quality of protection, identified by the qop directive, is first specified by the server in the Digest challenge, and then confirmed by the client in the challenge response.</span></span> <span data-ttu-id="c1f5e-105">Если клиенту требуется качество защиты, которое не поддерживается сервером, клиент должен завершить проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="c1f5e-105">If the client requires a quality of protection that the server does not support, the client must terminate the authentication.</span></span>

<span data-ttu-id="c1f5e-106">Возможные значения для директивы КОП описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c1f5e-106">The possible values for the qop directive are described in the following table.</span></span>



| <span data-ttu-id="c1f5e-107">Значение</span><span class="sxs-lookup"><span data-stu-id="c1f5e-107">Value</span></span>                   | <span data-ttu-id="c1f5e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c1f5e-108">Description</span></span>                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f5e-109">аутентификаци</span><span class="sxs-lookup"><span data-stu-id="c1f5e-109">"auth"</span></span>                  | <span data-ttu-id="c1f5e-110">Только проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="c1f5e-110">Authentication only.</span></span>                                                                                                                         |
| <span data-ttu-id="c1f5e-111">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="c1f5e-111">"auth-int"</span></span>              | <span data-ttu-id="c1f5e-112">Проверка подлинности и проверка [*целостности*](../secgloss/i-gly.md) с помощью сигнатур.</span><span class="sxs-lookup"><span data-stu-id="c1f5e-112">Authentication and [*integrity*](../secgloss/i-gly.md) checking using signatures.</span></span>                  |
| <span data-ttu-id="c1f5e-113">(Только SASL) "auth-conf"</span><span class="sxs-lookup"><span data-stu-id="c1f5e-113">(SASL only) "auth-conf"</span></span> | <span data-ttu-id="c1f5e-114">Проверка подлинности, целостность и конфиденциальность с помощью сигнатур и шифрования.</span><span class="sxs-lookup"><span data-stu-id="c1f5e-114">Authentication, integrity and confidentiality checking by using signatures and encryption.</span></span> <span data-ttu-id="c1f5e-115">Дополнительные сведения см. в разделе [ciphers](ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="c1f5e-115">For more information, see [Ciphers](ciphers.md).</span></span> |



 

<span data-ttu-id="c1f5e-116">Качество защиты определяется флагами требования контекста, передаваемыми в Microsoft Digest SSP.</span><span class="sxs-lookup"><span data-stu-id="c1f5e-116">Quality of protection is determined by context requirement flags passed to the Microsoft Digest SSP.</span></span> <span data-ttu-id="c1f5e-117">В следующей таблице перечислены флаги, связанные с качеством защиты, и результирующее значение директивы КОП.</span><span class="sxs-lookup"><span data-stu-id="c1f5e-117">The following table lists the flags related to quality of protection, and the resulting value of the qop directive.</span></span>



| <span data-ttu-id="c1f5e-118">Flag</span><span class="sxs-lookup"><span data-stu-id="c1f5e-118">Flag</span></span>                         | <span data-ttu-id="c1f5e-119">значение КОП</span><span class="sxs-lookup"><span data-stu-id="c1f5e-119">qop value</span></span>               |
|------------------------------|-------------------------|
| <span data-ttu-id="c1f5e-120">*Xxx* \_ \_Конфиденциальность требований</span><span class="sxs-lookup"><span data-stu-id="c1f5e-120">*XXX*\_REQ\_CONFIDENTIALITY</span></span>  | <span data-ttu-id="c1f5e-121">"auth-conf" (только SASL)</span><span class="sxs-lookup"><span data-stu-id="c1f5e-121">"auth-conf" (SASL only)</span></span> |
| <span data-ttu-id="c1f5e-122">*Xxx* \_ \_обнаружение воспроизведения заявок \_</span><span class="sxs-lookup"><span data-stu-id="c1f5e-122">*XXX*\_REQ\_REPLAY\_DETECT</span></span>   | <span data-ttu-id="c1f5e-123">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="c1f5e-123">"auth-int"</span></span>              |
| <span data-ttu-id="c1f5e-124">*Xxx* \_ \_Обнаружение последовательности \_ требований</span><span class="sxs-lookup"><span data-stu-id="c1f5e-124">*XXX*\_REQ\_SEQUENCE\_DETECT</span></span> | <span data-ttu-id="c1f5e-125">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="c1f5e-125">"auth-int"</span></span>              |
| <span data-ttu-id="c1f5e-126">*Xxx* \_ \_целостность требований</span><span class="sxs-lookup"><span data-stu-id="c1f5e-126">*XXX*\_REQ\_INTEGRITY</span></span>        | <span data-ttu-id="c1f5e-127">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="c1f5e-127">"auth-int"</span></span>              |
| <span data-ttu-id="c1f5e-128">(нет)</span><span class="sxs-lookup"><span data-stu-id="c1f5e-128">(none)</span></span>                       | <span data-ttu-id="c1f5e-129">аутентификаци</span><span class="sxs-lookup"><span data-stu-id="c1f5e-129">"auth"</span></span>                  |



 

> [!Note]  
> <span data-ttu-id="c1f5e-130">Флаги требования к контексту, заданные серверными приложениями, имеют префикс ASC, а значения, указанные клиентами, начинаются с версии ISC.</span><span class="sxs-lookup"><span data-stu-id="c1f5e-130">Context requirement flags specified by server applications have a prefix of ASC, and those specified by clients are prefixed with ISC.</span></span> <span data-ttu-id="c1f5e-131">Чтобы определить значения флагов, используемые приложением, замените один из этих префиксов на *xxx*.</span><span class="sxs-lookup"><span data-stu-id="c1f5e-131">To determine the flag values used by your application, substitute one of these prefixes for *XXX*.</span></span>

 

<span data-ttu-id="c1f5e-132">Дополнительные сведения, относящиеся к серверу, см. [в разделе Создание дайджест-запроса](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="c1f5e-132">For additional server-related information, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

<span data-ttu-id="c1f5e-133">Дополнительные сведения, относящиеся к клиенту, см. [в разделе Создание ответа на запрос дайджеста](generating-the-digest-challenge-response.md).</span><span class="sxs-lookup"><span data-stu-id="c1f5e-133">For additional client-related information, see [Generating the Digest Challenge Response](generating-the-digest-challenge-response.md).</span></span>

 

 
