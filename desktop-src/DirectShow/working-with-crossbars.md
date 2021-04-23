---
description: Работа с микшерами
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Работа с микшерами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d3a1c43703ac662d44854b0fc6bad8b280c368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684508"
---
# <a name="working-with-crossbars"></a><span data-ttu-id="39d61-103">Работа с микшерами</span><span class="sxs-lookup"><span data-stu-id="39d61-103">Working with Crossbars</span></span>

<span data-ttu-id="39d61-104">Если карта видеозаписи имеет несколько физических входных данных или поддерживает более одного аппаратного пути для данных, то граф фильтра может содержать [аналоговый фильтр микшера видео](analog-video-crossbar-filter.md).</span><span class="sxs-lookup"><span data-stu-id="39d61-104">If a video capture card has more than one physical input, or supports more than one hardware path for data, then the filter graph may contain the [Analog Video Crossbar Filter](analog-video-crossbar-filter.md).</span></span> <span data-ttu-id="39d61-105">Построитель диаграмм для записи автоматически добавляет этот фильтр при необходимости. Он будет вышестоящей из фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="39d61-105">The Capture Graph Builder automatically adds this filter when needed; it will be upstream from the capture filter.</span></span> <span data-ttu-id="39d61-106">В зависимости от оборудования граф фильтра может содержать более одного экземпляра фильтра микшера.</span><span class="sxs-lookup"><span data-stu-id="39d61-106">Depending on the hardware, the filter graph might contain more than one instance of the crossbar filter.</span></span>

