---
title: Выполнение индивидуальной управления цифровыми правами
description: Выполнение индивидуальной управления цифровыми правами
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- Windows Media Format SDK, расширенные API клиента DRM
- Пакет SDK для Windows Media Format, расширенные API клиента
- Windows Media Format SDK, расширенные API
- Windows Media Format SDK, API
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Пакет SDK для Windows Media Format, индивидуальное управление цифровыми правами DRM
- Пакет SDK для Windows Media Format, индивидуальное
- Управление цифровыми правами (DRM), расширенные API клиента
- DRM (Управление цифровыми правами), расширенные API клиента
- Управление цифровыми правами (DRM), расширенные API
- DRM (Управление цифровыми правами), расширенные API
- Управление цифровыми правами (DRM), API
- DRM (Управление цифровыми правами), API
- Управление цифровыми правами (DRM), индивидуальность
- DRM (Управление цифровыми правами), индивидуальность
- Управление цифровыми правами (DRM), Индивидуальная обработка DRM
- DRM (Управление цифровыми правами), Индивидуальная обработка DRM
- Расширенные API клиента DRM, индивидуальность
- Расширенные API клиента, индивидуальность
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331712"
---
# <a name="performing-drm-individualization"></a><span data-ttu-id="3e1f0-122">Выполнение индивидуальной управления цифровыми правами</span><span class="sxs-lookup"><span data-stu-id="3e1f0-122">Performing DRM Individualization</span></span>

<span data-ttu-id="3e1f0-123">Индивидуальная обработка — это процесс обновления компонента DRM на клиентском компьютере, его шифрование и создание уникального.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-123">Individualization is the process of updating the DRM component on the client computer, encrypting it, and making it unique.</span></span> <span data-ttu-id="3e1f0-124">Если компьютер является отдельным, компонент DRM привязан к компьютеру и не сможет декодировать содержимое на любом другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-124">When a computer is individualized, the DRM component is tied to the computer and will not be able to decode content on any other computer.</span></span> <span data-ttu-id="3e1f0-125">Расширенные API клиента Windows Media DRM обеспечивают поддержку индивидуализинг компонента DRM на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-125">The Windows Media DRM Client Extended APIs provide support for individualizing the DRM component on client computers.</span></span>

<span data-ttu-id="3e1f0-126">Для выполнения индивидуализации выполняется вызов метода [**ивмдрмсекурити::P ерформсекуритюпдате**](iwmdrmsecurity-performsecurityupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="3e1f0-126">Individualization is performed by calling the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method.</span></span> <span data-ttu-id="3e1f0-127">Можно вызвать **перформсекуритюпдате** , чтобы он индивидуализируйте только в том случае, если версия на сервере более новая, чем та, которая установлена на клиентском компьютере, или вы можете принудительно выполнить индивидуальную установку без учета относительных версий системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-127">You can call **PerformSecurityUpdate** so that it will individualize only if the version on the server is newer than the one installed on the client computer, or you can force individualization without regard to the relative security versions.</span></span> <span data-ttu-id="3e1f0-128">Флаг, необходимый для индивидуальной индивидуализации, заключается в \_ обеспечении безопасности WMDRM для \_ выполнения \_ индив.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-128">The flag for as-needed individualization is WMDRM\_SECURITY\_PERFORM\_INDIV.</span></span> <span data-ttu-id="3e1f0-129">Флаг принудительной индивидуализации является \_ защитой WMDRM \_ . выполните \_ принудительный \_ индив.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-129">The flag for forced individualization is WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV.</span></span>

<span data-ttu-id="3e1f0-130">**Перформсекуритюпдате** является асинхронным вызовом.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-130">**PerformSecurityUpdate** is an asynchronous call.</span></span> <span data-ttu-id="3e1f0-131">Он будет быстро возвращаться, а затем создавать события для предоставления сведений о состоянии процесса индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-131">It will return quickly and then generate events to provide status information about the individualization process.</span></span> <span data-ttu-id="3e1f0-132">Большинство создаваемых событий будут **мевмдрминдивидуализатионпрогресс** событиями, и у каждого из них будет связанный интерфейс [**ивмдрминдивидуализатионстатус**](iwmdrmindividualizationstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="3e1f0-132">The majority of the events generated will be **MEWMDRMIndividualizationProgress** events, and each has an associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span> <span data-ttu-id="3e1f0-133">Чтобы получить интерфейс состояния, необходимо вызвать метод **имфмедиаевент:: GetValue** , чтобы получить указатель **IUnknown** , наявляющийся в том же объекте, а затем запросить его для **ивмдрминдивидуализатионстатус**.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-133">To get the status interface, you must call **IMFMediaEvent::GetValue** to retrieve an **IUnknown** pointer that is on the same object and then query it for **IWMDRMIndividualizationStatus**.</span></span>

<span data-ttu-id="3e1f0-134">Вы можете получить данные для структуры [**\_ \_ состояния WM индивидуализируйте**](drmwm-individualize-status.md) , вызвав [**ивмдрминдивидуализестатус::-Status**](iwmdrmindividualizationstatus-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="3e1f0-134">You can get data for a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure by calling [**IWMDRMIndividualizeStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md).</span></span> <span data-ttu-id="3e1f0-135">Каждое создаваемое событие имеет свой собственный объект с состоянием, поэтому необходимо пройти процесс получения значения события и запроса состояния для каждого раза.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-135">Each event that is generated has its own object with status, so you must go through the process of getting the event value and querying for the status interface every time.</span></span>

<span data-ttu-id="3e1f0-136">В зависимости от размера загружаемых данных может возникнуть десятки или сотни событий **мевмдрминдивидуализатионпрогресс** .</span><span class="sxs-lookup"><span data-stu-id="3e1f0-136">Depending on the size of the download, there may be dozens or hundreds of **MEWMDRMIndividualizationProgress** events.</span></span> <span data-ttu-id="3e1f0-137">По завершении процесса индивидуализации создается событие **мевмдрминдивидуализатионкомплетед** .</span><span class="sxs-lookup"><span data-stu-id="3e1f0-137">When the individualization process is finished, an **MEWMDRMIndividualizationCompleted** event is generated.</span></span>

<span data-ttu-id="3e1f0-138">После завершения индивидуализации единственными существующими объектами, которые будут отражать новое отдельное состояние, являются те, которые наследуют от [**ивмдрмсекурити**](iwmdrmsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="3e1f0-138">When individualization is completed, the only existing objects that will reflect the new individualized state are those that inherit from [**IWMDRMSecurity**](iwmdrmsecurity.md).</span></span> <span data-ttu-id="3e1f0-139">Все остальные существующие объекты не будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-139">All other existing objects will not be updated.</span></span> <span data-ttu-id="3e1f0-140">Необходимо освободить и повторно создать все другие объекты, чтобы они отражали новое отдельное состояние.</span><span class="sxs-lookup"><span data-stu-id="3e1f0-140">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e1f0-141">См. также</span><span class="sxs-lookup"><span data-stu-id="3e1f0-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e1f0-142">**Пример индивидуализации DRM**</span><span class="sxs-lookup"><span data-stu-id="3e1f0-142">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="3e1f0-143">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="3e1f0-143">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="3e1f0-144">**Использование модели событий Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="3e1f0-144">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> <dt>

<span data-ttu-id="3e1f0-145">[Рекомендации по индивидуальному использованию DRM для Windows Media](/previous-versions/ms867216(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3e1f0-145">[Windows Media DRM Individualization Best Practices](/previous-versions/ms867216(v=msdn.10))</span></span>
</dt> </dl>

 

 




