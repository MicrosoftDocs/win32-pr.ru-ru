---
title: Использование элементов управления "индикатор выполнения"
description: В этом разделе объясняется, как использовать индикатор выполнения для указания хода выполнения длительной операции синтаксического анализа файлов.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e65d47d6b41422853d401a1fb2686e03e3d3f5bc378b78b7ba762b86fc7ffe30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826424"
---
# <a name="how-to-use-progress-bar-controls"></a>Использование элементов управления "индикатор выполнения"

В этом разделе объясняется, как использовать индикатор выполнения для указания хода выполнения длительной операции синтаксического анализа файлов.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="create-a-progress-bar-control"></a>Создание элемента управления "индикатор выполнения"

В следующем примере кода создается индикатор выполнения, который размещается в нижней части клиентской области родительского окна. Высота индикатора выполнения зависит от высоты растровой стрелки, используемой в полосе прокрутки. Диапазон основан на размере файла, деленном на 2 048. это размер каждого фрагмента данных, считываемых из файла. Этот пример также задает приращение и перемещает текущую позицию индикатора выполнения на шаг после анализа каждого фрагмента.


```C++
// ParseALargeFile - uses a progress bar to indicate the progress of a parsing operation.
//
// Returns TRUE if successful, or FALSE otherwise.
//
// hwndParent - parent window of the progress bar.
//
// lpszFileName - name of the file to parse. 
// 
// Global variable 
//     g_hinst - instance handle.
//

extern HINSTANCE g_hinst; 

BOOL ParseALargeFile(HWND hwndParent, LPTSTR lpszFileName) 
{ 
    RECT rcClient;  // Client area of parent window.
    int cyVScroll;  // Height of scroll bar arrow.
    HWND hwndPB;    // Handle of progress bar.
    HANDLE hFile;   // Handle of file.
    DWORD cb;       // Size of file and count of bytes read.
    LPCH pch;       // Address of data read from file.
    LPCH pchTmp;    // Temporary pointer.

    // Ensure that the common control DLL is loaded, and create a progress bar 
    // along the bottom of the client area of the parent window. 
    //
    // Base the height of the progress bar on the height of a scroll bar arrow.
    
    InitCommonControls(); 
    
    GetClientRect(hwndParent, &rcClient); 
    
    cyVScroll = GetSystemMetrics(SM_CYVSCROLL); 

    hwndPB = CreateWindowEx(0, PROGRESS_CLASS, (LPTSTR) NULL, 
                            WS_CHILD | WS_VISIBLE, rcClient.left, 
                            rcClient.bottom - cyVScroll, 
                            rcClient.right, cyVScroll, 
                            hwndParent, (HMENU) 0, g_hinst, NULL);

    // Open the file for reading, and retrieve the size of the file. 

    hFile = CreateFile(lpszFileName, GENERIC_READ, FILE_SHARE_READ, 
                       (LPSECURITY_ATTRIBUTES) NULL, OPEN_EXISTING, 
                       FILE_ATTRIBUTE_NORMAL, (HANDLE) NULL); 

    if (hFile == (HANDLE) INVALID_HANDLE_VALUE)
        return FALSE; 

    cb = GetFileSize(hFile, (LPDWORD) NULL); 

    // Set the range and increment of the progress bar. 

    SendMessage(hwndPB, PBM_SETRANGE, 0, MAKELPARAM(0, cb / 2048));
    
    SendMessage(hwndPB, PBM_SETSTEP, (WPARAM) 1, 0); 

    // Parse the file. 
    pch = (LPCH) LocalAlloc(LPTR, sizeof(char) * 2048); 
    
    pchTmp = pch; 
    
    do { 
        ReadFile(hFile, pchTmp, sizeof(char) * 2048, &cb, (LPOVERLAPPED) NULL);
        
        // TODO: Write an error handler to check that all the
        // requested data was read.
        //
        // Include here any code that parses the
        // file. 
        //  
        //  
        //  
        // Advance the current position of the progress bar by the increment.
        
        SendMessage(hwndPB, PBM_STEPIT, 0, 0); 
        
    } while (cb); 

    CloseHandle((HANDLE) hFile);
    
    DestroyWindow(hwndPB);

    return TRUE; 
}
```



## <a name="remarks"></a>Remarks

Необходимо правильно использовать функцию [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) , чтобы обеспечить безопасность приложения. Например, в примере кода следует проверить, чтобы убедиться, что `ReadFile` считывает все запрошенные данные.

Также обратите внимание, что четвертый параметр [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)— (лпсекурити \_ Attributes)**null**— задает значения безопасности по умолчанию. Если требуются определенные параметры безопасности, необходимо задать соответствующие значения в элементах структуры. Вызовите **sizeof** , чтобы задать правильный размер структуры **\_ атрибутов лпсекурити** .

дополнительные сведения см. в разделе [вопросы безопасности: элементы управления Microsoft Windows](sec-comctls.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления "индикатор выполнения"](using-progress-bar-controls.md)
</dt> <dt>

[вопросы безопасности: элементы управления Microsoft Windows](sec-comctls.md)
</dt> </dl>

 

 