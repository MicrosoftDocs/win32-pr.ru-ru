---
title: Шифрование и расшифровка
description: Шифрование и расшифровка
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Диспетчер устройств Windows Media, шифрование
- Диспетчер устройств, шифрование
- Классические приложения, шифрование
- поставщики услуг, шифрование
- инструкции по программированию, шифрование
- шифрование
- Диспетчер устройств Windows Media, расшифровка
- Диспетчер устройств, расшифровка
- Настольные приложения, расшифровка
- поставщики услуг, расшифровка
- инструкции по программированию, расшифровка
- расшифровка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78688c1b4ca9991d8b322c6991de96a51e7e8d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413560"
---
# <a name="encryption-and-decryption"></a><span data-ttu-id="89ba5-115">Шифрование и расшифровка</span><span class="sxs-lookup"><span data-stu-id="89ba5-115">Encryption and Decryption</span></span>

<span data-ttu-id="89ba5-116">Диспетчер устройств Windows Media требует шифрования файлов, передаваемых между поставщиком службы и приложением.</span><span class="sxs-lookup"><span data-stu-id="89ba5-116">Windows Media Device Manager requires encryption of files sent between the service provider and the application.</span></span> <span data-ttu-id="89ba5-117">Создать его можно двумя способами:</span><span class="sxs-lookup"><span data-stu-id="89ba5-117">This can be done in one of two ways:</span></span>

