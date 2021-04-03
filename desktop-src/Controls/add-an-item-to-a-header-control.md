---
title: Добавление элемента в элемент управления "заголовок"
description: В этом разделе показано, как добавить элемент в элемент управления "заголовок".
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988012"
---
# <a name="how-to-add-an-item-to-a-header-control"></a><span data-ttu-id="2d572-103">Добавление элемента в элемент управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="2d572-103">How to Add an Item to a Header Control</span></span>

<span data-ttu-id="2d572-104">В этом разделе показано, как добавить элемент в элемент управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="2d572-104">This topic demonstrates how to add an item to a header control.</span></span> <span data-ttu-id="2d572-105">Элемент управления "заголовок" обычно имеет несколько элементов заголовка, определяющих столбцы элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2d572-105">A header control typically has several header items that define the columns of the control.</span></span> <span data-ttu-id="2d572-106">Вы можете добавить элемент в элемент управления "заголовок", отправив сообщение [**\_ INSERTITEM HDM**](hdm-insertitem.md) в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="2d572-106">You can add an item to a header control by sending the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2d572-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="2d572-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2d572-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="2d572-108">Technologies</span></span>

-   [<span data-ttu-id="2d572-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="2d572-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2d572-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="2d572-110">Prerequisites</span></span>

-   <span data-ttu-id="2d572-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="2d572-111">C/C++</span></span>
-   <span data-ttu-id="2d572-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="2d572-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2d572-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="2d572-113">Instructions</span></span>


<span data-ttu-id="2d572-114">Используйте сообщение [**HDM \_ INSERTITEM**](hdm-insertitem.md) , чтобы добавить элемент в элемент управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="2d572-114">Use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to add an item to the header control.</span></span> <span data-ttu-id="2d572-115">Сообщение должно включать адрес структуры [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) .</span><span class="sxs-lookup"><span data-stu-id="2d572-115">The message must include the address of an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="2d572-116">Эта структура определяет свойства элемента заголовка, которые могут включать строку, Растровое изображение, начальный размер и определяемое приложением 32-разрядное значение.</span><span class="sxs-lookup"><span data-stu-id="2d572-116">This structure defines the properties of the header item, which can include a string, a bitmapped image, an initial size, and an application-defined 32-bit value.</span></span>

<span data-ttu-id="2d572-117">В следующем примере показано, как использовать сообщение [**\_ INSERTITEM HDM**](hdm-insertitem.md) и структуру [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) для добавления элемента в элемент управления заголовка.</span><span class="sxs-lookup"><span data-stu-id="2d572-117">The following example illustrates how to use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message and the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure to add an item to a header control.</span></span> <span data-ttu-id="2d572-118">Новый элемент состоит из строки, выровненной по левому краю внутри прямоугольника элемента.</span><span class="sxs-lookup"><span data-stu-id="2d572-118">The new item consists of a string that is left-justified within the item rectangle.</span></span>



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a><span data-ttu-id="2d572-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2d572-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d572-120">Сведения об элементах управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="2d572-120">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="2d572-121">Справочник по элементу Header</span><span class="sxs-lookup"><span data-stu-id="2d572-121">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="2d572-122">Использование элементов управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="2d572-122">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 




