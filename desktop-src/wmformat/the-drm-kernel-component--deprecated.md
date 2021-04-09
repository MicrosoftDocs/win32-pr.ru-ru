---
title: Компонент ядра DRM (не рекомендуется)
description: Компонент ядра DRM (не рекомендуется)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Пакет SDK для формата Windows Media, Microsoft Secure Audio Path (SAP)
- Управление цифровыми правами (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Управление цифровыми правами), Microsoft Secure Audio Path (SAP)
- Windows Media Format SDK, защищенный звуковой путь (SAP)
- Управление цифровыми правами (DRM), защищенный звуковой путь (SAP)
- DRM (Управление цифровыми правами), безопасный звуковой путь (SAP)
- Windows Media Format SDK, компонент ядра DRM
- Управление цифровыми правами (DRM), компонент ядра
- DRM (Управление цифровыми правами), компонент ядра
- Microsoft Secure Audio Path (SAP), компонент ядра DRM
- Безопасный звуковой путь (SAP), компонент ядра DRM
- SAP (безопасный звуковой путь), компонент ядра DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacc0074fdf390ca478ed41b59188ad42ec193c1
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070836"
---
# <a name="the-drm-kernel-component-deprecated"></a><span data-ttu-id="396f2-115">Компонент ядра DRM (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="396f2-115">The DRM Kernel Component (deprecated)</span></span>

<span data-ttu-id="396f2-116">На этой странице документируется функция, которая будет поддерживаться с другим техническим решением в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="396f2-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="396f2-117">В модели Microsoft Secure Audio Path (SAP) компонент ядра DRM предоставляет две основные функции, которые защищают целостность зашифрованной музыки.</span><span class="sxs-lookup"><span data-stu-id="396f2-117">In the Microsoft Secure Audio Path (SAP) model, the DRM kernel component provides two basic features that protect the integrity of encrypted music.</span></span>

<span data-ttu-id="396f2-118">Во-первых, клиентский компонент DRM и компонент ядра DRM находятся в связи при воспроизведении музыкального файла.</span><span class="sxs-lookup"><span data-stu-id="396f2-118">First, the DRM client component and the DRM kernel component are in communication when a music file is played.</span></span> <span data-ttu-id="396f2-119">Такое взаимодействие между компонентами предотвращает незаконное изменение зашифрованного сигнала или вставку ложных сведений.</span><span class="sxs-lookup"><span data-stu-id="396f2-119">This communication between components prevents anyone from tampering with the encrypted signal or from inserting false information.</span></span>

<span data-ttu-id="396f2-120">Во вторых, компонент ядра DRM не расшифровывает звуковый сигнал до тех пор, пока все остальные компоненты не проходят проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="396f2-120">Second, the DRM kernel component does not decrypt the music signal until all remaining components are authenticated.</span></span> <span data-ttu-id="396f2-121">То есть перед расшифровкой содержимого и передачей его следующему системному компоненту Компонент ядра DRM проверяет каждый компонент, который остается в пути к звуковой плате (каждый компонент, который имеет доступ к содержимому), и проверяет, подписаны ли эти компоненты сертификатом от Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="396f2-121">That is, before decrypting content and passing it to the next system component, the DRM kernel component checks each component that remains in the path to the sound card (each component that can access the content) and verifies that these components are signed with a certificate from Microsoft.</span></span> <span data-ttu-id="396f2-122">Неподписанный компонент может указывать на подозрительный компонент или вредоносный драйвер.</span><span class="sxs-lookup"><span data-stu-id="396f2-122">An unsigned component might indicate a suspicious component or a malicious driver.</span></span> <span data-ttu-id="396f2-123">Таким образом, когда компонент ядра DRM проверяет оставшиеся компоненты, если какой-либо компонент не проходит этот тест, сигнал останавливается и не может быть воспроизведен.</span><span class="sxs-lookup"><span data-stu-id="396f2-123">So, when the DRM kernel component validates remaining components, if any component fails this test, the signal is halted and cannot be played.</span></span> <span data-ttu-id="396f2-124">В противном случае, если все компоненты прошли проверку, компонент ядра DRM расшифровывает музыку и передает ее следующему компоненту.</span><span class="sxs-lookup"><span data-stu-id="396f2-124">Otherwise, if all components pass validation, the DRM kernel component decrypts the music and passes it to the next component.</span></span>

<span data-ttu-id="396f2-125">Корпорация Майкрософт использует цифровые подписи драйверов, которые® проходят тесты лаборатории WHQL, чтобы гарантировать, что пользователи используют драйверы самого высокого качества.</span><span class="sxs-lookup"><span data-stu-id="396f2-125">Microsoft digitally signs drivers that pass the Windows® Hardware Quality Lab (WHQL) tests to assure users that they are using the highest-quality drivers.</span></span> <span data-ttu-id="396f2-126">Такой подход является стандартным и гарантирует подлинность компонентов, так как подпись не может быть подделана, а код не может быть изменен без уничтожения подписи.</span><span class="sxs-lookup"><span data-stu-id="396f2-126">This practice is standard and guarantees the authenticity of components because the signature cannot be forged, nor can the code be modified without destroying the signature.</span></span> <span data-ttu-id="396f2-127">Драйверы, сертифицированные для защищенного аудио пути, должны защищать звуковые данные, которые они обрабатывают, от доступа ненадежных компонентов.</span><span class="sxs-lookup"><span data-stu-id="396f2-127">Drivers that are certified for Secure Audio Path must protect the audio data they process from access by untrusted components.</span></span> 

<span data-ttu-id="396f2-128">Драйверы, входящие в состав Windows Millennium Edition и Windows XP, обновляются для обеспечения защищенного аудио пути и подписания.</span><span class="sxs-lookup"><span data-stu-id="396f2-128">Drivers included with Windows Millennium Edition and Windows XP are updated for Secure Audio Path and signed.</span></span> <span data-ttu-id="396f2-129">Драйверы, которые не подписаны на использование с Windows Me или Windows XP, не могут воспроизвести защищенную музыку.</span><span class="sxs-lookup"><span data-stu-id="396f2-129">Drivers that are not signed for use with Windows Me or Windows XP cannot play protected music.</span></span> <span data-ttu-id="396f2-130">Изготовители драйверов могут повторно выдавать обновленные версии драйверов, подписанные WHQL, и публиковать их в Интернете для загрузки клиентами.</span><span class="sxs-lookup"><span data-stu-id="396f2-130">Driver manufacturers can reissue updated versions of their drivers that are signed by WHQL, and publish them on the Internet for consumers to download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="396f2-131">См. также</span><span class="sxs-lookup"><span data-stu-id="396f2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="396f2-132">**Путь безопасного аудио (Майкрософт)**</span><span class="sxs-lookup"><span data-stu-id="396f2-132">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




