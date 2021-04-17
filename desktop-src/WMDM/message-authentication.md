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
# <a name="message-authentication"></a><span data-ttu-id="5e534-111">Проверка подлинности сообщений</span><span class="sxs-lookup"><span data-stu-id="5e534-111">Message Authentication</span></span>

<span data-ttu-id="5e534-112">Проверка подлинности сообщений — это процесс, позволяющий приложениям и поставщикам служб проверять, что данные, передаваемые между ними, не были изменены.</span><span class="sxs-lookup"><span data-stu-id="5e534-112">Message authentication is a process that enables applications and service providers to verify that data passed between them has not been tampered with.</span></span> <span data-ttu-id="5e534-113">Диспетчер устройств Windows Media позволяет приложениям и поставщикам служб выполнять проверку подлинности сообщений с помощью кодов проверки подлинности сообщений (Mac).</span><span class="sxs-lookup"><span data-stu-id="5e534-113">Windows Media Device Manager allows applications and service providers to perform message authentication by using message authentication codes (MACs).</span></span> <span data-ttu-id="5e534-114">Вот как работает проверка подлинности MAC:</span><span class="sxs-lookup"><span data-stu-id="5e534-114">Here is how MAC authentication works:</span></span>

<span data-ttu-id="5e534-115">Отправитель данных, как правило, является поставщиком услуг, передает один или несколько фрагментов данных через одностороннюю криптографическую функцию, которая создает одну подпись (MAC) для всех данных.</span><span class="sxs-lookup"><span data-stu-id="5e534-115">The data sender, usually the service provider, passes one or more pieces of data through a one-way cryptographic function that produces a single signature, the MAC, for all the data.</span></span> <span data-ttu-id="5e534-116">Затем отправитель отправляет все подписанные фрагменты данных вместе с компьютером MAC в приемник (обычно это приложение).</span><span class="sxs-lookup"><span data-stu-id="5e534-116">The sender then sends all the signed pieces of data together with the MAC to the receiver (usually the application).</span></span> <span data-ttu-id="5e534-117">Получатель передает данные с помощью одной и той же криптографической функции для создания компьютера MAC и сравнивает его с отправленным компьютером MAC.</span><span class="sxs-lookup"><span data-stu-id="5e534-117">The receiver passes the data through the same cryptographic function to generate a MAC and compares it to the MAC that was sent.</span></span> <span data-ttu-id="5e534-118">Если MAC соответствует, данные не изменялись.</span><span class="sxs-lookup"><span data-stu-id="5e534-118">If the MAC matches, the data has not been modified.</span></span>

