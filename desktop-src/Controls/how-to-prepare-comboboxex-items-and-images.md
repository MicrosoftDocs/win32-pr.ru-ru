---
title: Подготовка ComboBoxEx элементов и изображений
description: В этом разделе показано, как добавлять элементы в элемент управления ComboBoxEx.
ms.assetid: 2603DFBE-9E7A-4B2F-BE33-418997D323B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7474b46e5227d91b1cc2b51462a43a0fb75d8b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891109"
---
# <a name="how-to-prepare-comboboxex-items-and-images"></a><span data-ttu-id="6d059-103">Подготовка ComboBoxEx элементов и изображений</span><span class="sxs-lookup"><span data-stu-id="6d059-103">How to Prepare ComboBoxEx Items and Images</span></span>

<span data-ttu-id="6d059-104">В этом разделе показано, как добавлять элементы в элемент управления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="6d059-104">This topic demonstrates how to add items to a ComboBoxEx control.</span></span>

<span data-ttu-id="6d059-105">Чтобы добавить элемент в элемент управления ComboBoxEx, сначала определите структуру [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) .</span><span class="sxs-lookup"><span data-stu-id="6d059-105">To add an item to a ComboBoxEx control, first define a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span> <span data-ttu-id="6d059-106">Затем задайте элемент **маски** структуры, чтобы указать, какие элементы должны использоваться элементом управления.</span><span class="sxs-lookup"><span data-stu-id="6d059-106">Then, set the **mask** member of the structure to indicate which members you want the control to use.</span></span> <span data-ttu-id="6d059-107">Наконец, задайте нужные значения для указанных элементов структуры и отправьте сообщение [**кбем \_ INSERTITEM**](cbem-insertitem.md) , чтобы добавить элемент в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="6d059-107">Finally, set the specified members of the structure to the desired values and send the [**CBEM\_INSERTITEM**](cbem-insertitem.md) message to add the item to the control.</span></span>

<span data-ttu-id="6d059-108">Следующая определяемая приложением функция добавляет 15 элементов к существующему элементу управления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="6d059-108">The following application-defined function adds 15 items to an existing ComboBoxEx control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6d059-109">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="6d059-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6d059-110">Технологии</span><span class="sxs-lookup"><span data-stu-id="6d059-110">Technologies</span></span>

