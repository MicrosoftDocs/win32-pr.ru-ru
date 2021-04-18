---
title: Упаковка подключаемых модулей DSP
description: Упаковка подключаемых модулей DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Подключаемые модули проигрывателя Windows Media, конвейер Media Foundation
- подключаемые модули, конвейер Media Foundation
- подключаемые модули обработки цифровых сигналов, конвейер Media Foundation
- Подключаемые модули DSP, конвейер Media Foundation
- Конвейер Media Foundation
- Подключаемые модули проигрывателя Windows Media, конвейер DirectShow
- подключаемые модули, конвейер DirectShow
- подключаемые модули обработки цифровых сигналов, конвейер DirectShow
- Подключаемые модули DSP, конвейер DirectShow
- Конвейер DirectShow
- подключаемые модули обработки цифровых сигналов, базовый
- Подключаемые модули DSP, базовый
- Подключаемые модули проигрывателя Windows Media, базовый DSP
- подключаемые модули, базовый DSP
- базовые подключаемые модули DSP
- Подключаемые модули проигрывателя Windows Media с двойным режимом DSP
- подключаемые модули с двойным режимом (DSP)
- подключаемые модули обработки цифровых сигналов, двойной режим
- Подключаемые модули DSP, двойной режим
- подключаемые модули DSP с двойным режимом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691568"
---
# <a name="dsp-plug-in-packaging"></a><span data-ttu-id="8e95a-123">Упаковка подключаемых модулей DSP</span><span class="sxs-lookup"><span data-stu-id="8e95a-123">DSP Plug-in Packaging</span></span>

<span data-ttu-id="8e95a-124">Проигрыватель Windows Media визуализирует аудио и видео с помощью одного из следующих конвейеров.</span><span class="sxs-lookup"><span data-stu-id="8e95a-124">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="8e95a-125">DirectShow</span><span class="sxs-lookup"><span data-stu-id="8e95a-125">DirectShow</span></span>
-   <span data-ttu-id="8e95a-126">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8e95a-126">Media Foundation</span></span>

<span data-ttu-id="8e95a-127">В Microsoft Windows XP и более ранних версиях проигрыватель использует DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8e95a-127">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="8e95a-128">В Windows Vista проигрыватель иногда использует DirectShow и иногда использует Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8e95a-128">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="8e95a-129">Подключаемый модуль DSP, предназначенный для работы в конвейере DirectShow, называется *базовым подключаемым модулем DSP*.</span><span class="sxs-lookup"><span data-stu-id="8e95a-129">A DSP plug-in that is designed to run in the DirectShow pipeline is called a *basic DSP plug-in*.</span></span> <span data-ttu-id="8e95a-130">Основные подключаемые модули DSP выступает в качестве объекта мультимедиа DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="8e95a-130">A basic DSP plug-ins acts as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="8e95a-131">Базовый подключаемый модуль DSP может работать в конвейере DirectShow в собственном режиме и также может выполняться в конвейере Media Foundation в оболочке, предоставляемой Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8e95a-131">A basic DSP plug-in can run natively in the DirectShow pipeline and can also run in the Media Foundation pipeline inside a wrapper provided by Media Foundation.</span></span>

