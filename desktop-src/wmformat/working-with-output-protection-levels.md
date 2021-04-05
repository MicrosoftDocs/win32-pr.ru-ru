---
title: Работа с уровнями защиты выходных данных
description: Работа с уровнями защиты выходных данных
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows Media Format SDK, уровни защиты выходных данных (ОПЛ)
- Windows Media Format SDK, уровни защиты
- Расширенный формат систем (ASF), уровни защиты выходных данных (ОПЛ)
- ASF (Расширенный системный формат), уровни защиты выходных данных (ОПЛ)
- Расширенный формат систем (ASF), уровни защиты
- ASF (Расширенный системный формат), уровни защиты
- Расширенный формат систем (ASF), несколько лицензий
- ASF (Расширенный системный формат), несколько лицензий
- Управление цифровыми правами (DRM), уровни защиты выходных данных (ОПЛ)
- DRM (Управление цифровыми правами), уровни защиты выходных данных (ОПЛ)
- Управление цифровыми правами (DRM), уровни защиты
- DRM (Управление цифровыми правами), уровни защиты
- Управление цифровыми правами (DRM), оценка уровней защиты выходных данных (ОПЛ)
- DRM (Управление цифровыми правами), оценка уровней защиты выходных данных (ОПЛ)
- Управление цифровыми правами (DRM), несколько лицензий
- DRM (Управление цифровыми правами), несколько лицензий
- уровни защиты выходных данных (ОПЛ)
- ОПЛ (уровни защиты выходных данных)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336255"
---
# <a name="working-with-output-protection-levels"></a><span data-ttu-id="23025-121">Работа с уровнями защиты выходных данных</span><span class="sxs-lookup"><span data-stu-id="23025-121">Working with Output Protection Levels</span></span>

<span data-ttu-id="23025-122">Лицензии, созданные с помощью пакета SDK Windows Media Rights Manager 10, могут определять ограничения действий с помощью уровней защиты выходных данных (Оплс).</span><span class="sxs-lookup"><span data-stu-id="23025-122">Licenses created by using the Windows Media Rights Manager 10 SDK can specify action restrictions using output protection levels (OPLs).</span></span> <span data-ttu-id="23025-123">Оплс позволяют создателю лицензий разрешать некоторые действия только на устройствах с определенными технологиями.</span><span class="sxs-lookup"><span data-stu-id="23025-123">OPLs enable a license creator to allow some actions only on devices with specific technologies.</span></span> <span data-ttu-id="23025-124">Преимущества использования Оплс в том, что вы получаете больше гибкости при создании ограничений лицензий по сравнению с предыдущими версиями.</span><span class="sxs-lookup"><span data-stu-id="23025-124">The benefits of using OPLs is that you get more flexibility in creating license restrictions than previous versions.</span></span> <span data-ttu-id="23025-125">Кроме того, Оплс можно развернуть для поддержки будущих технологий.</span><span class="sxs-lookup"><span data-stu-id="23025-125">In addition, OPLs are expandable to accommodate future technologies.</span></span> <span data-ttu-id="23025-126">Вы можете поддерживать такие лицензии в приложениях с помощью методов интерфейса [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) .</span><span class="sxs-lookup"><span data-stu-id="23025-126">You can support such licenses in your applications by using the methods of the [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) interface.</span></span>

<span data-ttu-id="23025-127">Для чтения файлов, защищенных с помощью лицензии с указанием Оплс, необходимо проверить ОПЛ для требуемого действия.</span><span class="sxs-lookup"><span data-stu-id="23025-127">To read files that are protected by a license that specifies OPLs, you must check the OPL for the desired action.</span></span> <span data-ttu-id="23025-128">Технология вывода, используемая приложением, должна быть разрешена ОПЛ в лицензии.</span><span class="sxs-lookup"><span data-stu-id="23025-128">The output technology your application is using must be allowed by the OPL in the license.</span></span> <span data-ttu-id="23025-129">Например, некоторые лицензии для защищенного звука могут потребовать использования защищенного звукового пути для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="23025-129">For example, some licenses for protected audio may require that you use secure audio path to play it.</span></span>

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a><span data-ttu-id="23025-130">Настройка модуля чтения для вычисления уровней защиты выходных данных</span><span class="sxs-lookup"><span data-stu-id="23025-130">Configuring the Reader to Evaluate Output Protection Levels</span></span>

