---
title: Обзорное размытие DWM
description: Один из эффектов Signature диспетчер окон рабочего стола (DWM) является полупрозрачной и размытой неклиентской областью. Интерфейсы API DWM позволяют приложениям применять эти эффекты к клиентской области своих окон верхнего уровня.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Диспетчер окон рабочего стола (DWM), эффект размытия позади
- DWM (диспетчер окон рабочего стола), эффект размытия позади
- эффект размытия позади
- Полупрозрачный результат
- эффект прозрачного стекла
- Диспетчер окон рабочего стола (DWM), полупрозрачный результат
- DWM (диспетчер окон рабочего стола), полупрозрачный результат
- Диспетчер окон рабочего стола (DWM), эффект прозрачного стекла
- DWM (диспетчер окон рабочего стола), эффект прозрачного стекла
- Диспетчер окон рабочего стола (DWM), расширение рамки окна в клиентскую область
- DWM (диспетчер окон рабочего стола), расширение рамки окна на клиентскую область
- расширение рамки окна на клиентскую область
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf7378cfcaff93aa9a54ce399890ec1bfd8cc1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070519"
---
# <a name="dwm-blur-behind-overview"></a>Обзорное размытие DWM

Один из эффектов Signature диспетчер окон рабочего стола (DWM) является полупрозрачной и размытой неклиентской областью. Интерфейсы API DWM позволяют приложениям применять эти эффекты к клиентской области своих окон верхнего уровня.

> [!Note]  
> Windows Vista Home Basic Edition не поддерживает эффект прозрачного стекла. Области, которые обычно отображаются с эффектом прозрачного стекла в других выпусках Windows, отображаются как непрозрачные.
> Начиная с Windows 8, вызов этой функции не приводит к эффекту размытия из-за изменения стиля в способе отрисовки окон.


 

В этом разделе обсуждаются следующие сценарии размытия клиента, которые предоставляет DWM.

-   [Добавление размытия в конкретный регион клиентской области](#adding-blur-to-a-specific-region-of-the-client-area)
-   [Расширение рамки окна в клиентскую область](#extending-the-window-frame-into-the-client-area)
-   [См. также](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a>Добавление размытия в конкретный регион клиентской области

Приложение может применить эффект размытия для всей клиентской области окна или для конкретной подобласти. Это позволяет приложениям добавлять контуры в стиле и панели поиска, которые визуально отделены от остальной части приложения.

API, используемый в этом сценарии, — это функция [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) , которая использует [**размытие DWM за константами**](dwm-bb-constants.md) и структуру [**DWM \_ блурбехинд**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) .

В следующем примере функции `EnableBlurBehind` показано, как применить эффект размытия для всего окна.


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



Обратите внимание, что в параметре *хргнблур* указано **значение NULL** . Это означает, что DWM будет применять размытие позади всего окна.

На следующем рисунке показан эффект размытия, применяемый ко всему окну.

![эффект размытия, применяемый к окну](images/dwm-blurbehindwindow.png)

Чтобы применить размытие за подрегионом, примените допустимый маркер области (ХРГН) к элементу **хргнблур** структуры [**DWM \_ Блурбехинд**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) и добавьте флаг **DWM \_ BB \_ блуррегион** к элементу **dwFlags** .

При применении эффект размытия для подобласти окна используется альфа-канал окна для неразмытой области. Это может вызвать непредвиденную прозрачность в неразмытой области окна. Поэтому будьте внимательны при применении к подобласти эффект размытия.

## <a name="extending-the-window-frame-into-the-client-area"></a>Расширение рамки окна в клиентскую область

Приложение может расширять размытие рамки окна в клиентскую область. Это полезно, если применить эффект размытия для окна с закрепленной панелью инструментов или визуально отделять элементы управления от остальной части приложения. Эта функция предоставляется функцией [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .

Чтобы включить размытие с помощью [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), используйте структуру [**Margins**](/windows/win32/api/uxtheme/ns-uxtheme-margins) , чтобы указать степень расширения в клиентской области. Следующий пример функции, `ExtendIntoClientBottom` ,, переключает расширение размытия в нижней части неклиентской рамки в клиентскую область.


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



На следующем рисунке показан эффект размытия за рамку, расширенный в нижней части клиентской области.

![изображение, показывающее эффект размытия в нижней части клиентской области](images/dwm-extendedbottom.png)

Кроме того, с помощью метода [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) можно применить эффект «страница стекла», где эффект размытия применяется ко всей области окна без видимой границы окна. В следующем примере показан этот результат, когда клиентская область отображается без границы окна.


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



На следующем рисунке показано размытие в стиле окна «окно стекла».

![изображение, демонстрирующее эффект размытия в стиле окна "окно стекла"](images/dwm-sheetofglass.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие сведения о диспетчере окон рабочего стола](dwm-overview.md)
</dt> <dt>

[Включение и контроль композиции DWM](composition-ovw.md)
</dt> <dt>

[Вопросы производительности и рекомендации](bestpractices-ovw.md)
</dt> </dl>

 

 