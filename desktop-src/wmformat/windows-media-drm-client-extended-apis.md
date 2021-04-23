---
title: Расширенные API клиента DRM Windows Media
description: Расширенные API клиента DRM Windows Media
ms.assetid: c0397aa8-1f5a-48f5-a96b-555079e9a292
keywords:
- Windows Media Format SDK, расширенные API клиента DRM
- Пакет SDK для Windows Media Format, расширенные API клиента
- Windows Media Format SDK, расширенные API
- Windows Media Format SDK, API
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Управление цифровыми правами (DRM), расширенные API клиента
- DRM (Управление цифровыми правами), расширенные API клиента
- Управление цифровыми правами (DRM), расширенные API
- DRM (Управление цифровыми правами), расширенные API
- Управление цифровыми правами (DRM), API
- DRM (Управление цифровыми правами), API
- Расширенные API клиента DRM, о
- Расширенные API клиента, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c33ef3649f2cda63713ebd22a0116fdd025144
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413041"
---
# <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="d8522-116">Расширенные API клиента DRM Windows Media</span><span class="sxs-lookup"><span data-stu-id="d8522-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="d8522-117">\[Компонент Windows Media DRM является устаревшим и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="d8522-117">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="d8522-118">Вместо этого используйте [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="d8522-118">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="d8522-119">В этой документации описываются расширенные API-интерфейсы Microsoft Windows Media Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="d8522-119">This documentation describes the Microsoft Windows Media Digital Rights Management (DRM) Client Extended Application Programming Interfaces (APIs).</span></span> <span data-ttu-id="d8522-120">Расширенные API клиента DRM Windows Media включают объекты, которые можно использовать для управления операциями с цифровыми Rights Managementми Windows Media на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="d8522-120">The Windows Media DRM Client Extended APIs include objects that can be used to manage Windows Media Digital Rights Management (DRM) operations on a client computer.</span></span>

<span data-ttu-id="d8522-121">Основной задачей этих API является Управление лицензиями для защищенного цифрового содержимого мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d8522-121">The primary focus of these APIs is the management of licenses for protected digital media content.</span></span> <span data-ttu-id="d8522-122">Кроме того, API-интерфейсы можно использовать для обновления компонентов DRM на клиентском компьютере и для создания приложений, передающих содержимое с помощью Windows Media DRM для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="d8522-122">In addition, the APIs can be used to update the DRM components on the client computer and to create applications that transmit content using Windows Media DRM for Network Devices.</span></span>

<span data-ttu-id="d8522-123">Эти интерфейсы API составляют клиентский аналог пакета SDK Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="d8522-123">These APIs constitute the client-side counterpart to the Windows Media Rights Manager SDK.</span></span> <span data-ttu-id="d8522-124">Когда Windows Media Rights Manager используется для создания веб-службы, защищающих файлы и выдающий лицензии, расширенные API клиента DRM Windows Media используются для создания приложений, использующих это содержимое.</span><span class="sxs-lookup"><span data-stu-id="d8522-124">Where Windows Media Rights Manager is used to create online services that protect files and issue licenses, the Windows Media DRM Client Extended APIs are used to create applications that consume that content.</span></span>

<span data-ttu-id="d8522-125">Этот документ содержит следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="d8522-125">This document includes the following sections.</span></span>



| <span data-ttu-id="d8522-126">Section</span><span class="sxs-lookup"><span data-stu-id="d8522-126">Section</span></span>                                                                                                  | <span data-ttu-id="d8522-127">Описание</span><span class="sxs-lookup"><span data-stu-id="d8522-127">Description</span></span>                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8522-128">О расширенных API-интерфейсах клиента DRM Windows Media</span><span class="sxs-lookup"><span data-stu-id="d8522-128">About the Windows Media DRM Client Extended APIs</span></span>](about-the-windows-media-drm-client-extended-apis.md) | <span data-ttu-id="d8522-129">Содержит обзор и общие сведения, с которыми следует ознакомиться до разработки приложений, использующих API-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="d8522-129">Provides overview and background information that you should be familiar with before developing applications that use the APIs.</span></span>                                                        |
| [<span data-ttu-id="d8522-130">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="d8522-130">Programming Guide</span></span>](drm-programming-guide.md)                                                           | <span data-ttu-id="d8522-131">Содержит подробные инструкции по выполнению различных операций управления цифровыми правами на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="d8522-131">Provides detailed instructions for performing various client-side DRM operations.</span></span>                                                                                                      |
| [<span data-ttu-id="d8522-132">Справочник по программированию</span><span class="sxs-lookup"><span data-stu-id="d8522-132">Programming Reference</span></span>](drm-programming-reference.md)                                                   | <span data-ttu-id="d8522-133">Содержит справочные сведения о интерфейсах, методах, функциях, структурах, типах перечислений и константах, которые включены в расширенные API клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d8522-133">Provides reference information about the interfaces, methods, functions, structures, enumeration types, and constants that are included in the Windows Media DRM Client Extended APIs.</span></span> |



 

 

 