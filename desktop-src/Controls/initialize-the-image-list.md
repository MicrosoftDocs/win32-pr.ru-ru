---
title: Инициализация списка изображений
description: Каждый элемент в элементе управления "дерево" может иметь два связанных с ним изображения.
ms.assetid: 3683DB35-D70F-4181-9181-95354599B9FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011d789da4eec39febae9d93436e23c23fa59507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104133519"
---
# <a name="how-to-initialize-the-image-list"></a><span data-ttu-id="0b1dc-103">Инициализация списка изображений</span><span class="sxs-lookup"><span data-stu-id="0b1dc-103">How to Initialize the Image List</span></span>

<span data-ttu-id="0b1dc-104">Каждый элемент в элементе управления "дерево" может иметь два связанных с ним изображения.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-104">Every item in a tree-view control can have two images associated with it.</span></span> <span data-ttu-id="0b1dc-105">Элемент отображает одно изображение, если оно выбрано, а другое — нет.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-105">An item displays one image when it is selected and the other when it is not.</span></span> <span data-ttu-id="0b1dc-106">Чтобы включить изображения с элементами представления в виде дерева, сначала используйте функции [списков изображений](image-lists.md) , чтобы создать список изображений и добавить в него изображения.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-106">To include images with tree-view items, first use the [Image Lists](image-lists.md) functions to create an image list and add images to it.</span></span> <span data-ttu-id="0b1dc-107">Затем свяжите список изображений с элементом управления "дерево-представление", используя сообщение [**TVM \_ сетимажелист**](tvm-setimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1dc-107">Then associate the image list with the tree-view control by using the [**TVM\_SETIMAGELIST**](tvm-setimagelist.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0b1dc-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="0b1dc-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0b1dc-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="0b1dc-109">Technologies</span></span>

-   [<span data-ttu-id="0b1dc-110">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="0b1dc-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0b1dc-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="0b1dc-111">Prerequisites</span></span>

-   <span data-ttu-id="0b1dc-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="0b1dc-112">C/C++</span></span>
-   <span data-ttu-id="0b1dc-113">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="0b1dc-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0b1dc-114">Инструкции</span><span class="sxs-lookup"><span data-stu-id="0b1dc-114">Instructions</span></span>

### <a name="initialize-the-image-list"></a><span data-ttu-id="0b1dc-115">Инициализация списка изображений</span><span class="sxs-lookup"><span data-stu-id="0b1dc-115">Initialize the Image List</span></span>

<span data-ttu-id="0b1dc-116">В следующем примере создается список изображений, в список добавляется три точечных рисунка, а список изображений связывается с элементом управления "дерево".</span><span class="sxs-lookup"><span data-stu-id="0b1dc-116">The following example creates an image list, adds three bitmaps to the list, and associates the image list with a tree-view control.</span></span>


```C++
// InitTreeViewImageLists - creates an image list, adds three bitmaps 
// to it, and associates the image list with a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 
//
// Global variables and constants: 
// g_hInst - the global instance handle.
// g_nOpen, g_nClosed, and g_nDocument - global indexes of the images. 
// CX_BITMAP and CY_BITMAP - width and height of an icon. 
// NUM_BITMAPS - number of bitmaps to add to the image list. 
// IDB_OPEN_FILE, IDB_CLOSED_FILE, IDB_DOCUMENT -
//     resource identifiers of the bitmaps.

BOOL InitTreeViewImageLists(HWND hwndTV) 
{ 
    HIMAGELIST himl;  // handle to image list 
    HBITMAP hbmp;     // handle to bitmap 

    // Create the image list. 
    if ((himl = ImageList_Create(CX_BITMAP, 
                                 CY_BITMAP,
                                 FALSE, 
                                 NUM_BITMAPS, 0)) == NULL) 
        return FALSE; 

    // Add the open file, closed file, and document bitmaps. 
    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_OPEN_FILE)); 
    g_nOpen = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_CLOSED_FILE)); 
    g_nClosed = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_DOCUMENT)); 
    g_nDocument = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    // Fail if not all of the images were added. 
    if (ImageList_GetImageCount(himl) < 3) 
        return FALSE; 

    // Associate the image list with the tree-view control. 
    TreeView_SetImageList(hwndTV, himl, TVSIL_NORMAL); 

    return TRUE; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="0b1dc-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0b1dc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b1dc-118">Использование элементов управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="0b1dc-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="0b1dc-119">Пример Кустдтв иллюстрирует пользовательский вывод в элементе управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="0b1dc-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




