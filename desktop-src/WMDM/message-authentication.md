---
title: Проверка подлинности сообщений
description: Проверка подлинности сообщений
ms.assetid: 6cb49f6b-e303-4840-9343-9891e75e07a4
keywords:
- Диспетчер устройств Windows Media, проверка подлинности сообщений
- Диспетчер устройств, проверка подлинности сообщений
- Классические приложения, проверка подлинности сообщений
- поставщики услуг, проверка подлинности сообщений
- инструкции по программированию, проверка подлинности сообщений
- Проверка подлинности сообщений
- код проверки подлинности сообщения (MAC)
- MAC (код проверки подлинности сообщения)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14805e2074509e918902aae9eb9e9680ca52a6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691148"
---
# <a name="message-authentication"></a>Проверка подлинности сообщений

Проверка подлинности сообщений — это процесс, позволяющий приложениям и поставщикам служб проверять, что данные, передаваемые между ними, не были изменены. Диспетчер устройств Windows Media позволяет приложениям и поставщикам служб выполнять проверку подлинности сообщений с помощью кодов проверки подлинности сообщений (Mac). Вот как работает проверка подлинности MAC:

Отправитель данных, как правило, является поставщиком услуг, передает один или несколько фрагментов данных через одностороннюю криптографическую функцию, которая создает одну подпись (MAC) для всех данных. Затем отправитель отправляет все подписанные фрагменты данных вместе с компьютером MAC в приемник (обычно это приложение). Получатель передает данные с помощью одной и той же криптографической функции для создания компьютера MAC и сравнивает его с отправленным компьютером MAC. Если MAC соответствует, данные не изменялись.

Для выполнения проверки подлинности MAC поставщику приложения или службы требуется ключ шифрования и соответствующий сертификат. Сведения о том, где их можно получить, см. в разделе [средства для разработки](tools-for-development.md).

Следующие шаги описывают, как данные подписываются отправителем и затем проверяются получателем. В Windows Media диспетчер устройств поставщик услуг использует класс [ксекуречаннелсервер](csecurechannelserver-class.md) для создания компьютеров Макинтош, а приложение использует класс [ксекуречаннелклиент](csecurechannelclient-class.md) . Оба класса предоставляют одинаковые функции с одинаковыми параметрами, поэтому следующие шаги применяются к обоим классам.

Отправитель (обычно поставщик услуг):

1.  Получите данные для подписи.
2.  Создайте новый MAC-маркер, вызвав **маЦинит**.
3.  Добавьте фрагмент данных для подписи в обработчик, вызвав **макупдате**. Эта функция принимает ранее созданный маркер и фрагмент данных, которые должны быть подписаны.
4.  Повторите шаг 3 с каждым дополнительным фрагментом данных, который должен быть подписан. Не имеет значения, какие данные о заказах добавляются на компьютер MAC.
5.  Скопируйте MAC из обработчика в новый буфер байтов, вызвав **макфинал**. Эта функция принимает маркер MAC и выделенный буфер, а затем копирует MAC из этого обработчика в предоставленный буфер.

При выполнении проверки подлинности MAC важно, чтобы отправитель и получатель помещают одни и те же данные в MAC. Для методов приложения, предоставляющих MAC, обычно все параметры включаются в значение MAC (за исключением самого компьютера MAC). Например, рассмотрим метод **ивмдмоператион:: трансферобжектдата** :

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

В этом методе MAC будет включать *pData* и *пдвсизе*. Если не указать оба параметра, создаваемый MAC-адрес не будет соответствовать MAC-адресу, переданному в *абмак*. Поставщик услуг должен обязательно разместить все необходимые параметры в методе приложения в MAC-значение.

Следующий код C++ демонстрирует создание MAC в реализации [**имдспсторажеглобалс:: жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)поставщика услуг.


```C++
HRESULT CMyDevice::GetSerialNumber(
    PWMDMID pSerialNumber, 
    BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT hr;

    // g_pSecureChannelServer is a global CSecureChannelServer object
    // created earlier.

    // Standard check that the CSecureChannelServer was authenticated previously.
    if ( !(g_pSecureChannelServer->fIsAuthenticated()) )
    {
        return WMDM_E_NOTCERTIFIED;
    }

    // Call a helper function to get the device serial number.
    hr = UtilGetSerialNumber(m_wcsName, pSerialNumber, TRUE);
    if(hr == HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED))
    {
        hr = WMDM_E_NOTSUPPORTED;
    }

    if(hr == S_OK)
    {
        // Create the MAC handle.
        HMAC hMAC;
        hr = g_pSecureChannelServer->MACInit(&hMAC);
        if(FAILED(hr))
            return hr;

        // Add the serial number to the MAC.
        g_pSecureChannelServer->MACUpdate(hMAC, (BYTE*)(pSerialNumber), sizeof(WMDMID));
        if(FAILED(hr))
            return hr;

        // Get the created MAC value from the handle.
        g_pSecureChannelServer->MACFinal(hMAC, abMac);
        if(FAILED(hr))
            return hr;
    }

    return hr;
}
```



Получатель (как правило, приложение):

Если получатель не реализовал интерфейс [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) , он должен выполнить те же действия, что и отправитель, а затем сравнить два значения Mac. В следующем примере кода C++ показано, как приложение проверяет полученный MAC в вызове [**ивмдмсторажеглобалс:: жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) , чтобы гарантировать, что серийный номер не был изменен при передаче.


```C++
//
// Get and verify the serial number.
//
WMDMID serialNumber;
BYTE receivedMAC[WMDM_MAC_LENGTH];
hr = pIWMDMDevice->GetSerialNumber(&serialNumber, receivedMAC);

// Check the MAC to guarantee the serial number has not been tampered with.
if (hr == S_OK)
{
    // Initialize a MAC handle, 
    // add all parameters to the MAC,
    // and retrieve the calculated MAC value.
    // m_pSAC is a global CSecureChannelClient object created earlier.
    HMAC hMAC;
    BYTE calculatedMAC[WMDM_MAC_LENGTH];
    hr = m_pSAC->MACInit(&hMAC);
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACUpdate(hMAC, (BYTE*)(&serialNumber), sizeof(serialNumber));
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACFinal(hMAC, (BYTE*)calculatedMAC);
    if(FAILED(hr))
        return hr;

    // If the two MAC values match, the MAC is authentic. 
    if (memcmp(calculatedMAC, receivedMAC, sizeof(calculatedMAC)) == 0)
    {
        // The MAC is authentic; print the serial number.
        CHAR* serialNumberBuffer = 
            new CHAR[serialNumber.SerialNumberLength + 1];
        ZeroMemory(serialNumberBuffer, 
            (serialNumber.SerialNumberLength + 1) * sizeof(CHAR));
        memcpy(serialNumberBuffer, serialNumber.pID, 
            serialNumber.SerialNumberLength * sizeof(CHAR));
        // TODO: Display the serial number.
        delete serialNumberBuffer;
    }
    else
    {
        // TODO: Display a message indicating that the serial number MAC 
        // does not match.
    }
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование защищенных каналов с проверкой подлинности**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




