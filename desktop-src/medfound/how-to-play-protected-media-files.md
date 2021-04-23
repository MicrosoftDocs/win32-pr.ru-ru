---
description: Воспроизведение файлов, содержащих носитель, защищенный с использованием DRM.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Воспроизведение защищенных файлов мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f8f7af78881e43f2f7f85e8f333ab31b1bc2de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703467"
---
# <a name="how-to-play-protected-media-files"></a><span data-ttu-id="12a94-103">Воспроизведение защищенных файлов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="12a94-103">How to Play Protected Media Files</span></span>

<span data-ttu-id="12a94-104">Защищенный файл мультимедиа — это любой файл мультимедиа со связанными правилами для использования содержимого.</span><span class="sxs-lookup"><span data-stu-id="12a94-104">A protected media file is any media file that has associated rules for using the content.</span></span> <span data-ttu-id="12a94-105">В некоторых случаях защищенный файл мультимедиа шифруется с помощью некоторых форм шифрования цифрового управления цифровыми правами (DRM).</span><span class="sxs-lookup"><span data-stu-id="12a94-105">In some cases, a protected media file is encrypted using some form of digital rights management (DRM) encryption.</span></span> <span data-ttu-id="12a94-106">Для воспроизведения защищенного файла мультимедиа воспроизведение должно выполняться внутри пути к защищенному носителю (PMP).</span><span class="sxs-lookup"><span data-stu-id="12a94-106">To play a protected media file, playback must occur inside the protected media path (PMP).</span></span> <span data-ttu-id="12a94-107">Кроме того, пользователю может потребоваться получить права доступа к содержимому.</span><span class="sxs-lookup"><span data-stu-id="12a94-107">In addition, the user might have to acquire rights to the content.</span></span>

