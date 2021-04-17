---
title: Вопросы безопасности Платформа текстовых служб
description: Вопросы безопасности Платформа текстовых служб
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Платформа текстовых служб (TSF), безопасность
- TSF (платформа текстовых служб), безопасность
- службы текстового ввода, безопасность
- Приложения с поддержкой TSF, безопасность
- безопасность для TSF
- Платформа текстовых служб (TSF), рекомендации
- TSF (платформа текстовых служб), рекомендации
- Приложения с поддержкой TSF, рекомендации
- текстовые службы, рекомендации
- рекомендации по использованию TSF
- Платформа текстовых служб (TSF), проверка ошибок
- TSF (платформа текстовых служб), проверка ошибок
- Приложения с поддержкой TSF, проверка ошибок
- текстовые службы, проверка ошибок
- проверка ошибок
- Платформа текстовых служб (TSF), цифровые подписи
- TSF (платформа текстовых служб), цифровые подписи
- текстовые службы, цифровые подписи
- Приложения с поддержкой TSF, цифровые подписи
- Цифровые подписи
- Платформа текстовых служб (TSF), вызовы LoadLibrary
- TSF (платформа текстовых служб), вызовы LoadLibrary
- текстовые службы, вызовы LoadLibrary
- Приложения с поддержкой TSF, вызовы LoadLibrary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d71966106cde0f59d39442f7e2bf9b2a216cd94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681628"
---
# <a name="security-considerations-text-services-framework"></a><span data-ttu-id="07a76-127">Вопросы безопасности. Платформа текстовых служб</span><span class="sxs-lookup"><span data-stu-id="07a76-127">Security Considerations: Text Services Framework</span></span>

## <a name="best-practices-for-developing-with-tsf"></a><span data-ttu-id="07a76-128">Рекомендации по разработке с помощью TSF</span><span class="sxs-lookup"><span data-stu-id="07a76-128">Best Practices for Developing with TSF</span></span>

-   <span data-ttu-id="07a76-129">**Цифровые подписи:** Поставщики текстовых служб должны предоставлять цифровые подписи для двоичных исполняемых файлов.</span><span class="sxs-lookup"><span data-stu-id="07a76-129">**Digital Signatures:** Text service providers should provide digital signatures with their binary executables.</span></span> <span data-ttu-id="07a76-130">Зарегистрированная служба текстового ввода имеет доступ к системным потокам и может предоставлять информацию, которая в противном случае была бы недоступна.</span><span class="sxs-lookup"><span data-stu-id="07a76-130">A registered text service has access to system threads and could expose information that would otherwise not be accessible.</span></span> <span data-ttu-id="07a76-131">Чтобы обеспечить стабильную и безопасную работу, пользователь должен проверить цифровую подпись службы текстового ввода, прежде чем служба текстового ввода сможет загрузиться.</span><span class="sxs-lookup"><span data-stu-id="07a76-131">To help ensure stable and secure operation, the user should verify the digital signature of a text service before the text service is allowed to load.</span></span> <span data-ttu-id="07a76-132">Инструкции по созданию цифровой подписи см. в разделе [Введение в подписывание кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="07a76-132">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) for the proper procedure to create a digital signature.</span></span>
-   <span data-ttu-id="07a76-133">**Проверка ошибок:** Каждый вызов метода или функции должен быть проверен на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="07a76-133">**Error Checking:** Each method or function call should be checked for success.</span></span> <span data-ttu-id="07a76-134">В случае сбоя оставшийся метод или вызовы функций должны быть пропущены.</span><span class="sxs-lookup"><span data-stu-id="07a76-134">In the event of failure, the remaining method or function calls should be skipped.</span></span> <span data-ttu-id="07a76-135">Большинство примеров кода в этой документации имеют ограниченную проверку на наличие ошибок или ни одного, чтобы не скрывать проиллюстрированную точку.</span><span class="sxs-lookup"><span data-stu-id="07a76-135">Most of the code examples in this documentation have limited error checking, or none at all, to avoid obscuring the point to be illustrated.</span></span> <span data-ttu-id="07a76-136">Не следует вставлять примеры из документации непосредственно в рабочий код; Вместо этого следует усовершенствовать примеры, добавив собственную проверку ошибок.</span><span class="sxs-lookup"><span data-stu-id="07a76-136">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

-   <span data-ttu-id="07a76-137">**Вызовы LoadLibrary:** Чтобы получить указатель на любую из [функций TSF](text-services-framework-functions.md), необходимо использовать [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="07a76-137">**LoadLibrary Calls:** To obtain a pointer to any of the [TSF functions](text-services-framework-functions.md), you will need to use [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="07a76-138">Однако важно следовать процедурам форматирования имени пути библиотеки DLL, как указано в документации по **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="07a76-138">However, it is important to follow procedures for formatting the DLL path name, as given in **LoadLibrary** documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07a76-139">См. также</span><span class="sxs-lookup"><span data-stu-id="07a76-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07a76-140">Рекомендации по обеспечению безопасности</span><span class="sxs-lookup"><span data-stu-id="07a76-140">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

<span data-ttu-id="07a76-141">[Знакомство с подписыванием кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07a76-141">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="07a76-142">Функции TSF</span><span class="sxs-lookup"><span data-stu-id="07a76-142">TSF functions</span></span>](text-services-framework-functions.md)
</dt> <dt>

[<span data-ttu-id="07a76-143">LoadLibrary</span><span class="sxs-lookup"><span data-stu-id="07a76-143">LoadLibrary</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="07a76-144">Функция GetProcAddress</span><span class="sxs-lookup"><span data-stu-id="07a76-144">GetProcAddress</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 