<span data-ttu-id="23025-131">Прежде чем можно будет проверить Оплс для файлов, загруженных в средство чтения, необходимо вызвать метод [**IWMDRMReader2:: сетевалуатеаутпутлевеллиценсес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) , передав **значение true** для параметра *февалуате* .</span><span class="sxs-lookup"><span data-stu-id="23025-131">Before you can check OPLs for files loaded in the reader, you must call the [**IWMDRMReader2::SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) method, passing **TRUE** for the *fEvaluate* parameter.</span></span> <span data-ttu-id="23025-132">Если не вызвать этот метод, лицензии, требующие Оплс, не будут видны вашему приложению.</span><span class="sxs-lookup"><span data-stu-id="23025-132">If you do not call this method, licenses that require OPLs are not visible to your application.</span></span>

## <a name="evaluating-copy-output-protection-levels"></a><span data-ttu-id="23025-133">Оценка уровней защиты выходных данных копирования</span><span class="sxs-lookup"><span data-stu-id="23025-133">Evaluating Copy Output Protection Levels</span></span>

<span data-ttu-id="23025-134">Чтобы получить уровни защиты выходных данных для действия копирования, вызовите метод [**IWMDRMReader2:: жеткопйоутпутлевелс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) .</span><span class="sxs-lookup"><span data-stu-id="23025-134">To get output protection levels for the copy action, call the [**IWMDRMReader2::GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) method.</span></span> <span data-ttu-id="23025-135">Данные, получаемые из вызова, хранятся в структуре [**\_ \_ ОПЛ копии DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) .</span><span class="sxs-lookup"><span data-stu-id="23025-135">The data you receive from the call is stored in a [**DRM\_COPY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) structure.</span></span> <span data-ttu-id="23025-136">Структура содержит базовый уровень защиты выходных данных, который указывает минимальный уровень вывода для действия копирования в лицензии.</span><span class="sxs-lookup"><span data-stu-id="23025-136">The structure contains a base output protection level, which specifies the minimum output level for the copy action in the license.</span></span> <span data-ttu-id="23025-137">Однако \_ Структура копирования ОПЛ DRM \_ также содержит два списка идентификаторов технологий: один для допустимых технологий, которые оцениваются на более низком ОПЛ, чем базовый, и один для технологий, оценка которых равна или выше базовой ОПЛ, но ограничена лицензией.</span><span class="sxs-lookup"><span data-stu-id="23025-137">However, the DRM\_COPY\_OPL structure also contains two lists of technology identifiers: one for allowed technologies that are rated at a lower OPL than the base, and one for technologies that are rated equal to or higher than the base OPL but that are restricted by the license.</span></span> <span data-ttu-id="23025-138">Необходимо проверить включения и исключения, чтобы убедиться, что технология, используемая приложением, разрешена лицензией.</span><span class="sxs-lookup"><span data-stu-id="23025-138">You must check the inclusions and exclusions to ensure that the technology your application is using is allowed by the license.</span></span>

## <a name="evaluating-play-output-protection-levels"></a><span data-ttu-id="23025-139">Оценка уровней защиты выходных данных воспроизведения</span><span class="sxs-lookup"><span data-stu-id="23025-139">Evaluating Play Output Protection Levels</span></span>

