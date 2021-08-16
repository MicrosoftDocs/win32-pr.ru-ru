---
description: Успешный кодек
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Успешный кодек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56112942aa8378b2016616d0e090e17eb7225ca27b363c96e37eb7cccb6286e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065131"
---
# <a name="codec-merit"></a>Успешный кодек

начиная с Windows 7, для кодека Media Foundation может быть назначено *значение.* При перечислении кодеков кодеки с более высоким уровнем проявляются предпочтительнее кодеков с более низкими уровнями. Кодеки с любыми преимуществами являются предпочтительными для кодеков без назначенного. Дополнительные сведения о перечислении кодеков см. в разделе [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).

Эти значения назначаются корпорацией Майкрософт. В настоящее время получить значение недостаточного значения могут только аппаратные кодеки. Поставщик кодеков также выдает цифровой сертификат, который используется для проверки значения соответствия кодека. Чтобы получить сертификат, отправьте запрос по электронной почте wmla@microsoft.com . Процесс получения сертификата включает подпись лицензии и предоставление набора информационных файлов корпорации Майкрософт.

Он работает следующим образом:

1.  Поставщик кодека реализует один из следующих элементов:
    -   Мини-драйвер Австреам. Media Foundation предоставляет стандартную основную таблицу файлов прокси для драйверов Австреам. Это желательно сделать.
    -   Преобразование Media Foundation (MFT), которое выступает в качестве прокси-сервера для оборудования. Дополнительные сведения см. в разделе [Hardware МФТС](hardware-mfts.md).
