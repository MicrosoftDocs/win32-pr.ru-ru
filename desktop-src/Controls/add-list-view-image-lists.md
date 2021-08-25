---
title: Добавление List-View списков изображений
description: В этом разделе показано, как добавлять списки изображений к элементу управления "представление списка".
ms.assetid: 3C282FBC-5E37-4D8E-A2C4-B2876874E9A7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8875573634cd47fb5ccb271c3dabfca99daf9061469e31c1178b3e4ed938347e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922063"
---
# <a name="how-to-add-list-view-image-lists"></a>Добавление List-View списков изображений

В этом разделе показано, как добавлять списки изображений к элементу управления "представление списка".

Вы создадите только те списки изображений, которые использует элемент управления. Например, если приложение не разрешает пользователю переключаться в представление значков, создавать и назначать крупные списки значков не требуется. При создании больших и мелких списков изображений они должны содержать одни и те же изображения в том же порядке, поскольку одно значение используется для задания значка элемента представления списка в обоих списках изображений.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


Для отображения изображений элементов необходимо назначить список изображений элементу управления "представление списка". Для этого используйте сообщение [**LVM \_ сетимажелист**](lvm-setimagelist.md) или соответствующий макрос [**ListView \_ сетимажелист**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist), указав, содержит ли список изображений полный размер значков, мелких значков или изображений состояний. Чтобы получить маркер для списка изображений, который в настоящий момент назначен элементу управления "представление списка", используйте сообщение [**LVM- \_ ImageList**](lvm-getimagelist.md) . Для определения подходящих размеров для полноразмерных и мелких значков можно использовать функцию [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .

В следующем примере кода C++ функция, определяемая приложением, сначала создает списки изображений, а затем назначает их элементу управления "представление списка".


```C++
// InitListViewImageLists: Creates image lists for a list-view control.
// This function only creates image lists. It does not insert the items into
// the control, which is necessary for the control to be visible.   
//
// Returns TRUE if successful, or FALSE otherwise. 
//
// hWndListView: Handle to the list-view control. 
// global variable g_hInst: The handle to the module of either a 
// dynamic-link library (DLL) or executable (.exe) that contains
// the image to be loaded. If loading a standard or system
// icon, set g_hInst to NULL.
//
BOOL InitListViewImageLists(HWND hWndListView) 
{ 
    HICON hiconItem;     // Icon for list-view items.
    HIMAGELIST hLarge;   // Image list for icon view.
    HIMAGELIST hSmall;   // Image list for other views.

    // Create the full-sized icon image lists. 
    hLarge = ImageList_Create(GetSystemMetrics(SM_CXICON), 
                              GetSystemMetrics(SM_CYICON), 
                              ILC_MASK, 1, 1); 

    hSmall = ImageList_Create(GetSystemMetrics(SM_CXSMICON), 
                              GetSystemMetrics(SM_CYSMICON), 
                              ILC_MASK, 1, 1); 
    
    // Add an icon to each image list.  
    hiconItem = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ITEM));

    ImageList_AddIcon(hLarge, hiconItem);
    ImageList_AddIcon(hSmall, hiconItem);

    DestroyIcon(hiconItem);
 
// When you are dealing with multiple icons, you can use the previous four lines of 
// code inside a loop. The following code shows such a loop. The 
// icons are defined in the application's header file as resources, which 
// are numbered consecutively starting with IDS_FIRSTICON. The number of 
// icons is defined in the header file as C_ICONS.
/*    
    for(index = 0; index < C_ICONS; index++)
    {
        hIconItem = LoadIcon (g_hinst, MAKEINTRESOURCE(IDS_FIRSTICON + index));
        ImageList_AddIcon(hSmall, hIconItem);
        ImageList_AddIcon(hLarge, hIconItem);
        Destroy(hIconItem);
    }
*/
    
    // Assign the image lists to the list-view control. 
    ListView_SetImageList(hWndListView, hLarge, LVSIL_NORMAL); 
    ListView_SetImageList(hWndListView, hSmall, LVSIL_SMALL); 
    
    return TRUE; 
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по элементу управления представления списка](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Сведения об элементах управления List-View](list-view-controls-overview.md)
</dt> <dt>

[Использование элементов управления List-View](using-list-view-controls.md)
</dt> </dl>

 

 