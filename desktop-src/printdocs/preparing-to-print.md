---
description: В этом разделе описывается, как получать сведения о задании печати от пользователя.
ms.assetid: 98ae97e2-25c1-455c-8283-45bb07fb8251
title: Инструкции. Получение сведений о задании печати от пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4ddbc874ddbb36aa9b82e8eafeadb46883f528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080774"
---
# <a name="how-to-collect-print-job-information-from-the-user"></a><span data-ttu-id="0731e-103">Инструкции. Получение сведений о задании печати от пользователя</span><span class="sxs-lookup"><span data-stu-id="0731e-103">How To: Collect Print Job Information from the User</span></span>

<span data-ttu-id="0731e-104">В этом разделе описывается, как получать сведения о задании печати от пользователя.</span><span class="sxs-lookup"><span data-stu-id="0731e-104">This topic describes how to collect print job information from the user.</span></span>

## <a name="overview"></a><span data-ttu-id="0731e-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="0731e-105">Overview</span></span>

<span data-ttu-id="0731e-106">Получение сведений о задании печати от пользователя путем вызова функции [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0731e-106">Collect print job information from the user by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="0731e-107">Эта функция отображает для пользователя общее диалоговое окно **печати** и возвращает сведения о задании печати в структуре данных [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="0731e-107">This function displays the **Print** common dialog box to the user, and returns the print job information in a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>

<span data-ttu-id="0731e-108">Когда пользователь запускает задание печати, отображается общее диалоговое окно **Печать** .</span><span class="sxs-lookup"><span data-stu-id="0731e-108">The **Print** common dialog box is displayed when the user starts a print job.</span></span> <span data-ttu-id="0731e-109">Диалоговое окно Общие **Печать** представляет собой модальное диалоговое окно, означающее, что пользователь не может взаимодействовать с главным окном, пока не закроется общее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="0731e-109">The **Print** common dialog box is a modal dialog box, which means that the user cannot interact with the main window until the common dialog box is closed.</span></span>

## <a name="collecting-print-job-information"></a><span data-ttu-id="0731e-110">Сбор сведений о задании печати</span><span class="sxs-lookup"><span data-stu-id="0731e-110">Collecting Print Job Information</span></span>

1.  <span data-ttu-id="0731e-111">Инициализируйте элемент структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="0731e-111">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure element.</span></span>

    <span data-ttu-id="0731e-112">Прежде чем программа сможет отобразить общее диалоговое окно **Печать** , она должна выделить и инициализировать структуру [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="0731e-112">Before a program can display the **Print** common dialog box , it must allocate and initialize a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="0731e-113">Затем она передает эту структуру функции [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , которая отображает диалоговое окно и возвращает данные задания печати в той же структуре.</span><span class="sxs-lookup"><span data-stu-id="0731e-113">It then passes this structure to the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, which displays the dialog and returns the print job data in the same structure.</span></span> <span data-ttu-id="0731e-114">В следующем примере кода показано, как пример программы выполняет этот шаг.</span><span class="sxs-lookup"><span data-stu-id="0731e-114">The following code example shows how the sample program performs this step.</span></span>

    ```C++
    // Initialize the print dialog box's data structure.
    pd.lStructSize = sizeof( pd );
    pd.Flags = 
        // Return a printer device context
        PD_RETURNDC 
        // Don't allow separate print to file.
        | PD_HIDEPRINTTOFILE        
        | PD_DISABLEPRINTTOFILE 
        // Don't allow selecting individual document pages to print.
        | PD_NOSELECTION;
    ```

    

2.  <span data-ttu-id="0731e-115">Отображение общего диалогового окна **Печать** .</span><span class="sxs-lookup"><span data-stu-id="0731e-115">Display the **Print** common dialog box.</span></span>

    <span data-ttu-id="0731e-116">Вызовите [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) с помощью инициализированной структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) , чтобы отобразить общее диалоговое окно **печати** и получить данные пользователя, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0731e-116">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) with the initialized [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to display the **Print** common dialog box and collect the user data, as shown in the following code example.</span></span>

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  <span data-ttu-id="0731e-117">Сохраните поля из структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) и запустите задание печати.</span><span class="sxs-lookup"><span data-stu-id="0731e-117">Save the fields from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and start the print job.</span></span>

    <span data-ttu-id="0731e-118">Структура [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) содержит данные, описывающие варианты выбора, сделанные пользователем в диалоговом окне Печать.</span><span class="sxs-lookup"><span data-stu-id="0731e-118">The [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure contains the data that describes the selections that the user made in the print dialog box.</span></span> <span data-ttu-id="0731e-119">Некоторые члены структуры **принтдлг** являются дескрипторами глобальных объектов памяти.</span><span class="sxs-lookup"><span data-stu-id="0731e-119">Some members of the **PRINTDLG** structure are handles to global memory objects.</span></span> <span data-ttu-id="0731e-120">[Образец программы печати](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) копирует данные из глобальных объектов памяти в блоки памяти, которыми управляет программа, и копирует другие поля из структуры **принтдлг** в поля структуры данных, определенной программой.</span><span class="sxs-lookup"><span data-stu-id="0731e-120">The [Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copies the data from the global memory objects to memory blocks that the program manages and copies other fields from the **PRINTDLG** structure to fields in a data structure that the program defined.</span></span>

    <span data-ttu-id="0731e-121">После сохранения данных из структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) в структуре данных программы можно открыть диалоговое окно «Ход печати».</span><span class="sxs-lookup"><span data-stu-id="0731e-121">After you store the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure in the program's data structure, you can open the print progress dialog box.</span></span> <span data-ttu-id="0731e-122">Процедура диалогового окна «ход печати» обрабатывает сообщения диалогового окна и запускает поток обработки печати.</span><span class="sxs-lookup"><span data-stu-id="0731e-122">The print progress dialog box procedure handles the dialog box messages and starts the print processing thread.</span></span>

    <span data-ttu-id="0731e-123">В следующем примере кода показано, как скопировать данные из структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) в структуру данных программы и как запустить задание печати.</span><span class="sxs-lookup"><span data-stu-id="0731e-123">The following code example shows how to copy the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to the program's data structure and how to start the print job.</span></span>

    ```C++
    // A printer was returned so copy the information from 
    //  the dialog box structure and save it to the application's
    //  data structure.
    //
    //  Lock the handles to get pointers to the memory they refer to.
    PDEVMODE    devmode = (PDEVMODE)GlobalLock(pd.hDevMode);
    LPDEVNAMES  devnames = (LPDEVNAMES)GlobalLock(pd.hDevNames);

    // Free any old devmode structures and allocate a new one and
    // copy the data to the application's data structure.
    if (NULL != threadInfo->devmode)
    {
        HeapFree(GetProcessHeap(), 0L, threadInfo->devmode);
    }

    threadInfo->devmode = (LPDEVMODE)HeapAlloc(
        GetProcessHeap(), 
        PRINT_SAMPLE_HEAP_FLAGS, 
        devmode->dmSize);

    if (NULL != threadInfo->devmode) 
    {
        memcpy(
            (LPVOID)threadInfo->devmode,
            devmode, 
            devmode->dmSize);
    }
    else
    {
        // Unable to allocate a new structure so leave
        // the pointer as NULL to indicate that it's empty.
    }

    // Save the printer name from the devmode structure
    //  This is to make it easier to use. It could be
    //  used directly from the devmode structure.
    threadInfo->printerName = threadInfo->devmode->dmDeviceName;

    // Set the number of copies as entered by the user
    threadInfo->copies = pd.nCopies;

    // Some implementations might support printing more than
    // one package in a print job. For this program, only
    // one package (XPS document) can be printed per print job.
    threadInfo->packages = 1;

    // free allocated buffers from PRINTDLG structure
    if (NULL != pd.hDevMode) GlobalFree(pd.hDevMode);
    if (NULL != pd.hDevNames) GlobalFree(pd.hDevNames);

    // Display the print progress dialog box
    DialogBox(
        threadInfo->applicationInstance, 
        MAKEINTRESOURCE(IDD_PRINT_DLG), 
        hWnd, 
        PrintDlgProc);
    ```

    

4.  <span data-ttu-id="0731e-124">Если пользователь нажимает кнопку **Отмена** в диалоговом окне **«Общие»,** дальнейшая обработка не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0731e-124">If the user clicks the **Cancel** button in the **Print** common dialog box, no further processing is performed.</span></span>

 

 