2.  Значение соответствия кодека сохраняется в реестре для быстрого поиска.
3.  Функция [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) сортирует кодеки в порядке их получения. В списке для локально зарегистрированных кодеков отображаются кодеки с недостижением (см. [**мфтрегистерлокал**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), но перед другими кодеками.
4.  Когда создается таблица MFT, проверка подлинности кодека проверяется с помощью API [выхода из диспетчера исходящего Protection](output-protection-manager.md) (ОПМ).
5.  Для прокси-файлов MFT, кодек реализует интерфейс [**иопмвидеуутпут**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) . Для драйвера Австреам кодек реализует \_ набор свойств кспропсетид опмвидеуутпут.

На следующей схеме показана проверка в обоих случаях.

![Схема, на которой показаны два процесса: один из них ведет через прокси-сервер Media Foundation MFT и драйвер австреам, а другой — через пользовательский прокси-объект MFT.](images/codecmerit.png)

## <a name="custom-proxy-mft"></a>Таблица MFT пользовательского прокси-сервера

Если вы предоставляете основную таблицу файлов прокси для аппаратного кодека, примените значение получения кодека, как показано ниже.

1.  Реализуйте интерфейс [**иопмвидеуутпут**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) в MFT. Пример кода показан в следующем разделе этой статьи.
2.  Добавьте в реестр атрибут атрибута «подсистему [ \_ \_ \_ кодека MFT](mft-codec-merit-attribute.md) », как показано ниже.

    1.  Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать новое хранилище атрибутов.
    2.  Вызовите метод [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) , чтобы задать атрибут [ \_ \_ \_ атрибута для кодека MFT](mft-codec-merit-attribute.md) . Значением атрибута является назначение кодека.
    3.  Чтобы зарегистрировать MFT, вызовите [**мфтрегистер**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) . Передайте хранилище атрибутов в параметре *паттрибутес* .

3.  Приложение вызывает [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Эта функция возвращает массив указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , по одному для каждого кодека, соответствующего критериям перечисления.
4.  Приложение вызывает [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) для создания MFT.
5.  Метод [**активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) вызывает функцию [**мфжетмфтмерит**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) для проверки сертификата и значения несоответствия.
6.  Функция [**мфжетмфтмерит**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) вызывает [**иопмвидеуутпут::**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) и отправляет запрос состояния [**ОПМ \_ получения \_ кодека \_**](opm-get-codec-info.md) . Этот запрос состояния возвращает значение непоставленного кодека. Если это значение не соответствует значению реестра, [**активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) может завершиться ошибкой.

В следующем коде показано, как добавить значение в реестр при регистрации MFT:


```C++
// Shows how to register an MFT with a merit value.

HRESULT RegisterMFTWithMerit()
{
    // The following media types would apply to an H.264 decoder, 
    // and are used here as an example.

    MFT_REGISTER_TYPE_INFO aDecoderInputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_H264 },
    };

    MFT_REGISTER_TYPE_INFO aDecoderOutputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_RGB32 }
    };
    
    // Create an attribute store to hold the merit attribute.
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MFT_CODEC_MERIT_Attribute, 
            DECODER_MERIT   // Use the codec's assigned merit value.
            );
    }

    // Register the decoder for MFTEnum(Ex).
    if (SUCCEEDED(hr))
    {
        hr = MFTRegister(
            CLSID_MPEG1SampleDecoder,                   // CLSID
            MFT_CATEGORY_VIDEO_DECODER,                 // Category
            const_cast<LPWSTR>(SZ_DECODER_NAME),        // Friendly name
            0,                                          // Flags
            ARRAYSIZE(aDecoderInputTypes),              // Number of input types
            aDecoderInputTypes,                         // Input types
            ARRAYSIZE(aDecoderOutputTypes),             // Number of output types
            aDecoderOutputTypes,                        // Output types
            pAttributes                                 // Attributes 
            );
    }

    SafeRelease(&pAttributes);
    return hr;
}
```



### <a name="implementing-iopmvideooutput-for-codec-merit"></a>Реализация Иопмвидеуутпут для выполнения кодека

В следующем коде показано, как реализовать [**иопмвидеуутпут**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) для того, чтобы создать кодек. Более общее описание API ОПМ см. в разделе [Output Protection Manager](output-protection-manager.md).

> [!Note]  
> Приведенный здесь код не содержит запутывания или другие механизмы безопасности. Она должна показывать базовую реализацию ОПМ подтверждения и запроса состояния.

 

В этом примере предполагается, что *g \_ тестцерт* — байтовый массив, который содержит цепочку сертификатов кодека, а *g \_ PrivateKey* — байтовый массив, содержащий закрытый ключ из сертификата:


```C++
// Byte array that contains the codec's certificate.

const BYTE g_TestCert[] =
{
    // ... (certificate not shown)
```




```C++
// Byte array that contains the private key from the certificate.

const BYTE g_PrivateKey[] = 
{
    // .... (key not shown)
```



В методе [**иопмвидеуутпут:: стартинитиализатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) создайте случайное число для подтверждения. Верните это число и сертификат в вызывающий объект:


```C++
STDMETHODIMP CodecMerit::StartInitialization(
    OPM_RANDOM_NUMBER *prnRandomNumber,
    BYTE **ppbCertificate,
    ULONG *pulCertificateLength
    )
{
    HRESULT hr = S_OK;

    DWORD cbCertificate = sizeof(g_TestCert);
    const BYTE *pCertificate = g_TestCert;

    // Generate the random number for the OPM handshake.
    hr = BCryptGenRandom(
        NULL,  
        (PUCHAR)&m_RandomNumber, 
        sizeof(m_RandomNumber),
        BCRYPT_USE_SYSTEM_PREFERRED_RNG
        );

    // Allocate the buffer to copy the certificate.
    if (SUCCEEDED(hr))
    {
        *ppbCertificate = (PBYTE)CoTaskMemAlloc(cbCertificate);

        if (*ppbCertificate == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Copy the certificate and the random number.
    if (SUCCEEDED(hr))
    {
        *pulCertificateLength = cbCertificate;
        CopyMemory(*ppbCertificate, pCertificate, cbCertificate);
        *prnRandomNumber = m_RandomNumber;
    }
    return hr;
}
```



Метод [**иопмвидеуутпут:: финишинитиализатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) завершает синхронизацию ОПМ:


```C++
STDMETHODIMP CodecMerit::FinishInitialization(
    const OPM_ENCRYPTED_INITIALIZATION_PARAMETERS *pParameters
    )
{
    HRESULT hr = S_OK;
    BCRYPT_ALG_HANDLE hAlg = NULL;
    BCRYPT_KEY_HANDLE hKey = NULL;
    BCRYPT_OAEP_PADDING_INFO paddingInfo = {0};
    DWORD DecryptedLength = 0;
    PBYTE pbDecryptedParams = NULL;

    // The caller should pass the following structure in
    // pParameters:

    typedef struct {
        GUID  guidCOPPRandom;   // Our random number.
        GUID  guidKDI;          // AES signing key.
        DWORD StatusSeqStart;   // Status sequence number.
        DWORD CommandSeqStart;  // Command sequence number.
    } InitParams;

    paddingInfo.pszAlgId = BCRYPT_SHA512_ALGORITHM;

    //  Decrypt the input using the decoder's private key.

    hr = BCryptOpenAlgorithmProvider(
        &hAlg,
        BCRYPT_RSA_ALGORITHM,
        MS_PRIMITIVE_PROVIDER,
        0
        );

    //  Import the private key.
    if (SUCCEEDED(hr))
    {
        hr = BCryptImportKeyPair(
            hAlg,
            NULL,
            BCRYPT_RSAPRIVATE_BLOB,
            &hKey,
            (PUCHAR)g_PrivateKey, //pbData,
            sizeof(g_PrivateKey), //cbData,
            0
            );
    }

    //  Decrypt the input data.

    if (SUCCEEDED(hr))
    {
        hr = BCryptDecrypt(
            hKey,
            (PBYTE)pParameters,
            OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
            &paddingInfo,
            NULL,
            0,
            NULL,
            0,
            &DecryptedLength,
            BCRYPT_PAD_OAEP
            );
    }

    if (SUCCEEDED(hr))
    {
        pbDecryptedParams = new (std::nothrow) BYTE[DecryptedLength];

        if (pbDecryptedParams == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    if (SUCCEEDED(hr))
    {
         hr = BCryptDecrypt(
             hKey,
             (PBYTE)pParameters,
             OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
             &paddingInfo,
             NULL,
             0,
             pbDecryptedParams,
             DecryptedLength,
             &DecryptedLength,
             BCRYPT_PAD_OAEP
             );
    }

    if (SUCCEEDED(hr))
    {
        InitParams *Params = (InitParams *)pbDecryptedParams;
        
        //  Check the random number.
        if (0 != memcmp(&m_RandomNumber, &Params->guidCOPPRandom, sizeof(m_RandomNumber)))
        {
            hr = E_ACCESSDENIED;
        } 
        else 
        {
            //  Save the key and the sequence numbers.

            CopyMemory(m_AESKey.abRandomNumber, &Params->guidKDI, sizeof(m_AESKey));
            m_StatusSequenceNumber = Params->StatusSeqStart;
            m_CommandSequenceNumber = Params->CommandSeqStart;
        }
    }

    //  Clean up.

    if (hKey)
    {
        BCryptDestroyKey(hKey);
    }
    if (hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg, 0);
    }
    delete [] pbDecryptedParams;

    return hr;
}
```



В методе [**иопмвидеуутпут::**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) i реализуйте запрос состояния [**ОПМ \_ Get \_ кодека \_**](opm-get-codec-info.md) . Входными данными является структура [**\_ параметров ОПМ Get для \_ кодека \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) , содержащая идентификаторы CLSID для MFT. Выходные данные представляют собой структуру [**ОПМ \_ Get для получения \_ сведений о кодека \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) , которая содержит сведения о получении кодека.


```C++
STDMETHODIMP CodecMerit::GetInformation( 
    const OPM_GET_INFO_PARAMETERS *Parameters,
    OPM_REQUESTED_INFORMATION *pRequest
    )
{

    HRESULT hr = S_OK;
    OPM_GET_CODEC_INFO_PARAMETERS *CodecInfoParameters;

    //  Check the MAC.
    OPM_OMAC Tag = { 0 };

    hr = ComputeOMAC(
        m_AESKey, 
        (PBYTE)Parameters + OPM_OMAC_SIZE, 
        sizeof(OPM_GET_INFO_PARAMETERS) - OPM_OMAC_SIZE, 
        &Tag
        );

    if (SUCCEEDED(hr))
    {
        if (0 != memcmp(Tag.abOMAC, &Parameters->omac, OPM_OMAC_SIZE))
        {
            hr = E_ACCESSDENIED;
        }
    }

    // Validate the status sequence number. This must be consecutive
    // from the previous sequence number.

    if (SUCCEEDED(hr))
    {
        if (Parameters->ulSequenceNumber != m_StatusSequenceNumber++)
        {
            hr = E_ACCESSDENIED;
        }
    }

    //  Check the status request.

    if (SUCCEEDED(hr))
    {
        if (Parameters->guidInformation != OPM_GET_CODEC_INFO) 
        {
            hr = E_NOTIMPL;
        }
    }

    //  Check parameters.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;

        if (Parameters->cbParametersSize > OPM_GET_INFORMATION_PARAMETERS_SIZE ||
            Parameters->cbParametersSize < sizeof(ULONG) ||
            Parameters->cbParametersSize - sizeof(ULONG) != CodecInfoParameters->cbVerifier
            ) 
        {
            hr = E_INVALIDARG;
        }
    }

    //  The input data should consist of the CLSID of the decoder.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;
    
        if (CodecInfoParameters->cbVerifier != sizeof(CLSID) ||
            0 != memcmp(&CLSID_MPEG1SampleDecoder,
                        CodecInfoParameters->Verifier,
                        CodecInfoParameters->cbVerifier)) 
        {
            hr = E_ACCESSDENIED;
        }
    }

    if (SUCCEEDED(hr))
    {
        // Now return the decoder merit to the caller.

        ZeroMemory(pRequest, sizeof(OPM_REQUESTED_INFORMATION));

        OPM_GET_CODEC_INFO_INFORMATION *pInfo = 
            (OPM_GET_CODEC_INFO_INFORMATION *)pRequest->abRequestedInformation;

        pInfo->Merit = DECODER_MERIT;
        pInfo->rnRandomNumber = Parameters->rnRandomNumber;

        pRequest->cbRequestedInformationSize = sizeof(OPM_GET_CODEC_INFO_INFORMATION);

        //  Sign it with the key.

        hr = ComputeOMAC(
            m_AESKey, 
            (PBYTE)pRequest + OPM_OMAC_SIZE, 
            sizeof(OPM_REQUESTED_INFORMATION) - OPM_OMAC_SIZE, 
            &pRequest->omac
            );
    }

    return hr;
}
```



Метод [**ОМАК**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) должен вычислить код проверки подлинности сообщения (Mac) с помощью алгоритма "1. см. раздел [Вычисление значения ОМАК-1](opm-example-code.md).

Нет необходимости поддерживать какие-либо другие запросы состояния ОПМ.

Методы [**иопмвидеуутпут:: коппкомпатиблежетинформатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) и [**Иопмвидеуутпут:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) не являются обязательными для получения кодека, поэтому эти методы могут возвращать **E \_ нотимпл**.


```C++
STDMETHODIMP CodecMerit::COPPCompatibleGetInformation( 
    const OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
    OPM_REQUESTED_INFORMATION *pRequestedInformation)
{
    return E_NOTIMPL;
}

STDMETHODIMP CodecMerit::Configure( 
    const OPM_CONFIGURE_PARAMETERS *pParameters,
    ULONG ulAdditionalParametersSize,
    const BYTE *pbAdditionalParameters)
{
    return E_NOTIMPL;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[Запись пользовательского MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



