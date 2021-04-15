---
description: Описывает, как проверить подпись другой стороны с помощью Криптмсгверификаунтерсигнатуринкодед.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Проверка подписи другой стороны
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682976"
---
# <a name="verifying-a-countersignature"></a><span data-ttu-id="9af6e-103">Проверка подписи другой стороны</span><span class="sxs-lookup"><span data-stu-id="9af6e-103">Verifying a Countersignature</span></span>

<span data-ttu-id="9af6e-104">**Проверка подписи другой стороны**</span><span class="sxs-lookup"><span data-stu-id="9af6e-104">**To verify a countersignature**</span></span>

1.  <span data-ttu-id="9af6e-105">Вызовите [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , чтобы получить маркер подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="9af6e-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="9af6e-106">Получение указателя на сертификат каунтерсигнер ( [**\_ сведения о**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)сертификате).</span><span class="sxs-lookup"><span data-stu-id="9af6e-106">Get a pointer to the countersigner's certificate ( [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).</span></span>
3.  <span data-ttu-id="9af6e-107">Вызовите [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) , чтобы получить сведения о подписавшем из сообщения.</span><span class="sxs-lookup"><span data-stu-id="9af6e-107">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the signer information from the message.</span></span>
4.  <span data-ttu-id="9af6e-108">Вызовите [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) , чтобы получить [*подпись*](../secgloss/c-gly.md) от сообщения.</span><span class="sxs-lookup"><span data-stu-id="9af6e-108">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the [*countersignature*](../secgloss/c-gly.md) from the message.</span></span>
5.  <span data-ttu-id="9af6e-109">Вызовите [**криптмсгверификаунтерсигнатуринкодед**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) , чтобы проверить подпись другой стороны.</span><span class="sxs-lookup"><span data-stu-id="9af6e-109">Call [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) to verify the countersignature.</span></span>

<span data-ttu-id="9af6e-110">Если вызов функции [**криптмсгверификаунтерсигнатуринкодед**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) выполнен, [*подпись другой стороны*](../secgloss/c-gly.md) проверяется.</span><span class="sxs-lookup"><span data-stu-id="9af6e-110">If the [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) function call succeeds, the [*countersignature*](../secgloss/c-gly.md) is verified.</span></span>

 

 
