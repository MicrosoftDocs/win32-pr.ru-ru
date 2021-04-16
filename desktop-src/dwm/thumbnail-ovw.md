---
title: Обзор эскизов DWM
description: Диспетчер окон рабочего стола (DWM) включает отображение эскизных представлений окон приложений.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Диспетчер окон рабочего стола (DWM), эскизы
- DWM (диспетчер окон рабочего стола), эскизы
- Диспетчер окон рабочего стола (DWM), эскизные связи
- DWM (диспетчер окон рабочего стола), отношения эскиза
- Эскизы
- отношения эскиза
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104550596"
---
# <a name="dwm-thumbnail-overview"></a>Обзор эскизов DWM

Диспетчер окон рабочего стола (DWM) включает отображение эскизных представлений окон приложений. Это не статические моментальные снимки окна, но они являются динамическими, постоянными соединениями между окном исходного кода эскиза и расположением в окне назначения, которое получает визуализацию динамического эскиза. Это позволяет быстро просматривать работающие приложения путем наведения указателя мыши на приложение на панели задач или с помощью жеста клавиши ALT + TAB для просмотра и быстрого переключения приложения.

На следующем рисунке показан экран Windows Vista Live thumbnail, отображаемый при наведении указателя мыши на приложение на панели задач.

![Снимок экрана, на котором показан эскиз D W M, отображаемый при наведении указателя мыши на приложение на панели задач.](images/dwm-livethumbnail.png)

На следующем рисунке показана перелистывание Windows Vista (ALT-TAB), включенная диспетчером DWM.

![снимок экрана с окном рабочего стола с Alt-Tab](images/dwm-flip.png)

> [!Note]  
> Эскизы DWM не позволяют разработчикам создавать такие приложения, как функция Windows Vista Flip3D (ВИНКЭЙ-TAB). Эскизы подготавливаются к просмотру непосредственно в окне назначения в виде 2-мерная.

 

## <a name="dwm-thumbnail-relationships"></a>Связи эскизов DWM

Чтобы отобразить эскизы в приложении, необходимо сначала установить связь между окном исходного кода и конечным окном. Это делается путем вызова функции [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) .

[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) не отображает эскиз в окне назначения, но только создает связь и предоставляет маркер эскиза. Эскиз отображается после установки [**\_ \_ свойств эскиза DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) и вызова функции [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) . Последующие вызовы **DwmUpdateThumbnailProperties** обновляют эскиз с помощью нового набора свойств. DWM также предоставляет вспомогательную функцию [**двмкуерисумбнаилсаурцесизе**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) для получения размера окна исходного кода из эскиза.

Чтобы завершить связь эскиза, вызовите функцию [**двмунрегистерсумбнаил**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) .

В следующем примере показано, как создать релеатионшип с рабочим столом Windows и отобразить его в приложении.


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие сведения о диспетчере окон рабочего стола](dwm-overview.md)
</dt> <dt>

[Включение и контроль композиции DWM](composition-ovw.md)
</dt> <dt>

[Вопросы производительности и рекомендации](bestpractices-ovw.md)
</dt> </dl>

 

 




