---
title: Новые возможности в TSF
description: В выпуске Microsoft WindowsXP Service пакетом среда текстовых служб (TSF) имеет несколько новых функций.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Платформа текстовых служб (TSF), новые функции
- TSF (платформа текстовых служб), новые функции
- текстовые службы, новые функции
- Приложения с поддержкой TSF, новые функции
- Платформа текстовых служб (TSF), расширенная поддержка
- TSF (платформа текстовых служб), расширенная поддержка
- службы текстового ввода, расширенная поддержка
- Приложения с поддержкой TSF, расширенная поддержка
- Платформа текстовых служб (TSF), Расширенное редактирование
- TSF (платформа текстовых служб), Расширенное редактирование
- текстовые службы, Расширенное редактирование
- Приложения с поддержкой TSF, Расширенное редактирование
- Расширенное редактирование
- Платформа текстовых служб (TSF), безопасность
- TSF (платформа текстовых служб), безопасность
- службы текстового ввода, безопасность
- Приложения с поддержкой TSF, безопасность
- безопасность для TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a345087304be638be93fa352845cdd468bf15
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413054"
---
# <a name="new-features-in-tsf"></a><span data-ttu-id="5456e-121">Новые возможности в TSF</span><span class="sxs-lookup"><span data-stu-id="5456e-121">New Features in TSF</span></span>

<span data-ttu-id="5456e-122">В выпуске Microsoft WindowsXP Service пакетом среда текстовых служб (TSF) имеет несколько новых функций.</span><span class="sxs-lookup"><span data-stu-id="5456e-122">With the release of Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) has several new features.</span></span>

## <a name="extended-support-of-advanced-text-services"></a><span data-ttu-id="5456e-123">Расширенная поддержка расширенных текстовых служб</span><span class="sxs-lookup"><span data-stu-id="5456e-123">Extended Support of Advanced Text Services</span></span>

<span data-ttu-id="5456e-124">В TSF и Windows добавлена поддержка для обеспечения согласованного пользовательского интерфейса для всех приложений на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="5456e-124">Support has been added to TSF and Windows to provide a consistent user interface for all applications across the desktop.</span></span> <span data-ttu-id="5456e-125">Эта новая поддержка позволяет использовать устаревшие приложения или элементы управления, не поддерживающие TSF, для бесплатной работы с некоторыми расширенными текстовыми службами.</span><span class="sxs-lookup"><span data-stu-id="5456e-125">This new support enables legacy applications or controls that are not aware of TSF to take advantage of some advanced text services for free.</span></span> <span data-ttu-id="5456e-126">Например, Диктовка речи и рукописный ввод теперь можно использовать для ввода текста в документ в любом приложении.</span><span class="sxs-lookup"><span data-stu-id="5456e-126">For example, speech dictation and handwriting can now be used to enter text into a document in any application.</span></span>

<span data-ttu-id="5456e-127">Эта новая функция доступна только для WindowsXP Service пакетом или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5456e-127">This new feature is available only for WindowsXP Service Pack1 or later.</span></span> <span data-ttu-id="5456e-128">По умолчанию он отключен.</span><span class="sxs-lookup"><span data-stu-id="5456e-128">It is turned off by default.</span></span> <span data-ttu-id="5456e-129">Чтобы включить его, установите флажок на вкладке " **Дополнительно** " в разделе " **службы текстового ввода и входные языки** " панели управления " **язык и региональные стандарты** ".</span><span class="sxs-lookup"><span data-stu-id="5456e-129">To enable it, click the check box in the new **Advanced** tab in the **Text Services and Input Languages** portion of the **Regional and Language Options** control panel.</span></span>

![Поддержка неосведомленных приложений в панели управления TSF](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a><span data-ttu-id="5456e-131">Поддержка расширенного редактирования</span><span class="sxs-lookup"><span data-stu-id="5456e-131">Rich Edit Support</span></span>

<span data-ttu-id="5456e-132">[Расширенное редактирование Microsoft®](../controls/rich-edit-controls.md) Версия 4,1, используемая приложениями для просмотра и редактирования текста со специальным форматированием символов и абзацев, теперь предоставляет функциональные возможности TSF.</span><span class="sxs-lookup"><span data-stu-id="5456e-132">[Microsoft® Rich Edit](../controls/rich-edit-controls.md) Version 4.1, used by applications to view and edit text with special character and paragraph formatting, now exposes TSF functionality.</span></span> <span data-ttu-id="5456e-133">По умолчанию эта поддержка отключена.</span><span class="sxs-lookup"><span data-stu-id="5456e-133">By default this support is turned off.</span></span> <span data-ttu-id="5456e-134">Чтобы включить TSF в расширенном редактировании, приложение размещения отправляет специальное сообщение в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="5456e-134">To enable TSF in Rich Edit, a hosting application sends a special window message to the Rich Edit control.</span></span>

## <a name="security-improvements"></a><span data-ttu-id="5456e-135">Усовершенствования системы безопасности</span><span class="sxs-lookup"><span data-stu-id="5456e-135">Security Improvements</span></span>

<span data-ttu-id="5456e-136">Безопасность и надежность TSF были значительно улучшены, чтобы снизить вероятность того, что вредоносная программа сможет получить доступ к стеку, куче или другим защищенным местам в памяти.</span><span class="sxs-lookup"><span data-stu-id="5456e-136">The security and robustness of TSF have been substantially improved, to reduce the likelihood of a hostile program being able to access the stack, heap, or other secure memory locations.</span></span> <span data-ttu-id="5456e-137">Также улучшена безопасность примеров приложений и текстовых служб пакета средств разработки программного обеспечения (SDK).</span><span class="sxs-lookup"><span data-stu-id="5456e-137">The security of software development kit (SDK) sample applications and text services has also been improved.</span></span>

 

 