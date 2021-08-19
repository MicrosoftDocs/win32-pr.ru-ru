---
title: Использование Hot-Tracking с панелями инструментов
description: Когда указатель мыши наводится на элемент, он начинает быть активным. Если включено отслеживание, горячий элемент выделяется. Панель инструментов, созданная с помощью ТБСТИЛЕ \_ плоского стиля или использующего стили оформления, поддерживает по умолчанию функцию оперативного отслеживания.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd735828675ca360cfa91aceefb2d76d34252a96aa7b5edb776e3d48a1fcdc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829093"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a>Использование Hot-Tracking с панелями инструментов

Когда указатель мыши наводится на элемент, он начинает быть активным. Если включено отслеживание, горячий элемент выделяется. Панель инструментов, созданная с помощью [**тбстиле \_ плоского**](toolbar-control-and-button-styles.md) стиля или использующего [стили оформления](themes-overview.md), поддерживает по умолчанию функцию оперативного отслеживания.

Для оперативного отслеживания необходимо создавать списки изображений. Таким образом, нельзя использовать сообщение [**\_ аддбитмап ТБ**](tb-addbitmap.md) или функцию [**креатетулбарекс**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) для создания панели инструментов.

При наведении указателя мыши на кнопку на панели инструментов отображается кнопка, выделенная для выделения. На следующем рисунке показана панель инструментов с включенной функцией оперативного отслеживания. указатель мыши наводится на кнопку Save (сохранить), когда был сделан снимок экрана.

![снимок экрана: диалоговое окно с тремя элементами панели инструментов; Выбранный значок отображается в контуре](images/tb-withstyles.png)

Если необходимо изменить изображение кнопки панели инструментов при изменении состояния элемента управления, сохраните другие изображения в [списках изображений](image-lists.md). Например, некоторые приложения имеют черные и белые кнопки панели инструментов, которые становятся цветными, когда они выбраны. Два разных образа хранятся в списках изображений. Панели инструментов поддерживают использование до трех списков изображений. Как правило, в приложении используется список образов по умолчанию, отключен и горячая отслеживание. Чтобы задать и получить списки изображений для кнопок активной панели инструментов, используйте сообщения [**\_ Жесотимажелист**](tb-gethotimagelist.md) в [**ТБ \_ сесотимажелист**](tb-sethotimagelist.md) и ТБ.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="use-hot-tracking-with-a-toolbar"></a>Использование Hot-Tracking с панелью инструментов

В следующем примере кода создается, заполняется и назначается список изображений для горячих кнопок.


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления ToolBar](using-toolbar-controls.md)
</dt> <dt>

[демонстрация Windows стандартных элементов управления (кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