-   <span data-ttu-id="89ba5-118">Если поставщик услуг поддерживает только [**имдспобжект:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) и [**Имдспобжект:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), данные должны быть зашифрованы и расшифрованы приложением и поставщиком служб с помощью методов [ксекуречаннелклиент](csecurechannelclient-class.md) и [ксекуречаннелсервер](csecurechannelserver-class.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="89ba5-118">If the service provider supports only [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) and [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), the data must be encrypted and decrypted by the application and service provider by using [CSecureChannelClient](csecurechannelclient-class.md) and [CSecureChannelServer](csecurechannelserver-class.md) methods respectively.</span></span>
-   <span data-ttu-id="89ba5-119">Если поставщик услуг поддерживает [**IMDSPObject2:: реадонклеарчаннел**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) и [**IMDSPObject2:: вритеонклеарчаннел**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), приложение может избежать дорогостоящей проверки подлинности сообщений безопасного канала.</span><span class="sxs-lookup"><span data-stu-id="89ba5-119">If the service provider supports [**IMDSPObject2::ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) and [**IMDSPObject2::WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), your application can avoid costly secure channel message authentication.</span></span> <span data-ttu-id="89ba5-120">(Безопасный канал сохраняется таким образом, что устаревшие поставщики услуг, которые не реализуют [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) , могут продолжать функционировать.)</span><span class="sxs-lookup"><span data-stu-id="89ba5-120">(The secure channel is retained so that legacy service providers that do not implement [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) can still continue to function.)</span></span>

<span data-ttu-id="89ba5-121">Требование шифрования не позволяет вредоносным приложениям получать данные, передаваемые между компонентами программного обеспечения, а также обеспечивает защиту целостности данных, отправляемых на устройство или с устройства.</span><span class="sxs-lookup"><span data-stu-id="89ba5-121">The encryption requirement prevents malicious applications from obtaining data that is being passed between software components, and also protects the integrity of data being sent to or from the device.</span></span>

<span data-ttu-id="89ba5-122">Для следующих трех методов требуется шифрование или расшифровка.</span><span class="sxs-lookup"><span data-stu-id="89ba5-122">The following three methods require encryption or decryption.</span></span>



| <span data-ttu-id="89ba5-123">Метод</span><span class="sxs-lookup"><span data-stu-id="89ba5-123">Method</span></span>                                                                          | <span data-ttu-id="89ba5-124">Описание</span><span class="sxs-lookup"><span data-stu-id="89ba5-124">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89ba5-125">**Ивмдмоператион:: Трансферобжектдата**</span><span class="sxs-lookup"><span data-stu-id="89ba5-125">**IWMDMOperation::TransferObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | <span data-ttu-id="89ba5-126">Приклад Шифрование или расшифровка в зависимости от того, отправляет ли приложение данные или получает их.</span><span class="sxs-lookup"><span data-stu-id="89ba5-126">(Application) Encryption or decryption, depending on whether the application is sending or receiving data.</span></span> |
| [<span data-ttu-id="89ba5-127">**Имдспобжект:: Read**</span><span class="sxs-lookup"><span data-stu-id="89ba5-127">**IMDSPObject::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | <span data-ttu-id="89ba5-128">(Поставщик услуг) Ключ.</span><span class="sxs-lookup"><span data-stu-id="89ba5-128">(Service provider) Encryption.</span></span>                                                                             |
| [<span data-ttu-id="89ba5-129">**Имдспобжект:: Write**</span><span class="sxs-lookup"><span data-stu-id="89ba5-129">**IMDSPObject::Write**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | <span data-ttu-id="89ba5-130">(Поставщик услуг) Расшифровки.</span><span class="sxs-lookup"><span data-stu-id="89ba5-130">(Service Provider) Decryption.</span></span>                                                                             |



 

<span data-ttu-id="89ba5-131">Шифрование и расшифровка выполняются с помощью одного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="89ba5-131">Encryption and decryption are both done by single method calls.</span></span> <span data-ttu-id="89ba5-132">Шифрование выполняется с помощью [**ксекуречаннелклиент:: енкриптпарам**](/previous-versions/bb231587(v=vs.85)) for Applications или [**Ксекуречаннелсервер:: енкриптпарам**](/previous-versions/ms868509(v=msdn.10)) для поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="89ba5-132">Encryption is done by [**CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)) for applications or by [**CSecureChannelServer::EncryptParam**](/previous-versions/ms868509(v=msdn.10)) for service providers.</span></span> <span data-ttu-id="89ba5-133">Расшифровка выполняется с помощью [**ксекуречаннелклиент::D екриптпарам**](/previous-versions/bb231586(v=vs.85)) для приложений или [**Ксекуречаннелсервер::D екриптпарам**](/previous-versions/bb231598(v=vs.85)) для поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="89ba5-133">Decryption is done by [**CSecureChannelClient::DecryptParam**](/previous-versions/bb231586(v=vs.85)) for applications or [**CSecureChannelServer::DecryptParam**](/previous-versions/bb231598(v=vs.85)) for service providers.</span></span> <span data-ttu-id="89ba5-134">Параметры одинаковы для клиентских и серверных методов.</span><span class="sxs-lookup"><span data-stu-id="89ba5-134">The parameters are identical between the client and server methods.</span></span>

<span data-ttu-id="89ba5-135">Ниже приведены инструкции по шифрованию и расшифровке данных.</span><span class="sxs-lookup"><span data-stu-id="89ba5-135">The following steps show how to encrypt and decrypt data.</span></span> <span data-ttu-id="89ba5-136">(Эти шаги важны, только если приложение взаимодействует с устаревшим поставщиком услуг, который не реализует [IWMDMOperation3:: трансферобжектдатаонклеарчаннел](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)</span><span class="sxs-lookup"><span data-stu-id="89ba5-136">(These steps are important only if your application communicates with a legacy service provider that does not implement [IWMDMOperation3::TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)</span></span>

<span data-ttu-id="89ba5-137">**Шифрование**</span><span class="sxs-lookup"><span data-stu-id="89ba5-137">**Encryption**</span></span>

1.  <span data-ttu-id="89ba5-138">Создайте ключ MAC для зашифрованных данных, как описано в разделе [Проверка подлинности сообщений](message-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="89ba5-138">Create the MAC key for the encrypted data, as described in [Message Authentication](message-authentication.md).</span></span>
2.  <span data-ttu-id="89ba5-139">Вызовите **енкриптпарам** с данными для шифрования, чтобы выполнить шифрование на месте.</span><span class="sxs-lookup"><span data-stu-id="89ba5-139">Call **EncryptParam** with the data to encrypt, to perform in-place encryption.</span></span>

<span data-ttu-id="89ba5-140">В следующем примере кода демонстрируется реализация [**имдспобжект:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="89ba5-140">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read).</span></span> <span data-ttu-id="89ba5-141">Этот метод создает ключ MAC, используя данные для шифрования и размер данных, и отправляет их в приложение.</span><span class="sxs-lookup"><span data-stu-id="89ba5-141">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Read(
    BYTE  *pData,
    DWORD *pdwSize,
    BYTE   abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwToRead;         // Bytes to read.
    DWORD    dwRead   = NULL;  // Bytes read.
    BYTE    *pTmpData = NULL;  // Temporary buffer to hold data before 
                               // it is copied to pData.

    // Use a global CSecureChannelServer member to verify that 
    // the client is authenticated.
    if (!(g_pAppSCServer->fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    

    // Verify that the handle to the file to read is valid.
    if(m_hFile == INVALID_HANDLE_VALUE)
    {
        return E_FAIL;
    }

    // Create a buffer to hold the data read.    
    dwToRead = *pdwSize;
    pTmpData = new BYTE [dwToRead] ;
    if(!pTmpData)
        return E_OUTOFMEMORY;

    // Read data into the temporary buffer.
    if(ReadFile(m_hFile,(LPVOID)pTmpData,dwToRead,&dwRead,NULL)) 
    { 
        *pdwSize = dwRead; 

        if( dwRead )
        {
            // Create a MAC from all the parameters.
            // CORg is a macro that goes to Error label on failure.
            // MAC consists of data and size of data.
            HMAC hMAC;
            
            CORg(g_pAppSCServer->MACInit(&hMAC));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD)));
            CORg(g_pAppSCServer->MACFinal(hMAC, abMac));
            
            // Encrypt the data.
            CORg(g_pAppSCServer->EncryptParam(pTmpData, dwRead));
            
            // Copy data from the temporary buffer into the out parameter.
            memcpy(pData, pTmpData, dwRead);
        }
    
        hr = S_OK; 
    }
    else
    { 
        *pdwSize = 0; 

        hr = E_FAIL; 
    }

Error:

    if(pTmpData) 
    {
        delete [] pTmpData;
    }

    return hr;
} 
```



<span data-ttu-id="89ba5-142">**Расшифровка**</span><span class="sxs-lookup"><span data-stu-id="89ba5-142">**Decryption**</span></span>

1.  <span data-ttu-id="89ba5-143">Вызовите **декриптпарам** с данными для шифрования, чтобы выполнить расшифровку на месте.</span><span class="sxs-lookup"><span data-stu-id="89ba5-143">Call **DecryptParam** with the data to encrypt, to perform in-place decryption.</span></span>
2.  <span data-ttu-id="89ba5-144">Проверьте ключ MAC для расшифрованных данных, как описано в разделе [Проверка подлинности сообщений](message-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="89ba5-144">Verify the MAC key for the decrypted data, as described in [Message Authentication](message-authentication.md).</span></span>

<span data-ttu-id="89ba5-145">В следующем примере кода демонстрируется реализация [**имдспобжект:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="89ba5-145">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write).</span></span> <span data-ttu-id="89ba5-146">Этот метод создает ключ MAC, используя данные для шифрования и размер данных, и отправляет их в приложение.</span><span class="sxs-lookup"><span data-stu-id="89ba5-146">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Write(BYTE *pData, DWORD *pdwSize,
                                 BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwWritten = 0;
    BYTE    *pTmpData  = NULL;          // Temporary buffer to hold the 
                                        // data during decryption.
    BYTE     pTempMac[WMDM_MAC_LENGTH]; // Temporary MAC that will be 
                                        // copied into the abMac
                                        // out parameter.

    if( m_hFile == INVALID_HANDLE_VALUE )
    {
        return E_FAIL;
    }

    // Allocate the temporary buffer and copy the encrypted data into it.
    pTmpData = new BYTE [*pdwSize];
    if(!pTmpData)
        return E_OUTOFMEMORY;
    memcpy(pTmpData, pData, *pdwSize);

    // Decrypt the data.
    CHRg(g_pAppSCServer->DecryptParam(pTmpData, *pdwSize));

    // Check the MAC passed to the method. The MAC is built from
    // the data and data size parameters.
    // CORg is a macro that goes to the Error label on failure.
    HMAC hMAC;
    CORg(g_pAppSCServer->MACInit(&hMAC));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), *pdwSize));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(*pdwSize)));
    CORg(g_pAppSCServer->MACFinal(hMAC, pTempMac));

    // If the MAC values don't match, return an error.
    if (memcmp(abMac, pTempMac, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto Error;
    }

    // The MAC values matched, so write the decrypted data to a local file.
    if( WriteFile(m_hFile,pTmpData,*pdwSize,&dwWritten,NULL) ) 
    {
        hr = S_OK;
    }
    else 
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    *pdwSize = dwWritten;

Error:

    if( pTmpData )
    {
        delete [] pTmpData;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="89ba5-147">См. также</span><span class="sxs-lookup"><span data-stu-id="89ba5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89ba5-148">**Использование защищенных каналов с проверкой подлинности**</span><span class="sxs-lookup"><span data-stu-id="89ba5-148">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 