---
title: Расшифровка полезных данных ASF и повторное шифрование
description: Расшифровка полезных данных ASF и повторное шифрование
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- Windows Media Format SDK, расшифровка полезных данных ASF и повторное шифрование
- Windows Media Format SDK, расшифровка полезных данных и повторное шифрование
- Windows Media Format SDK, расшифровка
- Windows Media Format SDK, повторное шифрование
- Управление цифровыми правами (DRM), расшифровка полезных данных ASF и повторное шифрование
- DRM (Управление цифровыми правами), расшифровка полезных данных ASF и повторное шифрование
- Управление цифровыми правами (DRM), расшифровка полезных данных и повторное шифрование
- DRM (Управление цифровыми правами), расшифровка полезных данных и повторное шифрование
- Управление цифровыми правами (DRM), расшифровка
- DRM (Управление цифровыми правами), расшифровка
- Управление цифровыми правами (DRM), повторное шифрование
- DRM (Управление цифровыми правами), повторное шифрование
- Расширенные API клиента DRM, расшифровка полезных данных ASF и повторное шифрование
- Расширенные API клиента, расшифровка полезных данных ASF и повторное шифрование
- Расширенные API клиента DRM, расшифровка полезных данных и повторное шифрование
- Расширенные API клиента, расшифровка полезных данных и повторное шифрование
- Расширенные API клиента DRM, расшифровка
- Расширенные API клиента, расшифровка
- Расширенные API клиента DRM, повторное шифрование
- Расширенные API клиента, повторное шифрование
- Расширенный формат систем (ASF), повторное шифрование
- ASF (расширенный формат систем), повторное шифрование
- Расширенный формат систем (ASF), расшифровка
- ASF (Расширенный системный формат), расшифровка
- Расширенный формат систем (ASF), расшифровка полезных данных и повторное шифрование
- ASF (Расширенный системный формат), расшифровка полезных данных и повторное шифрование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c6dcab1d483b737b6b05636b51b8af0502350
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773403"
---
# <a name="asf-payload-decryption-and-re-encryption"></a><span data-ttu-id="15290-129">Расшифровка полезных данных ASF и повторное шифрование</span><span class="sxs-lookup"><span data-stu-id="15290-129">ASF Payload Decryption and Re-encryption</span></span>

<span data-ttu-id="15290-130">Ниже описаны действия, которые должны быть выполнены приложением для расшифровки и повторного шифрования каждой полезной нагрузки.</span><span class="sxs-lookup"><span data-stu-id="15290-130">The steps below describe the actions that an application must complete to decrypt and re-encrypt each payload:</span></span>

1.  <span data-ttu-id="15290-131">Увеличение расширяющего значения.</span><span class="sxs-lookup"><span data-stu-id="15290-131">Increment the salt value.</span></span>
2.  <span data-ttu-id="15290-132">Передайте полезные данные (зашифрованные с помощью Windows Media DRM) и расширяющее значение функции расшифровки [**ивмдрмдекрипт::D екрипт**](iwmdrmdecrypt-decrypt.md), которая возвращает полезные данные, зашифрованные с помощью открытого ключа RC4.</span><span class="sxs-lookup"><span data-stu-id="15290-132">Pass the payload (encrypted with Windows Media DRM) and the salt value to the decryption function, [**IWMDRMDecrypt::Decrypt**](iwmdrmdecrypt-decrypt.md), which will return the payload, encrypted using the RC4 public key.</span></span>
3.  <span data-ttu-id="15290-133">Создайте объект транзитного ключа RC4, применив хэш SHA-1 вектора инициализации, сцепленный с расширяющим значением.</span><span class="sxs-lookup"><span data-stu-id="15290-133">Derive a transitory RC4 key by applying an SHA-1 hash of the initialization vector concatenated with the salt value.</span></span>
4.  <span data-ttu-id="15290-134">Используйте транзитный ключ для расшифровки полезных данных.</span><span class="sxs-lookup"><span data-stu-id="15290-134">Use your transitory key to decrypt the payload.</span></span>
5.  <span data-ttu-id="15290-135">Немедленно повторно зашифровать полезные данные с помощью схемы защиты содержимого, соответствующей требованиям к экспорту Windows Media DRM и правилам надежности.</span><span class="sxs-lookup"><span data-stu-id="15290-135">Immediately re-encrypt the payload with the authorized content protection scheme according to the Windows Media DRM export compliance and robustness rules.</span></span>
6.  <span data-ttu-id="15290-136">Нахождение следующих полезных данных.</span><span class="sxs-lookup"><span data-stu-id="15290-136">Locate the next payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15290-137">См. также</span><span class="sxs-lookup"><span data-stu-id="15290-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15290-138">**Экспорт сжатого содержимого**</span><span class="sxs-lookup"><span data-stu-id="15290-138">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