<span data-ttu-id="39d61-107">Фильтр микшера предоставляет интерфейс [**иамкроссбар**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) , который можно использовать для направления определенных входных данных в определенный выход.</span><span class="sxs-lookup"><span data-stu-id="39d61-107">The crossbar filter exposes the [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) interface, which you can use to route a particular input to a particular output.</span></span> <span data-ttu-id="39d61-108">Например, видеоадаптер может иметь соединитель коаксиального подключения и вход S-Video.</span><span class="sxs-lookup"><span data-stu-id="39d61-108">For example, a video card might have a coaxial connector and an S-Video input.</span></span> <span data-ttu-id="39d61-109">Они будут представлены в качестве входных контактов фильтра микшера.</span><span class="sxs-lookup"><span data-stu-id="39d61-109">These would be represented as input pins on the crossbar filter.</span></span> <span data-ttu-id="39d61-110">Чтобы выбрать входные данные, направьте соответствующий входной закрепление к выходному закрепления микшера с помощью метода [**иамкроссбар:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .</span><span class="sxs-lookup"><span data-stu-id="39d61-110">To select an input, route the corresponding input pin to the crossbar's output pin, using the [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) method.</span></span>

<span data-ttu-id="39d61-111">Чтобы найти фильтры микширования на диаграмме, можно использовать метод [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) для поиска фильтров, поддерживающих **иамкроссбар**.</span><span class="sxs-lookup"><span data-stu-id="39d61-111">To locate crossbar filters in the graph, you can use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to search for filters that support **IAMCrossbar**.</span></span> <span data-ttu-id="39d61-112">Например, следующий код выполняет поиск двух микшеров:</span><span class="sxs-lookup"><span data-stu-id="39d61-112">For example, the following code searches for two crossbars:</span></span>


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



<span data-ttu-id="39d61-113">Более обобщенный подход см. в описании класса Ккроссбар в [примере амкап](amcap-sample.md).</span><span class="sxs-lookup"><span data-stu-id="39d61-113">For a more generalized approach, see the CCrossbar class in the [AmCap Sample](amcap-sample.md).</span></span>

<span data-ttu-id="39d61-114">Получив указатель на интерфейс **иамкроссбар** , можно получить сведения о фильтре микшера, включая физический тип каждого ПИН-кода, а также матрицу, на которой входные контакты могут маршрутизироваться с контактами выходных данных.</span><span class="sxs-lookup"><span data-stu-id="39d61-114">Once you have a pointer to the **IAMCrossbar** interface, you can get information about the crossbar filter, including the physical type of each pin, and the matrix of which input pins can be routed to which output pins.</span></span>

-   <span data-ttu-id="39d61-115">Чтобы определить тип физического соединителя, которому соответствует ПИН-код, вызовите метод [**иамкроссбар:: Get \_ кроссбарпининфо**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) .</span><span class="sxs-lookup"><span data-stu-id="39d61-115">To determine the type of physical connector to which a pin corresponds, call the [**IAMCrossbar::get\_CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) method.</span></span> <span data-ttu-id="39d61-116">Метод возвращает член перечисления [**фисикалконнектортипе**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) .</span><span class="sxs-lookup"><span data-stu-id="39d61-116">The method returns a member of the [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) enumeration.</span></span> <span data-ttu-id="39d61-117">Например, в S-Video ПИН-код возвращает значение Фисконн \_ Video \_ свидео.</span><span class="sxs-lookup"><span data-stu-id="39d61-117">For example, an S-Video pin returns the value PhysConn\_Video\_SVideo.</span></span>

    <span data-ttu-id="39d61-118">Метод **Get \_ кроссбаринфо** также указывает, связаны ли два контакта друг с другом.</span><span class="sxs-lookup"><span data-stu-id="39d61-118">The **get\_CrossbarInfo** method also indicates whether two pins are related to each other.</span></span> <span data-ttu-id="39d61-119">Например, ПИН-код видеотюнера может быть связан с ПИН-кодом звукового тюнера.</span><span class="sxs-lookup"><span data-stu-id="39d61-119">For example, a video tuner pin might be related to an audio tuner pin.</span></span> <span data-ttu-id="39d61-120">Связанные контакты имеют одинаковое направление ПИН-кода и обычно являются частью одной и той же физической розетки или соединителя на карте.</span><span class="sxs-lookup"><span data-stu-id="39d61-120">Related pins have the same pin direction, and are typically part of the same physical jack or connector on the card.</span></span>

-   <span data-ttu-id="39d61-121">Чтобы определить, можно ли направить входной ПИН-код на определенный ПИН-код вывода, вызовите метод [**иамкроссбар:: канрауте**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) .</span><span class="sxs-lookup"><span data-stu-id="39d61-121">To determine whether you can route an input pin to a particular output pin, call the [**IAMCrossbar::CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) method.</span></span>
-   <span data-ttu-id="39d61-122">Чтобы определить текущую маршрутизацию между закреплениями, вызовите метод [**иамкроссбар:: Get \_ исраутедто**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) .</span><span class="sxs-lookup"><span data-stu-id="39d61-122">To determine the current routing between pins, call the [**IAMCrossbar::get\_IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) method.</span></span>

<span data-ttu-id="39d61-123">В предыдущих методах все задаются ПИН-коды по номеру индекса, а выходные контакты и входные контакты индексируются из нуля.</span><span class="sxs-lookup"><span data-stu-id="39d61-123">The previous methods all specify pins by index number, with output pins and input pins both indexed from zero.</span></span> <span data-ttu-id="39d61-124">Вызовите метод **иамкроссбар:: Get \_ пинкаунтс** , чтобы найти количество ПИН-кодов в фильтре.</span><span class="sxs-lookup"><span data-stu-id="39d61-124">Call the **IAMCrossbar::get\_PinCounts** method to find the number of pins on the filter.</span></span>

<span data-ttu-id="39d61-125">Например, следующий код отображает сведения о фильтре микшера в окне консоли:</span><span class="sxs-lookup"><span data-stu-id="39d61-125">For example, the following code displays information about a crossbar filter to the console window:</span></span>


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



<span data-ttu-id="39d61-126">Для гипотетических карт эта функция может выдавать следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="39d61-126">For a hypothetical card, this function might produce the following output:</span></span>


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



<span data-ttu-id="39d61-127">На стороне вывода S-Video и Video тюнер связаны с аудио-декодером.</span><span class="sxs-lookup"><span data-stu-id="39d61-127">On the output side, the S-Video and the video tuner are both related to the audio decoder.</span></span> <span data-ttu-id="39d61-128">На стороне входа видеотюнер связан с звуковым тюнером, а S-Video — со звуковой линией в.</span><span class="sxs-lookup"><span data-stu-id="39d61-128">On the input side, the video tuner is related to the audio tuner, and the S-Video is related to the audio line in.</span></span> <span data-ttu-id="39d61-129">Входные данные S-Video направляются на выход S-Video; и входные видеотюнеры направляются в выходные данные видеотюнера.</span><span class="sxs-lookup"><span data-stu-id="39d61-129">The S-Video input is routed to the S-Video output; and the video tuner input is routed to the video tuner output.</span></span> <span data-ttu-id="39d61-130">В настоящее время не направляется в звуковой декодер, но в него можно направлять звуковую строку или звуковой тюнер.</span><span class="sxs-lookup"><span data-stu-id="39d61-130">Currently nothing is routed to the audio decoder, but either the audio line in or the audio tuner could be routed to it.</span></span>

<span data-ttu-id="39d61-131">Можно изменить существующую маршрутизацию, вызвав метод [**иамкроссбар:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .</span><span class="sxs-lookup"><span data-stu-id="39d61-131">You can change the existing routing by calling the [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) method.</span></span>

 

 



