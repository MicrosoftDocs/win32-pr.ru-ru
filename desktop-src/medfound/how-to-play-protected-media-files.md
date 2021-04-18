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
# <a name="how-to-play-protected-media-files"></a>Воспроизведение защищенных файлов мультимедиа

Защищенный файл мультимедиа — это любой файл мультимедиа со связанными правилами для использования содержимого. В некоторых случаях защищенный файл мультимедиа шифруется с помощью некоторых форм шифрования цифрового управления цифровыми правами (DRM). Для воспроизведения защищенного файла мультимедиа воспроизведение должно выполняться внутри пути к защищенному носителю (PMP). Кроме того, пользователю может потребоваться получить права доступа к содержимому.

Термин "получение прав" относится к любому действию, которое должно выполнить приложение, прежде чем пользователь сможет воспроизвести содержимое. Наиболее распространенный пример — получение лицензии DRM, но Media Foundation определяет универсальный механизм, который может поддерживать другие типы получения прав. Этот универсальный механизм определяется интерфейсом [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .

Получение прав должно выполняться за пределами PMP в процессе приложения. Сеанс мультимедиа уведомляет приложение через интерфейс [**имфконтентпротектионманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) , который реализуется приложением. Сеанс мультимедиа использует интерфейс **имфконтентпротектионманажер** для пересылки объекта средства включения содержимого в приложение. Content созидателями реализует интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) . Приложение использует этот интерфейс для получения необходимых прав.

Модуль включения содержимого может поддерживать автоматическое получение прав. в этом случае функция включения содержимого реализует весь процесс, а приложение просто наблюдает за состоянием. В противном случае приложение должно использовать получение прав без уведомления, которое представляет собой процесс, в котором приложение отправляет данные HTTP POST по URL-адресу, предоставленному средством включения содержимого.

Для воспроизведения защищенного мультимедиа приложение выполняет те же действия, которые приведены в разделе [Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md)и следующие дополнительные действия.

1.  Запрос того, содержит ли источник мультимедиа защищенное содержимое. (Необязательно.)
2.  Создайте сеанс мультимедиа в процессе PMP, а не в процессе приложения.
3.  Получение прав, если оно получится через сеанс мультимедиа. Эта операция выполняется приложением асинхронно.
4.  Завершите асинхронную операцию.

## <a name="query-for-protected-content"></a>Запрос защищенного содержимого

Чтобы запросить, содержит ли источник мультимедиа защищенное содержимое, вызовите функцию [**мфрекуирепротектеденвиронмент**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) в дескрипторе представления источника мультимедиа. Если функция возвращает значение S \_ , необходимо использовать PMP для воспроизведения содержимого. Если функция возвращает \_ значение false, PMP не требуется, и вы можете создать сеанс мультимедиа в процессе приложения. Кроме того, можно использовать PMP для воспроизведения обоих типов содержимого, защищенного и незащищенного. В этом случае вам не нужно вызывать **мфрекуирепротектеденвиронмент**.

Дополнительные сведения о дескрипторах презентаций см. в разделе [дескрипторы представления](presentation-descriptors.md).

## <a name="create-the-pmp-media-session"></a>Создание сеанса мультимедиа PMP

