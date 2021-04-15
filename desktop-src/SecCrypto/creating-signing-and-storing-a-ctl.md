---
description: Создайте подписанный список доверия сертификатов (CTL) и сохраните его в хранилище сертификатов.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Создание, подписывание и хранение списка доверия сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682598"
---
# <a name="creating-signing-and-storing-a-ctl"></a><span data-ttu-id="db14e-103">Создание, подписывание и хранение списка доверия сертификатов</span><span class="sxs-lookup"><span data-stu-id="db14e-103">Creating, Signing, and Storing a CTL</span></span>

<span data-ttu-id="db14e-104">Следующие процедуры создают подписанный [*список доверия сертификатов*](../secgloss/c-gly.md) (CTL) и сохраняют его в [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="db14e-104">The following procedures create a signed [*certificate trust list*](../secgloss/c-gly.md) (CTL) and save it to a [*certificate store*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="db14e-105">**Создание и подписание списка доверия сертификатов**</span><span class="sxs-lookup"><span data-stu-id="db14e-105">**To create and sign a CTL**</span></span>

1.  <span data-ttu-id="db14e-106">Создайте массив элементов, которые будут храниться в списке [*доверия сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="db14e-106">Create an array of items to be stored in the [*CTL*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="db14e-107">В случае доверенных сертификатов это должны быть хэши SHA1 или MD5 доверенных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="db14e-107">In the case of trusted certificates, this must be the SHA1 or MD5 hashes of the trusted certificates.</span></span>
2.  <span data-ttu-id="db14e-108">Инициализируйте [**структуру \_ сведений CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) , содержащую только что созданный массив элементов.</span><span class="sxs-lookup"><span data-stu-id="db14e-108">Initialize a [**CTL\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) structure that includes the array of items just created.</span></span>
3.  <span data-ttu-id="db14e-109">Инициализируйте [**структуру \_ \_ \_ сведений о кодировании со знаком КМСГ**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .</span><span class="sxs-lookup"><span data-stu-id="db14e-109">Initialize a [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) structure.</span></span>
4.  <span data-ttu-id="db14e-110">Вызовите [**криптмсженкодеандсигнктл**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span><span class="sxs-lookup"><span data-stu-id="db14e-110">Call [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span></span> <span data-ttu-id="db14e-111">Этот вызов функции возвращает указатель на подписанный, закодированный CTL (в формате PKCS \# 7), содержащий список элементов, созданных на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="db14e-111">This function call returns a pointer to a signed, encoded CTL (in PKCS \#7 format) that contains the list of items created in step 1.</span></span>

<span data-ttu-id="db14e-112">**Добавление CTL в хранилище сертификатов**</span><span class="sxs-lookup"><span data-stu-id="db14e-112">**To add a CTL to a certificate store**</span></span>

1.  <span data-ttu-id="db14e-113">Получение указателя на подписанный и закодированный список доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="db14e-113">Get a pointer to a signed and encoded CTL.</span></span>
2.  <span data-ttu-id="db14e-114">Откройте целевое хранилище сертификатов, вызвав [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="db14e-114">Open the target certificate store with a call to [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
3.  <span data-ttu-id="db14e-115">Вызовите [**цертадденкодедктлтосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span><span class="sxs-lookup"><span data-stu-id="db14e-115">Call [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span></span>

 

 
