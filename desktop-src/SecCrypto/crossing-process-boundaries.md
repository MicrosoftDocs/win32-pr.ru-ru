---
description: Механизм протокола Schannel выполняет подтверждение и проверку подлинности в безопасном процессе, а также в процессе приложения.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Пересечение границ процессов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046bc6f53d609ec22ed37edd08d6967cc4ae73e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682596"
---
# <a name="crossing-process-boundaries"></a><span data-ttu-id="eaac7-103">Пересечение границ процессов</span><span class="sxs-lookup"><span data-stu-id="eaac7-103">Crossing Process Boundaries</span></span>

<span data-ttu-id="eaac7-104">Механизм протокола [*SChannel*](../secgloss/s-gly.md) выполняет подтверждение и проверку подлинности в безопасном [*процессе*](../secgloss/p-gly.md) , а также в процессе приложения.</span><span class="sxs-lookup"><span data-stu-id="eaac7-104">The [*Schannel*](../secgloss/s-gly.md) protocol engine performs the handshaking and authentication in a secure [*process*](../secgloss/p-gly.md) and the bulk encryption/message passing in the application process.</span></span> <span data-ttu-id="eaac7-105">Это означает, что [*ключи с массовым шифрованием*](../secgloss/b-gly.md) и ключи [*Mac*](../secgloss/m-gly.md) должны быть скопированы из одного процесса в другой.</span><span class="sxs-lookup"><span data-stu-id="eaac7-105">This means that the [*bulk encryption keys*](../secgloss/b-gly.md) and [*MAC*](../secgloss/m-gly.md) keys must be copied from one process to another.</span></span> <span data-ttu-id="eaac7-106">Чтобы скопировать ключи из одного процесса в другой, используйте функции [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) и [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eaac7-106">To copy the keys from one process to another, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) functions as follows:</span></span>

1.  <span data-ttu-id="eaac7-107">Безопасный процесс экспортирует каждый ключ в [*опакуекэйблоб*](../secgloss/o-gly.md) с помощью [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), а затем уничтожает ключ с помощью [**криптдестройкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span><span class="sxs-lookup"><span data-stu-id="eaac7-107">The secure process exports each key into an [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) using [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), then destroys the key using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span> <span data-ttu-id="eaac7-108">Обратите внимание, что если ключ хранится на оборудовании, CSP должен распознать его и не должен пытаться уничтожить ключ.</span><span class="sxs-lookup"><span data-stu-id="eaac7-108">Note that if the key is stored in hardware, the CSP must recognize this and must not attempt to destroy the key.</span></span>
2.  <span data-ttu-id="eaac7-109">Безопасный процесс передает Опакуекэйблобс в процесс приложения за пределами области этого документа.</span><span class="sxs-lookup"><span data-stu-id="eaac7-109">The secure process passes the OPAQUEKEYBLOBs to the application process in a manner beyond the scope of this document.</span></span>
3.  <span data-ttu-id="eaac7-110">Процесс приложения импортирует каждый ОПАКУЕКЭЙБЛОБ обратно в CSP с помощью [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="eaac7-110">The application process imports each OPAQUEKEYBLOB back into the CSP using [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="eaac7-111">На этом этапе ключ должен находиться в том же [*состоянии*](../secgloss/s-gly.md) , что и при его экспорте.</span><span class="sxs-lookup"><span data-stu-id="eaac7-111">At this point, the key must be in exactly the same [*state*](../secgloss/s-gly.md) as when it was exported.</span></span>

 

 
