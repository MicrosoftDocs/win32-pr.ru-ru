---
description: Чтобы Интерлопер заменять фиктивный список доверия сертификатов (CTL) для существующего, проверьте подпись в списке доверия сертификатов при каждом использовании списка доверия сертификатов.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Проверка списка доверия сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543511"
---
# <a name="verifying-a-ctl"></a><span data-ttu-id="bada2-103">Проверка списка доверия сертификатов</span><span class="sxs-lookup"><span data-stu-id="bada2-103">Verifying a CTL</span></span>

<span data-ttu-id="bada2-104">Чтобы Интерлопер заменять фиктивный [*список доверия сертификатов*](../secgloss/c-gly.md) (CTL) для существующего, проверьте подпись в списке доверия сертификатов при каждом использовании списка доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="bada2-104">To make it more difficult for an interloper to substitute a bogus [*certificate trust list*](../secgloss/c-gly.md) (CTL) for an existing one, verify the signature on the CTL each time the CTL is used.</span></span> <span data-ttu-id="bada2-105">Не используйте CTL, который не содержит доверенную подпись.</span><span class="sxs-lookup"><span data-stu-id="bada2-105">Do not use a CTL that does not contain a trusted signature.</span></span>

<span data-ttu-id="bada2-106">**Проверка подписи CTL**</span><span class="sxs-lookup"><span data-stu-id="bada2-106">**To verify a CTL signature**</span></span>

1.  <span data-ttu-id="bada2-107">Откройте [*хранилище сертификатов*](../secgloss/c-gly.md) , содержащее нужный список доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="bada2-107">Open the [*certificate store*](../secgloss/c-gly.md) containing the desired CTL.</span></span>
2.  <span data-ttu-id="bada2-108">Получение маркера для [**\_ контекста CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) для CTL.</span><span class="sxs-lookup"><span data-stu-id="bada2-108">Get a handle to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) for the CTL.</span></span> <span data-ttu-id="bada2-109">Это можно сделать, вызвав любую функцию, которая возвращает маркер в **\_ контекст CTL**, например [**цертфиндктлинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="bada2-109">This can be done by calling any of the functions that return a handle to the **CTL\_CONTEXT**, such as [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span>
3.  <span data-ttu-id="bada2-110">Вызовите [**криптмсгжетандверифисигнер**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), передав [**\_ контекст CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) , полученный на шаге 2, в параметре *хкриптмсг* , маркер хранилища сертификатов, который содержит сертификат доверенного источника для CTL в параметре *ргхсигнерсторе* , и флаг КМСГ \_ Trusted Sign (доверенный) \_ \_ в параметре *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="bada2-110">Call [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passing the [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) retrieved in step 2 in the *hCryptMsg* parameter, a handle to the certificate store containing the certificate of the trusted source for CTLs in the *rghSignerStore* parameter, and the CMSG\_TRUSTED\_SIGNER\_FLAG in the *dwFlags* parameter.</span></span> <span data-ttu-id="bada2-111">Если функция возвращает **значение true**, подпись была проверена, а в параметре *ппсигнер* возвращается указатель на [**\_ контекст пкцерт**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) для подписанного доверия.</span><span class="sxs-lookup"><span data-stu-id="bada2-111">If the function returns **TRUE**, the signature was verified, and a pointer to the CTL signer's [**PCCERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) is returned in the *ppSigner* parameter.</span></span>

 

 
