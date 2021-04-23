---
description: XAudio2 инициализируется для воспроизведения звука путем создания экземпляра механизма XAudio2 и создания основного голоса.
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: 'Руководство: инициализация XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a613c1ae2b7c3a7f0c55ab5349a0a605aaeb2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897718"
---
# <a name="how-to-initialize-xaudio2"></a><span data-ttu-id="a31f1-103">Руководство: инициализация XAudio2</span><span class="sxs-lookup"><span data-stu-id="a31f1-103">How to: Initialize XAudio2</span></span>

<span data-ttu-id="a31f1-104">XAudio2 инициализируется для воспроизведения звука путем создания экземпляра механизма XAudio2 и создания основного голоса.</span><span class="sxs-lookup"><span data-stu-id="a31f1-104">XAudio2 is initialized for audio playback by creating an instance of the XAudio2 engine, and creating a mastering voice.</span></span>

<span data-ttu-id="a31f1-105">**Инициализация XAudio2**</span><span class="sxs-lookup"><span data-stu-id="a31f1-105">**To initialize XAudio2**</span></span>

1.  <span data-ttu-id="a31f1-106">Убедитесь, что инициализирован COM.</span><span class="sxs-lookup"><span data-stu-id="a31f1-106">Make sure you have initialized COM.</span></span> <span data-ttu-id="a31f1-107">Для приложения Магазина Windows это выполняется как часть инициализации среда выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="a31f1-107">For a Windows Store app, this is done as part of initializing the Windows Runtime.</span></span> <span data-ttu-id="a31f1-108">В противном случае используйте [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="a31f1-108">Otherwise, use [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  <span data-ttu-id="a31f1-109">Используйте функцию [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) для создания экземпляра подсистемы XAudio2.</span><span class="sxs-lookup"><span data-stu-id="a31f1-109">Use the [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) function to create an instance of the XAudio2 engine.</span></span>

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="a31f1-110">Используйте метод [**креатемастерингвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) для создания основного голоса.</span><span class="sxs-lookup"><span data-stu-id="a31f1-110">Use the [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) method to create a mastering voice.</span></span>

    <span data-ttu-id="a31f1-111">Голоса в главном канале инкапсулирует звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="a31f1-111">The mastering voices encapsulates an audio device.</span></span> <span data-ttu-id="a31f1-112">Он является конечным местом для всех аудио, проходящих через аудио граф.</span><span class="sxs-lookup"><span data-stu-id="a31f1-112">It is the ultimate destination for all audio that passes through an audio graph.</span></span>

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="a31f1-113">Примечания для приложений Магазина Windows</span><span class="sxs-lookup"><span data-stu-id="a31f1-113">Notes for Windows Store apps</span></span>

<span data-ttu-id="a31f1-114">Рекомендуется использовать [Интеллектуальный указатель](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) для управления временем существования объектов XAUDIO2 в безопасном режиме исключения.</span><span class="sxs-lookup"><span data-stu-id="a31f1-114">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="a31f1-115">Для приложений Магазина Windows можно использовать шаблон смарт-указателя [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) из библиотеки шаблонов среда выполнения Windows C++ (WRL).</span><span class="sxs-lookup"><span data-stu-id="a31f1-115">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


```C++
Microsoft::WRL::ComPtr<IXAudio2> XAudio2;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &XAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    throw Platform::Exception::CreateException(hr);

IXAudio2MasteringVoice* pMasterVoice = nullptr;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
    return hr;
```



> [!Note]  
> <span data-ttu-id="a31f1-116">Перед освобождением объекта [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) убедитесь, что все дочерние объекты XAUDIO2 полностью освобождены.</span><span class="sxs-lookup"><span data-stu-id="a31f1-116">Ensure that all XAUDIO2 child objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a31f1-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a31f1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a31f1-118">XAudio2 начало работы</span><span class="sxs-lookup"><span data-stu-id="a31f1-118">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="a31f1-119">Руководство: загрузка файлов звуковых данных в XAudio2</span><span class="sxs-lookup"><span data-stu-id="a31f1-119">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="a31f1-120">Руководство: воспроизведение звука при помощи XAudio2</span><span class="sxs-lookup"><span data-stu-id="a31f1-120">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
