---
title: Создание списка каталогов в ListBox
description: В этом разделе показано, как использовать список с одним выбором для отображения и доступа к содержимому каталога.
ms.assetid: 11C0DB10-59BA-47C4-8687-101A2A85D660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03829990605271574a2030486ac5aba428867ec3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103987993"
---
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a>Создание списка каталогов в списке с одним выбором

В этом разделе показано, как использовать список с одним выбором для отображения и доступа к содержимому каталога. Список с одним выбором является типом списка по умолчанию. Пользователь может выбрать только один элемент за раз из списка с одним выбором.

Пример кода C++ в этом разделе позволяет пользователю просмотреть список файлов в текущем каталоге, выбрать файл из списка и удалить его.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции


Приложение, содержащее список каталогов, должно выполнять следующие задачи, связанные со списком:

-   Инициализируйте список.
-   Извлеките выбранные пользователем элементы из списка.
-   Удалите имя файла из списка после удаления выбранного файла.

В следующем примере кода C++ процедура диалогового окна инициализирует список с единственным выбором (IDC \_ FileList) с помощью функции [**длгдирлист**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) для заполнения списка именами всех файлов в текущем каталоге. Когда пользователь выбирает файл и нажимает кнопку **Удалить** , функция [**длгдирселектекс**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) извлекает имя выбранного файла. Код удаляет файл с помощью функции [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) и обновляет список каталогов, отправляя сообщение [**\_ делетестринг балансировки нагрузки**](lb-deletestring.md) .



```C++
INT_PTR CALLBACK DlgDelFileProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int iLBItem; 
    int cStringsRemaining; 
    int iRet; 
    TCHAR achBuffer[MAX_PATH]; 
    TCHAR achTemp[MAX_PATH]; 
    BOOL fResult;     
 
    switch (message) 
    { 
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
                    // first retrieve the selected file. 
                    pszFileToDelete = achBuffer; 
                    DlgDirSelectEx(hDlg, pszFileToDelete, MAX_PATH, 
                        IDC_FILELIST); 

                    // Make sure the user really wants to delete the file.
                    achTemp[MAX_PATH];
                    StringCbPrintf (achTemp, ARRAYSIZE(achTemp),  
                            TEXT("Are you sure you want to delete %s?"), 
                            pszFileToDelete);
                    iRet = MessageBox(hDlg, achTemp, L"Deleting Files", 
                        MB_YESNO | MB_ICONEXCLAMATION);
                    if (iRet == IDNO)
                        return TRUE;;

                    // Delete the file.
                    fResult = DeleteFile(pszFileToDelete); 
                    if (!fResult) 
                    { 
                        MessageBox(hDlg, L"Could not delete file.", 
                            NULL, MB_OK); 
                    } 
                    else // Remove the filename from the list box.
                    { 
                        // Get the selected item.
                        iLBItem = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_GETCURSEL, 0, 0); 
 
                        // Delete the selected item.
                        cStringsRemaining = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_DELETESTRING, iLBItem, 0); 
 
                        // If this is not the last item, set the selection to 
                        // the item immediately following the one just deleted.
                        // Otherwise, set the selection to the last item.
                         if (cStringsRemaining > iLBItem) 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, iLBItem, 0); 
                        } 
                        else 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, cStringsRemaining, 0); 
                        } 
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

 

 