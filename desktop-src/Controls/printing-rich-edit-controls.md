---
title: Печать содержимого элементов управления Rich Edit
description: В этом разделе содержатся сведения о печати содержимого элементов управления Rich Edit.
ms.assetid: d61e2e11-d848-43fc-9622-b3b2032bda48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a304e5c09b5f8ea934c90873c3d915179295964e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654383"
---
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a>Печать содержимого элементов управления Rich Edit

В этом разделе содержатся сведения о печати содержимого элементов управления Rich Edit.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="use-print-preview"></a>Использовать предварительный просмотр

Чтобы отформатировать текст в элементе управления Rich Edit, который будет отображаться на целевом устройстве (обычно на печатной странице), отправьте сообщение [**\_ сеттаржетдевице EM**](em-settargetdevice.md) , передав маркер в контекст устройства (HDC) целевого устройства и желаемую ширину линии. Обычно вы получаете толщину линии, вызывая [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) для целевого HDC.

### <a name="format-print-for-a-specific-device"></a>Форматирование печати для определенного устройства

Чтобы форматировать часть содержимого элемента управления Rich Edit для конкретного устройства, отправьте сообщение [**EM \_ форматранже**](em-formatrange.md) . Структура [**форматранже**](/windows/desktop/api/Richedit/ns-richedit-formatrange) , используемая с этим сообщением, определяет диапазон текста для форматирования, а также параметр hdc для целевого устройства. При необходимости это сообщение также отправляет текст на принтер.

### <a name="use-banding"></a>Использовать чередование

Чередование — это процесс, с помощью которого одна страница выходных данных создается с использованием одного или нескольких отдельных прямоугольников или делений. Когда на странице помещаются все полосы, происходит полное изображение. Этот подход часто используется для растровых принтеров, которые не имеют достаточного объема памяти или могут одновременно создавать изображения на полной странице.

Чтобы реализовать чередование, используйте сообщение [**EM \_ дисплайбанд**](em-displayband.md) для отправки последовательных частей содержимого элемента управления Rich Edit на устройство. Это сообщение выводится на устройство, указанное в предыдущем вызове [**EM \_ форматранже**](em-formatrange.md). Конечно, параметр *wParam* сообщения **EM \_ форматранже** должен быть равен нулю, поэтому печать не инициируется этим сообщением.

## <a name="printrtf-code-example"></a>Пример кода Принтртф

Следующий пример кода выводит содержимое элемента управления Rich Edit на указанный принтер.


```C++
// hwnd is the HWND of the rich edit control.
// hdc is the HDC of the printer. This value can be obtained for the 
// default printer as follows:
//
//     PRINTDLG pd = { sizeof(pd) };
//     pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
//
//     if (PrintDlg(&pd))
//     {
//        HDC hdc = pd.hDC;
//        ...
//     }

BOOL PrintRTF(HWND hwnd, HDC hdc)
{
    DOCINFO di = { sizeof(di) };
    
    if (!StartDoc(hdc, &di))
    {
        return FALSE;
    }

    int cxPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETX);
    int cyPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETY);
    
    int cxPhys = GetDeviceCaps(hdc, PHYSICALWIDTH);
    int cyPhys = GetDeviceCaps(hdc, PHYSICALHEIGHT);

    // Create "print preview". 
    SendMessage(hwnd, EM_SETTARGETDEVICE, (WPARAM)hdc, cxPhys/2);

    FORMATRANGE fr;

    fr.hdc       = hdc;
    fr.hdcTarget = hdc;

    // Set page rect to physical page size in twips.
    fr.rcPage.top    = 0;  
    fr.rcPage.left   = 0;  
    fr.rcPage.right  = MulDiv(cxPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSX));  
    fr.rcPage.bottom = MulDiv(cyPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSY)); 

    // Set the rendering rectangle to the pintable area of the page.
    fr.rc.left   = cxPhysOffset;
    fr.rc.right  = cxPhysOffset + cxPhys;
    fr.rc.top    = cyPhysOffset;
    fr.rc.bottom = cyPhysOffset + cyPhys;

    SendMessage(hwnd, EM_SETSEL, 0, (LPARAM)-1);          // Select the entire contents.
    SendMessage(hwnd, EM_EXGETSEL, 0, (LPARAM)&fr.chrg);  // Get the selection into a CHARRANGE.

    BOOL fSuccess = TRUE;

    // Use GDI to print successive pages.
    while (fr.chrg.cpMin < fr.chrg.cpMax && fSuccess) 
    {
        fSuccess = StartPage(hdc) > 0;
        
        if (!fSuccess) break;
        
        int cpMin = SendMessage(hwnd, EM_FORMATRANGE, TRUE, (LPARAM)&fr);
        
        if (cpMin <= fr.chrg.cpMin) 
        {
            fSuccess = FALSE;
            break;
        }
        
        fr.chrg.cpMin = cpMin;
        fSuccess = EndPage(hdc) > 0;
    }
    
    SendMessage(hwnd, EM_FORMATRANGE, FALSE, 0);
    
    if (fSuccess)
    {
        EndDoc(hdc);
    } 
    
    else 
    
    {
        AbortDoc(hdc);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 