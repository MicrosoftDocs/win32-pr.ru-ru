---
title: Создание списка Multiple-Selection
description: В этом разделе показано, как отобразить содержимое каталога и получить доступ к нему в списке с множественным выбором.
ms.assetid: 5192E171-8CEF-4921-9378-A7C3A52A9024
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd47b1d582d53a66bc77284927aef4230043e92
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070871"
---
# <a name="how-to-create-a-multiple-selection-list-box"></a>Создание списка Multiple-Selection

В этом разделе показано, как отобразить содержимое каталога и получить доступ к нему в списке с множественным выбором. В списке с множественным выбором пользователь может одновременно выбрать несколько элементов.

Пример кода C++ в этом разделе позволяет пользователю просматривать список файлов в текущем каталоге, выбирать из списка группу файлов и удалять их.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции


Приложение, содержащее список каталогов, должно выполнять следующие задачи, связанные с окном списка.

-   Инициализируйте список.
-   Получение параметров пользователя из списка.
-   Удалить имена файлов из списка после удаления выбранных файлов.

В следующем примере кода C++ процедура диалогового окна инициализирует список с множественным выбором (IDC \_ FileList) с помощью функции [**длгдирлист**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) для заполнения списка именами всех файлов в текущем каталоге.

Когда пользователь выбирает группу файлов и нажимает кнопку **Удалить** , процедура диалогового окна отправляет сообщение [**\_ жетселкаунт балансировки нагрузки**](lb-getselcount.md) , чтобы получить количество выбранных файлов и сообщение [**\_ жетселитемс балансировки нагрузки**](lb-getselitems.md) , чтобы получить массив выбранных элементов списка. После удаления файла процедура диалогового окна удаляет соответствующий элемент из списка, отправляя сообщение [**\_ делетестринг балансировки нагрузки**](lb-deletestring.md) .



```C++
#define BIGBUFF 8192 
 
INT_PTR CALLBACK DlgDelFilesProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int cSelItems; 
    int cSelItemsInBuffer; 
    TCHAR achBuffer[MAX_PATH]; 
    int aSelItems[BIGBUFF]; 
    int i; 
    BOOL fResult; 
    HWND hListBox;
    int iRet;
 
    switch (message) { 
 
        case WM_INITDIALOG: 
 
            // Initialize the list box by filling it with files from 
            // the current directory. 
            pszCurDir = achBuffer; 
            GetCurrentDirectory(MAX_PATH, pszCurDir);
            DlgDirList(hDlg, pszCurDir, IDC_FILELIST, IDS_PATHTOFILL, 0); 
            SetFocus(GetDlgItem(hDlg, IDC_FILELIST)); 
 
            return FALSE; 
 
        case WM_COMMAND: 
 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
 
                    // When the user presses the DEL (IDOK) button, 
                    // first retrieve the list of selected files. 
                    pszFileToDelete = achBuffer; 
                    hListBox = GetDlgItem(hDlg, IDC_FILELIST); 
                    cSelItems = SendMessage(hListBox, 
                            LB_GETSELCOUNT, 0, 0); 
 
                    cSelItemsInBuffer = SendMessage(hListBox, 
                            LB_GETSELITEMS, 512, (LPARAM) aSelItems); 
 
                    if (cSelItems > cSelItemsInBuffer) 
                    { 
                        MessageBox(hDlg, L"Too many items selected.", 
                                NULL, MB_OK); 
                    } 
                    else 
                    { 

                        // Make sure the user really wants to delete the files.
                        iRet = MessageBox(hDlg, 
                            L"Are you sure you want to delete these files?", 
                            L"Deleting Files", MB_YESNO | MB_ICONEXCLAMATION);
                        if (iRet == IDNO)
                            return TRUE;

                        // Go through the list backward because after deleting
                        // an item the indices change for every subsequent 
                        // item. By going backward, the indices are never 
                        // invalidated. 
                        for (i = cSelItemsInBuffer - 1; i >= 0; i--) 
                        { 
                            SendMessage(hListBox, LB_GETTEXT, 
                                        aSelItems[i], 
                                        (LPARAM) pszFileToDelete); 
 
                            fResult = DeleteFile(pszFileToDelete); 
                            if (!fResult) 
                            {                     
                                MessageBox(hDlg, L"Could not delete file.", 
                                    NULL, MB_OK);     
                            } 
                            else 
                            { 
                                SendMessage(hListBox, LB_DELETESTRING, 
                                        aSelItems[i], 0); 
                            } 
                        } 
                        SendMessage(hListBox, LB_SETCARETINDEX, 0, 0); 
                    } 
                    return TRUE; 
 
                case IDCANCEL: 
 
                    // Destroy the dialog box. 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    return FALSE; 
            } 
 
        default: 
                return FALSE; 
    } 
} 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по элементу управления "список"](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Сведения о списках](about-list-boxes.md)
</dt> <dt>

[Использование списков](using-list-boxes.md)
</dt> </dl>

 

 




