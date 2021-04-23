---
title: Создание списка изображений
description: В этом разделе показано, как использовать \_ функцию ImageList Create для создания списка изображений.
ms.assetid: 6092C555-B5B6-49DB-B07B-684EDB890761
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c81ff3a46138c210474a1b00ddd2ba647d1368
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988010"
---
# <a name="how-to-create-an-image-list"></a><span data-ttu-id="cc682-103">Создание списка изображений</span><span class="sxs-lookup"><span data-stu-id="cc682-103">How to Create an Image List</span></span>

<span data-ttu-id="cc682-104">В этом разделе показано, как использовать функцию [**ImageList \_ CREATE**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) для создания списка изображений.</span><span class="sxs-lookup"><span data-stu-id="cc682-104">This topic demonstrates how to use the [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) function to create an image list.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cc682-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="cc682-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cc682-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="cc682-106">Technologies</span></span>

-   [<span data-ttu-id="cc682-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="cc682-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cc682-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="cc682-108">Prerequisites</span></span>

-   <span data-ttu-id="cc682-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="cc682-109">C/C++</span></span>
-   <span data-ttu-id="cc682-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="cc682-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cc682-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="cc682-111">Instructions</span></span>


<span data-ttu-id="cc682-112">Чтобы создать список изображений, вызовите функцию [**ImageList \_ CREATE**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) .</span><span class="sxs-lookup"><span data-stu-id="cc682-112">You create an image list by calling the [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) function.</span></span> <span data-ttu-id="cc682-113">Параметры включают тип создаваемого списка изображений, размеры каждого изображения и количество изображений, которые вы собираетесь добавить в список.</span><span class="sxs-lookup"><span data-stu-id="cc682-113">The parameters include the type of image list to create, the dimensions of each image, and the number of images that you intend to add to the list.</span></span>

<span data-ttu-id="cc682-114">В следующем примере создается маскированный список изображений с использованием макроса [**ImageList \_ аддикон**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) для добавления в список двух значков.</span><span class="sxs-lookup"><span data-stu-id="cc682-114">The following example creates a masked image list and uses the [**ImageList\_AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) macro to add two icons to the list.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="cc682-115">См. также</span><span class="sxs-lookup"><span data-stu-id="cc682-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc682-116">Справочник по спискам изображений</span><span class="sxs-lookup"><span data-stu-id="cc682-116">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="cc682-117">О списках изображений</span><span class="sxs-lookup"><span data-stu-id="cc682-117">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="cc682-118">Использование списков изображений</span><span class="sxs-lookup"><span data-stu-id="cc682-118">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 