<span data-ttu-id="8e95a-132">Подключаемый модуль DSP, предназначенный для работы в собственном режиме (не требуется обертка) в конвейерах DirectShow и Media Foundation называется *подключаемым модулем DSP с двойным режимом*.</span><span class="sxs-lookup"><span data-stu-id="8e95a-132">A DSP plug-in that is designed to run natively (no wrapper required) in both the DirectShow and Media Foundation pipelines is called a *dual-mode DSP plug-in*.</span></span> <span data-ttu-id="8e95a-133">Подключаемый модуль DSP с двойным режимом может действовать как DMO или как преобразование Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="8e95a-133">A dual-mode DSP plug-in can act as a DMO or as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="8e95a-134">Подключаемый модуль DSP — это COM-объект, упакованный в виде DLL-файла с собственной регистрацией.</span><span class="sxs-lookup"><span data-stu-id="8e95a-134">A DSP plug-in is a COM object that is packaged as a self-registering .dll file.</span></span> <span data-ttu-id="8e95a-135">Интерфейсы, реализуемые подключаемым модулем, зависят от того, является ли подключаемый модуль базовым подключаемым модулем DSP или подключаемым модулем DSP с двойным режимом.</span><span class="sxs-lookup"><span data-stu-id="8e95a-135">The interfaces that the plug-in implements depend on whether the plug-in is designed as a basic DSP plug-in or as a dual-mode DSP plug-in.</span></span> <span data-ttu-id="8e95a-136">Подробные сведения о интерфейсах, которые должны реализовывать подключаемые модули DSP, см. в разделе [необходимые интерфейсы](required-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="8e95a-136">For detailed information about the interfaces that DSP plug-ins must implement, see [Required Interfaces](required-interfaces.md).</span></span>

<span data-ttu-id="8e95a-137">Подключаемый модуль DSP, который выполняется в конвейере Media Foundation (в собственном или упакованном), должен зарегистрировать свою потоковую модель как "оба".</span><span class="sxs-lookup"><span data-stu-id="8e95a-137">A DSP plug-in that runs in the Media Foundation pipeline (either natively or wrapped) must register its threading model as "Both".</span></span> <span data-ttu-id="8e95a-138">Подробные сведения о подразделах и записях реестра, связанных с подключаемыми модулями DSP, см. в разделе [Регистрация подключаемых модулей DSP](registering-dsp-plug-ins.md).</span><span class="sxs-lookup"><span data-stu-id="8e95a-138">For detailed information about registry subkeys and entries associated with DSP plug-ins, see [Registering DSP Plug-ins](registering-dsp-plug-ins.md).</span></span>

<span data-ttu-id="8e95a-139">Подключаемый модуль DSP, реализующий пользовательские интерфейсы и выполняющийся в конвейере Media Foundation (в собственном или упакованном), должен составлять пару с файлом прокси-заглушки. dll, который может маршалировать пользовательские интерфейсы через границы процесса.</span><span class="sxs-lookup"><span data-stu-id="8e95a-139">A DSP plug-in that implements custom interfaces and runs in the Media Foundation pipeline (either natively or wrapped) must be paired with a proxy-stub .dll file that can marshal the custom interfaces across process boundaries.</span></span> <span data-ttu-id="8e95a-140">Сведения о компоненте прокси-заглушки см. в разделе [обновление существующих подключаемых модулей DSP](updating-existing-dsp-plug-ins.md) и [обновлений в мастере подключаемых модулей DSP для проигрывателя Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="8e95a-140">For information about the proxy-stub component, see [Updating Existing DSP Plug-ins](updating-existing-dsp-plug-ins.md) and [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span>

<span data-ttu-id="8e95a-141">Подключаемые модули DSP не должны создаваться как singleton-объекты.</span><span class="sxs-lookup"><span data-stu-id="8e95a-141">DSP plug-in objects must not be created as singletons.</span></span> <span data-ttu-id="8e95a-142">Проигрыватель Windows Media должен иметь возможность создавать несколько отдельных экземпляров определенного подключаемого модуля DSP.</span><span class="sxs-lookup"><span data-stu-id="8e95a-142">Windows Media Player must be able to create multiple separate instances of a particular DSP plug-in.</span></span>

<span data-ttu-id="8e95a-143">Подключаемые модули DSP, которые выполняются в пути к защищенному носителю (PMP) Windows Vista, должны быть подписаны.</span><span class="sxs-lookup"><span data-stu-id="8e95a-143">DSP plug-ins that run in the Windows Vista Protected Media Path (PMP) must be signed.</span></span> <span data-ttu-id="8e95a-144">Дополнительные сведения см. [в статье подписывание кода для защищенных компонентов мультимедиа в Windows Vista](/windows-hardware/test/hlk/).</span><span class="sxs-lookup"><span data-stu-id="8e95a-144">For more information, see [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e95a-145">См. также</span><span class="sxs-lookup"><span data-stu-id="8e95a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e95a-146">**Обзор подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="8e95a-146">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 