-   [<span data-ttu-id="6d059-111">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="6d059-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="6d059-112">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="6d059-112">Prerequisites</span></span>

-   <span data-ttu-id="6d059-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="6d059-113">C/C++</span></span>
-   <span data-ttu-id="6d059-114">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="6d059-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="6d059-115">Инструкции</span><span class="sxs-lookup"><span data-stu-id="6d059-115">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="6d059-116">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="6d059-116">Step 1:</span></span>

<span data-ttu-id="6d059-117">Чтобы добавить элемент в элемент управления ComboBoxEx, сначала определите структуру [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) .</span><span class="sxs-lookup"><span data-stu-id="6d059-117">To add an item to a ComboBoxEx control, first define a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span>


```C++
COMBOBOXEXITEM cbei;
int iCnt;


typedef struct {
    int iImage;
    int iSelectedImage;
    int iIndent;
    LPTSTR pszText;
} ITEMINFO, *PITEMINFO;

ITEMINFO IInf[ ] = {
    { 0, 3,  0, L"first"}, 
    { 1, 4,  1, L"second"},
    { 2, 5,  2, L"third"},
    { 0, 3,  0, L"fourth"},
    { 1, 4,  1, L"fifth"},
    { 2, 5,  2, L"sixth"},
    { 0, 3,  0, L"seventh"},
    { 1, 4,  1, L"eighth"},
    { 2, 5,  2, L"ninth"},
    { 0, 3,  0, L"tenth"},
    { 1, 4,  1, L"eleventh"},
    { 2, 5,  2, L"twelfth"},
    { 0, 3,  0, L"thirteenth"},
    { 1, 4,  1, L"fourteenth"},
    { 2, 5,  2, L"fifteenth"}
};
```



### <a name="step-2"></a><span data-ttu-id="6d059-118">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="6d059-118">Step 2:</span></span>

<span data-ttu-id="6d059-119">Установите элемент **маски** структуры, чтобы указать, какие элементы должны использоваться элементом управления.</span><span class="sxs-lookup"><span data-stu-id="6d059-119">Set the **mask** member of the structure to indicate which members you want the control to use.</span></span> <span data-ttu-id="6d059-120">Обратите внимание, что элемент **маски** структуры [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) включает значения флагов, которые указывают элементу управления отображать изображения для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="6d059-120">Note that the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure includes flag values that tell the control to display images for each item.</span></span>


```C++
// Set the mask common to all items.
cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
            CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;
```



### <a name="step-3"></a><span data-ttu-id="6d059-121">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="6d059-121">Step 3:</span></span>

<span data-ttu-id="6d059-122">Задайте для указанных элементов структуры нужные значения, а затем отправьте сообщение [**кбем \_ INSERTITEM**](cbem-insertitem.md) , чтобы добавить элемент в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="6d059-122">Set the specified members of the structure to the values you want, and then send the [**CBEM\_INSERTITEM**](cbem-insertitem.md) message to add the item to the control.</span></span>


```C++
for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
    // Initialize the COMBOBOXEXITEM struct.
    cbei.iItem          = iCnt;
    cbei.pszText        = IInf[iCnt].pszText;
    cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
    cbei.iImage         = IInf[iCnt].iImage;
    cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
    cbei.iIndent        = IInf[iCnt].iIndent;

    
    // Tell the ComboBoxEx to add the item. Return FALSE if 
    // this fails.
    if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
        return FALSE;
```



### <a name="step-4"></a><span data-ttu-id="6d059-123">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="6d059-123">Step 4:</span></span>

<span data-ttu-id="6d059-124">Назначьте существующий список изображений элементу управления ComboBoxEx и задайте размер элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6d059-124">Assign the existing image list to the ComboBoxEx control and set the size of control.</span></span>


```C++
// Assign the existing image list to the ComboBoxEx control 
// and return TRUE. 
// g_himl is the handle to the existing image list
SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

// Set size of control to make sure it's displayed correctly now
// that the image list is set.
SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

return TRUE; 
```



## <a name="complete-example"></a><span data-ttu-id="6d059-125">Полный пример</span><span class="sxs-lookup"><span data-stu-id="6d059-125">Complete example</span></span>


```C++
// AddItems - Uses the CBEM_INSERTITEM message to add items to an
// existing ComboBoxEx control.

BOOL WINAPI AddItems(HWND hwndCB)
{
    
    //  Declare and init locals.
    COMBOBOXEXITEM cbei;
    int iCnt;
    

    typedef struct {
        int iImage;
        int iSelectedImage;
        int iIndent;
        LPTSTR pszText;
    } ITEMINFO, *PITEMINFO;

    ITEMINFO IInf[ ] = {
        { 0, 3,  0, L"first"}, 
        { 1, 4,  1, L"second"},
        { 2, 5,  2, L"third"},
        { 0, 3,  0, L"fourth"},
        { 1, 4,  1, L"fifth"},
        { 2, 5,  2, L"sixth"},
        { 0, 3,  0, L"seventh"},
        { 1, 4,  1, L"eighth"},
        { 2, 5,  2, L"ninth"},
        { 0, 3,  0, L"tenth"},
        { 1, 4,  1, L"eleventh"},
        { 2, 5,  2, L"twelfth"},
        { 0, 3,  0, L"thirteenth"},
        { 1, 4,  1, L"fourteenth"},
        { 2, 5,  2, L"fifteenth"}
    };

    // Set the mask common to all items.
    cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
                CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;

    for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
        // Initialize the COMBOBOXEXITEM struct.
        cbei.iItem          = iCnt;
        cbei.pszText        = IInf[iCnt].pszText;
        cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
        cbei.iImage         = IInf[iCnt].iImage;
        cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
        cbei.iIndent        = IInf[iCnt].iIndent;
    
        
        // Tell the ComboBoxEx to add the item. Return FALSE if 
        // this fails.
        if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
            return FALSE;
    }
    // Assign the existing image list to the ComboBoxEx control 
    // and return TRUE. 
    // g_himl is the handle to the existing image list
    SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

    // Set size of control to make sure it's displayed correctly now
    // that the image list is set.
    SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="6d059-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6d059-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d059-127">Сведения об элементах управления ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="6d059-127">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="6d059-128">Справочник по элементу управления ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="6d059-128">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="6d059-129">Использование элементов управления ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="6d059-129">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="6d059-130">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="6d059-130">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 