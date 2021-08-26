---
description: В этом разделе описано, как приложение может программно изменять параметры изображения и камеры на устройстве видеозаписи.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Настройка качества видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5987352eb329410efd3fc74d6bf12539e968da8e24d2f0a65af9c9ac7b5cb85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871774"
---
# <a name="configure-the-video-quality"></a>Настройка качества видео

В этом разделе описано, как приложение может программно изменять параметры изображения и камеры на устройстве видеозаписи.

-   [Параметры camp](#procamp-settings)
-   [Параметры камеры](#camera-settings)
-   [Связанные темы](#related-topics)

## <a name="procamp-settings"></a>Параметры camp

Windows Видеокамеры в модели WDM могут поддерживать свойства, управляющие качеством изображения:

-   Компенсация с подсветкой
-   Brightness
-   Контраст
-   Выигрыш
-   Gamma
-   Оттенок
-   Насыщенность
-   Четкость
-   Баланс белого

Управление этими свойствами осуществляется через интерфейс [**иамвидеопрокамп**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) . Используйте этот интерфейс следующим образом:

1.  Вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в фильтре записи для интерфейса [**иамвидеопрокамп**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .
2.  Для каждого свойства, которое необходимо задать, вызовите метод [**иамвидеопрокамп:: дальнего**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) . Свойства задаются перечислением [**видеопрокамппроперти**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) . Если метод метода **дальнего действия** завершается неудачно, это означает, что камера не поддерживает это конкретное свойство.
3.  Если методического [**диапазона**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) завершается, возвращается диапазон поддерживаемых значений для свойства, значение по умолчанию и минимальный шаг приращения.
4.  Чтобы получить текущее значение свойства, вызовите метод [**иамвидеопрокамп:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).
5.  Чтобы задать свойство, вызовите метод [**иамвидеопрокамп:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) . Чтобы восстановить значение по умолчанию для свойства, вызовите метод "- [**Range**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) ", чтобы найти значение по умолчанию, и передайте его для метода **Set** .

При задании свойств не нужно прерывать граф фильтра.

Следующий код настраивает элемент управления TrackBar таким образом, чтобы его можно было использовать для установки яркости. Диапазон значений TrackBar соответствует диапазону яркости, поддерживаемому устройством, а расположение TrackBar соответствует начальной настройке яркости устройства.


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



## <a name="camera-settings"></a>Параметры камеры

Интерфейс [**иамкамераконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) похож на [**иамвидеопрокамп**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), но управляет различными настройки на самой камере:

-   Экспозиция
-   Фокус
-   Ирисы
-   Сдвиг
-   Roll
-   Индикатор
-   Масштабирование

Чтобы использовать этот интерфейс, выполните те же действия, которые используются для [**иамвидеопрокамп**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):

1.  Запросите фильтр записи для [**иамкамераконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).
2.  Вызовите [**иамкамераконтрол:: Range**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) , чтобы узнать, какие параметры поддерживаются, и возможные диапазоны для каждого из параметров.
3.  Вызовите метод [**иамкамераконтрол:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) , чтобы получить текущее значение параметра.
4.  Вызовите метод [**иамкамераконтрол:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) , чтобы задать значение.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка устройства видеозаписи](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
