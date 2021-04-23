---
title: Экспорт сжатого содержимого
description: Экспорт сжатого содержимого
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows Media Format SDK, экспорт DRM
- Пакет Windows Media Format SDK, экспорт
- Windows Media Format SDK, сжатое содержимое
- Управление цифровыми правами (DRM), экспорт
- DRM (Управление цифровыми правами), экспорт
- Управление цифровыми правами (DRM), сжатое содержимое
- DRM (Управление цифровыми правами), сжатое содержимое
- Расширенные API клиента DRM, сжатое содержимое
- Расширенные API клиента, сжатое содержимое
- Расширенные API клиента DRM, экспорт
- Расширенные API клиента, экспорт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888155"
---
# <a name="exporting-compressed-content"></a><span data-ttu-id="e5ce2-114">Экспорт сжатого содержимого</span><span class="sxs-lookup"><span data-stu-id="e5ce2-114">Exporting Compressed Content</span></span>

<span data-ttu-id="e5ce2-115">В этом разделе описывается экспорт защищенного мультимедиа Windows Media DRM в файл Windows Media, где приложение получает сжатые цифровые данные мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-115">This section describes exporting Windows Media DRM protected media on a Windows Media file where the application receives compressed digital media data.</span></span> <span data-ttu-id="e5ce2-116">Для этого приложение должно выполнить встроенную расшифровку всех зашифрованных полезных данных Windows Media DRM в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-116">To do this, your application must perform inline decryption of all Windows Media DRM encrypted payloads in an ASF file.</span></span>

> [!Note]  
> <span data-ttu-id="e5ce2-117">Библиотека синтаксического анализа ASF предоставляется как часть соглашения об экспорте DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-117">An ASF parsing library is supplied to you as part of the Windows Media DRM Export agreement.</span></span>

 

<span data-ttu-id="e5ce2-118">Основные этапы экспорта сжатого содержимого:</span><span class="sxs-lookup"><span data-stu-id="e5ce2-118">The primary steps involved in exporting compressed content are:</span></span>

1.  <span data-ttu-id="e5ce2-119">При необходимости выполните индивидуальную разработку DRM.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-119">Perform DRM individualization, if needed.</span></span>
2.  <span data-ttu-id="e5ce2-120">Убедитесь, что Целевая схема защиты содержимого разрешена явно.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-120">Verify that the target content protection scheme is explicitly permitted.</span></span>
3.  <span data-ttu-id="e5ce2-121">Создайте объект дешифратора для расшифровки каждой полезной нагрузки ASF.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-121">Create a decryptor object to decrypt each ASF payload.</span></span>
4.  <span data-ttu-id="e5ce2-122">Система DRM преобразует все полезные данные ASF из Windows Media DRM в RC4 перед передачей их в приложение.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-122">The DRM system transcrypts each ASF payload from Windows Media DRM into RC4 before passing it to your application.</span></span>

<span data-ttu-id="e5ce2-123">Если приложение изменяет размер полезных данных ASF во время передачи, необходимо также Ремультиплексирование файла ASF.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-123">If your application changes the size of an ASF payload during transcryption, you must also remultiplex the ASF file.</span></span>

<span data-ttu-id="e5ce2-124">Передайте в библиотеку-заглушку сертификат приложения для экспорта Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-124">Pass to the stub library a Windows Media DRM Export Application Certificate.</span></span> <span data-ttu-id="e5ce2-125">Сертификат проверяется, и, если он является допустимым, система DRM создает вектор инициализации и шифрует его с помощью RSA OAEP.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-125">The certificate is verified, and if it is valid, the DRM system generates an initialization vector and encrypts it using RSA OAEP.</span></span>

-   <span data-ttu-id="e5ce2-126">Ключ сеанса RC4 создается для каждой полезной нагрузки путем сцепления вектора инициализации и расширяющего значения.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-126">An RC4 session key is created for each payload by concatenating the initialization vector and a salt value.</span></span> <span data-ttu-id="e5ce2-127">Вы предоставляете расширяющее значение API-интерфейсу расшифровки, и вы должны увеличить его на положительное ненулевое целочисленное значение для каждой полезной нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-127">You supply the salt value to the decryption API, and you must increment it by a positive non-zero integer value for each payload.</span></span>

<span data-ttu-id="e5ce2-128">Вы будете предоставлять средства корпорацией Майкрософт в рамках соглашения об экспорте DRM для Windows Media, которое позволит создать собственную пару из открытого и закрытого ключей RSA.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-128">You will be provided a tool by Microsoft as part of the Windows Media DRM export agreement that will enable you to generate your own RSA public/private key pair.</span></span> <span data-ttu-id="e5ce2-129">Открытый ключ будет отправлен в корпорацию Майкрософт, где корпорация Майкрософт будет включать его в подписанный сертификат приложения Windows Media DRM и возвращать его.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-129">You will send the public key to Microsoft, where Microsoft will incorporate it into a signed Windows Media DRM Application Certificate, and return it.</span></span>

<span data-ttu-id="e5ce2-130">Каждая полезная нагрузка после расшифровки с помощью ключа расшифровки RC4 должна быть немедленно зашифрована в выходных данных CPS.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-130">Each payload, after it is decrypted using the RC4 decryption key, must be immediately encrypted into the output CPS.</span></span> <span data-ttu-id="e5ce2-131">Существуют другие ограничения на обработку незашифрованных полезных данных, которые описаны в правилах надежности и соответствия требованиям, сопровождающих соглашение об экспорте DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e5ce2-131">There are other restrictions on handling of unencrypted payloads that are outlined in the robustness and compliance rules, which accompany the Windows Media DRM Export agreement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5ce2-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e5ce2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5ce2-133">**Расшифровка полезных данных ASF и повторное шифрование**</span><span class="sxs-lookup"><span data-stu-id="e5ce2-133">**ASF Payload Decryption and Re-encryption**</span></span>](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[<span data-ttu-id="e5ce2-134">**Экспорт DRM**</span><span class="sxs-lookup"><span data-stu-id="e5ce2-134">**DRM Export**</span></span>](drm-export.md)
</dt> <dt>

[<span data-ttu-id="e5ce2-135">**Выполнение индивидуальной управления цифровыми правами**</span><span class="sxs-lookup"><span data-stu-id="e5ce2-135">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> <dt>

[<span data-ttu-id="e5ce2-136">**Проверка и инициализация**</span><span class="sxs-lookup"><span data-stu-id="e5ce2-136">**Verification and Initialization**</span></span>](verification-and-initialization.md)
</dt> </dl>

 

 




