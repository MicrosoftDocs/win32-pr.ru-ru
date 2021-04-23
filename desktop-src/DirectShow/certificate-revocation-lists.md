---
description: списки отзыва сертификатов.
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: списки отзыва сертификатов.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51ddee9f77b147d69b8895b3335d41e041da7f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662023"
---
# <a name="certificate-revocation-lists"></a><span data-ttu-id="41b7d-103">списки отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="41b7d-103">Certificate Revocation Lists</span></span>

<span data-ttu-id="41b7d-104">В этом разделе описывается, как проверить список отзыва сертификатов (CRL) для отозванных драйверов при использовании протокола сертифицированной выходной защиты (Копп).</span><span class="sxs-lookup"><span data-stu-id="41b7d-104">This topic describes how to examine the certificate revocation list (CRL) for revoked drivers when using Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="41b7d-105">Список отзыва сертификатов содержит дайджесты отозванных сертификатов и может предоставляться и подписываться только корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="41b7d-105">The CRL contains digests of revoked certificates and can be provided and signed only by Microsoft.</span></span> <span data-ttu-id="41b7d-106">Список отзыва сертификатов распространяется по лицензиям управления цифровыми правами (DRM).</span><span class="sxs-lookup"><span data-stu-id="41b7d-106">The CRL is distributed through digital rights management (DRM) licenses.</span></span> <span data-ttu-id="41b7d-107">Список отзыва сертификатов может отозвать любой сертификат в цепочке сертификатов драйвера.</span><span class="sxs-lookup"><span data-stu-id="41b7d-107">The CRL can revoke any certificate in the driver's certificates chain.</span></span> <span data-ttu-id="41b7d-108">Если какой-либо сертификат в цепочке отозван, то этот сертификат и все сертификаты, приведенные ниже в цепочке, также будут отозваны.</span><span class="sxs-lookup"><span data-stu-id="41b7d-108">If any certificate in the chain is revoked, then that certificate and all of the certificates below it in the chain are also revoked.</span></span>

<span data-ttu-id="41b7d-109">Чтобы получить список отзыва сертификатов, приложение должно использовать пакет SDK Windows Media Format, версии 9 или более поздней, и выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="41b7d-109">To get the CRL, the application must use the Windows Media Format SDK, version 9 or later, and perform the following steps:</span></span>

1.  <span data-ttu-id="41b7d-110">Вызовите **вмкреатереадер** , чтобы создать объект средства чтения пакета SDK для формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="41b7d-110">Call **WMCreateReader** to create the Windows Media Format SDK reader object.</span></span>
2.  <span data-ttu-id="41b7d-111">Запросите объект модуля чтения для интерфейса **ивмдрмреадер** .</span><span class="sxs-lookup"><span data-stu-id="41b7d-111">Query the reader object for the **IWMDRMReader** interface.</span></span>
3.  <span data-ttu-id="41b7d-112">Вызовите **ивмдрмреадер:: жетдрмпроперти** со значением g \_ всзвмдрмнет \_ отзыва, чтобы получить список отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="41b7d-112">Call **IWMDRMReader::GetDRMProperty** with a value of g\_wszWMDRMNet\_Revocation to get the CRL.</span></span> <span data-ttu-id="41b7d-113">Этот метод необходимо вызывать дважды: один раз, чтобы получить размер буфера для выделения, и один раз для заполнения буфера.</span><span class="sxs-lookup"><span data-stu-id="41b7d-113">You must call this method twice: Once to get the size of the buffer to allocate, and once to fill the buffer.</span></span> <span data-ttu-id="41b7d-114">Второй вызов возвращает строку, содержащую список отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="41b7d-114">The second call returns a string that contains the CRL.</span></span> <span data-ttu-id="41b7d-115">Вся строка имеет кодировку Base-64.</span><span class="sxs-lookup"><span data-stu-id="41b7d-115">The entire string is base-64 encoded.</span></span>
4.  <span data-ttu-id="41b7d-116">Декодирование строки в кодировке Base-64.</span><span class="sxs-lookup"><span data-stu-id="41b7d-116">Decode the base-64 encoded string.</span></span> <span data-ttu-id="41b7d-117">Для этого можно использовать функцию **криптстрингтобинари** .</span><span class="sxs-lookup"><span data-stu-id="41b7d-117">You can use the **CryptStringToBinary** function to do this.</span></span> <span data-ttu-id="41b7d-118">Эта функция является частью CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="41b7d-118">This function is part of CryptoAPI.</span></span>

