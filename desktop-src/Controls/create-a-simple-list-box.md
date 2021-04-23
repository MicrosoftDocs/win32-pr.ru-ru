---
title: Создание простого списка
description: В этом разделе показано, как инициализировать и извлечь элементы из простого списка.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca2230b265d61e9a59a8892e14127d25bf2cfd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070865"
---
# <a name="how-to-create-a-simple-list-box"></a><span data-ttu-id="23a30-103">Создание простого списка</span><span class="sxs-lookup"><span data-stu-id="23a30-103">How to Create a Simple List Box</span></span>

<span data-ttu-id="23a30-104">В этом разделе показано, как инициализировать и извлечь элементы из простого списка.</span><span class="sxs-lookup"><span data-stu-id="23a30-104">This topic demonstrates how to initialize and retrieve items from a simple list box.</span></span>

<span data-ttu-id="23a30-105">Пример кода C++ в этом разделе включает процедуру диалогового окна, которая заполняет список сведениями о игроках в спортивной команде.</span><span class="sxs-lookup"><span data-stu-id="23a30-105">The C++ code example in this topic includes a dialog box procedure that fills a list box with information about players on a sports team.</span></span> <span data-ttu-id="23a30-106">Когда пользователь выбирает имя игрока из списка, в диалоговом окне отображаются сведения о проигрывателе.</span><span class="sxs-lookup"><span data-stu-id="23a30-106">When the user selects the name of a player from the list, information about the player is displayed in the dialog box.</span></span> <span data-ttu-id="23a30-107">Стиль окна списка включает [**фунтов \_ сортировки**](list-box-styles.md), что приводит к упорядоченному списку элементов.</span><span class="sxs-lookup"><span data-stu-id="23a30-107">The window style for the list box includes [**LBS\_SORT**](list-box-styles.md), which results in a sorted list of items.</span></span> <span data-ttu-id="23a30-108">На следующем снимке экрана показано диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="23a30-108">The following screen shot shows the dialog box.</span></span>

