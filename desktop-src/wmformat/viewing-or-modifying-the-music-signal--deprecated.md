---
title: Просмотр или изменение музыкального сигнала (не рекомендуется)
description: Просмотр или изменение музыкального сигнала (не рекомендуется)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- Пакет SDK для формата Windows Media, Microsoft Secure Audio Path (SAP)
- Управление цифровыми правами (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Управление цифровыми правами), Microsoft Secure Audio Path (SAP)
- Windows Media Format SDK, защищенный звуковой путь (SAP)
- Управление цифровыми правами (DRM), защищенный звуковой путь (SAP)
- DRM (Управление цифровыми правами), безопасный звуковой путь (SAP)
- Пакет SDK для Windows Media Format, просмотр или изменение музыкального сигнала
- Управление цифровыми правами (DRM), просмотр или изменение музыкального сигнала
- DRM (Управление цифровыми правами), просмотр или изменение музыкального сигнала
- Microsoft Secure Audio Path (SAP), просмотр или изменение музыкального сигнала
- Безопасный звуковой путь (SAP), просмотр или изменение музыкального сигнала
- SAP (безопасный звуковой путь), просмотр или изменение музыкального сигнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691358"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a><span data-ttu-id="f9ff3-115">Просмотр или изменение музыкального сигнала (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="f9ff3-115">Viewing or Modifying the Music Signal (deprecated)</span></span>

<span data-ttu-id="f9ff3-116">На этой странице документируется функция, которая будет поддерживаться с другим техническим решением в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="f9ff3-117">В модели Microsoft Secure Audio Path (SAP) приложения не могут изменять защищенную музыку каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-117">In the Microsoft Secure Audio Path (SAP) model, applications cannot modify protected music in any way.</span></span> <span data-ttu-id="f9ff3-118">Например, когда приложение пытается перехватить музыкальный сигнал, сигнал звучит как случайный шум.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-118">For example, when an application attempts to intercept a music signal, the signal sounds like random noise.</span></span> <span data-ttu-id="f9ff3-119">В результате приложения, которые обычно изменяют сигналы (например, эквалайзер), не могут изменить звук музыки.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-119">As a result, applications that normally modify signals (such as an equalizer) cannot change the sound of the music.</span></span>

<span data-ttu-id="f9ff3-120">Некоторые приложения просто просматривают музыкальный сигнал.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-120">Some applications merely view a music signal.</span></span> <span data-ttu-id="f9ff3-121">Например, некоторые приложения отображают мигающие индикаторы во времени с помощью звукового сигнала, но не изменяют их.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-121">For example, some applications display flashing lights in time with the music signal, but do not modify it.</span></span> <span data-ttu-id="f9ff3-122">Для размещения приложений, которые просматривают сигналы, небольшая часть музыки расшифровывается и передается в виде четких данных с зашифрованным содержимым.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-122">To accommodate applications that view signals, a small part of the music is decrypted and passed in clear form with the encrypted content.</span></span> <span data-ttu-id="f9ff3-123">Полученный сигнал очень плох (хуже, чем качество телефона), но может быть достаточно для приложений, которые просматривают сигналы.</span><span class="sxs-lookup"><span data-stu-id="f9ff3-123">The resulting signal is very poor (worse than telephone quality) but can suffice for applications that view signals.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9ff3-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f9ff3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9ff3-125">**Путь безопасного аудио (Майкрософт)**</span><span class="sxs-lookup"><span data-stu-id="f9ff3-125">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