> [!Note]  
> <span data-ttu-id="41b7d-119">Чтобы использовать интерфейс **ивмдрмреадер** , необходимо получить СТАТИЧЕСКУЮ библиотеку DRM от корпорации Майкрософт и связать приложение с этим файлом библиотеки.</span><span class="sxs-lookup"><span data-stu-id="41b7d-119">To use the **IWMDRMReader** interface, you must obtain a static DRM library from Microsoft and link your application to this library file.</span></span> <span data-ttu-id="41b7d-120">Дополнительные сведения см. в разделе «получение требуемой библиотеки DRM» в документации по пакету SDK для Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="41b7d-120">For more information, see the topic "Obtaining the Required DRM Library" in the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="41b7d-121">Если список отзыва сертификатов отсутствует на компьютере пользователя, метод **жетдрмпроперти** ВОЗВРАЩАЕТ \_ \_ \_ неподдерживаемое свойство NS E DRM \_ .</span><span class="sxs-lookup"><span data-stu-id="41b7d-121">If the CRL is not present on the user's computer, the **GetDRMProperty** method returns NS\_E\_DRM\_UNSUPPORTED\_PROPERTY.</span></span> <span data-ttu-id="41b7d-122">В настоящее время единственным способом получения списка отзыва сертификатов является получение лицензии DRM.</span><span class="sxs-lookup"><span data-stu-id="41b7d-122">Currently, the only way to obtain the CRL is to acquire a DRM license.</span></span>

<span data-ttu-id="41b7d-123">В следующем коде показана функция, возвращающая список отзыва сертификатов:</span><span class="sxs-lookup"><span data-stu-id="41b7d-123">The following code shows a function that returns the CRL:</span></span>


```C++
////////////////////////////////////////////////////////////////////////
//  Name: GetCRL
//  Description: Gets the certificate revocation list (CRL).
//
//  ppBuffer: Receives a pointer to the buffer that contains the CRL.
//  pcbBuffer: Receives the size of the buffer returned in ppBuffer.
//
//  The caller must free the returned buffer by calling CoTaskMemFree.
////////////////////////////////////////////////////////////////////////
HRESULT GetCRL(BYTE **ppBuffer, DWORD *pcbBuffer)
{
    IWMReader *pReader = NULL;
    IWMDRMReader *pDrmReader = NULL;
    HRESULT hr = S_OK;

    // DRM attribute data.
    WORD cbAttributeLength = 0;
    BYTE *pDataBase64 = NULL;
    WMT_ATTR_DATATYPE type;

    // Buffer for base-64 decoded CRL.
    BYTE *pCRL = NULL;
    DWORD cbCRL = 0;

    // Create the WMReader object.
    hr = WMCreateReader(NULL, 0, &pReader);

    // Query for the IWMDRMReader interface.
    if (SUCCEEDED(hr))
    {
        hr = pReader->QueryInterface(
            IID_IWMDRMReader, (void**)&pDrmReader);
    }

    // Call GetDRMProperty once to find the size of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            NULL,
            &cbAttributeLength
            );
    }

    // Allocate a buffer.
    if (SUCCEEDED(hr))
    {
        pDataBase64 = (BYTE*)CoTaskMemAlloc(cbAttributeLength);
        if (pDataBase64 == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Call GetDRMProperty again to get the property.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            pDataBase64,
            &cbAttributeLength
            );
    }

    // Find the size of the buffer for the base-64 decoding.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            NULL,                   // Buffer (NULL).
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Allocate a buffer for the CRL.
    if (SUCCEEDED(hr))
    {
        pCRL = (BYTE*)CoTaskMemAlloc(cbCRL);
        if (pCRL == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Base-64 decode to get the CRL.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            pCRL,                   // Buffer.
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Return the buffer to the caller. Caller must free the buffer.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pCRL;
        *pcbBuffer = cbCRL;
    }
    else
    {
        CoTaskMemFree(pCRL);
    }

    CoTaskMemFree(pDataBase64);
    SAFE_RELEASE(pReader);
    SAFE_RELEASE(pDrmReader);
    return hr;
}
```