![снимок экрана: диалоговое окно, содержащее поле со списком с надписью, текст о выбранном элементе списка и кнопка "ОК"](images/lb-roster.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="23a30-110">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="23a30-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="23a30-111">Технологии</span><span class="sxs-lookup"><span data-stu-id="23a30-111">Technologies</span></span>

-   [<span data-ttu-id="23a30-112">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="23a30-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="23a30-113">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="23a30-113">Prerequisites</span></span>

-   <span data-ttu-id="23a30-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="23a30-114">C/C++</span></span>
-   <span data-ttu-id="23a30-115">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="23a30-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="23a30-116">Инструкции</span><span class="sxs-lookup"><span data-stu-id="23a30-116">Instructions</span></span>


<span data-ttu-id="23a30-117">Приложение должно выполнить следующие задачи, связанные со списком:</span><span class="sxs-lookup"><span data-stu-id="23a30-117">The application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="23a30-118">Инициализация списка</span><span class="sxs-lookup"><span data-stu-id="23a30-118">Initialize the list box</span></span>
-   <span data-ttu-id="23a30-119">Получение выбора пользователя из списка</span><span class="sxs-lookup"><span data-stu-id="23a30-119">Retrieve the user's selection from the list box</span></span>

<span data-ttu-id="23a30-120">В следующем примере кода C++ сведения о проигрывателях хранятся в массиве структур.</span><span class="sxs-lookup"><span data-stu-id="23a30-120">In the following C++ code example, information about players is stored in an array of structures.</span></span> <span data-ttu-id="23a30-121">Во время инициализации процедура диалогового окна использует сообщение [**\_ ADDSTRING балансировки нагрузки**](lb-addstring.md) для добавления имен членов команды в список (**\_ \_ Пример** в списке IDC) по одному за раз.</span><span class="sxs-lookup"><span data-stu-id="23a30-121">During initialization, the dialog box procedure uses the [**LB\_ADDSTRING**](lb-addstring.md) message to add the names of team members to the list box (**IDC\_LISTBOX\_EXAMPLE**) one at a time.</span></span> <span data-ttu-id="23a30-122">Он также использует сообщение [**\_ сетитемдата балансировки нагрузки**](lb-setitemdata.md) для добавления индекса массива проигрывателя в список в качестве данных элемента.</span><span class="sxs-lookup"><span data-stu-id="23a30-122">It also uses the [**LB\_SETITEMDATA**](lb-setitemdata.md) message to add the array index of the player to the list box as item data.</span></span> <span data-ttu-id="23a30-123">Позже, когда пользователь выбирает проигрыватель из списка, процедура диалогового окна использует сообщение [**\_ жетитемдата балансировки нагрузки**](lb-getitemdata.md) для получения соответствующего индекса массива.</span><span class="sxs-lookup"><span data-stu-id="23a30-123">Later, when the user selects a player from the list box, the dialog box procedure uses the [**LB\_GETITEMDATA**](lb-getitemdata.md) message to retrieve the corresponding array index.</span></span> <span data-ttu-id="23a30-124">Затем он использует индекс массива для получения сведений о проигрывателе из массива.</span><span class="sxs-lookup"><span data-stu-id="23a30-124">It then uses the array index to retrieve player information from the array.</span></span>



```C++
typedef struct 
{ 
    TCHAR achName[MAX_PATH]; 
    TCHAR achPosition[12]; 
    int nGamesPlayed; 
    int nGoalsScored; 
} Player; 

Player Roster[] = 
{ 
    {TEXT("Haas, Jonathan"), TEXT("Midfield"), 18, 4 }, 
    {TEXT("Pai, Jyothi"), TEXT("Forward"), 36, 12 }, 
    {TEXT("Hanif, Kerim"), TEXT("Back"), 26, 0 }, 
    {TEXT("Anderberg, Michael"), TEXT("Back"), 24, 2 }, 
    {TEXT("Jelitto, Jacek"), TEXT("Midfield"), 26, 3 }, 
    {TEXT("Raposo, Rui"), TEXT("Back"), 24, 3}, 
    {TEXT("Joseph, Brad"), TEXT("Forward"), 13, 3 }, 
    {TEXT("Bouchard, Thomas"), TEXT("Forward"), 28, 5 }, 
    {TEXT("Salmre, Ivo "), TEXT("Midfield"), 27, 7 }, 
    {TEXT("Camp, David"), TEXT("Midfield"), 22, 3 }, 
    {TEXT("Kohl, Franz"), TEXT("Goalkeeper"), 17, 0 }, 
}; 


INT_PTR CALLBACK ListBoxExampleProc(HWND hDlg, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_INITDIALOG:
        {
            // Add items to list. 
            HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE);  
            for (int i = 0; i < ARRAYSIZE(Roster); i++) 
            { 
                int pos = (int)SendMessage(hwndList, LB_ADDSTRING, 0, 
                    (LPARAM) Roster[i].achName); 
                // Set the array index of the player as item data.
                // This enables us to retrieve the item from the array
                // even after the items are sorted by the list box.
                SendMessage(hwndList, LB_SETITEMDATA, pos, (LPARAM) i); 
            } 
            // Set input focus to the list box.
            SetFocus(hwndList); 
            return TRUE;               
        } 

    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case IDOK:
        case IDCANCEL:
            EndDialog(hDlg, LOWORD(wParam));
            return TRUE;

        case IDC_LISTBOX_EXAMPLE:
            {
                switch (HIWORD(wParam)) 
                { 
                case LBN_SELCHANGE:
                    {
                        HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE); 

                        // Get selected index.
                        int lbItem = (int)SendMessage(hwndList, LB_GETCURSEL, 0, 0); 

                        // Get item data.
                        int i = (int)SendMessage(hwndList, LB_GETITEMDATA, lbItem, 0);

                        // Do something with the data from Roster[i]
                        TCHAR buff[MAX_PATH];
                        StringCbPrintf (buff, ARRAYSIZE(buff),  
                            TEXT("Position: %s\nGames played: %d\nGoals: %d"), 
                            Roster[i].achPosition, Roster[i].nGamesPlayed, 
                            Roster[i].nGoalsScored);

                        SetDlgItemText(hDlg, IDC_STATISTICS, buff); 
                        return TRUE; 
                    } 
                }
            }
            return TRUE;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="23a30-125">См. также</span><span class="sxs-lookup"><span data-stu-id="23a30-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23a30-126">Справочник по элементу управления "список"</span><span class="sxs-lookup"><span data-stu-id="23a30-126">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="23a30-127">Сведения о списках</span><span class="sxs-lookup"><span data-stu-id="23a30-127">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="23a30-128">Использование списков</span><span class="sxs-lookup"><span data-stu-id="23a30-128">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




