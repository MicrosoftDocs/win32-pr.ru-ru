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
# <a name="how-to-create-an-xapo"></a>Руководство: создание XAPO

API КСАПО предоставляет интерфейс [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo) и класс [**кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) для создания новых типов ксапо. Интерфейс **иксапо** содержит все методы, которые должны быть реализованы для создания нового ксапо. Класс **кксапобасе** предоставляет базовую реализацию интерфейса **иксапо** . **Кксапобасе** реализует все методы интерфейса **иксапо** , за исключением метода [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , который уникален для каждого ксапо.

## <a name="to-create-a-new-static-xapo"></a>Создание нового статического КСАПО

1.  Создайте новый класс КСАПО из базового класса [**кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .

    > [!Note]  
    > Ксапос реализуют интерфейс **IUnknown** . Интерфейсы [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo) и [**иксапопараметерс**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) включают в себя три метода **IUnknown** : **QueryInterface**, **AddRef** и **Release**. [**Кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) предоставляет реализации всех трех методов **IUnknown** . Новый экземпляр **кксапобасе** будет иметь счетчик ссылок, равный 1. Он будет уничтожен, когда счетчик ссылок станет равным 0. Чтобы разрешить XAudio2 уничтожить экземпляр КСАПО, когда он больше не нужен, вызовите метод **IUnknown:: Release** для ксапо после добавления в цепочку эффектов XAudio2. См. [инструкции по использованию ксапо в XAudio2](how-to--use-an-xapo-in-xaudio2.md) для получения дополнительных сведений об использовании Ксапо с XAudio2.

     

2.  Переопределите реализацию класса [**кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) метода [**Иксапо:: локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .

    Переопределение [**локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) позволяет сохранять данные о формате звуковых данных для использования в [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

3.  Реализуйте метод [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) .

    XAudio2 вызывает метод [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) каждый раз, когда ксапо требуется обработка звуковых данных. **Процесс** содержит основную часть кода для ксапо.

## <a name="implementing-the-process-method"></a>Реализация метода Process

Метод [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) принимает буферы потоков для входных и выходных звуковых данных. Типичный КСАПО предложит один буфер входного потока и один буфер потока вывода. Необходимо основывать обработку данных из буфера входного потока в формате, указанном в функции [**локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) , и всех флагах, переданных в функцию **Process** с помощью буфера входного потока. Скопируйте обработанные данные буфера входного потока в буфер потока вывода. Задайте параметр Буфферфлагс буфера выходного потока как [**\_ \_ допустимый буфер ксапо**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) или **ксапо в \_ \_ автоматическом буфере**.

В следующем примере демонстрируется реализация [**локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) и [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , которая просто копирует данные из входного буфера в выходной буфер. Однако обработка не выполняется, если входной буфер помечается [**ксапо \_ буфером \_ без уведомления**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).


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



При написании метода [**обработки**](/windows/win32/api/xapo/nf-xapo-ixapo-process) важно отметить, что XAudio2 звуковые данные чередуются. Это означает, что данные из каждого канала являются смежными для конкретного образца числа. Например, если имеется 4-канальный звук, воспроизводимый в XAudio2 исходного голоса, то звуковые данные представляют собой образец канала 0, образец канала 1, пример канала 2, пример канала 3, а затем следующий пример каналов 0, 1, 2, 3 и т. д.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Звуковые эффекты](audio-effects.md)
</dt> <dt>

[Обзор протокола XAPO](xapo-overview.md)
</dt> </dl>

 

 
