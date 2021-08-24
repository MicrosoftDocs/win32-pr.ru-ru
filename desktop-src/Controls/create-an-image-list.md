---
title: Создание списка изображений
description: В этом разделе показано, как использовать \_ функцию ImageList Create для создания списка изображений.
ms.assetid: 6092C555-B5B6-49DB-B07B-684EDB890761
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e04e3e22894546e887e1a4ca5348518b4e4a35c45f4a26b5b6125b81f9323bed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826484"
---
# <a name="how-to-create-an-image-list"></a>Создание списка изображений

В этом разделе показано, как использовать функцию [**ImageList \_ CREATE**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) для создания списка изображений.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


Чтобы создать список изображений, вызовите функцию [**ImageList \_ CREATE**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) . Параметры включают тип создаваемого списка изображений, размеры каждого изображения и количество изображений, которые вы собираетесь добавить в список.

В следующем примере создается маскированный список изображений с использованием макроса [**ImageList \_ аддикон**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) для добавления в список двух значков.



```C++
// AddIconsToImageList - creates a masked image list and adds some 
// icons to it. 
// Returns the handle to the new image list. 
// hinst - handle to the application instance. 
// 
// Global variables and constants 
//     g_nBird and g_nTree - indexes of the images. 
//     cx_icon and cy_icon - width and height of the icon. 
//     num_icons - number of icons to add to the image list. 
extern int g_nBird, g_nTree; 
 
#define CX_ICON  32 
#define CY_ICON  32 
#define NUM_ICONS 3 
 
HIMAGELIST AddIconsToImageList(HINSTANCE hinst) 
{ 
    HIMAGELIST himlIcons;  // handle to new image list 
    HICON hicon;           // handle to icon 
 
    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Create a masked image list large enough to hold the icons. 
    himlIcons = ImageList_Create(CX_ICON, CY_ICON, ILC_MASK, NUM_ICONS, 0); 
 
    // Load the icon resources, and add the icons to the image list. 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_BIRD)); 
    g_nBird = ImageList_AddIcon(himlIcons, hicon); 
 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_TREE)); 
    g_nTree = ImageList_AddIcon(himlIcons, hicon); 
 
    return himlIcons; 
} 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по спискам изображений](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[О списках изображений](image-lists.md)
</dt> <dt>

[Использование списков изображений](using-image-lists.md)
</dt> </dl>

 

 




