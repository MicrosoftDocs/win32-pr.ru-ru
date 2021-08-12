---
title: Шифрование и расшифровка
description: Шифрование и расшифровка
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Windows Диспетчер устройств мультимедиа, шифрование
- Диспетчер устройств, шифрование
- Классические приложения, шифрование
- поставщики услуг, шифрование
- инструкции по программированию, шифрование
- шифрование
- Windows Диспетчер устройств мультимедиа, расшифровка
- Диспетчер устройств, расшифровка
- Настольные приложения, расшифровка
- поставщики услуг, расшифровка
- инструкции по программированию, расшифровка
- расшифровка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c154910709007e502c1505fc6fc3274665942c9eabe8e24de5b30fe932d813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584672"
---
# <a name="encryption-and-decryption"></a>Шифрование и расшифровка

Windows Диспетчер устройств мультимедиа требует шифрования файлов, передаваемых между поставщиком службы и приложением. Создать его можно двумя способами:

-   Если поставщик услуг поддерживает только [**имдспобжект:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) и [**Имдспобжект:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), данные должны быть зашифрованы и расшифрованы приложением и поставщиком служб с помощью методов [ксекуречаннелклиент](csecurechannelclient-class.md) и [ксекуречаннелсервер](csecurechannelserver-class.md) соответственно.
-   Если поставщик услуг поддерживает [**IMDSPObject2:: реадонклеарчаннел**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) и [**IMDSPObject2:: вритеонклеарчаннел**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), приложение может избежать дорогостоящей проверки подлинности сообщений безопасного канала. (Безопасный канал сохраняется таким образом, что устаревшие поставщики услуг, которые не реализуют [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) , могут продолжать функционировать.)

Требование шифрования не позволяет вредоносным приложениям получать данные, передаваемые между компонентами программного обеспечения, а также обеспечивает защиту целостности данных, отправляемых на устройство или с устройства.

Для следующих трех методов требуется шифрование или расшифровка.



| Метод                                                                          | Описание                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Ивмдмоператион:: Трансферобжектдата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | Приклад Шифрование или расшифровка в зависимости от того, отправляет ли приложение данные или получает их. |
| [**Имдспобжект:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | (Поставщик услуг) Ключ.                                                                             |
| [**Имдспобжект:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | (Поставщик услуг) Расшифровки.                                                                             |



 

Шифрование и расшифровка выполняются с помощью одного вызова метода. Шифрование выполняется с помощью [**ксекуречаннелклиент:: енкриптпарам**](/previous-versions/bb231587(v=vs.85)) for Applications или [**Ксекуречаннелсервер:: енкриптпарам**](/previous-versions/ms868509(v=msdn.10)) для поставщиков услуг. Расшифровка выполняется с помощью [**ксекуречаннелклиент::D екриптпарам**](/previous-versions/bb231586(v=vs.85)) для приложений или [**Ксекуречаннелсервер::D екриптпарам**](/previous-versions/bb231598(v=vs.85)) для поставщиков услуг. Параметры одинаковы для клиентских и серверных методов.

Ниже приведены инструкции по шифрованию и расшифровке данных. (Эти шаги важны, только если приложение взаимодействует с устаревшим поставщиком услуг, который не реализует [IWMDMOperation3:: трансферобжектдатаонклеарчаннел](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)

**Шифрование**

1.  Создайте ключ MAC для зашифрованных данных, как описано в разделе [Проверка подлинности сообщений](message-authentication.md).
2.  Вызовите **енкриптпарам** с данными для шифрования, чтобы выполнить шифрование на месте.

В следующем примере кода демонстрируется реализация [**имдспобжект:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)поставщиком услуг. Этот метод создает ключ MAC, используя данные для шифрования и размер данных, и отправляет их в приложение.


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



**Расшифровка**

1.  Вызовите **декриптпарам** с данными для шифрования, чтобы выполнить расшифровку на месте.
2.  Проверьте ключ MAC для расшифрованных данных, как описано в разделе [Проверка подлинности сообщений](message-authentication.md).

В следующем примере кода демонстрируется реализация [**имдспобжект:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)поставщика услуг. Этот метод создает ключ MAC, используя данные для шифрования и размер данных, и отправляет их в приложение.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Использование защищенных каналов с проверкой подлинности**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 