---
title: Определение состояния синхронизации списка воспроизведения
description: Определение состояния синхронизации списка воспроизведения
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
- Проигрыватель Windows Media, списки воспроизведения синхронизации
- Объектная модель проигрывателя Windows Media, списки воспроизведения синхронизации
- Объектная модель, списки воспроизведения синхронизации
- Проигрыватель Windows Media Mobile, списки воспроизведения синхронизации
- Элемент управления ActiveX проигрывателя Windows Media, списки воспроизведения синхронизации
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, списки синхронизации
- Элемент управления ActiveX, списки воспроизведения синхронизации
- списки воспроизведения, синхронизация
- списки воспроизведения метафайлов, синхронизация
- Списки воспроизведения метафайлов Windows Media, синхронизация
- переносные устройства, определение состояния списка воспроизведения синхронизации
- списки воспроизведения синхронизации, состояние синхронизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9758cfbb73c698a40d6d4f48e645e57750d8a332
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691434"
---
# <a name="determining-playlist-synchronization-state"></a><span data-ttu-id="d65b7-115">Определение состояния синхронизации списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="d65b7-115">Determining Playlist Synchronization State</span></span>

<span data-ttu-id="d65b7-116">Проигрыватель Windows Media 10 или более поздней версии использует атрибут **синкстате** , чтобы содержать сведения о том, скопирован ли конкретный файл мультимедиа на портативное устройство, а в случае сбоя копирование не удалось, так как на устройстве недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="d65b7-116">Windows Media Player 10 or later uses the **SyncState** attribute to contain information about whether a particular digital media file has been copied to a portable device and, in the case of a failure, whether copying failed because the device did not have enough memory.</span></span>

<span data-ttu-id="d65b7-117">В следующем примере кода создается функция, которая получает эти сведения из цифрового файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d65b7-117">The following example code creates a function that retrieves this information from a digital media file.</span></span> <span data-ttu-id="d65b7-118">Функция принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="d65b7-118">The function takes the following parameters:</span></span>

-   <span data-ttu-id="d65b7-119">*пмедиа*.</span><span class="sxs-lookup"><span data-stu-id="d65b7-119">*pMedia*.</span></span> <span data-ttu-id="d65b7-120">Указатель на интерфейс **ивмпмедиа** , представляющий файл цифрового мультимедиа для проверки.</span><span class="sxs-lookup"><span data-stu-id="d65b7-120">Pointer to an **IWMPMedia** interface that represents the digital media file to inspect.</span></span>
-   <span data-ttu-id="d65b7-121">*лпсиндекс*.</span><span class="sxs-lookup"><span data-stu-id="d65b7-121">*lPsIndex*.</span></span> <span data-ttu-id="d65b7-122">Индекс партнерства текущего устройства.</span><span class="sxs-lookup"><span data-stu-id="d65b7-122">Partnership index of the current device.</span></span>
-   <span data-ttu-id="d65b7-123">*пулондевице*.</span><span class="sxs-lookup"><span data-stu-id="d65b7-123">*pulOnDevice*.</span></span> <span data-ttu-id="d65b7-124">Указатель на **длинную** переменную, которая получает значение, указывающее, скопирован ли цифровой файл мультимедиа на устройство.</span><span class="sxs-lookup"><span data-stu-id="d65b7-124">Pointer to a **long** variable that receives the value indicating whether the digital media file has been copied to the device.</span></span>
-   <span data-ttu-id="d65b7-125">*пулдиднотфит*.</span><span class="sxs-lookup"><span data-stu-id="d65b7-125">*pulDidNotFit*.</span></span> <span data-ttu-id="d65b7-126">Указатель на **длинную** переменную, которая получает значение, указывающее, завершилась ли операция копирования неудачно из-за нехватки памяти на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d65b7-126">Pointer to a **long** variable that receives the value indicating whether the copy operation failed because the device did not have enough memory.</span></span>

<span data-ttu-id="d65b7-127">Сведения, содержащиеся в атрибуте **синкстате** , кодируются побитовым способом.</span><span class="sxs-lookup"><span data-stu-id="d65b7-127">The information contained in the **SyncState** attribute is encoded in a bitwise fashion.</span></span> <span data-ttu-id="d65b7-128">Вы можете увидеть, как эта функция используется в примере кода в разделе [перечисление элементов мультимедиа](enumerating-the-media-items.md).</span><span class="sxs-lookup"><span data-stu-id="d65b7-128">You can see how this function is used in the example code in [Enumerating the Media Items](enumerating-the-media-items.md).</span></span>


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d65b7-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d65b7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d65b7-130">**Интерфейс Ивмпмедиа**</span><span class="sxs-lookup"><span data-stu-id="d65b7-130">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="d65b7-131">**IWMPMedia3:: Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="d65b7-131">**IWMPMedia3::getItemInfoByType**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[<span data-ttu-id="d65b7-132">**Управление списками воспроизведения синхронизации**</span><span class="sxs-lookup"><span data-stu-id="d65b7-132">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="d65b7-133">**Атрибут Синкстате**</span><span class="sxs-lookup"><span data-stu-id="d65b7-133">**SyncState Attribute**</span></span>](syncstate-attribute.md)
</dt> </dl>

 

 