<span data-ttu-id="5e534-119">Для выполнения проверки подлинности MAC поставщику приложения или службы требуется ключ шифрования и соответствующий сертификат.</span><span class="sxs-lookup"><span data-stu-id="5e534-119">To perform MAC authentication, the application or service provider requires an encryption key and a matching certificate.</span></span> <span data-ttu-id="5e534-120">Сведения о том, где их можно получить, см. в разделе [средства для разработки](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="5e534-120">For information on where to get these, see [Tools for Development](tools-for-development.md).</span></span>

<span data-ttu-id="5e534-121">Следующие шаги описывают, как данные подписываются отправителем и затем проверяются получателем.</span><span class="sxs-lookup"><span data-stu-id="5e534-121">The following steps describe how data is signed by the sender, and later checked by the receiver.</span></span> <span data-ttu-id="5e534-122">В Windows Media диспетчер устройств поставщик услуг использует класс [ксекуречаннелсервер](csecurechannelserver-class.md) для создания компьютеров Макинтош, а приложение использует класс [ксекуречаннелклиент](csecurechannelclient-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5e534-122">In Windows Media Device Manager, the service provider uses the [CSecureChannelServer](csecurechannelserver-class.md) class to generate MACs, and the application uses the [CSecureChannelClient](csecurechannelclient-class.md) class.</span></span> <span data-ttu-id="5e534-123">Оба класса предоставляют одинаковые функции с одинаковыми параметрами, поэтому следующие шаги применяются к обоим классам.</span><span class="sxs-lookup"><span data-stu-id="5e534-123">Both classes provide identical functions with identical parameters, so the following steps apply to both classes.</span></span>

<span data-ttu-id="5e534-124">Отправитель (обычно поставщик услуг):</span><span class="sxs-lookup"><span data-stu-id="5e534-124">The sender (typically the service provider):</span></span>

1.  <span data-ttu-id="5e534-125">Получите данные для подписи.</span><span class="sxs-lookup"><span data-stu-id="5e534-125">Get the data to be signed.</span></span>
2.  <span data-ttu-id="5e534-126">Создайте новый MAC-маркер, вызвав **маЦинит**.</span><span class="sxs-lookup"><span data-stu-id="5e534-126">Create a new MAC handle by calling **MACInit**.</span></span>
3.  <span data-ttu-id="5e534-127">Добавьте фрагмент данных для подписи в обработчик, вызвав **макупдате**.</span><span class="sxs-lookup"><span data-stu-id="5e534-127">Add a piece of data to be signed to the handle by calling **MACUpdate**.</span></span> <span data-ttu-id="5e534-128">Эта функция принимает ранее созданный маркер и фрагмент данных, которые должны быть подписаны.</span><span class="sxs-lookup"><span data-stu-id="5e534-128">This function accepts the previously created handle, plus a piece of data that must be signed.</span></span>
4.  <span data-ttu-id="5e534-129">Повторите шаг 3 с каждым дополнительным фрагментом данных, который должен быть подписан.</span><span class="sxs-lookup"><span data-stu-id="5e534-129">Repeat step 3 with each additional piece of data that must be signed.</span></span> <span data-ttu-id="5e534-130">Не имеет значения, какие данные о заказах добавляются на компьютер MAC.</span><span class="sxs-lookup"><span data-stu-id="5e534-130">It does not matter in what order data is added to the MAC.</span></span>
5.  <span data-ttu-id="5e534-131">Скопируйте MAC из обработчика в новый буфер байтов, вызвав **макфинал**.</span><span class="sxs-lookup"><span data-stu-id="5e534-131">Copy the MAC from the handle to a new byte buffer by calling **MACFinal**.</span></span> <span data-ttu-id="5e534-132">Эта функция принимает маркер MAC и выделенный буфер, а затем копирует MAC из этого обработчика в предоставленный буфер.</span><span class="sxs-lookup"><span data-stu-id="5e534-132">This function accepts the MAC handle and a buffer that you allocate, and copies the MAC from the handle into the provided buffer.</span></span>

<span data-ttu-id="5e534-133">При выполнении проверки подлинности MAC важно, чтобы отправитель и получатель помещают одни и те же данные в MAC.</span><span class="sxs-lookup"><span data-stu-id="5e534-133">When performing MAC authentication, it is important that both the sender and the receiver are putting the same data into the MAC.</span></span> <span data-ttu-id="5e534-134">Для методов приложения, предоставляющих MAC, обычно все параметры включаются в значение MAC (за исключением самого компьютера MAC).</span><span class="sxs-lookup"><span data-stu-id="5e534-134">For the application methods that provide a MAC, typically all parameters are included in the MAC value (except for the MAC itself, of course).</span></span> <span data-ttu-id="5e534-135">Например, рассмотрим метод **ивмдмоператион:: трансферобжектдата** :</span><span class="sxs-lookup"><span data-stu-id="5e534-135">For example, consider the **IWMDMOperation::TransferObjectData** method:</span></span>

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

<span data-ttu-id="5e534-136">В этом методе MAC будет включать *pData* и *пдвсизе*.</span><span class="sxs-lookup"><span data-stu-id="5e534-136">In this method, the MAC would include *pData* and *pdwSize*.</span></span> <span data-ttu-id="5e534-137">Если не указать оба параметра, создаваемый MAC-адрес не будет соответствовать MAC-адресу, переданному в *абмак*.</span><span class="sxs-lookup"><span data-stu-id="5e534-137">If you do not include both the parameters, the MAC you create will not match the MAC passed to *abMac*.</span></span> <span data-ttu-id="5e534-138">Поставщик услуг должен обязательно разместить все необходимые параметры в методе приложения в MAC-значение.</span><span class="sxs-lookup"><span data-stu-id="5e534-138">A service provider must be sure to put all the required parameters in the application method into the MAC value.</span></span>

<span data-ttu-id="5e534-139">Следующий код C++ демонстрирует создание MAC в реализации [**имдспсторажеглобалс:: жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="5e534-139">The following C++ code demonstrates creating a MAC in a service provider's implementation of [**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span></span>


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



<span data-ttu-id="5e534-140">Получатель (как правило, приложение):</span><span class="sxs-lookup"><span data-stu-id="5e534-140">The receiver (typically the application):</span></span>

<span data-ttu-id="5e534-141">Если получатель не реализовал интерфейс [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) , он должен выполнить те же действия, что и отправитель, а затем сравнить два значения Mac.</span><span class="sxs-lookup"><span data-stu-id="5e534-141">If the receiver has not implemented the [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) interface, it should perform the same steps as the sender, and then compare the two MAC values.</span></span> <span data-ttu-id="5e534-142">В следующем примере кода C++ показано, как приложение проверяет полученный MAC в вызове [**ивмдмсторажеглобалс:: жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) , чтобы гарантировать, что серийный номер не был изменен при передаче.</span><span class="sxs-lookup"><span data-stu-id="5e534-142">The following C++ code example shows how an application would check the MAC received in a call to [**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) to ensure that the serial number was not tampered with in transit.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5e534-143">См. также</span><span class="sxs-lookup"><span data-stu-id="5e534-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e534-144">**Использование защищенных каналов с проверкой подлинности**</span><span class="sxs-lookup"><span data-stu-id="5e534-144">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




