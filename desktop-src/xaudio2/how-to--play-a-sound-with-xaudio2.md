---
description: В этом разделе описаны минимальные шаги, необходимые для воспроизведения ранее загруженных звуковых данных в XAudio2.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 'Руководство: воспроизведение звука при помощи XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ee2636ae9b6513dba9a479d63e0fd14be2c198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542535"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a><span data-ttu-id="e5685-103">Руководство: воспроизведение звука при помощи XAudio2</span><span class="sxs-lookup"><span data-stu-id="e5685-103">How to: Play a Sound with XAudio2</span></span>

<span data-ttu-id="e5685-104">В этом разделе описаны минимальные шаги, необходимые для воспроизведения ранее загруженных звуковых данных в XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e5685-104">This topic describes the minimum steps required to play previously-loaded audio data in XAudio2.</span></span> <span data-ttu-id="e5685-105">После инициализации XAudio2 (см. раздел [как инициализировать XAudio2](how-to--initialize-xaudio2.md)) и загрузки звуковых данных (см. раздел как [загружать файлы звуковых данных в XAudio2](how-to--load-audio-data-files-in-xaudio2.md)) можно воспроизвести звук, создав исходный голос и передав ему звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="e5685-105">After you initialize XAudio2 (see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md)) and load the audio data (see How to: [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), you can play a sound by creating a source voice and passing audio data to it.</span></span>

## <a name="to-play-a-sound"></a><span data-ttu-id="e5685-106">Воспроизведение звука</span><span class="sxs-lookup"><span data-stu-id="e5685-106">To play a sound</span></span>

1.  <span data-ttu-id="e5685-107">Инициализируйте подсистему XAudio2, выполнив действия, описанные в разделе [инструкции. Инициализация XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="e5685-107">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="e5685-108">Заполните структуру [**\_ буфера**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) [**вавеформатекс**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) и XAUDIO2, выполнив действия, описанные в разделе [как загружать файлы аудиоданных в XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="e5685-108">Populate a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="e5685-109">В зависимости от формата звуковых данных может потребоваться использовать более крупную структуру данных, содержащую структуру [**вавеформатекс**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) вместо **вавеформатекс**.</span><span class="sxs-lookup"><span data-stu-id="e5685-109">Depending on the format of the audio data, you may need to use a larger data structure containing a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure in place of a **WAVEFORMATEX**.</span></span> <span data-ttu-id="e5685-110">Дополнительные сведения см. на странице справочника по **вавеформатекс** .</span><span class="sxs-lookup"><span data-stu-id="e5685-110">See the **WAVEFORMATEX** reference page for more information.</span></span>

     

3.  <span data-ttu-id="e5685-111">Создайте исходный голоса, вызвав метод [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) на экземпляре обработчика XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e5685-111">Create a source voice by calling the [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) method on an instance of the XAudio2 engine.</span></span> <span data-ttu-id="e5685-112">Формат голоса задается значениями, заданными в структуре [**вавеформатекс**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) .</span><span class="sxs-lookup"><span data-stu-id="e5685-112">The format of the voice is specified by the values set in a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure.</span></span>
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  <span data-ttu-id="e5685-113">Отправьте [**\_ буфер XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) в исходный голоса с помощью функции [**субмитсаурцебуффер**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="e5685-113">Submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice using the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span></span>
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > <span data-ttu-id="e5685-114">Образец данных аудио, в который все *буферные* точки все еще является владельцем приложения и должен оставаться выделенным и доступным до тех пор, пока воспроизведение звука не прекратится.</span><span class="sxs-lookup"><span data-stu-id="e5685-114">The audio sample data to which *buffer* points is still 'owned' by the app and must remain allocated and accessible until the sound stops playing.</span></span>

     

5.  <span data-ttu-id="e5685-115">Используйте функцию [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) для запуска исходного голоса.</span><span class="sxs-lookup"><span data-stu-id="e5685-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span> <span data-ttu-id="e5685-116">Так как все XAudio2ные голоса отправляют свои выходные данные на основной голос по умолчанию, звук из исходного голоса автоматически выполняет свои операции с звуковым устройством, выбранным при инициализации.</span><span class="sxs-lookup"><span data-stu-id="e5685-116">Since all XAudio2 voices send their output to the mastering voice by default, audio from the source voice automatically makes its way to the audio device selected at initialization.</span></span> <span data-ttu-id="e5685-117">В более сложной звуковой диаграмме исходный голос должен указать голос, на который должны отправляться выходные данные.</span><span class="sxs-lookup"><span data-stu-id="e5685-117">In a more complicated audio graph, the source voice would have to specify the voice to which its output should be sent.</span></span>
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="e5685-118">Примечания для приложений Магазина Windows</span><span class="sxs-lookup"><span data-stu-id="e5685-118">Notes for Windows Store apps</span></span>

<span data-ttu-id="e5685-119">Рекомендуется использовать [Интеллектуальный указатель](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) для управления временем существования объектов XAUDIO2 в безопасном режиме исключения.</span><span class="sxs-lookup"><span data-stu-id="e5685-119">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="e5685-120">Для приложений Магазина Windows можно использовать шаблон смарт-указателя [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) из библиотеки шаблонов среда выполнения Windows C++ (WRL).</span><span class="sxs-lookup"><span data-stu-id="e5685-120">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


```
Microsoft::WRL::ComPtr<IXAudio2SourceVoice> SourceVoice;
HRESULT hr;
if( FAILED(hr = pXAudio2->CreateSourceVoice( &SourceVoice, (WAVEFORMATEX*)&wfx ) ) )
    throw Platform::Exception::CreateException(hr); 

if( FAILED(hr = SourceVoice->SubmitSourceBuffer( &buffer ) ) )
    throw Platform::Exception::CreateException(hr); 

if ( FAILED(hr = SourceVoice->Start( 0 ) ) )
    throw Platform::Exception::CreateException(hr);
```



> [!Note]  
> <span data-ttu-id="e5685-121">Перед освобождением объекта [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) убедитесь, что все смарт-указатели на объекты XAUDIO2 полностью освобождены.</span><span class="sxs-lookup"><span data-stu-id="e5685-121">Ensure that all smart pointers to XAUDIO2 objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e5685-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e5685-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5685-123">XAudio2 начало работы</span><span class="sxs-lookup"><span data-stu-id="e5685-123">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="e5685-124">Руководство: инициализация XAudio2</span><span class="sxs-lookup"><span data-stu-id="e5685-124">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="e5685-125">Руководство: загрузка файлов звуковых данных в XAudio2</span><span class="sxs-lookup"><span data-stu-id="e5685-125">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
