---
title: Отображение точечного рисунка, предоставляемого приложением, на составном изображении
description: Отображение точечного рисунка Application-Supplied на составном изображении
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ecd8ac931d0a0bb83eafba09d8ca7dc8263f0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536584"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a>Отображение точечного рисунка, предоставляемого приложением, на составном изображении

Приложения могут использовать режим смешения VMR для показа логотипов каналов альфа-смешения, пользовательского интерфейса или рекламы частично или полностью в пределах прямоугольника видео. Так как смешивание выполняется с помощью графического процессора, существует минимальное влияние на производительность воспроизведения видеопотока, а также отсутствие обнаруживаемых помех или уничтожение артефактов. Приложения могут изменять отображаемое изображение так, как нужно. Следует отметить, что изменения отражаются только на экране, когда граф фильтра DirectShow находится в состоянии выполняется.

VMR использует свой компонент микшера для наложения точечного рисунка на композитный образ. С помощью VMR-7 приложение должно затребовать, чтобы VMR загрузил свое микшер, даже если имеется только один поток видео. Это не является обязательным для VMR-9, так как загружает микшер по умолчанию.

Для смешения статического растрового изображения с видеопотоком приложение создает VMR и добавляет его в граф, а затем вызывает [**ивмрфилтерконфиг:: сетнумберофстреамс**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). Значение, передаваемое этой функции, определяет количество входных ПИН-кодов, которые должен создать VMR. В приложениях можно указать любое значение от 1 до максимального количества \_ потоков микшера \_ ; Указание значения 1 допустимо, если приложение планирует отображать только один поток видео. Хотя фильтр VMR-7 по умолчанию имеет один входной ПИН-код, этот метод должен быть вызван для того, чтобы заставить его загрузить свой компонент микшера. (VMR-9 загружает микшер и настраивает четыре контакта по умолчанию.)

Чтобы задать точечный рисунок, используйте интерфейс [**ивмрмиксербитмап**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) на VMR-7 или интерфейс [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) на VMR-9.

Точечный рисунок может быть задан либо с помощью маркера контекста устройства GDI (hDC), либо через интерфейс поверхности DirectDraw. Если приложению требуется, чтобы изображение содержало внедренную альфа-информацию (также известную как на пиксель Alpha), данные изображения должны размещаться в интерфейсе поверхности DirectDraw. Это связано с тем, что в настоящий момент невозможно разместить сведения о альфа-канале в контексте устройства GDI. Поверхность DirectDraw должна быть либо RGB32, либо ARGB32, и, предпочтительнее, системной областью памяти. Размеры поверхности не обязательно должны быть степенью 2.

VMR позволяет приложениям указывать расположение и общее значение прозрачности для образа. В следующем коде показано, как передать данные изображения в VMR для последующего смешения:


```C++
HRESULT BlendApplicationImage( 
  HWND hwndApp,
  IVMRWindowlessControl* pWc,
  HBITMAP hbm
)
{
    LONG cx, cy;
    HRESULT hr;
    hr = pWc->GetNativeVideoSize(&cx, &cy, NULL, NULL);
    if (FAILED(hr))
        return hr;
    
    HDC hdc = GetDC(hwndApp);
    if (hdc == NULL)
    {
        return E_FAIL;
    }
    
    HDC hdcBmp = CreateCompatibleDC(hdc);
    ReleaseDC(hwndApp, hdc);
    
    if (hdcBmp == NULL)
    {
        return E_FAIL;
    }
    
    BITMAP bm;
    if (0 == GetObject(hbm, sizeof(bm), &bm))
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    HBITMAP hbmOld = (HBITMAP)SelectObject(hdcBmp, hbm);
    if (hbmOld == 0)
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    VMRALPHABITMAP bmpInfo;
    ZeroMemory(&bmpInfo, sizeof(bmpInfo) );
    bmpInfo.dwFlags = VMRBITMAP_HDC;
    bmpInfo.hdc = hdcBmp;
    
    // Show the entire bitmap in the top-left corner of the video image.
    SetRect(&bmpInfo.rSrc, 0, 0, bm.bmWidth, bm.bmHeight);
    bmpInfo.rDest.left = 0.f;
    bmpInfo.rDest.top = 0.f;
    bmpInfo.rDest.right = (float)bm.bmWidth / (float)cx;
    bmpInfo.rDest.bottom = (float)bm.bmHeight / (float)cy;
    
    // Set the transparency value (1.0 is opaque, 0.0 is transparent).
    bmpInfo.fAlpha = 0.2f;
    
    IVMRMixerBitmap* pBmp;
    hr = pWc->QueryInterface(IID_IVMRMixerBitmap, (LPVOID *)&pBmp);
    if (SUCCEEDED(hr)) 
    {
        pBmp->SetAlphaBitmap(&bmpInfo);
        pBmp->Release();
    }
    
    DeleteObject(SelectObject(hdcBmp, hbmOld));
    DeleteDC(hdcBmp);
    return hr;
}
```



Основные понятия, описанные в этом разделе, показаны в примере приложения [вмрплайер](vmrplayer-sample.md) .

**Создание простых анимаций с помощью растрового изображения**

Чтобы создать простой анимированный логотип точечного рисунка, разместите все растровые кадры в одном изображении, как показано на следующей иллюстрации.

![полоса изображений VMR](images/vmr-image-strip.png)

При первоначальном задании точечного рисунка с помощью [**ивмрмиксербитмап:: сеталфабитмап**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), если точечный рисунок находится в состоянии HDC, установите поле **rsrc** структуры **вмралфабитмап** , чтобы указать размер всей битовой карты в HDC. **Верхний** и **левый** элементы структуры имеют значение 0, а **правый** и **Нижний** элементы — ширина и высота растрового изображения. Если точечный рисунок находится в области DirectDraw, то известен размер поверхности, поэтому нет необходимости указывать rSrc в этом методе.

При вызове [**ивмрмиксербитмап:: упдатеалфабитмаппараметерс**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters)используйте элемент **rsrc** для точечных рисунков HDC и DirectDraw, чтобы указать конкретный фрейм или прямоугольник в изображении, который требуется отобразить, и установите флаг **вмрбитмап \_ SRCRECT** в элементе **dwFlags** .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование режима смешения VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



