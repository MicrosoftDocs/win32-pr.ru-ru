---
title: Создание простого списка
description: В этом разделе показано, как инициализировать и извлечь элементы из простого списка.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a037bfbdb5232cd30d3e13fbc251c22c18c71a76398a351939602301a745d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063182"
---
# <a name="how-to-create-a-simple-list-box"></a>Создание простого списка

В этом разделе показано, как инициализировать и извлечь элементы из простого списка.

Пример кода C++ в этом разделе включает процедуру диалогового окна, которая заполняет список сведениями о игроках в спортивной команде. Когда пользователь выбирает имя игрока из списка, в диалоговом окне отображаются сведения о проигрывателе. Стиль окна списка включает [**фунтов \_ сортировки**](list-box-styles.md), что приводит к упорядоченному списку элементов. На следующем снимке экрана показано диалоговое окно.

![снимок экрана: диалоговое окно, содержащее поле со списком с надписью, текст о выбранном элементе списка и кнопка "ОК"](images/lb-roster.png)

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


Приложение должно выполнить следующие задачи, связанные со списком:

-   Инициализация списка
-   Получение выбора пользователя из списка

В следующем примере кода C++ сведения о проигрывателях хранятся в массиве структур. Во время инициализации процедура диалогового окна использует сообщение [**\_ ADDSTRING балансировки нагрузки**](lb-addstring.md) для добавления имен членов команды в список (**\_ \_ Пример** в списке IDC) по одному за раз. Он также использует сообщение [**\_ сетитемдата балансировки нагрузки**](lb-setitemdata.md) для добавления индекса массива проигрывателя в список в качестве данных элемента. Позже, когда пользователь выбирает проигрыватель из списка, процедура диалогового окна использует сообщение [**\_ жетитемдата балансировки нагрузки**](lb-getitemdata.md) для получения соответствующего индекса массива. Затем он использует индекс массива для получения сведений о проигрывателе из массива.



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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по элементу управления "список"](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Сведения о списках](about-list-boxes.md)
</dt> <dt>

[Использование списков](using-list-boxes.md)
</dt> </dl>

 

 




