---
title: Обработка событий приобретения лицензий
description: Обработка событий приобретения лицензий
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Пакет SDK для Windows Media Format, обработка событий приобретения лицензий
- Пакет SDK для Windows Media Format, события приобретения лицензий
- Расширенный системный формат (ASF), обработка событий приобретения лицензий
- ASF (Расширенный системный формат), обработка событий приобретения лицензий
- Расширенный формат систем (ASF), события приобретения лицензий
- ASF (Расширенный системный формат), события приобретения лицензий
- Управление цифровыми правами (DRM), обработка событий приобретения лицензий
- DRM (Управление цифровыми правами), обработка событий приобретения лицензий
- Управление цифровыми правами (DRM), события приобретения лицензий
- DRM (Управление цифровыми правами), события приобретения лицензий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412525"
---
# <a name="handling-license-acquisition-events"></a><span data-ttu-id="0c31f-113">Обработка событий приобретения лицензий</span><span class="sxs-lookup"><span data-stu-id="0c31f-113">Handling License Acquisition Events</span></span>

<span data-ttu-id="0c31f-114">Приложение чтения с поддержкой DRM, в методе обратного вызова [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , обрабатывает следующие четыре события, связанные с процессом получения лицензии:</span><span class="sxs-lookup"><span data-stu-id="0c31f-114">A DRM-enabled reader application, in its [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, handles the following four events related to the license acquisition process:</span></span>

-   <span data-ttu-id="0c31f-115">**\_ \_ состояние подписи LICENSEURL \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="0c31f-115">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>
-   <span data-ttu-id="0c31f-116">**ВМТ \_ без \_ прав**</span><span class="sxs-lookup"><span data-stu-id="0c31f-116">**WMT\_NO\_RIGHTS**</span></span>
-   <span data-ttu-id="0c31f-117">**ВМТ \_ без \_ прав \_**</span><span class="sxs-lookup"><span data-stu-id="0c31f-117">**WMT\_NO\_RIGHTS\_EX**</span></span>
-   <span data-ttu-id="0c31f-118">**ВМТ \_ получить \_ лицензию**</span><span class="sxs-lookup"><span data-stu-id="0c31f-118">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="0c31f-119">**\_ \_ состояние подписи LICENSEURL \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="0c31f-119">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>

<span data-ttu-id="0c31f-120">Когда компонент DRM обнаруживает содержимое, защищенное DRM версии 7, сначала выполняется поиск действительной лицензии на локальную систему.</span><span class="sxs-lookup"><span data-stu-id="0c31f-120">When the DRM component detects content protected by DRM version 7, it first looks for a valid license on the local system.</span></span> <span data-ttu-id="0c31f-121">Если он не существует, он оценивает URL-адрес приобретения лицензии в заголовке DRM файла и отправляет событие **\_ \_ \_ состояния подписи ВМТ LICENSEURL** с параметром *pValue* , имеющим одно из [**значений \_ \_ доверия ВМТ дрмла**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) , указывая, является ли URL-адрес доверенным, недоверенным или незаконным.</span><span class="sxs-lookup"><span data-stu-id="0c31f-121">If none exists, it then evaluates the license acquisition URL in the file's DRM header and sends a **WMT\_LICENSEURL\_SIGNATURE\_STATE** event with *pValue* set to one of the [**WMT\_DRMLA\_TRUST**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) values, indicating whether the URL is trusted, untrusted, or has been tampered with.</span></span> <span data-ttu-id="0c31f-122">Если URL-адрес не является доверенным, приложение должно предупредить пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c31f-122">If the URL is not trusted, then the application should warn the user.</span></span> <span data-ttu-id="0c31f-123">Если URL-адрес был изменен, файл следует считать поврежденным, а приложение не должно переходить по URL-адресу без выдачи строгого предупреждения пользователю.</span><span class="sxs-lookup"><span data-stu-id="0c31f-123">If the URL has been tampered with, then the file should be considered corrupted, and the application should not navigate to the URL without issuing a strong warning the user.</span></span>

<span data-ttu-id="0c31f-124">**ВМТ \_ без \_ прав**</span><span class="sxs-lookup"><span data-stu-id="0c31f-124">**WMT\_NO\_RIGHTS**</span></span>

<span data-ttu-id="0c31f-125">Событие **ВМТ \_ No \_ Rights** отправляется только для содержимого DRM версии 1. Это означает, что лицензия должна быть получена не в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="0c31f-125">The **WMT\_NO\_RIGHTS** event is sent only for DRM version 1 content, which means that the license must be acquired non-silently.</span></span> <span data-ttu-id="0c31f-126">Иными словами, пользователь должен переходить на веб-страницу, чтобы получить лицензию.</span><span class="sxs-lookup"><span data-stu-id="0c31f-126">In other words, the user must navigate to a Web page to acquire a license.</span></span> <span data-ttu-id="0c31f-127">URL-адрес страницы извлекается в виде строки расширенных символов, заканчивающихся нулем, из параметра *pValue* в методе **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="0c31f-127">The URL for the page is retrieved as a wide-character null-terminated string from the *pValue* parameter in the **OnStatus** method.</span></span>

<span data-ttu-id="0c31f-128">При необходимости приложение может упростить переход на веб-страницу пользователя, открыв Internet Explorer в отдельном процессе или в другом месте, разместив элемент управления веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="0c31f-128">If appropriate, an application can make it easier for the user to navigate to the Web page, either by opening up Internet Explorer in a separate process or else by hosting the Web Browser control.</span></span> <span data-ttu-id="0c31f-129">Однако это не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="0c31f-129">This is not required, however.</span></span> <span data-ttu-id="0c31f-130">По крайней мере, приложение может просто отобразить URL-адрес пользователя в окне сообщения и предложить ему вставить его в адресную строку Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0c31f-130">At the very least, an application could simply display the URL to the user in a message box and prompt them to paste it into the address bar of Internet Explorer.</span></span> <span data-ttu-id="0c31f-131">В примере Audioplayer показана правильная обработка события **ВМТ \_ No \_ Rights** , включая форматирование строки URL-адреса и использование метода **CreateProcess** для открытия Internet Explorer и перехода по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="0c31f-131">The Audioplayer sample demonstrates proper handling of the **WMT\_NO\_RIGHTS** event, including how to format the URL string, and how to use the **CreateProcess** method to open Internet Explorer and navigate to the specified URL.</span></span>

<span data-ttu-id="0c31f-132">Так как приложение не может узнать, когда была получена лицензия DRM версии 1, пользователю будет предпринята попытка открыть файл еще раз после получения лицензии.</span><span class="sxs-lookup"><span data-stu-id="0c31f-132">Because the application has no way of knowing when a DRM version 1 license has been acquired, it is up to the user to attempt to open the file again after acquiring the license.</span></span>

<span data-ttu-id="0c31f-133">Этот же процесс приобретения лицензий с неавтоматической лицензией также можно использовать для лицензий версии 7, но в этом случае приложение может сначала вызвать [**ивмдрмреадер:: мониторлиценсеаккуиситион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span><span class="sxs-lookup"><span data-stu-id="0c31f-133">This same non-silent license acquisition process can also be used for version 7 licenses, but in this case the application can first call [**IWMDRMReader::MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span></span> <span data-ttu-id="0c31f-134">Этот метод приведет к многократной проверке локального хранилища лицензий до тех пор, пока не будет найдена лицензия для нового файла.</span><span class="sxs-lookup"><span data-stu-id="0c31f-134">This method will cause the local license store to be checked repeatedly until the license for the new file is found.</span></span> <span data-ttu-id="0c31f-135">На этом этапе приложение получит событие **\_ \_ лицензии ВМТ** .</span><span class="sxs-lookup"><span data-stu-id="0c31f-135">At that point, the application will receive a **WMT\_ACQUIRE\_LICENSE** event.</span></span> <span data-ttu-id="0c31f-136">Для всех лицензий версии 7 рекомендуется, чтобы приложения предоставляющих пользователям возможность получать лицензии автоматически или без уведомления.</span><span class="sxs-lookup"><span data-stu-id="0c31f-136">For all version 7 licenses, it is recommended that applications give users the option to obtain licenses silently or non-silently.</span></span>

<span data-ttu-id="0c31f-137">**ВМТ \_ без \_ прав \_**</span><span class="sxs-lookup"><span data-stu-id="0c31f-137">**WMT\_NO\_RIGHTS\_EX**</span></span>

<span data-ttu-id="0c31f-138">Событие **\_ \_ \_ ex ВМТ без прав** указывает на то, что содержимое защищено с помощью DRM версии 7, поэтому процесс приобретения лицензий может выполняться либо без уведомления, либо без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c31f-138">The **WMT\_NO\_RIGHTS\_EX** event indicates that the content is protected by DRM version 7, and therefore the license acquisition process can proceed either silently or non-silently.</span></span> <span data-ttu-id="0c31f-139">Как правило, для конечных пользователей удобнее использовать автоматическое получение лицензий, хотя некоторые пользователи предпочитают получать все лицензии без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c31f-139">In general, silent license acquisition is more convenient for end users, although some people prefer to acquire all licenses non-silently.</span></span> <span data-ttu-id="0c31f-140">Когда при получении лицензии пользователь должен отправить оплату или персональные данные, этот процесс всегда следует выполнять без уведомления.</span><span class="sxs-lookup"><span data-stu-id="0c31f-140">When license acquisition requires the user to submit payment or personal information, the process should always be performed non-silently.</span></span> <span data-ttu-id="0c31f-141">Неавтоматическое получение лицензий описано выше в разделе **ВМТ \_ No \_ Rights** .</span><span class="sxs-lookup"><span data-stu-id="0c31f-141">Non-silent license acquisition is described above under the **WMT\_NO\_RIGHTS** heading.</span></span> <span data-ttu-id="0c31f-142">Автоматическое приобретение продолжается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0c31f-142">Silent acquisition proceeds as follows:</span></span>

1.  <span data-ttu-id="0c31f-143">Приведите параметр *pValue* к структуре [**\_ данных для \_ получения \_ лицензии WM**](wm-get-license-data.md) и сохраните структуру в том случае, если она понадобится позже для приобретения лицензий без участия пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c31f-143">Cast the *pValue* parameter to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and store the structure in case it is needed later for non-silent license acquisition.</span></span>
2.  <span data-ttu-id="0c31f-144">Вызовите **QueryInterface** для объекта Reader, чтобы получить интерфейс [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .</span><span class="sxs-lookup"><span data-stu-id="0c31f-144">Call **QueryInterface** on the reader object to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
3.  <span data-ttu-id="0c31f-145">Вызовите [**ивмдрмреадер:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) и укажите 0x1 в параметре *dwFlags* , чтобы указать на автоматическое получение языка.</span><span class="sxs-lookup"><span data-stu-id="0c31f-145">Call [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) and specify 0x1 in the *dwFlags* parameter to indicate silent language acquisition.</span></span> <span data-ttu-id="0c31f-146">Это асинхронный вызов, который возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="0c31f-146">This is an asynchronous call that returns immediately.</span></span>
4.  <span data-ttu-id="0c31f-147">Дождитесь события **ВМТ \_ получения \_ лицензии** .</span><span class="sxs-lookup"><span data-stu-id="0c31f-147">Wait for the **WMT\_ACQUIRE\_LICENSE** event.</span></span>

<span data-ttu-id="0c31f-148">**ВМТ \_ получить \_ лицензию**</span><span class="sxs-lookup"><span data-stu-id="0c31f-148">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="0c31f-149">Событие **ВМТ \_ получения \_ лицензии** отправляется после завершения процесса получения лицензии для лицензии DRM версии 7.</span><span class="sxs-lookup"><span data-stu-id="0c31f-149">The **WMT\_ACQUIRE\_LICENSE** event is sent after the license acquisition process is completed for a DRM version 7 license.</span></span> <span data-ttu-id="0c31f-150">[**Ивмдрмреадер:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) вызывает отправку этого события для автоматического получения сообщений, а [**мониторлиценсеаккуиситион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) приводит к его отправке для неавтоматических приобретений.</span><span class="sxs-lookup"><span data-stu-id="0c31f-150">[**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) causes this event to be sent for silent acquisition, and [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) causes it to be sent for non-silent acquisition.</span></span> <span data-ttu-id="0c31f-151">В обработчике событий приведите параметр *pValue* к указателю на [**структуру \_ \_ \_ данных для получения лицензии WM**](wm-get-license-data.md) и изучите элемент **HR** , чтобы определить, успешно ли получена лицензия.</span><span class="sxs-lookup"><span data-stu-id="0c31f-151">In your event handler, cast *pValue* to a pointer to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and examine the **hr** member to determine whether the license was successfully acquired.</span></span> <span data-ttu-id="0c31f-152">Если **HR** равен NS \_ E \_ DRM \_ без \_ прав, это означает, что лицензия должна быть получена без уведомления.</span><span class="sxs-lookup"><span data-stu-id="0c31f-152">If **hr** equals NS\_E\_DRM\_NO\_RIGHTS, it indicates that the license must be acquired non-silently.</span></span> <span data-ttu-id="0c31f-153">Приложения должны позволять пользователям отменять процесс приобретения лицензий в любое время.</span><span class="sxs-lookup"><span data-stu-id="0c31f-153">Applications should enable users to cancel the license acquisition process at any time.</span></span> <span data-ttu-id="0c31f-154">Это делается путем вызова [**ивмдрмреадер:: канцеллиценсеаккуиситион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span><span class="sxs-lookup"><span data-stu-id="0c31f-154">This is done by calling [**IWMDRMReader::CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span></span> <span data-ttu-id="0c31f-155">При вызове этого метода будет отправлено событие **ВМТ \_ получения \_ лицензии** со значением **HRESULT** , \_ \_ полученным в результате \_ отмены запроса DRM S \_ .</span><span class="sxs-lookup"><span data-stu-id="0c31f-155">Calling this method will send a **WMT\_ACQUIRE\_LICENSE** event with an **HRESULT** value of NS\_S\_DRM\_ACQUIRE\_CANCELLED.</span></span>

<span data-ttu-id="0c31f-156">Если **HR** имеет значение \_ \_ \_ получена лицензия DRM NS, то лицензия была получена, \_ и приложение может попытаться воспроизвести файл или скопировать его на устройство или выполнить любое действие, для которого ему были запрошены права.</span><span class="sxs-lookup"><span data-stu-id="0c31f-156">If **hr** equals NS\_S\_DRM\_LICENSE\_ACQUIRED, then the license has been acquired and the application can attempt to play the file, or copy it to a device or perform whatever action it had requested rights for.</span></span>

<span data-ttu-id="0c31f-157">В Windows XP появился новый код ошибки: нотаккуиред лицензия на NS \_ E \_ DRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0c31f-157">On Windows XP, a new error code was introduced: NS\_E\_DRM\_LICENSE\_NOTACQUIRED.</span></span> <span data-ttu-id="0c31f-158">Этот код ошибки генерируется всякий раз, когда компоненты среды выполнения Windows Media в Windows XP не могут получить лицензию во время неудачного или неавтоматического получения лицензии.</span><span class="sxs-lookup"><span data-stu-id="0c31f-158">This error code is generated whenever the Windows Media Format run-time components on Windows XP fail to acquire a license during silent or non-silent license acquisition.</span></span> <span data-ttu-id="0c31f-159">На других платформах \_ \_ \_ \_ сообщение об ошибке хранилища лицензий NS E DRM \_ обычно возвращается при сбое приобретения лицензии.</span><span class="sxs-lookup"><span data-stu-id="0c31f-159">On other platforms, NS\_E\_DRM\_LICENSE\_STORE\_ERROR is usually returned when license acquisition fails.</span></span> <span data-ttu-id="0c31f-160">Новый код ошибки предназначен для различения сбоев при получении лицензий от других условий сбоя, когда \_ \_ \_ \_ \_ создается сообщение об ошибке хранилища лицензий управления цифровыми правами (DRM).</span><span class="sxs-lookup"><span data-stu-id="0c31f-160">The new error code is intended to distinguish license acquisition failure from other failure conditions where NS\_E\_DRM\_LICENSE\_STORE\_ERROR is generated.</span></span>

<span data-ttu-id="0c31f-161">Рекомендуемый способ устранения этих ошибок при возвращении после нежелательной попытки приобретения лицензии показан в следующем фрагменте кода:</span><span class="sxs-lookup"><span data-stu-id="0c31f-161">The recommended way to handle these errors when they are returned after a silent license acquisition attempt is shown in the following code snippet:</span></span>


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> <span data-ttu-id="0c31f-162">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="0c31f-162">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0c31f-163">См. также</span><span class="sxs-lookup"><span data-stu-id="0c31f-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c31f-164">**Чтение защищенных файлов**</span><span class="sxs-lookup"><span data-stu-id="0c31f-164">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




