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
# <a name="how-to-collect-print-job-information-from-the-user"></a>Инструкции. Получение сведений о задании печати от пользователя

В этом разделе описывается, как получать сведения о задании печати от пользователя.

## <a name="overview"></a>Обзор

Получение сведений о задании печати от пользователя путем вызова функции [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . Эта функция отображает для пользователя общее диалоговое окно **печати** и возвращает сведения о задании печати в структуре данных [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .

Когда пользователь запускает задание печати, отображается общее диалоговое окно **Печать** . Диалоговое окно Общие **Печать** представляет собой модальное диалоговое окно, означающее, что пользователь не может взаимодействовать с главным окном, пока не закроется общее диалоговое окно.

## <a name="collecting-print-job-information"></a>Сбор сведений о задании печати

1.  Инициализируйте элемент структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .

    Прежде чем программа сможет отобразить общее диалоговое окно **Печать** , она должна выделить и инициализировать структуру [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Затем она передает эту структуру функции [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , которая отображает диалоговое окно и возвращает данные задания печати в той же структуре. В следующем примере кода показано, как пример программы выполняет этот шаг.

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

    

2.  Отображение общего диалогового окна **Печать** .

    Вызовите [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) с помощью инициализированной структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) , чтобы отобразить общее диалоговое окно **печати** и получить данные пользователя, как показано в следующем примере кода.

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  Сохраните поля из структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) и запустите задание печати.

    Структура [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) содержит данные, описывающие варианты выбора, сделанные пользователем в диалоговом окне Печать. Некоторые члены структуры **принтдлг** являются дескрипторами глобальных объектов памяти. [Образец программы печати](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) копирует данные из глобальных объектов памяти в блоки памяти, которыми управляет программа, и копирует другие поля из структуры **принтдлг** в поля структуры данных, определенной программой.

    После сохранения данных из структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) в структуре данных программы можно открыть диалоговое окно «Ход печати». Процедура диалогового окна «ход печати» обрабатывает сообщения диалогового окна и запускает поток обработки печати.

    В следующем примере кода показано, как скопировать данные из структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) в структуру данных программы и как запустить задание печати.

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

    

4.  Если пользователь нажимает кнопку **Отмена** в диалоговом окне **«Общие»,** дальнейшая обработка не выполняется.

 

 
