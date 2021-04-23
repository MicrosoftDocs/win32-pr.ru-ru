---
title: Использование множественного взаимного исключения скорости
description: Использование множественного взаимного исключения скорости
ms.assetid: 69898b4d-fe10-422e-9ed2-87b65aa7bdb3
keywords:
- несколько битов (MBR), взаимное исключение
- MBR (Многоразрядная скорость), взаимное исключение
- взаимное исключение, Многоразрядная частота (MBR)
- профили, Многоразрядная скорость (MBR)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77c7615845d10d07982676dfdb4dc8c617cebe
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336260"
---
# <a name="using-multiple-bit-rate-mutual-exclusion"></a><span data-ttu-id="e5d7c-107">Использование множественного взаимного исключения скорости</span><span class="sxs-lookup"><span data-stu-id="e5d7c-107">Using Multiple Bit Rate Mutual Exclusion</span></span>

<span data-ttu-id="e5d7c-108">Взаимное исключение с несколькими битовыми частотами (MBR) полезно, если требуется кодировать содержимое для различных сценариев воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e5d7c-108">Multiple bit rate (MBR) mutual exclusion is useful when you want to encode content for a variety of playback scenarios.</span></span> <span data-ttu-id="e5d7c-109">Выходные данные MBR-видео состоят из одного входного кодирования несколько раз, каждый из которых имеет разные параметры битовой скорости.</span><span class="sxs-lookup"><span data-stu-id="e5d7c-109">An MBR video output consists of a single input encoded multiple times, each with different bit-rate settings.</span></span> <span data-ttu-id="e5d7c-110">При считывании файла с кодированием MBR средство чтения определит, какой поток использовать в зависимости от доступной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="e5d7c-110">When a file with MBR encoding is read, the reader will determine which stream to use based on the available bandwidth.</span></span>

<span data-ttu-id="e5d7c-111">Пакет SDK Windows Media Format поддерживает кодирование MBR как для видеопотоков, так и для звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="e5d7c-111">The Windows Media Format SDK supports MBR encoding for both video and audio streams.</span></span> <span data-ttu-id="e5d7c-112">Кроме того, можно создать специальный тип кодирования MBR, называемый форматом MBR для нескольких видеороликов.</span><span class="sxs-lookup"><span data-stu-id="e5d7c-112">In addition, you can create a special type of MBR encoding called multiple-video-size MBR encoding.</span></span> <span data-ttu-id="e5d7c-113">Видеороликы с несколькими видеороликами идентичны обычным видео MBR, за исключением того, что в взаимном исключении можно указать разные размеры изображения для потоков видео.</span><span class="sxs-lookup"><span data-stu-id="e5d7c-113">Multiple-video-size MBR video functions identically to normal MBR video except that you can specify different image sizes for the video streams in the mutual exclusion.</span></span>

<span data-ttu-id="e5d7c-114">В следующем примере показано, как настроить профиль для видео MBR с несколькими размерами видео.</span><span class="sxs-lookup"><span data-stu-id="e5d7c-114">The following example demonstrates how to set up a profile for MBR video with multiple video sizes.</span></span> <span data-ttu-id="e5d7c-115">Он создает новый профиль с тремя видеопотоками различной скорости и размерами и включает их в объект взаимного исключения.</span><span class="sxs-lookup"><span data-stu-id="e5d7c-115">It creates a new profile with three video streams of varying bit rates and sizes, and includes them in a mutual exclusion object.</span></span>


```C++
IWMProfileManager*  pProfileMgr = NULL;
IWMProfile*         pProfile    = NULL;
IWMMutualExclusion* pMutex      = NULL;
IWMStreamConfig*    pStream     = NULL;
IWMMediaProps*      pMediaProps = NULL;

WM_MEDIA_TYPE*      pMediaType  = NULL;
DWORD               cbMediaType = 0;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfile);

// Give the new profile a name and description.
hr = pProfile->SetName(L"MBR_Video_3_Stream_test");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// Get the media properties interface for the new stream.
hr = pStream->QueryInterface(IID_IWMMediaProps, (void**)&pMediaProps);

// Get the media-type structure.
// First, get the size of the media-type structure.
hr = pMediaProps->GetMediaType(NULL, &cbMediaType);

// Allocate memory for the structure based on the retrieved size.
pMediaType = (WM_MEDIA_TYPE*) new BYTE[cbMediaType];

// Retrieve the media-type structure.
hr = pMediaProps->GetMediaType(pMediaType, &cbMediaType);

// Change the video size to 640 x 480.
pMediaType->pbFormat->bmiHeader.biWidth  = 640;
pMediaType->pbFormat->bmiHeader.biHeight = 480;

// Replace the WM_MEDIA_TYPE in the profile with the one just changed.
hr = pMediaProps->SetMediaType(pMediaType);

// Release the media properties interface and delete the structure.
pMediaProps->Release();
pMediaProps = NULL;
delete[] pMediaType;
pMediaType = NULL;

// Set the bit rate to 200.
hr = pStream->SetBitrate(200000);

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// For the remaining two streams, leave the video at its default size of
// 320 x 240 <entity type="ndash"/>- just change the bit rates.

// Repeat for a 100K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(100000);
hr = pStream->SetStreamNumber(2);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Repeat for a 56K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(56000);
hr = pStream->SetStreamNumber(3);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Now that we have three streams, create a mutual exclusion object.
hr = pProfile->CreateNewMutualExclusion(&pMutex);

// Add the three streams to the mutual exclusion.
hr = pMutex->AddStream(1);
hr = pMutex->AddStream(2);
hr = pMutex->AddStream(3);

// Configure the mutual exclusion for MBR video.
hr = pMutex->SetType(CLSID_WMMUTEX_Bitrate);

// Add the mutual exclusion to the profile.
hr = pProfile->AddMutualExclusion(pMutex);

// Release the mutual exclusion object.
pMutex->Release();
pMutex = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a><span data-ttu-id="e5d7c-116">См. также</span><span class="sxs-lookup"><span data-stu-id="e5d7c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5d7c-117">**Интерфейс Ивммедиапропс**</span><span class="sxs-lookup"><span data-stu-id="e5d7c-117">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="e5d7c-118">**Интерфейс Ивммутуалексклусион**</span><span class="sxs-lookup"><span data-stu-id="e5d7c-118">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="e5d7c-119">**Интерфейс Ивмпрофиле**</span><span class="sxs-lookup"><span data-stu-id="e5d7c-119">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="e5d7c-120">**Интерфейс Ивмстреамконфиг**</span><span class="sxs-lookup"><span data-stu-id="e5d7c-120">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[<span data-ttu-id="e5d7c-121">**Использование взаимного исключения**</span><span class="sxs-lookup"><span data-stu-id="e5d7c-121">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="e5d7c-122">**\_тип мультимедиа \_ WM**</span><span class="sxs-lookup"><span data-stu-id="e5d7c-122">**WM\_MEDIA\_TYPE**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)
</dt> </dl>

 

 




