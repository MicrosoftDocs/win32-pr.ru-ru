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
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a><span data-ttu-id="5dcc1-103">Руководство: интегрирование X3DAudio с XAudio2</span><span class="sxs-lookup"><span data-stu-id="5dcc1-103">How to: Integrate X3DAudio with XAudio2</span></span>

<span data-ttu-id="5dcc1-104">В этом разделе показано, как интегрировать X3DAudio с XAudio2.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-104">This topic shows how to integrate X3DAudio with XAudio2.</span></span> <span data-ttu-id="5dcc1-105">X3DAudio можно использовать для предоставления значений громкости и высоты для голосов XAudio2 и параметров для XAudio2, встроенного в переглагол.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-105">You can use X3DAudio to provide the volume and pitch values for XAudio2 voices and the parameters for the XAudio2 built in reverb effect.</span></span> <span data-ttu-id="5dcc1-106">В этом разделе предполагается, что вы создали звуковую диаграмму, как описано в статье [как создать базовый график обработки звука](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="5dcc1-106">This topic assumes that you have created an audio graph as described in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="5dcc1-107">Если вы еще не создали звуковую диаграмму, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-107">If you have not already created an audio graph, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) will fail.</span></span>

<span data-ttu-id="5dcc1-108">**Инициализация X3DAudio**</span><span class="sxs-lookup"><span data-stu-id="5dcc1-108">**To initialize X3DAudio**</span></span>

1.  <span data-ttu-id="5dcc1-109">Инициализируйте X3DAudio, вызвав [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span><span class="sxs-lookup"><span data-stu-id="5dcc1-109">Initialize X3DAudio by calling [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span></span>

    <span data-ttu-id="5dcc1-110">Функция [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) принимает флаги, указывающие на настройку динамика, скорость звука в определяемых пользователем мировых единицах в секунду и маркер, возвращающий экземпляр подсистемы X3DAudio.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-110">The [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) function takes flags indicating the speaker setup, the speed of sound in user-defined world units per second, and a handle to return an instance of the X3DAudio engine.</span></span> <span data-ttu-id="5dcc1-111">Вызовите [**IXAudio2MasteringVoice:: жетчаннелмаск**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) , чтобы получить маску канала для формата вывода.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-111">Call [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) to get the output format's channel mask.</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  <span data-ttu-id="5dcc1-112">Создайте экземпляры [**\_ прослушивателя X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) и структуры [**\_ передатчика X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .</span><span class="sxs-lookup"><span data-stu-id="5dcc1-112">Create instances of the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span>

    <span data-ttu-id="5dcc1-113">Структура прослушивателя X3DAUDIO представляет собой расположение любого из [**\_ прослушиваемого**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) звука.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-113">The [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) structure represents the position of whatever is hearing the sound.</span></span> <span data-ttu-id="5dcc1-114">Как правило, это расположение камеры или расположение, близкое к нему.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-114">Generally, this is the position of the camera or a position close to it.</span></span> <span data-ttu-id="5dcc1-115">Структура [**\_ передатчика X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) представляет собой расположение вещи, которая делает звук.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-115">The [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structure represents the position of the thing making the sound.</span></span> <span data-ttu-id="5dcc1-116">Для каждого отслеживаемого звука будет использоваться одна структура **\_ передатчика X3DAUDIO** .</span><span class="sxs-lookup"><span data-stu-id="5dcc1-116">There will be one **X3DAUDIO\_EMITTER** structure for each sound that is being tracked.</span></span>

    <span data-ttu-id="5dcc1-117">Элементы структур, которые не будут обновляться в цикле игры, должны быть инициализированы здесь.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-117">Members of the structures that will not be updated in a game loop should be initialized here.</span></span> <span data-ttu-id="5dcc1-118">Большинство членов структур можно просто инициализировать в ноль.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-118">Most members of the structures can simply be initialized to zero.</span></span> <span data-ttu-id="5dcc1-119">Тем не менее некоторые члены [**X3DAUDIOного \_ передатчика**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) должны быть инициализированы как ненулевые значения.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-119">However, some members of [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) need to be set to be initialized to non-zero values.</span></span> <span data-ttu-id="5dcc1-120">Член Чаннелкаунт **\_ передатчика X3DAUDIO** должен быть инициализирован с числом каналов в голоса, которые представляет передатчик.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-120">The ChannelCount member of the **X3DAUDIO\_EMITTER** needs to be initialized to the number of channels in the voice the emitter represents.</span></span> <span data-ttu-id="5dcc1-121">Кроме того, член Курведистанцескалер в **\_ передатчике X3DAUDIO** должен находиться в диапазоне от ФЛТ \_ min до ФЛТ \_ Max.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-121">Also, the CurveDistanceScaler member of **X3DAUDIO\_EMITTER** must be in the range FLT\_MIN to FLT\_MAX.</span></span>

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  <span data-ttu-id="5dcc1-122">Создайте экземпляр структуры [**\_ \_ параметров DSP X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) .</span><span class="sxs-lookup"><span data-stu-id="5dcc1-122">Create an instance of the [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure.</span></span>

    <span data-ttu-id="5dcc1-123">Структура [**\_ \_ параметров X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) используется для возврата результатов, вычисляемых [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span><span class="sxs-lookup"><span data-stu-id="5dcc1-123">The [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure is used to return results calculated by [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span></span> <span data-ttu-id="5dcc1-124">Функция **X3DAudioCalculate** не выделяет память для всех ее параметров.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-124">The **X3DAudioCalculate** function does not allocate memory for any of its parameters.</span></span> <span data-ttu-id="5dcc1-125">Это означает, что необходимо выделить массивы для элементов ПматрикскоеффиЦиентс и Пделайтимес структуры **X3DAUDIO \_ DSP \_** , если вы планируете их использовать.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-125">This means that you need to allocate arrays for the **X3DAUDIO\_DSP\_SETTINGS** structure's pMatrixCoefficients and pDelayTimes members if you intend to use them.</span></span> <span data-ttu-id="5dcc1-126">Кроме того, в качестве членов Сркчаннелкаунт и Дстчаннелкаунт необходимо задать количество каналов в исходных и конечных голосовах.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-126">In addition, you need to set the SrcChannelCount and DstChannelCount members to the number of channels in the emitter's source and destination voices.</span></span>

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > <span data-ttu-id="5dcc1-127">Используйте [**IXAudio2Voice:: жетвоицедетаилс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) на главном голоса, чтобы получить число Инпутчаннелс для **нчаннелс**.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-127">Use [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) on the mastering voice to obtain the number of InputChannels for **nChannels**.</span></span> <span data-ttu-id="5dcc1-128">Для пакетов SDK для DirectX версии XAUDIO2 до Windows 8 используйте IXAudio2:: Жетдевицедетаилс.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-128">For DirectX SDK versions of XAUDIO2 prior to Windows 8, use IXAudio2::GetDeviceDetails.</span></span>

     

<span data-ttu-id="5dcc1-129">Выполните эти действия один раз для каждого из двух и трех кадров, чтобы вычислить новые параметры и применить их.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-129">Perform these steps once every two to three frames to calculate new settings and apply them.</span></span> <span data-ttu-id="5dcc1-130">В этом примере исходный голоса отправляется непосредственно на основной Voice и в субмикс голоса с примененным к нему переглаголом.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-130">In this example, a source voice is sending directly to the mastering voice and to a submix voice with a reverb effect applied to it.</span></span>

<span data-ttu-id="5dcc1-131">**Использование X3DAudio для вычисления и применения новых параметров 3D Audio**</span><span class="sxs-lookup"><span data-stu-id="5dcc1-131">**To use X3DAudio to calculate and apply new 3D audio settings**</span></span>

1.  <span data-ttu-id="5dcc1-132">Обновление [**X3DAUDIO \_ прослушивателя**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) и [**структур \_ передатчиков X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) с их текущей позицией, скоростью и ориентацией.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-132">Update the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures with their current position, velocity, and orientation.</span></span>

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

    

2.  <span data-ttu-id="5dcc1-133">Вызовите [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) , чтобы вычислить новые параметры для голосов.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-133">Call [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) to calculate new settings for the voices.</span></span>

    <span data-ttu-id="5dcc1-134">Параметры для [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) будут обновлены для [**X3DAUDIO \_ прослушивателя**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) и [**структур \_ передатчика X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .</span><span class="sxs-lookup"><span data-stu-id="5dcc1-134">The parameters for [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) will be the updated [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span> <span data-ttu-id="5dcc1-135">Флаги указывают, какие значения должны вычисляться **X3DAudioCalculate** , и какая структура [**\_ \_ параметров X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) будет хранить результаты выполненных вычислений.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-135">The flags will indicate what values **X3DAudioCalculate** should calculate, and which [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure will hold the results of the calculations performed.</span></span>

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  <span data-ttu-id="5dcc1-136">Используйте [**IXAudio2Voice:: сетаутпутматрикс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) и [**IXAudio2SourceVoice:: сетфрекуенциратио**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) , чтобы применить значения объема и шага к исходному голосу.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-136">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) and [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) to apply the volume and pitch values to the source voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  <span data-ttu-id="5dcc1-137">Используйте [**IXAudio2Voice:: сетаутпутматрикс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) , чтобы применить вычисляемый уровень передействия к голосовому субмикс.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-137">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) to apply the calculated reverb level to the submix voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  <span data-ttu-id="5dcc1-138">Используйте [**IXAudio2Voice:: сетфилтерпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) для применения к исходному голосовому коэффициенту вычисляемого нижнего уровня фильтра низкого прохода.</span><span class="sxs-lookup"><span data-stu-id="5dcc1-138">Use [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) to apply the calculated low pass filter direct coefficient to the source voice.</span></span>

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5dcc1-139">См. также</span><span class="sxs-lookup"><span data-stu-id="5dcc1-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dcc1-140">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="5dcc1-140">X3DAudio</span></span>](x3daudio.md)
</dt> <dt>

[<span data-ttu-id="5dcc1-141">Обзор X3DAudio</span><span class="sxs-lookup"><span data-stu-id="5dcc1-141">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="5dcc1-142">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="5dcc1-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="5dcc1-143">Элемент управления громкостью и шагом XAudio2</span><span class="sxs-lookup"><span data-stu-id="5dcc1-143">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
