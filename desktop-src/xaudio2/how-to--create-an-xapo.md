---
description: API КСАПО предоставляет интерфейс ИКСАПО и класс Кксапобасе для создания новых типов КСАПО.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: 'Руководство: создание XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549739462a0e76cbb437f0aa1403b099f72f5224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272824"
---
# <a name="how-to-create-an-xapo"></a><span data-ttu-id="2b405-103">Руководство: создание XAPO</span><span class="sxs-lookup"><span data-stu-id="2b405-103">How to: Create an XAPO</span></span>

<span data-ttu-id="2b405-104">API КСАПО предоставляет интерфейс [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo) и класс [**кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) для создания новых типов ксапо.</span><span class="sxs-lookup"><span data-stu-id="2b405-104">The XAPO API provides the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface and the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class for building new XAPO types.</span></span> <span data-ttu-id="2b405-105">Интерфейс **иксапо** содержит все методы, которые должны быть реализованы для создания нового ксапо.</span><span class="sxs-lookup"><span data-stu-id="2b405-105">The **IXAPO** interface contains all of the methods that need to be implemented to create a new XAPO.</span></span> <span data-ttu-id="2b405-106">Класс **кксапобасе** предоставляет базовую реализацию интерфейса **иксапо** .</span><span class="sxs-lookup"><span data-stu-id="2b405-106">The **CXAPOBase** class provides a basic implementation of the **IXAPO** interface.</span></span> <span data-ttu-id="2b405-107">**Кксапобасе** реализует все методы интерфейса **иксапо** , за исключением метода [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , который уникален для каждого ксапо.</span><span class="sxs-lookup"><span data-stu-id="2b405-107">**CXAPOBase** implements all of the **IXAPO** interface methods except the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, which is unique to each XAPO.</span></span>

## <a name="to-create-a-new-static-xapo"></a><span data-ttu-id="2b405-108">Создание нового статического КСАПО</span><span class="sxs-lookup"><span data-stu-id="2b405-108">To create a new static XAPO</span></span>

1.  <span data-ttu-id="2b405-109">Создайте новый класс КСАПО из базового класса [**кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .</span><span class="sxs-lookup"><span data-stu-id="2b405-109">Derive a new XAPO class from the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) base class.</span></span>

    > [!Note]  
    > <span data-ttu-id="2b405-110">Ксапос реализуют интерфейс **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="2b405-110">XAPOs implement the **IUnknown** interface.</span></span> <span data-ttu-id="2b405-111">Интерфейсы [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo) и [**иксапопараметерс**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) включают в себя три метода **IUnknown** : **QueryInterface**, **AddRef** и **Release**.</span><span class="sxs-lookup"><span data-stu-id="2b405-111">The [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) and [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interfaces include the three **IUnknown** methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="2b405-112">[**Кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) предоставляет реализации всех трех методов **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="2b405-112">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) provides implementations of all three of the **IUnknown** methods.</span></span> <span data-ttu-id="2b405-113">Новый экземпляр **кксапобасе** будет иметь счетчик ссылок, равный 1.</span><span class="sxs-lookup"><span data-stu-id="2b405-113">A new instance of **CXAPOBase** will have a reference count of 1.</span></span> <span data-ttu-id="2b405-114">Он будет уничтожен, когда счетчик ссылок станет равным 0.</span><span class="sxs-lookup"><span data-stu-id="2b405-114">It will be destroyed when its reference count becomes 0.</span></span> <span data-ttu-id="2b405-115">Чтобы разрешить XAudio2 уничтожить экземпляр КСАПО, когда он больше не нужен, вызовите метод **IUnknown:: Release** для ксапо после добавления в цепочку эффектов XAudio2.</span><span class="sxs-lookup"><span data-stu-id="2b405-115">To allow XAudio2 to destroy an instance of an XAPO when it is no longer needed, call **IUnknown::Release** on the XAPO after it is added to an XAudio2 effect chain.</span></span> <span data-ttu-id="2b405-116">См. [инструкции по использованию ксапо в XAudio2](how-to--use-an-xapo-in-xaudio2.md) для получения дополнительных сведений об использовании Ксапо с XAudio2.</span><span class="sxs-lookup"><span data-stu-id="2b405-116">See [How to: Use an XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md) for more information about using an XAPO with XAudio2.</span></span>

     

2.  <span data-ttu-id="2b405-117">Переопределите реализацию класса [**кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) метода [**Иксапо:: локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .</span><span class="sxs-lookup"><span data-stu-id="2b405-117">Override the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class implementation of the [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) method.</span></span>

    <span data-ttu-id="2b405-118">Переопределение [**локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) позволяет сохранять данные о формате звуковых данных для использования в [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span><span class="sxs-lookup"><span data-stu-id="2b405-118">Overriding [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) allows information about the format of audio data to be stored for use in [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

3.  <span data-ttu-id="2b405-119">Реализуйте метод [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) .</span><span class="sxs-lookup"><span data-stu-id="2b405-119">Implement the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method.</span></span>

    <span data-ttu-id="2b405-120">XAudio2 вызывает метод [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) каждый раз, когда ксапо требуется обработка звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="2b405-120">XAudio2 calls the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method whenever an XAPO needs to process audio data.</span></span> <span data-ttu-id="2b405-121">**Процесс** содержит основную часть кода для ксапо.</span><span class="sxs-lookup"><span data-stu-id="2b405-121">**Process** contains the bulk of the code for an XAPO.</span></span>

## <a name="implementing-the-process-method"></a><span data-ttu-id="2b405-122">Реализация метода Process</span><span class="sxs-lookup"><span data-stu-id="2b405-122">Implementing the Process Method</span></span>

<span data-ttu-id="2b405-123">Метод [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) принимает буферы потоков для входных и выходных звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="2b405-123">The [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method accepts stream buffers for input and output audio data.</span></span> <span data-ttu-id="2b405-124">Типичный КСАПО предложит один буфер входного потока и один буфер потока вывода.</span><span class="sxs-lookup"><span data-stu-id="2b405-124">A typical XAPO will expect one input stream buffer and one output stream buffer.</span></span> <span data-ttu-id="2b405-125">Необходимо основывать обработку данных из буфера входного потока в формате, указанном в функции [**локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) , и всех флагах, переданных в функцию **Process** с помощью буфера входного потока.</span><span class="sxs-lookup"><span data-stu-id="2b405-125">You should base the processing of data from the input stream buffer on the format specified in the [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) function and any flags passed to the **Process** function with the input stream buffer.</span></span> <span data-ttu-id="2b405-126">Скопируйте обработанные данные буфера входного потока в буфер потока вывода.</span><span class="sxs-lookup"><span data-stu-id="2b405-126">Copy the processed input stream buffer data to the output stream buffer.</span></span> <span data-ttu-id="2b405-127">Задайте параметр Буфферфлагс буфера выходного потока как [**\_ \_ допустимый буфер ксапо**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) или **ксапо в \_ \_ автоматическом буфере**.</span><span class="sxs-lookup"><span data-stu-id="2b405-127">Set the output stream buffer's BufferFlags parameter as either [**XAPO\_BUFFER\_VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) or **XAPO\_BUFFER\_SILENT**.</span></span>

<span data-ttu-id="2b405-128">В следующем примере демонстрируется реализация [**локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) и [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , которая просто копирует данные из входного буфера в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="2b405-128">The following example demonstrates a [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) and [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation that simply copies data from an input buffer to an output buffer.</span></span> <span data-ttu-id="2b405-129">Однако обработка не выполняется, если входной буфер помечается [**ксапо \_ буфером \_ без уведомления**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span><span class="sxs-lookup"><span data-stu-id="2b405-129">However, there is no processing if the input buffer is marked with [**XAPO\_BUFFER\_SILENT**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span></span>


```
STDMETHOD(LockForProcess) (UINT32 InputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pInputLockedParameters,
          UINT32 OutputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pOutputLockedParameters)
{
    assert(!IsLocked());
    assert(InputLockedParameterCount == 1);
    assert(OutputLockedParameterCount == 1);
    assert(pInputLockedParameters != NULL);
    assert(pOutputLockedParameters != NULL);
    assert(pInputLockedParameters[0].pFormat != NULL);
    assert(pOutputLockedParameters[0].pFormat != NULL);


    m_uChannels = pInputLockedParameters[0].pFormat->nChannels;
    m_uBytesPerSample = (pInputLockedParameters[0].pFormat->wBitsPerSample >> 3);

    return CXAPOBase::LockForProcess(
        InputLockedParameterCount,
        pInputLockedParameters,
        OutputLockedParameterCount,
        pOutputLockedParameters);
}
STDMETHOD_(void, Process)(UINT32 InputProcessParameterCount,
           const XAPO_PROCESS_BUFFER_PARAMETERS* pInputProcessParameters,
           UINT32 OutputProcessParameterCount,
           XAPO_PROCESS_BUFFER_PARAMETERS* pOutputProcessParameters,
           BOOL IsEnabled)
{
    assert(IsLocked());
    assert(InputProcessParameterCount == 1);
    assert(OutputProcessParameterCount == 1);
    assert(NULL != pInputProcessParameters);
    assert(NULL != pOutputProcessParameters);


    XAPO_BUFFER_FLAGS inFlags = pInputProcessParameters[0].BufferFlags;
    XAPO_BUFFER_FLAGS outFlags = pOutputProcessParameters[0].BufferFlags;

    // assert buffer flags are legitimate
    assert(inFlags == XAPO_BUFFER_VALID || inFlags == XAPO_BUFFER_SILENT);
    assert(outFlags == XAPO_BUFFER_VALID || outFlags == XAPO_BUFFER_SILENT);

    // check input APO_BUFFER_FLAGS
    switch (inFlags)
    {
    case XAPO_BUFFER_VALID:
        {
            void* pvSrc = pInputProcessParameters[0].pBuffer;
            assert(pvSrc != NULL);

            void* pvDst = pOutputProcessParameters[0].pBuffer;
            assert(pvDst != NULL);

            memcpy(pvDst,pvSrc,pInputProcessParameters[0].ValidFrameCount * m_uChannels * m_uBytesPerSample);
            break;
        }

    case XAPO_BUFFER_SILENT:
        {
            // All that needs to be done for this case is setting the
            // output buffer flag to XAPO_BUFFER_SILENT which is done below.
            break;
        }

    }

    // set destination valid frame count, and buffer flags
    pOutputProcessParameters[0].ValidFrameCount = pInputProcessParameters[0].ValidFrameCount; // set destination frame count same as source
    pOutputProcessParameters[0].BufferFlags     = pInputProcessParameters[0].BufferFlags;     // set destination buffer flags same as source

}
```



<span data-ttu-id="2b405-130">При написании метода [**обработки**](/windows/win32/api/xapo/nf-xapo-ixapo-process) важно отметить, что XAudio2 звуковые данные чередуются.</span><span class="sxs-lookup"><span data-stu-id="2b405-130">When writing a [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, it is important to note XAudio2 audio data is interleaved.</span></span> <span data-ttu-id="2b405-131">Это означает, что данные из каждого канала являются смежными для конкретного образца числа.</span><span class="sxs-lookup"><span data-stu-id="2b405-131">This means data from each channel is adjacent for a particular sample number.</span></span> <span data-ttu-id="2b405-132">Например, если имеется 4-канальный звук, воспроизводимый в XAudio2 исходного голоса, то звуковые данные представляют собой образец канала 0, образец канала 1, пример канала 2, пример канала 3, а затем следующий пример каналов 0, 1, 2, 3 и т. д.</span><span class="sxs-lookup"><span data-stu-id="2b405-132">For example, if there is a 4-channel wave playing into an XAudio2 source voice, the audio data is a sample of channel 0, a sample of channel 1, a sample of channel 2, a sample of channel 3, and then the next sample of channels 0, 1, 2, 3, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b405-133">См. также</span><span class="sxs-lookup"><span data-stu-id="2b405-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b405-134">Звуковые эффекты</span><span class="sxs-lookup"><span data-stu-id="2b405-134">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="2b405-135">Обзор протокола XAPO</span><span class="sxs-lookup"><span data-stu-id="2b405-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
