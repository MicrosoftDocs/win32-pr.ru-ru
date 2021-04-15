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
# <a name="certificate-revocation-lists"></a>списки отзыва сертификатов.

В этом разделе описывается, как проверить список отзыва сертификатов (CRL) для отозванных драйверов при использовании протокола сертифицированной выходной защиты (Копп).

Список отзыва сертификатов содержит дайджесты отозванных сертификатов и может предоставляться и подписываться только корпорацией Майкрософт. Список отзыва сертификатов распространяется по лицензиям управления цифровыми правами (DRM). Список отзыва сертификатов может отозвать любой сертификат в цепочке сертификатов драйвера. Если какой-либо сертификат в цепочке отозван, то этот сертификат и все сертификаты, приведенные ниже в цепочке, также будут отозваны.

Чтобы получить список отзыва сертификатов, приложение должно использовать пакет SDK Windows Media Format, версии 9 или более поздней, и выполнить следующие действия.

1.  Вызовите **вмкреатереадер** , чтобы создать объект средства чтения пакета SDK для формата Windows Media.
2.  Запросите объект модуля чтения для интерфейса **ивмдрмреадер** .
3.  Вызовите **ивмдрмреадер:: жетдрмпроперти** со значением g \_ всзвмдрмнет \_ отзыва, чтобы получить список отзыва сертификатов. Этот метод необходимо вызывать дважды: один раз, чтобы получить размер буфера для выделения, и один раз для заполнения буфера. Второй вызов возвращает строку, содержащую список отзыва сертификатов. Вся строка имеет кодировку Base-64.
4.  Декодирование строки в кодировке Base-64. Для этого можно использовать функцию **криптстрингтобинари** . Эта функция является частью CryptoAPI.

> [!Note]  
> Чтобы использовать интерфейс **ивмдрмреадер** , необходимо получить СТАТИЧЕСКУЮ библиотеку DRM от корпорации Майкрософт и связать приложение с этим файлом библиотеки. Дополнительные сведения см. в разделе «получение требуемой библиотеки DRM» в документации по пакету SDK для Windows Media Format.

 

Если список отзыва сертификатов отсутствует на компьютере пользователя, метод **жетдрмпроперти** ВОЗВРАЩАЕТ \_ \_ \_ неподдерживаемое свойство NS E DRM \_ . В настоящее время единственным способом получения списка отзыва сертификатов является получение лицензии DRM.

В следующем коде показана функция, возвращающая список отзыва сертификатов:


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



Затем приложение должно проверить допустимость списка отзыва сертификатов. Для этого убедитесь, что сертификат списка отзыва сертификатов, который является частью списка отзыва сертификатов, непосредственно подписан корневым сертификатом Майкрософт и имеет значение элемента Сигнкрл, установленное в 1. Кроме того, проверьте подпись списка отзыва сертификатов.

После проверки списка отзыва сертификатов приложение может его сохранить. Номер версии списка отзыва сертификатов также должен быть проверен перед сохранением, чтобы приложение всегда сохраняло последнюю версию.

Список отзыва сертификатов имеет следующий формат.



| Section            | Содержимое                                                             |
|--------------------|----------------------------------------------------------------------|
| Header             | 32-разрядный список CRL version32-разрядное число записей                           |
| Записи отзыва | Несколько 160-битных записей отзыва                                  |
| Certificate        | 32-разрядный сертификат Ленгсвариабле-length                 |
| Подпись          | 8-разрядная сигнатура type16-bit сигнатура Ленгсвариабле-length |



 

> [!Note]  
> Все целочисленные значения не подписаны и представлены в нотации с обратным порядком байтов (сетевой порядок байт).

 

Описания разделов списка отзыва сертификатов

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Заголовок
</dt> <dd>

Заголовок содержит номер версии списка отзыва сертификатов и число записей отзыва в списке отзыва сертификатов. Список отзыва сертификатов может содержать ноль или более записей.

</dd> <dt>

<span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Записи отзыва
</dt> <dd>

Каждая запись отзыва — это 160-разрядный дайджест отозванного сертификата. Сравните этот дайджест с элементом Дижествалуе в сертификате.

</dd> <dt>

<span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificate
</dt> <dd>

Раздел сертификата содержит 32-разрядное значение, указывающее длину (в байтах) XML-сертификата и цепочки сертификатов, а также массив байтов, который содержит как сертификат XML центра сертификации, так и цепочку сертификатов, в которой в качестве корня установлен Майкрософт. Сертификат должен быть подписан центром сертификации, имеющим право выдавать списки отзыва сертификатов.

> [!Note]  
> Сертификат не должен завершаться нулем.

 

</dd> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Образец
</dt> <dd>

Раздел сигнатуры содержит тип и длину подписи, а также саму цифровую подпись. 8-разрядный тип имеет значение 2, чтобы указать, что он использует SHA-1 с 1024-битным шифрованием RSA. Длина представляет собой 16-разрядное значение, содержащее длину цифровой подписи в байтах. Цифровая подпись рассчитывается для всех предыдущих разделов списка отзыва сертификатов.

Подпись вычисляется с помощью схемы цифровых подписей РСАССА-PSS, которая определена в PKCS \# 1 (версия 2,1). Хэш-функция — SHA – 1, которая определена в федеральном стандарте обработки информации (FIPS) 180-2, а функция формирования маски — ГЕНЕРАЦИИ маски MGF1, которая определена в разделе B. 2.1 в PKCS \# 1 (версия 2,1). Операции RSASP1 и RSAVP1 используют RSA с 1024-битным остатком с экспонентой проверки 65537.

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование протокола сертифицированной выходной защиты (Копп)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



