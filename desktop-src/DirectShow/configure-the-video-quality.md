---
description: В этом разделе описано, как приложение может программно изменять параметры изображения и камеры на устройстве видеозаписи.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Настройка качества видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb8d2d28e39f0083aac521f1953ebbb1ca8d5b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805692"
---
# <a name="configure-the-video-quality"></a><span data-ttu-id="369eb-103">Настройка качества видео</span><span class="sxs-lookup"><span data-stu-id="369eb-103">Configure the Video Quality</span></span>

<span data-ttu-id="369eb-104">В этом разделе описано, как приложение может программно изменять параметры изображения и камеры на устройстве видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="369eb-104">This topic describes how an application can programmatically change the image and camera settings on a video capture device.</span></span>

-   [<span data-ttu-id="369eb-105">Параметры параметра cAmp</span><span class="sxs-lookup"><span data-stu-id="369eb-105">ProcAmp Settings</span></span>](#procamp-settings)
-   [<span data-ttu-id="369eb-106">Параметры камеры</span><span class="sxs-lookup"><span data-stu-id="369eb-106">Camera Settings</span></span>](#camera-settings)
-   [<span data-ttu-id="369eb-107">См. также</span><span class="sxs-lookup"><span data-stu-id="369eb-107">Related topics</span></span>](#related-topics)

## <a name="procamp-settings"></a><span data-ttu-id="369eb-108">Параметры параметра cAmp</span><span class="sxs-lookup"><span data-stu-id="369eb-108">ProcAmp Settings</span></span>

<span data-ttu-id="369eb-109">Видеокамеры WDM (WDM) могут поддерживать свойства, управляющие качеством изображения.</span><span class="sxs-lookup"><span data-stu-id="369eb-109">Windows Driver Model (WDM) video cameras can support properties that control the quality of the image:</span></span>

-   <span data-ttu-id="369eb-110">Компенсация с подсветкой</span><span class="sxs-lookup"><span data-stu-id="369eb-110">Backlight compensation</span></span>
-   <span data-ttu-id="369eb-111">Brightness</span><span class="sxs-lookup"><span data-stu-id="369eb-111">Brightness</span></span>
-   <span data-ttu-id="369eb-112">Контраст</span><span class="sxs-lookup"><span data-stu-id="369eb-112">Contrast</span></span>
-   <span data-ttu-id="369eb-113">Выигрыш</span><span class="sxs-lookup"><span data-stu-id="369eb-113">Gain</span></span>
-   <span data-ttu-id="369eb-114">Gamma</span><span class="sxs-lookup"><span data-stu-id="369eb-114">Gamma</span></span>
-   <span data-ttu-id="369eb-115">Оттенок</span><span class="sxs-lookup"><span data-stu-id="369eb-115">Hue</span></span>
-   <span data-ttu-id="369eb-116">Насыщенность</span><span class="sxs-lookup"><span data-stu-id="369eb-116">Saturation</span></span>
-   <span data-ttu-id="369eb-117">Четкость</span><span class="sxs-lookup"><span data-stu-id="369eb-117">Sharpness</span></span>
-   <span data-ttu-id="369eb-118">Баланс белого</span><span class="sxs-lookup"><span data-stu-id="369eb-118">White balance</span></span>

<span data-ttu-id="369eb-119">Управление этими свойствами осуществляется через интерфейс [**иамвидеопрокамп**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .</span><span class="sxs-lookup"><span data-stu-id="369eb-119">These properties are controlled through the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span> <span data-ttu-id="369eb-120">Используйте этот интерфейс следующим образом:</span><span class="sxs-lookup"><span data-stu-id="369eb-120">Use this interface as follows:</span></span>

1.  <span data-ttu-id="369eb-121">Вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в фильтре записи для интерфейса [**иамвидеопрокамп**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .</span><span class="sxs-lookup"><span data-stu-id="369eb-121">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the capture filter for the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span>
2.  <span data-ttu-id="369eb-122">Для каждого свойства, которое необходимо задать, вызовите метод [**иамвидеопрокамп:: дальнего**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) .</span><span class="sxs-lookup"><span data-stu-id="369eb-122">For each property that you want to set, call the [**IAMVideoProcAmp::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) method.</span></span> <span data-ttu-id="369eb-123">Свойства задаются перечислением [**видеопрокамппроперти**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) .</span><span class="sxs-lookup"><span data-stu-id="369eb-123">Properties are specified by the [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) enumeration.</span></span> <span data-ttu-id="369eb-124">Если метод метода **дальнего действия** завершается неудачно, это означает, что камера не поддерживает это конкретное свойство.</span><span class="sxs-lookup"><span data-stu-id="369eb-124">If the **GetRange** method fails, it means the camera does not support that particular property.</span></span>
3.  <span data-ttu-id="369eb-125">Если методического [**диапазона**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) завершается, возвращается диапазон поддерживаемых значений для свойства, значение по умолчанию и минимальный шаг приращения.</span><span class="sxs-lookup"><span data-stu-id="369eb-125">If [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) succeeds, it returns the range of supported values for the property, the default value, and the minimum increment.</span></span>
4.  <span data-ttu-id="369eb-126">Чтобы получить текущее значение свойства, вызовите метод [**иамвидеопрокамп:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span><span class="sxs-lookup"><span data-stu-id="369eb-126">To get the current value of a property, call [**IAMVideoProcAmp::Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span></span>
5.  <span data-ttu-id="369eb-127">Чтобы задать свойство, вызовите метод [**иамвидеопрокамп:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) .</span><span class="sxs-lookup"><span data-stu-id="369eb-127">To set a property, call the [**IAMVideoProcAmp::Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) method.</span></span> <span data-ttu-id="369eb-128">Чтобы восстановить значение по умолчанию для свойства, вызовите метод "- [**Range**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) ", чтобы найти значение по умолчанию, и передайте его для метода **Set** .</span><span class="sxs-lookup"><span data-stu-id="369eb-128">To restore a property to its default value, call [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) to find the default and pass that value to the **Set** method.</span></span>

<span data-ttu-id="369eb-129">При задании свойств не нужно прерывать граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="369eb-129">You do not have to stop the filter graph when you set the properties.</span></span>

<span data-ttu-id="369eb-130">Следующий код настраивает элемент управления TrackBar таким образом, чтобы его можно было использовать для установки яркости.</span><span class="sxs-lookup"><span data-stu-id="369eb-130">The following code configures a trackbar control so that it can be used to set the brightness.</span></span> <span data-ttu-id="369eb-131">Диапазон значений TrackBar соответствует диапазону яркости, поддерживаемому устройством, а расположение TrackBar соответствует начальной настройке яркости устройства.</span><span class="sxs-lookup"><span data-stu-id="369eb-131">The range of the trackbar corresponds to the brightness range that the device supports, and position of the trackbar corresponds to the device's initial brightness setting.</span></span>


```C++
HWND hTrackbar; // Handle to the trackbar control. 
// Initialize hTrackbar (not shown).

// Query the capture filter for the IAMVideoProcAmp interface.
IAMVideoProcAmp *pProcAmp = 0;
hr = pCap->QueryInterface(IID_IAMVideoProcAmp, (void**)&pProcAmp);
if (FAILED(hr))
{
    // The device does not support IAMVideoProcAmp, so disable the control.
    EnableWindow(hTrackbar, FALSE);
}
else
{
    long Min, Max, Step, Default, Flags, Val;

    // Get the range and default value. 
    hr = m_pProcAmp->GetRange(VideoProcAmp_Brightness, &Min, &Max, &Step,
        &Default, &Flags);
    if (SUCCEEDED(hr))
    {
        // Get the current value.
        hr = m_pProcAmp->Get(VideoProcAmp_Brightness, &Val, &Flags);
    }
    if (SUCCEEDED(hr))
    {
        // Set the trackbar range and position.
        SendMessage(hTrackbar, TBM_SETRANGE, TRUE, MAKELONG(Min, Max));
        SendMessage(hTrackbar, TBM_SETPOS, TRUE, Val);
        EnableWindow(hTrackbar, TRUE);
    }
    else
    {
        // This property is not supported, so disable the control.
        EnableWindow(hTrackbar, FALSE);
    }
}
```



## <a name="camera-settings"></a><span data-ttu-id="369eb-132">Параметры камеры</span><span class="sxs-lookup"><span data-stu-id="369eb-132">Camera Settings</span></span>

<span data-ttu-id="369eb-133">Интерфейс [**иамкамераконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) похож на [**иамвидеопрокамп**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), но управляет различными настройки на самой камере:</span><span class="sxs-lookup"><span data-stu-id="369eb-133">The [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) interface is similar to [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), but controls various setttings on the camera itself:</span></span>

-   <span data-ttu-id="369eb-134">Экспозиция</span><span class="sxs-lookup"><span data-stu-id="369eb-134">Exposure</span></span>
-   <span data-ttu-id="369eb-135">Фокус</span><span class="sxs-lookup"><span data-stu-id="369eb-135">Focus</span></span>
-   <span data-ttu-id="369eb-136">IRI</span><span class="sxs-lookup"><span data-stu-id="369eb-136">Iris</span></span>
-   <span data-ttu-id="369eb-137">Сдвиг</span><span class="sxs-lookup"><span data-stu-id="369eb-137">Pan</span></span>
-   <span data-ttu-id="369eb-138">Roll</span><span class="sxs-lookup"><span data-stu-id="369eb-138">Roll</span></span>
-   <span data-ttu-id="369eb-139">Индикатор</span><span class="sxs-lookup"><span data-stu-id="369eb-139">Tilt</span></span>
-   <span data-ttu-id="369eb-140">Масштабирование</span><span class="sxs-lookup"><span data-stu-id="369eb-140">Zoom</span></span>

<span data-ttu-id="369eb-141">Чтобы использовать этот интерфейс, выполните те же действия, которые используются для [**иамвидеопрокамп**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span><span class="sxs-lookup"><span data-stu-id="369eb-141">To use this interface, follow the same steps used for [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span></span>

1.  <span data-ttu-id="369eb-142">Запросите фильтр записи для [**иамкамераконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span><span class="sxs-lookup"><span data-stu-id="369eb-142">Query the capture filter for the [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span></span>
2.  <span data-ttu-id="369eb-143">Вызовите [**иамкамераконтрол:: Range**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) , чтобы узнать, какие параметры поддерживаются, и возможные диапазоны для каждого из параметров.</span><span class="sxs-lookup"><span data-stu-id="369eb-143">Call [**IAMCameraControl::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) to find which settings are supported, and the possible range for each settings.</span></span>
3.  <span data-ttu-id="369eb-144">Вызовите метод [**иамкамераконтрол:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) , чтобы получить текущее значение параметра.</span><span class="sxs-lookup"><span data-stu-id="369eb-144">Call [**IAMCameraControl::Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) to get the current value of a setting.</span></span>
4.  <span data-ttu-id="369eb-145">Вызовите метод [**иамкамераконтрол:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) , чтобы задать значение.</span><span class="sxs-lookup"><span data-stu-id="369eb-145">Call [**IAMCameraControl::Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) to set the value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="369eb-146">См. также</span><span class="sxs-lookup"><span data-stu-id="369eb-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="369eb-147">Настройка устройства видеозаписи</span><span class="sxs-lookup"><span data-stu-id="369eb-147">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