<span data-ttu-id="41b7d-124">Затем приложение должно проверить допустимость списка отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="41b7d-124">Next, the application must verify that the CRL is valid.</span></span> <span data-ttu-id="41b7d-125">Для этого убедитесь, что сертификат списка отзыва сертификатов, который является частью списка отзыва сертификатов, непосредственно подписан корневым сертификатом Майкрософт и имеет значение элемента Сигнкрл, установленное в 1.</span><span class="sxs-lookup"><span data-stu-id="41b7d-125">To do so, verify that the CRL certificate, which is part of the CRL, is directly signed by the Microsoft Root Certificate and has the SignCRL element value set to 1.</span></span> <span data-ttu-id="41b7d-126">Кроме того, проверьте подпись списка отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="41b7d-126">Also, verify the signature of the CRL.</span></span>

<span data-ttu-id="41b7d-127">После проверки списка отзыва сертификатов приложение может его сохранить.</span><span class="sxs-lookup"><span data-stu-id="41b7d-127">After the CRL is verified, the application can store it.</span></span> <span data-ttu-id="41b7d-128">Номер версии списка отзыва сертификатов также должен быть проверен перед сохранением, чтобы приложение всегда сохраняло последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="41b7d-128">The CRL version number should also be checked before storing so that the application always stores the newest version.</span></span>

<span data-ttu-id="41b7d-129">Список отзыва сертификатов имеет следующий формат.</span><span class="sxs-lookup"><span data-stu-id="41b7d-129">The CRL has the following format.</span></span>



| <span data-ttu-id="41b7d-130">Section</span><span class="sxs-lookup"><span data-stu-id="41b7d-130">Section</span></span>            | <span data-ttu-id="41b7d-131">Содержимое</span><span class="sxs-lookup"><span data-stu-id="41b7d-131">Contents</span></span>                                                             |
|--------------------|----------------------------------------------------------------------|
| <span data-ttu-id="41b7d-132">Header</span><span class="sxs-lookup"><span data-stu-id="41b7d-132">Header</span></span>             | <span data-ttu-id="41b7d-133">32-разрядный список CRL version32-разрядное число записей</span><span class="sxs-lookup"><span data-stu-id="41b7d-133">32-bit CRL version32-bit number of entries</span></span>                           |
| <span data-ttu-id="41b7d-134">Записи отзыва</span><span class="sxs-lookup"><span data-stu-id="41b7d-134">Revocation Entries</span></span> | <span data-ttu-id="41b7d-135">Несколько 160-битных записей отзыва</span><span class="sxs-lookup"><span data-stu-id="41b7d-135">Multiple 160-bit revocation entries</span></span>                                  |
| <span data-ttu-id="41b7d-136">Certificate</span><span class="sxs-lookup"><span data-stu-id="41b7d-136">Certificate</span></span>        | <span data-ttu-id="41b7d-137">32-разрядный сертификат Ленгсвариабле-length</span><span class="sxs-lookup"><span data-stu-id="41b7d-137">32-bit certificate lengthVariable-length certificate</span></span>                 |
| <span data-ttu-id="41b7d-138">Подпись</span><span class="sxs-lookup"><span data-stu-id="41b7d-138">Signature</span></span>          | <span data-ttu-id="41b7d-139">8-разрядная сигнатура type16-bit сигнатура Ленгсвариабле-length</span><span class="sxs-lookup"><span data-stu-id="41b7d-139">8-bit signature type16-bit signature lengthVariable-length signature</span></span> |



 

> [!Note]  
> <span data-ttu-id="41b7d-140">Все целочисленные значения не подписаны и представлены в нотации с обратным порядком байтов (сетевой порядок байт).</span><span class="sxs-lookup"><span data-stu-id="41b7d-140">All integer values are unsigned and are represented in big-endian (network byte order) notation.</span></span>

 

<span data-ttu-id="41b7d-141">Описания разделов списка отзыва сертификатов</span><span class="sxs-lookup"><span data-stu-id="41b7d-141">CRL Section Descriptions</span></span>

<dl> <dt>

<span data-ttu-id="41b7d-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Заголовок</span><span class="sxs-lookup"><span data-stu-id="41b7d-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="41b7d-143">Заголовок содержит номер версии списка отзыва сертификатов и число записей отзыва в списке отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="41b7d-143">The header contains the version number of the CRL and the number of revocation entries in the CRL.</span></span> <span data-ttu-id="41b7d-144">Список отзыва сертификатов может содержать ноль или более записей.</span><span class="sxs-lookup"><span data-stu-id="41b7d-144">A CRL can contain zero or more entries.</span></span>

</dd> <dt>