<span data-ttu-id="12a94-108">Термин "получение прав" относится к любому действию, которое должно выполнить приложение, прежде чем пользователь сможет воспроизвести содержимое.</span><span class="sxs-lookup"><span data-stu-id="12a94-108">The term rights acquisition refers to any action that the application must perform before the user can play the content.</span></span> <span data-ttu-id="12a94-109">Наиболее распространенный пример — получение лицензии DRM, но Media Foundation определяет универсальный механизм, который может поддерживать другие типы получения прав.</span><span class="sxs-lookup"><span data-stu-id="12a94-109">The most common example is obtaining a DRM license, but Media Foundation defines a generic mechanism that can support other types of rights acquisition.</span></span> <span data-ttu-id="12a94-110">Этот универсальный механизм определяется интерфейсом [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="12a94-110">The [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface defines this generic mechanism.</span></span>

<span data-ttu-id="12a94-111">Получение прав должно выполняться за пределами PMP в процессе приложения.</span><span class="sxs-lookup"><span data-stu-id="12a94-111">Rights acquisition must be done outside of the PMP, from the application process.</span></span> <span data-ttu-id="12a94-112">Сеанс мультимедиа уведомляет приложение через интерфейс [**имфконтентпротектионманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) , который реализуется приложением.</span><span class="sxs-lookup"><span data-stu-id="12a94-112">The Media Session notifies the application through the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface, which is implemented by the application.</span></span> <span data-ttu-id="12a94-113">Сеанс мультимедиа использует интерфейс **имфконтентпротектионманажер** для пересылки объекта средства включения содержимого в приложение.</span><span class="sxs-lookup"><span data-stu-id="12a94-113">The Media Session uses the **IMFContentProtectionManager** interface to forward a content enabler object to the application.</span></span> <span data-ttu-id="12a94-114">Content созидателями реализует интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="12a94-114">Content enablers implement the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="12a94-115">Приложение использует этот интерфейс для получения необходимых прав.</span><span class="sxs-lookup"><span data-stu-id="12a94-115">The application uses this interface to acquire the necessary rights.</span></span>

<span data-ttu-id="12a94-116">Модуль включения содержимого может поддерживать автоматическое получение прав. в этом случае функция включения содержимого реализует весь процесс, а приложение просто наблюдает за состоянием.</span><span class="sxs-lookup"><span data-stu-id="12a94-116">A content enabler might support automatic rights acquisition, in which case the content enabler implements the entire process, and the application simply monitors the status.</span></span> <span data-ttu-id="12a94-117">В противном случае приложение должно использовать получение прав без уведомления, которое представляет собой процесс, в котором приложение отправляет данные HTTP POST по URL-адресу, предоставленному средством включения содержимого.</span><span class="sxs-lookup"><span data-stu-id="12a94-117">Otherwise, the application must use non-silent rights acquisition, which is a process where the application sends HTTP POST data to a URL provided by the content enabler.</span></span>

<span data-ttu-id="12a94-118">Для воспроизведения защищенного мультимедиа приложение выполняет те же действия, которые приведены в разделе [Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md)и следующие дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="12a94-118">To play protected media, an application follows the same steps given in the topic [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), with the following additional steps:</span></span>

1.  <span data-ttu-id="12a94-119">Запрос того, содержит ли источник мультимедиа защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="12a94-119">Query whether the media source contains protected content.</span></span> <span data-ttu-id="12a94-120">(Необязательно.)</span><span class="sxs-lookup"><span data-stu-id="12a94-120">(Optional.)</span></span>
2.  <span data-ttu-id="12a94-121">Создайте сеанс мультимедиа в процессе PMP, а не в процессе приложения.</span><span class="sxs-lookup"><span data-stu-id="12a94-121">Create the Media Session in the PMP process, instead of the application process.</span></span>
3.  <span data-ttu-id="12a94-122">Получение прав, если оно получится через сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="12a94-122">Perform rights acquisition, if notified to do so by the Media Session.</span></span> <span data-ttu-id="12a94-123">Эта операция выполняется приложением асинхронно.</span><span class="sxs-lookup"><span data-stu-id="12a94-123">This operation is performed asynchronously by the application.</span></span>
4.  <span data-ttu-id="12a94-124">Завершите асинхронную операцию.</span><span class="sxs-lookup"><span data-stu-id="12a94-124">Complete the asynchronous operation.</span></span>

## <a name="query-for-protected-content"></a><span data-ttu-id="12a94-125">Запрос защищенного содержимого</span><span class="sxs-lookup"><span data-stu-id="12a94-125">Query for Protected Content</span></span>

<span data-ttu-id="12a94-126">Чтобы запросить, содержит ли источник мультимедиа защищенное содержимое, вызовите функцию [**мфрекуирепротектеденвиронмент**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) в дескрипторе представления источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="12a94-126">To query whether a media source contains protected content, call the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function on the media source's presentation descriptor.</span></span> <span data-ttu-id="12a94-127">Если функция возвращает значение S \_ , необходимо использовать PMP для воспроизведения содержимого.</span><span class="sxs-lookup"><span data-stu-id="12a94-127">If the function returns S\_OK, you must use the PMP to play the content.</span></span> <span data-ttu-id="12a94-128">Если функция возвращает \_ значение false, PMP не требуется, и вы можете создать сеанс мультимедиа в процессе приложения.</span><span class="sxs-lookup"><span data-stu-id="12a94-128">If the function returns S\_FALSE, the PMP is not required, and you can create the Media Session in the application process.</span></span> <span data-ttu-id="12a94-129">Кроме того, можно использовать PMP для воспроизведения обоих типов содержимого, защищенного и незащищенного.</span><span class="sxs-lookup"><span data-stu-id="12a94-129">Alternatively, you can use the PMP to play both types of content, protected and unprotected.</span></span> <span data-ttu-id="12a94-130">В этом случае вам не нужно вызывать **мфрекуирепротектеденвиронмент**.</span><span class="sxs-lookup"><span data-stu-id="12a94-130">If you do that, you do not need to call **MFRequireProtectedEnvironment**.</span></span>

<span data-ttu-id="12a94-131">Дополнительные сведения о дескрипторах презентаций см. в разделе [дескрипторы представления](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="12a94-131">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

## <a name="create-the-pmp-media-session"></a><span data-ttu-id="12a94-132">Создание сеанса мультимедиа PMP</span><span class="sxs-lookup"><span data-stu-id="12a94-132">Create the PMP Media Session</span></span>

<span data-ttu-id="12a94-133">Чтобы создать сеанс мультимедиа в PMP, вызовите [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="12a94-133">To create the Media Session in the PMP, call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="12a94-134">Эта функция похожа на [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), но вместо создания сеанса мультимедиа в процессе приложения он создает сеанс мультимедиа в процессе PMP.</span><span class="sxs-lookup"><span data-stu-id="12a94-134">This function is similar to [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), but instead of creating the Media Session in the application's process, it creates the Media Session in the PMP process.</span></span> <span data-ttu-id="12a94-135">Приложение получает указатель на прокси-объект для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="12a94-135">The application receives a pointer to a proxy object for the Media Session.</span></span> <span data-ttu-id="12a94-136">Приложение вызывает методы [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) для прокси-объекта так же, как в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="12a94-136">The application calls [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods on the proxy object, just as it would on the Media Session.</span></span> <span data-ttu-id="12a94-137">Прокси-объект перенаправляет вызовы сеанса мультимедиа через границу процесса.</span><span class="sxs-lookup"><span data-stu-id="12a94-137">The proxy object forwards the calls to the Media Session across the process boundary.</span></span>

<span data-ttu-id="12a94-138">Создайте сеанс PMP Media следующим образом:</span><span class="sxs-lookup"><span data-stu-id="12a94-138">Create the PMP Media Session as follows:</span></span>

1.  <span data-ttu-id="12a94-139">Создайте новое хранилище атрибутов, вызвав [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="12a94-139">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="12a94-140">Задайте атрибут [**\_ \_ \_ \_ диспетчера защиты содержимого сеанса MF**](mf-session-content-protection-manager-attribute.md) в хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="12a94-140">Set the [**MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER**](mf-session-content-protection-manager-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="12a94-141">Значение этого атрибута является указателем на реализацию [**имфконтентпротектионманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)приложения.</span><span class="sxs-lookup"><span data-stu-id="12a94-141">The value of this attribute is a pointer to your application's implementation of [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager).</span></span> <span data-ttu-id="12a94-142">Вызовите метод [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) , чтобы задать атрибут.</span><span class="sxs-lookup"><span data-stu-id="12a94-142">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the attribute.</span></span>
3.  <span data-ttu-id="12a94-143">Вызовите [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , чтобы создать сеанс мультимедиа в процессе PMP.</span><span class="sxs-lookup"><span data-stu-id="12a94-143">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session in the PMP process.</span></span> <span data-ttu-id="12a94-144">Параметр *пконфигуратион* является указателем на интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) хранилища атрибутов.</span><span class="sxs-lookup"><span data-stu-id="12a94-144">The *pConfiguration* parameter is a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the attribute store.</span></span>


```C++
IMFAttributes *pAttributes = NULL;
IMFMediaSession *pSession = NULL;

// Create the attribute store.
hr = MFCreateAttributes(&pAttributes, 1);

// Set the IMFContentProtectionManager pointer.
if (SUCCEEDED(hr))
{
    hr = pAttributes->SetUnknown(
        MF_SESSION_CONTENT_PROTECTION_MANAGER, 
        pCPM  // Your implementation of IMFContentProtectionManager.
        );
}

// Create the Media Session.
if (SUCCEEDED(hr))
{
    hr = MFCreatePMPMediaSession(
        0,
        pAttributes, 
        &pSession,
        NULL
    );
}

SAFE_RELEASE(pAttributes); // Release the attribute store.
// Use the Media Session to control playback (not shown).
```



<span data-ttu-id="12a94-145">Затем создайте топологию воспроизведения и поочередно помещает ее в сеанс мультимедиа, как описано в разделе [Создание топологий воспроизведения](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="12a94-145">Next, create a playback topology and queue it on the Media Session, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

## <a name="perform-rights-acquisition"></a><span data-ttu-id="12a94-146">Получение прав</span><span class="sxs-lookup"><span data-stu-id="12a94-146">Perform Rights Acquisition</span></span>

<span data-ttu-id="12a94-147">Если для воспроизведения требуется получение прав, сеанс мультимедиа вызывает [**имфконтентпротектионманажер:: бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span><span class="sxs-lookup"><span data-stu-id="12a94-147">If playback requires rights acquisition, the Media Session calls [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="12a94-148">Параметр *пенаблерактивате* этого метода является указателем на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="12a94-148">The *pEnablerActivate* parameter of this method is a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="12a94-149">Используйте этот интерфейс для создания объекта включения содержимого, который предоставляет интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="12a94-149">Use this interface to create the content enabler object, which exposes the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="12a94-150">Затем используйте функцию включения содержимого для выполнения шага получения прав.</span><span class="sxs-lookup"><span data-stu-id="12a94-150">Then use the content enabler to perform the rights acquisition step.</span></span>

<span data-ttu-id="12a94-151">Чтобы создать модуль включения содержимого, вызовите [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span><span class="sxs-lookup"><span data-stu-id="12a94-151">To create the content enabler, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span></span>


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



<span data-ttu-id="12a94-152">Запросите возвращенный указатель [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) для интерфейса [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="12a94-152">Query the returned [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pointer for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="12a94-153">Используйте этот интерфейс для получения событий из объекта включения содержимого.</span><span class="sxs-lookup"><span data-stu-id="12a94-153">Use this interface to get events from the content enabler object.</span></span> <span data-ttu-id="12a94-154">Дополнительные сведения о событиях см. в разделе [генераторы событий мультимедиа](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="12a94-154">For more information about events, see [Media Event Generators](media-event-generators.md).</span></span>

<span data-ttu-id="12a94-155">Чтобы узнать, поддерживает ли модуль включения содержимого автоматическое получение, вызовите [**имфконтентенаблер:: исаутоматиксуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span><span class="sxs-lookup"><span data-stu-id="12a94-155">To find out whether the content enabler supports automatic acquisition, call [**IMFContentEnabler::IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span></span> <span data-ttu-id="12a94-156">Если этот метод возвращает значение **true**, приложение должно использовать автоматическое получение.</span><span class="sxs-lookup"><span data-stu-id="12a94-156">If this method returns the value **TRUE**, the application should use automatic acquisition.</span></span> <span data-ttu-id="12a94-157">В противном случае используйте неавтоматические получение.</span><span class="sxs-lookup"><span data-stu-id="12a94-157">Otherwise, use non-silent acquisition.</span></span>

<span data-ttu-id="12a94-158">Метод [**бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) является асинхронным.</span><span class="sxs-lookup"><span data-stu-id="12a94-158">The [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method is asynchronous.</span></span> <span data-ttu-id="12a94-159">Приложение должно выполнить шаг приобретения в потоке приложения.</span><span class="sxs-lookup"><span data-stu-id="12a94-159">The application should perform the acquisition step on the application's thread.</span></span> <span data-ttu-id="12a94-160">Один из подходов — опубликовать сообщение частного окна в главном окне приложения, уведомляя поток приложения, чтобы выполнить получение.</span><span class="sxs-lookup"><span data-stu-id="12a94-160">One approach is to post a private window message to the application's main window, notifying the application thread to perform the acquisition.</span></span> <span data-ttu-id="12a94-161">Пока операция находится в состоянии ожидания, приложение должно сохранить указатель обратного вызова и объект состояния, полученный в параметрах *пкаллбакк* и *пункстате* **бегиненаблеконтент**.</span><span class="sxs-lookup"><span data-stu-id="12a94-161">While the operation is pending, the application must store the callback pointer and the state object that it received in the *pCallback* and *punkState* parameters of **BeginEnableContent**.</span></span> <span data-ttu-id="12a94-162">Они будут использоваться для завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="12a94-162">These will be used to complete the asynchronous operation.</span></span>

### <a name="automatic-acquisition"></a><span data-ttu-id="12a94-163">Автоматическое получение</span><span class="sxs-lookup"><span data-stu-id="12a94-163">Automatic Acquisition</span></span>

<span data-ttu-id="12a94-164">Чтобы выполнить автоматическое получение, вызовите [**имфконтентенаблер:: аутоматиценабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span><span class="sxs-lookup"><span data-stu-id="12a94-164">To perform automatic acquisition, call [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span></span> <span data-ttu-id="12a94-165">Этот метод является асинхронным.</span><span class="sxs-lookup"><span data-stu-id="12a94-165">This method is asynchronous.</span></span> <span data-ttu-id="12a94-166">После завершения операции модуль включения содержимого отправляет событие [минаблеркомплетед](meenablercompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="12a94-166">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span> <span data-ttu-id="12a94-167">Код состояния события указывает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="12a94-167">The event's status code indicates whether the operation was successful.</span></span> <span data-ttu-id="12a94-168">Если код состояния из события Минаблеркомплетед — это \_ нотаккуиред лицензия на NS E \_ DRM \_ \_ , приложение должно использовать неавтоматическую приемку.</span><span class="sxs-lookup"><span data-stu-id="12a94-168">If the status code from the MEEnablerCompleted event is NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should try using non-silent acquisition.</span></span>

<span data-ttu-id="12a94-169">Пока выполняется операция приобретения, объект-получатель может отправить событие [минаблерпрогресс](meenablerprogress.md) , чтобы указать ход выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="12a94-169">While the acquisition operation is in progress, the enabler object might send the [MEEnablerProgress](meenablerprogress.md) event to indicate the progress of the operation.</span></span> <span data-ttu-id="12a94-170">Чтобы отменить операцию, вызовите метод [**имфконтентенаблер:: Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span><span class="sxs-lookup"><span data-stu-id="12a94-170">To cancel the operation, call [**IMFContentEnabler::Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span></span>

### <a name="non-silent-acquisition"></a><span data-ttu-id="12a94-171">Получение без уведомления</span><span class="sxs-lookup"><span data-stu-id="12a94-171">Non-Silent Acquisition</span></span>

<span data-ttu-id="12a94-172">Если метод [**исаутоматиксуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) возвращает **значение false** или метод [**аутоматиценабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) завершается с кодом ошибки NS \_ E \_ DRM \_ License \_ нотаккуиред, приложение должно выполнять неавтоматическую процедуру приобретения, как описано в следующих шагах:</span><span class="sxs-lookup"><span data-stu-id="12a94-172">If the [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) method returns **FALSE** or the [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method fails with the error code NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should perform non-silent acquisition as described in the following steps:</span></span>

1.  <span data-ttu-id="12a94-173">Вызовите [**имфконтентенаблер:: жетенаблеурл**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) , чтобы получить URL-адрес для получения прав.</span><span class="sxs-lookup"><span data-stu-id="12a94-173">Call [**IMFContentEnabler::GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) to get the URL for the rights acquisition.</span></span> <span data-ttu-id="12a94-174">Этот метод также возвращает флаг, указывающий, является ли URL-адрес доверенным.</span><span class="sxs-lookup"><span data-stu-id="12a94-174">This method also returns a flag indicating whether the URL is trusted.</span></span>
2.  <span data-ttu-id="12a94-175">Вызовите метод [**имфконтентенаблер:: жетенабледата**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) , чтобы получить данные HTTP POST.</span><span class="sxs-lookup"><span data-stu-id="12a94-175">Call [**IMFContentEnabler::GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) to get the HTTP POST data.</span></span>
3.  <span data-ttu-id="12a94-176">Вызовите [**имфконтентенаблер:: мониторенабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span><span class="sxs-lookup"><span data-stu-id="12a94-176">Call [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span></span> <span data-ttu-id="12a94-177">Этот метод заставляет модуль включения содержимого отслеживать ход выполнения действия получения прав.</span><span class="sxs-lookup"><span data-stu-id="12a94-177">This method causes the content enabler to monitor the progress of the rights acquisition action.</span></span>

4.  <span data-ttu-id="12a94-178">Отправьте данные в URL-адрес получения прав с помощью действия HTTP POST.</span><span class="sxs-lookup"><span data-stu-id="12a94-178">Submit the data to the rights acquisition URL by using an HTTP POST action.</span></span> <span data-ttu-id="12a94-179">Можно использовать элемент управления Internet Explorer или API Windows Internet (WinINet).</span><span class="sxs-lookup"><span data-stu-id="12a94-179">You can use the Internet Explorer control or the Windows Internet (WinINet) APIs.</span></span>

<span data-ttu-id="12a94-180">В следующем коде показаны шаги 1 – 3.</span><span class="sxs-lookup"><span data-stu-id="12a94-180">The following code shows steps 1–3.</span></span> <span data-ttu-id="12a94-181">Шаг 4 зависит от конкретных требований приложения.</span><span class="sxs-lookup"><span data-stu-id="12a94-181">Step 4 depends on your application's particular requirements.</span></span>


```C++
WCHAR   *sURL = NULL;  // URL.
DWORD   cchURL = 0;    // Size of the URL in characters.

// Trust status of the URL.
MF_URL_TRUST_STATUS  trustStatus = MF_LICENSE_URL_UNTRUSTED;

BYTE    *pPostData = NULL;  // Buffer to hold HTTP POST data.
DWORD   cbPostDataSize = 0; // Size of the buffer, in bytes.

HRESULT hr = S_OK;

// Get the URL. 
hr = m_pEnabler->GetEnableURL(&sURL, &cchURL, &trustStatus);

if (SUCCEEDED(hr))
{
    if (trustStatus != MF_LICENSE_URL_TRUSTED)
    {
        // The URL is not trusted. Do not proceed.
        hr = E_FAIL;
    }
}

// Monitor the rights acquisition. 
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->MonitorEnable();
}

// Get the HTTP POST data.
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->GetEnableData(&pPostData, &cbPostDataSize);
}

// Open the URL and send the HTTP POST data. (Not shown.)

// Release the buffers.
CoTaskMemFree(pPostData);
CoTaskMemFree(sURL);
```



<span data-ttu-id="12a94-182">После завершения операции модуль включения содержимого отправляет событие [минаблеркомплетед](meenablercompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="12a94-182">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span>

## <a name="complete-the-asynchronous-operation"></a><span data-ttu-id="12a94-183">Завершение асинхронной операции</span><span class="sxs-lookup"><span data-stu-id="12a94-183">Complete the Asynchronous Operation</span></span>

<span data-ttu-id="12a94-184">Когда получение прав завершается успешно или иначе, приложение должно уведомить сеанс мультимедиа, вызвав указатель обратного вызова, заданный в методе [**бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="12a94-184">When the rights acquisition is completed, successfully or otherwise, the application must notify the Media Session, by invoking the callback pointer given in the [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

1.  <span data-ttu-id="12a94-185">Создайте объект асинхронного результата, вызвав [**мфкреатеасинкресулт**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span><span class="sxs-lookup"><span data-stu-id="12a94-185">Create an asynchronous result object by calling [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span></span>
2.  <span data-ttu-id="12a94-186">Вызов обратного вызова сеанса мультимедиа путем вызова [**мфинвокекаллбакк**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span><span class="sxs-lookup"><span data-stu-id="12a94-186">Invoke the Media Session's callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>
3.  <span data-ttu-id="12a94-187">Сеанс мультимедиа будет вызывать [**имфконтентпротектионманажер:: енденаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span><span class="sxs-lookup"><span data-stu-id="12a94-187">The Media Session will call [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span></span> <span data-ttu-id="12a94-188">В реализации этого метода Освободите все указатели или ресурсы, выделенные внутри [**бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span><span class="sxs-lookup"><span data-stu-id="12a94-188">In your implementation of this method, release any pointers or resources that you allocated inside [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="12a94-189">Возвращает **значение HRESULT** , указывающее на общее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="12a94-189">Return an **HRESULT** that indicates the overall success of the operation.</span></span> <span data-ttu-id="12a94-190">Если не удалось получить права или пользователь отменил операцию до его завершения, возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="12a94-190">If the rights acquisition failed or the user canceled before it was completed, return an error code.</span></span>

<span data-ttu-id="12a94-191">В следующем коде показано, как создать асинхронный результат и вызвать обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="12a94-191">The following code shows how to create the asynchronous result and invoke the callback.</span></span>


```C++
IMFAsyncResult  *pResult = NULL;

// Create the asynchronous result object.
hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);

// Invoke the callback.
if (SUCCEEDED(hr))
{
    pResult->SetStatus(hrStatus);
    hr = MFInvokeCallback(pResult);
}
SAFE_RELEASE(pResult);
```



## <a name="related-topics"></a><span data-ttu-id="12a94-192">См. также</span><span class="sxs-lookup"><span data-stu-id="12a94-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12a94-193">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="12a94-193">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="12a94-194">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="12a94-194">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



