---
description: В этом разделе показано, как интегрировать X3DAudio с XAudio2.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 'Руководство: интегрирование X3DAudio с XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc54fa5f673e319712808ca6d2b587b8ad2d0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815280"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a>Руководство: интегрирование X3DAudio с XAudio2

В этом разделе показано, как интегрировать X3DAudio с XAudio2. X3DAudio можно использовать для предоставления значений громкости и высоты для голосов XAudio2 и параметров для XAudio2, встроенного в переглагол. В этом разделе предполагается, что вы создали звуковую диаграмму, как описано в статье [как создать базовый график обработки звука](how-to--build-a-basic-audio-processing-graph.md). Если вы еще не создали звуковую диаграмму, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) завершится ошибкой.

**Инициализация X3DAudio**

1.  Инициализируйте X3DAudio, вызвав [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).

    Функция [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) принимает флаги, указывающие на настройку динамика, скорость звука в определяемых пользователем мировых единицах в секунду и маркер, возвращающий экземпляр подсистемы X3DAudio. Вызовите [**IXAudio2MasteringVoice:: жетчаннелмаск**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) , чтобы получить маску канала для формата вывода.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  Создайте экземпляры [**\_ прослушивателя X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) и структуры [**\_ передатчика X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .

    Структура прослушивателя X3DAUDIO представляет собой расположение любого из [**\_ прослушиваемого**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) звука. Как правило, это расположение камеры или расположение, близкое к нему. Структура [**\_ передатчика X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) представляет собой расположение вещи, которая делает звук. Для каждого отслеживаемого звука будет использоваться одна структура **\_ передатчика X3DAUDIO** .

    Элементы структур, которые не будут обновляться в цикле игры, должны быть инициализированы здесь. Большинство членов структур можно просто инициализировать в ноль. Тем не менее некоторые члены [**X3DAUDIOного \_ передатчика**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) должны быть инициализированы как ненулевые значения. Член Чаннелкаунт **\_ передатчика X3DAUDIO** должен быть инициализирован с числом каналов в голоса, которые представляет передатчик. Кроме того, член Курведистанцескалер в **\_ передатчике X3DAUDIO** должен находиться в диапазоне от ФЛТ \_ min до ФЛТ \_ Max.

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  Создайте экземпляр структуры [**\_ \_ параметров DSP X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) .

    Структура [**\_ \_ параметров X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) используется для возврата результатов, вычисляемых [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate). Функция **X3DAudioCalculate** не выделяет память для всех ее параметров. Это означает, что необходимо выделить массивы для элементов ПматрикскоеффиЦиентс и Пделайтимес структуры **X3DAUDIO \_ DSP \_** , если вы планируете их использовать. Кроме того, в качестве членов Сркчаннелкаунт и Дстчаннелкаунт необходимо задать количество каналов в исходных и конечных голосовах.

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > Используйте [**IXAudio2Voice:: жетвоицедетаилс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) на главном голоса, чтобы получить число Инпутчаннелс для **нчаннелс**. Для пакетов SDK для DirectX версии XAUDIO2 до Windows 8 используйте IXAudio2:: Жетдевицедетаилс.

     

Выполните эти действия один раз для каждого из двух и трех кадров, чтобы вычислить новые параметры и применить их. В этом примере исходный голоса отправляется непосредственно на основной Voice и в субмикс голоса с примененным к нему переглаголом.

**Использование X3DAudio для вычисления и применения новых параметров 3D Audio**

1.  Обновление [**X3DAUDIO \_ прослушивателя**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) и [**структур \_ передатчиков X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) с их текущей позицией, скоростью и ориентацией.

    ```
    Emitter.OrientFront = EmitterOrientFront;
    Emitter.OrientTop = EmitterOrientTop;
    Emitter.Position = EmitterPosition;
    Emitter.Velocity = EmitterVelocity;
    Listener.OrientFront = ListenerOrientFront;
    Listener.OrientTop = ListenerOrientTop;
    Listener.Position = ListenerPosition;
    Listener.Velocity = ListenerVelocity;
    ```

    

2.  Вызовите [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) , чтобы вычислить новые параметры для голосов.

    Параметры для [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) будут обновлены для [**X3DAUDIO \_ прослушивателя**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) и [**структур \_ передатчика X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) . Флаги указывают, какие значения должны вычисляться **X3DAudioCalculate** , и какая структура [**\_ \_ параметров X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) будет хранить результаты выполненных вычислений.

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  Используйте [**IXAudio2Voice:: сетаутпутматрикс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) и [**IXAudio2SourceVoice:: сетфрекуенциратио**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) , чтобы применить значения объема и шага к исходному голосу.

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  Используйте [**IXAudio2Voice:: сетаутпутматрикс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) , чтобы применить вычисляемый уровень передействия к голосовому субмикс.

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  Используйте [**IXAudio2Voice:: сетфилтерпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) для применения к исходному голосовому коэффициенту вычисляемого нижнего уровня фильтра низкого прохода.

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> <dt>

[Обзор X3DAudio](x3daudio-overview.md)
</dt> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Элемент управления громкостью и шагом XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