Чтобы создать сеанс мультимедиа в PMP, вызовите [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Эта функция похожа на [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), но вместо создания сеанса мультимедиа в процессе приложения он создает сеанс мультимедиа в процессе PMP. Приложение получает указатель на прокси-объект для сеанса мультимедиа. Приложение вызывает методы [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) для прокси-объекта так же, как в сеансе мультимедиа. Прокси-объект перенаправляет вызовы сеанса мультимедиа через границу процесса.

Создайте сеанс PMP Media следующим образом:

1.  Создайте новое хранилище атрибутов, вызвав [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Задайте атрибут [**\_ \_ \_ \_ диспетчера защиты содержимого сеанса MF**](mf-session-content-protection-manager-attribute.md) в хранилище атрибутов. Значение этого атрибута является указателем на реализацию [**имфконтентпротектионманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)приложения. Вызовите метод [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) , чтобы задать атрибут.
3.  Вызовите [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , чтобы создать сеанс мультимедиа в процессе PMP. Параметр *пконфигуратион* является указателем на интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) хранилища атрибутов.


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



Затем создайте топологию воспроизведения и поочередно помещает ее в сеанс мультимедиа, как описано в разделе [Создание топологий воспроизведения](creating-playback-topologies.md).

## <a name="perform-rights-acquisition"></a>Получение прав

Если для воспроизведения требуется получение прав, сеанс мультимедиа вызывает [**имфконтентпротектионманажер:: бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). Параметр *пенаблерактивате* этого метода является указателем на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Используйте этот интерфейс для создания объекта включения содержимого, который предоставляет интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) . Затем используйте функцию включения содержимого для выполнения шага получения прав.

Чтобы создать модуль включения содержимого, вызовите [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



Запросите возвращенный указатель [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) для интерфейса [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Используйте этот интерфейс для получения событий из объекта включения содержимого. Дополнительные сведения о событиях см. в разделе [генераторы событий мультимедиа](media-event-generators.md).

Чтобы узнать, поддерживает ли модуль включения содержимого автоматическое получение, вызовите [**имфконтентенаблер:: исаутоматиксуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported). Если этот метод возвращает значение **true**, приложение должно использовать автоматическое получение. В противном случае используйте неавтоматические получение.

Метод [**бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) является асинхронным. Приложение должно выполнить шаг приобретения в потоке приложения. Один из подходов — опубликовать сообщение частного окна в главном окне приложения, уведомляя поток приложения, чтобы выполнить получение. Пока операция находится в состоянии ожидания, приложение должно сохранить указатель обратного вызова и объект состояния, полученный в параметрах *пкаллбакк* и *пункстате* **бегиненаблеконтент**. Они будут использоваться для завершения асинхронной операции.

### <a name="automatic-acquisition"></a>Автоматическое получение

Чтобы выполнить автоматическое получение, вызовите [**имфконтентенаблер:: аутоматиценабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable). Этот метод является асинхронным. После завершения операции модуль включения содержимого отправляет событие [минаблеркомплетед](meenablercompleted.md) . Код состояния события указывает, была ли операция успешной. Если код состояния из события Минаблеркомплетед — это \_ нотаккуиред лицензия на NS E \_ DRM \_ \_ , приложение должно использовать неавтоматическую приемку.

Пока выполняется операция приобретения, объект-получатель может отправить событие [минаблерпрогресс](meenablerprogress.md) , чтобы указать ход выполнения операции. Чтобы отменить операцию, вызовите метод [**имфконтентенаблер:: Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).

### <a name="non-silent-acquisition"></a>Получение без уведомления

Если метод [**исаутоматиксуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) возвращает **значение false** или метод [**аутоматиценабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) завершается с кодом ошибки NS \_ E \_ DRM \_ License \_ нотаккуиред, приложение должно выполнять неавтоматическую процедуру приобретения, как описано в следующих шагах:

1.  Вызовите [**имфконтентенаблер:: жетенаблеурл**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) , чтобы получить URL-адрес для получения прав. Этот метод также возвращает флаг, указывающий, является ли URL-адрес доверенным.
2.  Вызовите метод [**имфконтентенаблер:: жетенабледата**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) , чтобы получить данные HTTP POST.
3.  Вызовите [**имфконтентенаблер:: мониторенабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable). Этот метод заставляет модуль включения содержимого отслеживать ход выполнения действия получения прав.

4.  Отправьте данные в URL-адрес получения прав с помощью действия HTTP POST. Можно использовать элемент управления Internet Explorer или API Windows Internet (WinINet).

В следующем коде показаны шаги 1 – 3. Шаг 4 зависит от конкретных требований приложения.


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



После завершения операции модуль включения содержимого отправляет событие [минаблеркомплетед](meenablercompleted.md) .

## <a name="complete-the-asynchronous-operation"></a>Завершение асинхронной операции

Когда получение прав завершается успешно или иначе, приложение должно уведомить сеанс мультимедиа, вызвав указатель обратного вызова, заданный в методе [**бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .

1.  Создайте объект асинхронного результата, вызвав [**мфкреатеасинкресулт**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).
2.  Вызов обратного вызова сеанса мультимедиа путем вызова [**мфинвокекаллбакк**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).
3.  Сеанс мультимедиа будет вызывать [**имфконтентпротектионманажер:: енденаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent). В реализации этого метода Освободите все указатели или ресурсы, выделенные внутри [**бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). Возвращает **значение HRESULT** , указывающее на общее успешное выполнение операции. Если не удалось получить права или пользователь отменил операцию до его завершения, возвращается код ошибки.

В следующем коде показано, как создать асинхронный результат и вызвать обратный вызов.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Сеанс мультимедиа](media-session.md)
</dt> <dt>

[Воспроизведение звука/видео](audio-video-playback.md)
</dt> </dl>

 

 



