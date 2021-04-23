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
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a><span data-ttu-id="cbff7-103">Создание списка каталогов в списке с одним выбором</span><span class="sxs-lookup"><span data-stu-id="cbff7-103">How to create a directory listing in a single-selection ListBox</span></span>

<span data-ttu-id="cbff7-104">В этом разделе показано, как использовать список с одним выбором для отображения и доступа к содержимому каталога.</span><span class="sxs-lookup"><span data-stu-id="cbff7-104">This topic demonstrates how to use a single-selection list box to display and access the contents of a directory.</span></span> <span data-ttu-id="cbff7-105">Список с одним выбором является типом списка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cbff7-105">The single-selection list box is the default list box type.</span></span> <span data-ttu-id="cbff7-106">Пользователь может выбрать только один элемент за раз из списка с одним выбором.</span><span class="sxs-lookup"><span data-stu-id="cbff7-106">A user can only select one item at a time from a single-selection list box.</span></span>

<span data-ttu-id="cbff7-107">Пример кода C++ в этом разделе позволяет пользователю просмотреть список файлов в текущем каталоге, выбрать файл из списка и удалить его.</span><span class="sxs-lookup"><span data-stu-id="cbff7-107">The C++ code example in this topic enables a user to view a list of files in the current directory, select a file from the list, and delete it.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cbff7-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="cbff7-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cbff7-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="cbff7-109">Technologies</span></span>

-   [<span data-ttu-id="cbff7-110">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="cbff7-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cbff7-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="cbff7-111">Prerequisites</span></span>

-   <span data-ttu-id="cbff7-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="cbff7-112">C/C++</span></span>
-   <span data-ttu-id="cbff7-113">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="cbff7-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cbff7-114">Инструкции</span><span class="sxs-lookup"><span data-stu-id="cbff7-114">Instructions</span></span>


<span data-ttu-id="cbff7-115">Приложение, содержащее список каталогов, должно выполнять следующие задачи, связанные со списком:</span><span class="sxs-lookup"><span data-stu-id="cbff7-115">The directory listing application must perform the following list box related tasks:</span></span>

-   <span data-ttu-id="cbff7-116">Инициализируйте список.</span><span class="sxs-lookup"><span data-stu-id="cbff7-116">Initialize the list box.</span></span>
-   <span data-ttu-id="cbff7-117">Извлеките выбранные пользователем элементы из списка.</span><span class="sxs-lookup"><span data-stu-id="cbff7-117">Retrieve the user's selection from the list box.</span></span>
-   <span data-ttu-id="cbff7-118">Удалите имя файла из списка после удаления выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="cbff7-118">Remove the file name from the list box after the selected file has been deleted.</span></span>

<span data-ttu-id="cbff7-119">В следующем примере кода C++ процедура диалогового окна инициализирует список с единственным выбором (IDC \_ FileList) с помощью функции [**длгдирлист**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) для заполнения списка именами всех файлов в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="cbff7-119">In the following C++ code example, the dialog box procedure initializes the single-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span> <span data-ttu-id="cbff7-120">Когда пользователь выбирает файл и нажимает кнопку **Удалить** , функция [**длгдирселектекс**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) извлекает имя выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="cbff7-120">When the user selects a file and chooses the **Delete** button, the [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) function retrieves the name of the selected file.</span></span> <span data-ttu-id="cbff7-121">Код удаляет файл с помощью функции [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) и обновляет список каталогов, отправляя сообщение [**\_ делетестринг балансировки нагрузки**](lb-deletestring.md) .</span><span class="sxs-lookup"><span data-stu-id="cbff7-121">The code deletes the file by using the [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) function and updates the directory list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="cbff7-122">См. также</span><span class="sxs-lookup"><span data-stu-id="cbff7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbff7-123">Справочник по элементу управления "список"</span><span class="sxs-lookup"><span data-stu-id="cbff7-123">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="cbff7-124">Сведения о списках</span><span class="sxs-lookup"><span data-stu-id="cbff7-124">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="cbff7-125">Использование списков</span><span class="sxs-lookup"><span data-stu-id="cbff7-125">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 