<span data-ttu-id="23025-140">Чтобы получить уровни защиты выходных данных для действия воспроизведения, вызовите метод [**IWMDRMReader2:: жетплайаутпутлевелс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) .</span><span class="sxs-lookup"><span data-stu-id="23025-140">To get output protection levels for the play action, call the [**IWMDRMReader2::GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) method.</span></span> <span data-ttu-id="23025-141">Данные, получаемые из вызова, хранятся в структуре [**DRM \_ Play \_ ОПЛ**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) .</span><span class="sxs-lookup"><span data-stu-id="23025-141">The data you receive from the call is stored in a [**DRM\_PLAY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) structure.</span></span> <span data-ttu-id="23025-142">Структура содержит несколько других структур.</span><span class="sxs-lookup"><span data-stu-id="23025-142">The structure contains several other structures.</span></span> <span data-ttu-id="23025-143">Базовые уровни защиты выходных данных для действия воспроизведения хранятся в структуре [**\_ минимальных \_ \_ \_ уровней защиты данных DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (элемент **минопл** элемента **управления DRM \_ Play \_ ОПЛ**), который определяет минимальное ОПЛ, необходимое для воспроизведения содержимого в различных форматах.</span><span class="sxs-lookup"><span data-stu-id="23025-143">The base output protection levels for the play action are stored in a [**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) structure (the **minOPL** member of **DRM\_PLAY\_OPL**), which defines the minimum OPL required to play content in a variety of formats.</span></span> <span data-ttu-id="23025-144">Необходимо проверить элемент на предмет типа выходных форматов, которые доставляет ваше приложение.</span><span class="sxs-lookup"><span data-stu-id="23025-144">You must check the member for the type of output formats that your application delivers.</span></span>

<span data-ttu-id="23025-145">Структура **DRM \_ Play \_ ОПЛ** определяет два типа ограничений: требуется понижение выборки и допустимые идентификаторы защиты вывода видео.</span><span class="sxs-lookup"><span data-stu-id="23025-145">The **DRM\_PLAY\_OPL** structure defines two kinds of restrictions: required down-sampling and allowed video output protection identifiers.</span></span>

<span data-ttu-id="23025-146">Требуемая пониженная выборка определяется как список идентификаторов технологий вывода (элемент **оплиддовнсампле** элемента **управления DRM \_ Play \_ ОПЛ**), который, при использовании, может получить содержимое для воспроизведения только в том случае, если содержимое сначала уменьшается до более низкой скорости.</span><span class="sxs-lookup"><span data-stu-id="23025-146">Required down-sampling is defined as a list of output technology identifiers (the **oplIdDownsample** member of **DRM\_PLAY\_OPL**) that, if used, can receive the content for playback only if the content is first down-sampled to a lower bit rate.</span></span>

<span data-ttu-id="23025-147">Разрешенные идентификаторы защиты видео определяются как список технологий вывода видео с информацией о конфигурации для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="23025-147">Allowed video output protection identifiers are defined as a list of video output technologies with configuration information for each.</span></span>

## <a name="handling-multiple-licenses"></a><span data-ttu-id="23025-148">Обработка нескольких лицензий</span><span class="sxs-lookup"><span data-stu-id="23025-148">Handling Multiple Licenses</span></span>

<span data-ttu-id="23025-149">Некоторые файлы могут иметь несколько лицензий, связанных с ними в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="23025-149">Some files may have multiple licenses associated with them in the local license store.</span></span> <span data-ttu-id="23025-150">При оценке Оплс для файла, который вы читаете, можно проверить наличие дополнительных лицензий, вызвав метод [**IWMDRMReader2:: тринекстлиценсе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) .</span><span class="sxs-lookup"><span data-stu-id="23025-150">When you evaluate OPLs for a file that you are reading, you can check for additional licenses by calling the [**IWMDRMReader2::TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) method.</span></span> <span data-ttu-id="23025-151">Следует продолжать использовать лицензии, пока не найдете ту, которая разрешает выполнение действия или пока Тринекстлиценсе возвращает DRM \_ S \_ false, что указывает на отсутствие лицензий.</span><span class="sxs-lookup"><span data-stu-id="23025-151">You should continue trying licenses until you find one that allows the action you want to perform or until TryNextLicense returns DRM\_S\_FALSE, which indicates that there are no more licenses.</span></span>

<span data-ttu-id="23025-152">В некоторых случаях файл может иметь связанную лицензию, для которой требуется ОПЛ, которую приложение не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="23025-152">In some cases, a file might have an associated license that requires an OPL that your application cannot support.</span></span> <span data-ttu-id="23025-153">В этом случае важно проверить наличие дополнительных лицензий, так как может существовать лицензия, не указывающая на Оплс.</span><span class="sxs-lookup"><span data-stu-id="23025-153">In such a case it is important to check for additional licenses because a license may exist that does not specify OPLs.</span></span>

<span data-ttu-id="23025-154">**Примечание** . DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="23025-154">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23025-155">См. также</span><span class="sxs-lookup"><span data-stu-id="23025-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23025-156">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="23025-156">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="23025-157">**Интерфейс IWMDRMReader2**</span><span class="sxs-lookup"><span data-stu-id="23025-157">**IWMDRMReader2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




