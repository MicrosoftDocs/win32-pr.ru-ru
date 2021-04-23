---
description: Успешный кодек
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Успешный кодек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd177c3c32084a030ce75c15cecd5d4c04fc3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554927"
---
# <a name="codec-merit"></a><span data-ttu-id="899d3-103">Успешный кодек</span><span class="sxs-lookup"><span data-stu-id="899d3-103">Codec Merit</span></span>

<span data-ttu-id="899d3-104">Начиная с Windows 7, для Media Foundation кодека может быть назначено *значение.*</span><span class="sxs-lookup"><span data-stu-id="899d3-104">Starting in Windows 7, a Media Foundation codec can be assigned a *merit* value.</span></span> <span data-ttu-id="899d3-105">При перечислении кодеков кодеки с более высоким уровнем проявляются предпочтительнее кодеков с более низкими уровнями.</span><span class="sxs-lookup"><span data-stu-id="899d3-105">When codecs are enumerated, codecs with higher merit are preferred over codecs with lower merit.</span></span> <span data-ttu-id="899d3-106">Кодеки с любыми преимуществами являются предпочтительными для кодеков без назначенного.</span><span class="sxs-lookup"><span data-stu-id="899d3-106">Codecs with any merit value are preferred over codecs without an assigned merit.</span></span> <span data-ttu-id="899d3-107">Дополнительные сведения о перечислении кодеков см. в разделе [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="899d3-107">For details about codec enumeration, see [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

<span data-ttu-id="899d3-108">Эти значения назначаются корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="899d3-108">Merit values are assigned by Microsoft.</span></span> <span data-ttu-id="899d3-109">В настоящее время получить значение недостаточного значения могут только аппаратные кодеки.</span><span class="sxs-lookup"><span data-stu-id="899d3-109">Currently, only hardware codecs are eligible to receive a merit value.</span></span> <span data-ttu-id="899d3-110">Поставщик кодеков также выдает цифровой сертификат, который используется для проверки значения соответствия кодека.</span><span class="sxs-lookup"><span data-stu-id="899d3-110">The codec vendor is also issued a digital certificate, which is used to verify the codec's merit value.</span></span> <span data-ttu-id="899d3-111">Чтобы получить сертификат, отправьте запрос по электронной почте wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="899d3-111">To obtain a certificate, send an email request to wmla@microsoft.com.</span></span> <span data-ttu-id="899d3-112">Процесс получения сертификата включает подпись лицензии и предоставление набора информационных файлов корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="899d3-112">The process for obtaining a certificate includes signing a license and providing a set of information files to Microsoft.</span></span>

<span data-ttu-id="899d3-113">Он работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="899d3-113">Codec merit works as follows:</span></span>

1.  <span data-ttu-id="899d3-114">Поставщик кодека реализует один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="899d3-114">The codec vendor implements one of the following:</span></span>
    -   <span data-ttu-id="899d3-115">Мини-драйвер Австреам.</span><span class="sxs-lookup"><span data-stu-id="899d3-115">An AVStream mini-driver.</span></span> <span data-ttu-id="899d3-116">Media Foundation предоставляет стандартную основную таблицу файлов прокси для драйверов Австреам.</span><span class="sxs-lookup"><span data-stu-id="899d3-116">Media Foundation provides an standard proxy MFT for AVStream drivers.</span></span> <span data-ttu-id="899d3-117">Это желательно сделать.</span><span class="sxs-lookup"><span data-stu-id="899d3-117">This is the recommended option.</span></span>
    -   <span data-ttu-id="899d3-118">Преобразование Media Foundation (MFT), которое выступает в качестве прокси-сервера для оборудования.</span><span class="sxs-lookup"><span data-stu-id="899d3-118">A Media Foundation transform (MFT) that acts as a proxy to the hardware.</span></span> <span data-ttu-id="899d3-119">Дополнительные сведения см. в разделе [Hardware МФТС](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="899d3-119">For more information, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="899d3-120">Значение соответствия кодека сохраняется в реестре для быстрого поиска.</span><span class="sxs-lookup"><span data-stu-id="899d3-120">The codec's merit value is stored in the registry for quick lookup.</span></span>
3.  <span data-ttu-id="899d3-121">Функция [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) сортирует кодеки в порядке их получения.</span><span class="sxs-lookup"><span data-stu-id="899d3-121">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function sorts codecs in order of merit.</span></span> <span data-ttu-id="899d3-122">В списке для локально зарегистрированных кодеков отображаются кодеки с недостижением (см. [**мфтрегистерлокал**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), но перед другими кодеками.</span><span class="sxs-lookup"><span data-stu-id="899d3-122">Codecs with merit values appear in the list behind locally registered codecs (see [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), but ahead of other codecs.</span></span>
4.  <span data-ttu-id="899d3-123">Когда создается таблица MFT, проверка подлинности кодека проверяется с помощью API [выхода из диспетчера исходящего Protection](output-protection-manager.md) (ОПМ).</span><span class="sxs-lookup"><span data-stu-id="899d3-123">When the MFT is created, the codec's merit is verified using the [Output Protection Manager](output-protection-manager.md) (OPM) API.</span></span>
5.  <span data-ttu-id="899d3-124">Для прокси-файлов MFT, кодек реализует интерфейс [**иопмвидеуутпут**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) .</span><span class="sxs-lookup"><span data-stu-id="899d3-124">For a proxy MFT, the codec implements the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface.</span></span> <span data-ttu-id="899d3-125">Для драйвера Австреам кодек реализует \_ набор свойств кспропсетид опмвидеуутпут.</span><span class="sxs-lookup"><span data-stu-id="899d3-125">For an AVStream driver, the codec implements the KSPROPSETID\_OPMVideoOutput property set.</span></span>

<span data-ttu-id="899d3-126">На следующей схеме показана проверка в обоих случаях.</span><span class="sxs-lookup"><span data-stu-id="899d3-126">The following diagram shows how merit is verified in both cases:</span></span>

![Схема, на которой показаны два процесса: один из них ведет через прокси-сервер Media Foundation MFT и драйвер австреам, а другой — через пользовательский прокси-объект MFT.](images/codecmerit.png)

## <a name="custom-proxy-mft"></a><span data-ttu-id="899d3-128">Таблица MFT пользовательского прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="899d3-128">Custom Proxy MFT</span></span>

<span data-ttu-id="899d3-129">Если вы предоставляете основную таблицу файлов прокси для аппаратного кодека, примените значение получения кодека, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="899d3-129">If you provide a proxy MFT for the hardware codec, implement the codec merit value as follows:</span></span>

1.  <span data-ttu-id="899d3-130">Реализуйте интерфейс [**иопмвидеуутпут**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) в MFT.</span><span class="sxs-lookup"><span data-stu-id="899d3-130">Implement the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface in the MFT.</span></span> <span data-ttu-id="899d3-131">Пример кода показан в следующем разделе этой статьи.</span><span class="sxs-lookup"><span data-stu-id="899d3-131">Example code is shown in the next section of this topic.</span></span>
2.  <span data-ttu-id="899d3-132">Добавьте в реестр атрибут атрибута «подсистему [ \_ \_ \_ кодека MFT](mft-codec-merit-attribute.md) », как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="899d3-132">Add the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute to the registry, as follows:</span></span>

    1.  <span data-ttu-id="899d3-133">Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать новое хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="899d3-133">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    2.  <span data-ttu-id="899d3-134">Вызовите метод [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) , чтобы задать атрибут [ \_ \_ \_ атрибута для кодека MFT](mft-codec-merit-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="899d3-134">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute.</span></span> <span data-ttu-id="899d3-135">Значением атрибута является назначение кодека.</span><span class="sxs-lookup"><span data-stu-id="899d3-135">The value of the attribute is the codec's assigned merit.</span></span>
    3.  <span data-ttu-id="899d3-136">Чтобы зарегистрировать MFT, вызовите [**мфтрегистер**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) .</span><span class="sxs-lookup"><span data-stu-id="899d3-136">Call [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) to register the MFT.</span></span> <span data-ttu-id="899d3-137">Передайте хранилище атрибутов в параметре *паттрибутес* .</span><span class="sxs-lookup"><span data-stu-id="899d3-137">Pass the attribute store in the *pAttributes* parameter.</span></span>

3.  <span data-ttu-id="899d3-138">Приложение вызывает [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="899d3-138">The application calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="899d3-139">Эта функция возвращает массив указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , по одному для каждого кодека, соответствующего критериям перечисления.</span><span class="sxs-lookup"><span data-stu-id="899d3-139">This function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, one for each codec that matches the enumeration criteria.</span></span>
4.  <span data-ttu-id="899d3-140">Приложение вызывает [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) для создания MFT.</span><span class="sxs-lookup"><span data-stu-id="899d3-140">The application calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the MFT.</span></span>
5.  <span data-ttu-id="899d3-141">Метод [**активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) вызывает функцию [**мфжетмфтмерит**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) для проверки сертификата и значения несоответствия.</span><span class="sxs-lookup"><span data-stu-id="899d3-141">The [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method calls the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function to verify the certificate and the merit value.</span></span>
6.  <span data-ttu-id="899d3-142">Функция [**мфжетмфтмерит**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) вызывает [**иопмвидеуутпут::**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) и отправляет запрос состояния [**ОПМ \_ получения \_ кодека \_**](opm-get-codec-info.md) .</span><span class="sxs-lookup"><span data-stu-id="899d3-142">The [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function calls [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) and sends an [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="899d3-143">Этот запрос состояния возвращает значение непоставленного кодека.</span><span class="sxs-lookup"><span data-stu-id="899d3-143">This status request returns the codec's assigned merit value.</span></span> <span data-ttu-id="899d3-144">Если это значение не соответствует значению реестра, [**активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) может завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="899d3-144">If this value does not match the registry value, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) may fail.</span></span>

<span data-ttu-id="899d3-145">В следующем коде показано, как добавить значение в реестр при регистрации MFT:</span><span class="sxs-lookup"><span data-stu-id="899d3-145">The following code shows how to add the merit value to the registry when you register the MFT:</span></span>


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



### <a name="implementing-iopmvideooutput-for-codec-merit"></a><span data-ttu-id="899d3-146">Реализация Иопмвидеуутпут для выполнения кодека</span><span class="sxs-lookup"><span data-stu-id="899d3-146">Implementing IOPMVideoOutput for Codec Merit</span></span>

<span data-ttu-id="899d3-147">В следующем коде показано, как реализовать [**иопмвидеуутпут**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) для того, чтобы создать кодек.</span><span class="sxs-lookup"><span data-stu-id="899d3-147">The following code shows how to implement [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) for codec merit.</span></span> <span data-ttu-id="899d3-148">Более общее описание API ОПМ см. в разделе [Output Protection Manager](output-protection-manager.md).</span><span class="sxs-lookup"><span data-stu-id="899d3-148">For a more general discussion of the OPM API, see [Output Protection Manager](output-protection-manager.md).</span></span>

> [!Note]  
> <span data-ttu-id="899d3-149">Приведенный здесь код не содержит запутывания или другие механизмы безопасности.</span><span class="sxs-lookup"><span data-stu-id="899d3-149">The code shown here has no obfuscation or other security mechanisms.</span></span> <span data-ttu-id="899d3-150">Она должна показывать базовую реализацию ОПМ подтверждения и запроса состояния.</span><span class="sxs-lookup"><span data-stu-id="899d3-150">It is meant to show the basic implementation of the OPM handshake and status request.</span></span>

 

<span data-ttu-id="899d3-151">В этом примере предполагается, что *g \_ тестцерт* — байтовый массив, который содержит цепочку сертификатов кодека, а *g \_ PrivateKey* — байтовый массив, содержащий закрытый ключ из сертификата:</span><span class="sxs-lookup"><span data-stu-id="899d3-151">This example assumes that *g\_TestCert* is a byte array that contains the codec's certificate chain, and *g\_PrivateKey* is a byte array that contains the private key from the certificate:</span></span>


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



<span data-ttu-id="899d3-152">В методе [**иопмвидеуутпут:: стартинитиализатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) создайте случайное число для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="899d3-152">In the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method, generate a random number for the handshake.</span></span> <span data-ttu-id="899d3-153">Верните это число и сертификат в вызывающий объект:</span><span class="sxs-lookup"><span data-stu-id="899d3-153">Return this number and the certificate to the caller:</span></span>


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



<span data-ttu-id="899d3-154">Метод [**иопмвидеуутпут:: финишинитиализатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) завершает синхронизацию ОПМ:</span><span class="sxs-lookup"><span data-stu-id="899d3-154">The [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) method completes the OPM handshake:</span></span>


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



<span data-ttu-id="899d3-155">В методе [**иопмвидеуутпут::**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) i реализуйте запрос состояния [**ОПМ \_ Get \_ кодека \_**](opm-get-codec-info.md) .</span><span class="sxs-lookup"><span data-stu-id="899d3-155">In the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method, implement the [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="899d3-156">Входными данными является структура [**\_ параметров ОПМ Get для \_ кодека \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) , содержащая идентификаторы CLSID для MFT.</span><span class="sxs-lookup"><span data-stu-id="899d3-156">The input data is an [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure that contains the CLSID of your MFT.</span></span> <span data-ttu-id="899d3-157">Выходные данные представляют собой структуру [**ОПМ \_ Get для получения \_ сведений о кодека \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) , которая содержит сведения о получении кодека.</span><span class="sxs-lookup"><span data-stu-id="899d3-157">The output data is an [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure that contains the codec merit.</span></span>


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



<span data-ttu-id="899d3-158">Метод [**ОМАК**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) должен вычислить код проверки подлинности сообщения (Mac) с помощью алгоритма "1. см. раздел [Вычисление значения ОМАК-1](opm-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="899d3-158">The [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method must compute a Message Authentication Code (MAC) using the OMAC-1 algorithm; see [Computing the OMAC-1 Value](opm-example-code.md).</span></span>

<span data-ttu-id="899d3-159">Нет необходимости поддерживать какие-либо другие запросы состояния ОПМ.</span><span class="sxs-lookup"><span data-stu-id="899d3-159">It is not necessary to support any other OPM status requests.</span></span>

<span data-ttu-id="899d3-160">Методы [**иопмвидеуутпут:: коппкомпатиблежетинформатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) и [**Иопмвидеуутпут:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) не являются обязательными для получения кодека, поэтому эти методы могут возвращать **E \_ нотимпл**.</span><span class="sxs-lookup"><span data-stu-id="899d3-160">The [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) and [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) methods are not required for codec merit, so these methods can return **E\_NOTIMPL**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="899d3-161">См. также</span><span class="sxs-lookup"><span data-stu-id="899d3-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="899d3-162">Преобразования Media Foundation</span><span class="sxs-lookup"><span data-stu-id="899d3-162">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="899d3-163">Запись пользовательского MFT</span><span class="sxs-lookup"><span data-stu-id="899d3-163">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