<span data-ttu-id="41b7d-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Записи отзыва</span><span class="sxs-lookup"><span data-stu-id="41b7d-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Revocation entries</span></span>
</dt> <dd>

<span data-ttu-id="41b7d-146">Каждая запись отзыва — это 160-разрядный дайджест отозванного сертификата.</span><span class="sxs-lookup"><span data-stu-id="41b7d-146">Each revocation entry is the 160-bit digest of a revoked certificate.</span></span> <span data-ttu-id="41b7d-147">Сравните этот дайджест с элементом Дижествалуе в сертификате.</span><span class="sxs-lookup"><span data-stu-id="41b7d-147">Compare this digest with the DigestValue element within the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="41b7d-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificate</span><span class="sxs-lookup"><span data-stu-id="41b7d-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificate</span></span>
</dt> <dd>

<span data-ttu-id="41b7d-149">Раздел сертификата содержит 32-разрядное значение, указывающее длину (в байтах) XML-сертификата и цепочки сертификатов, а также массив байтов, который содержит как сертификат XML центра сертификации, так и цепочку сертификатов, в которой в качестве корня установлен Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="41b7d-149">The certificate section contains a 32-bit value indicating the length (in bytes) of the XML certificate and its certificate chain, along with a byte array that contains both the XML certificate of the Certificate Authority (CA) and the certificate chain that has Microsoft as the Root.</span></span> <span data-ttu-id="41b7d-150">Сертификат должен быть подписан центром сертификации, имеющим право выдавать списки отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="41b7d-150">The certificate must be signed by a CA that has the authority to issue CRLs.</span></span>

> [!Note]  
> <span data-ttu-id="41b7d-151">Сертификат не должен завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="41b7d-151">The certificate must not be null-terminated.</span></span>

 

</dd> <dt>

<span data-ttu-id="41b7d-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Образец</span><span class="sxs-lookup"><span data-stu-id="41b7d-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="41b7d-153">Раздел сигнатуры содержит тип и длину подписи, а также саму цифровую подпись.</span><span class="sxs-lookup"><span data-stu-id="41b7d-153">The signature section contains the signature type and length, and the digital signature itself.</span></span> <span data-ttu-id="41b7d-154">8-разрядный тип имеет значение 2, чтобы указать, что он использует SHA-1 с 1024-битным шифрованием RSA.</span><span class="sxs-lookup"><span data-stu-id="41b7d-154">The 8-bit type is set to 2 to indicate that it uses SHA-1 with 1024-bit RSA encryption.</span></span> <span data-ttu-id="41b7d-155">Длина представляет собой 16-разрядное значение, содержащее длину цифровой подписи в байтах.</span><span class="sxs-lookup"><span data-stu-id="41b7d-155">The length is a 16-bit value containing the length of the digital signature in bytes.</span></span> <span data-ttu-id="41b7d-156">Цифровая подпись рассчитывается для всех предыдущих разделов списка отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="41b7d-156">The digital signature is calculated over all prior sections of the CRL.</span></span>

<span data-ttu-id="41b7d-157">Подпись вычисляется с помощью схемы цифровых подписей РСАССА-PSS, которая определена в PKCS \# 1 (версия 2,1).</span><span class="sxs-lookup"><span data-stu-id="41b7d-157">The signature is calculated using the RSASSA-PSS digital signature scheme that is defined in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="41b7d-158">Хэш-функция — SHA – 1, которая определена в федеральном стандарте обработки информации (FIPS) 180-2, а функция формирования маски — ГЕНЕРАЦИИ маски MGF1, которая определена в разделе B. 2.1 в PKCS \# 1 (версия 2,1).</span><span class="sxs-lookup"><span data-stu-id="41b7d-158">The hash function is SHA-1, which is defined in Federal Information Processing Standard (FIPS) 180-2, and the mask generation function is MGF1, which is defined in section B.2.1 in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="41b7d-159">Операции RSASP1 и RSAVP1 используют RSA с 1024-битным остатком с экспонентой проверки 65537.</span><span class="sxs-lookup"><span data-stu-id="41b7d-159">The RSASP1 and RSAVP1 operations use RSA with a 1024-bit modulus with a verification exponent of 65537.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="41b7d-160">См. также</span><span class="sxs-lookup"><span data-stu-id="41b7d-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41b7d-161">Использование протокола сертифицированной выходной защиты (Копп)</span><span class="sxs-lookup"><span data-stu-id="41b7d-161">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



