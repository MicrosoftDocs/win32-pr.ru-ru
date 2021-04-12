---
title: Использование потоков
description: Потоки можно использовать для перемещения данных в элемент управления Rich Edit или из него. Поток определяется структурой ЕДИТСТРЕАМ, которая задает буфер и функцию обратного вызова, определяемую приложением.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89a9cc2a8caa157f9c65220fc5cead7564bc555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "104133618"
---
# <a name="how-to-use-streams"></a>Использование потоков

Потоки можно использовать для перемещения данных в элемент управления Rich Edit или из него. Поток определяется структурой [**едитстреам**](/windows/desktop/api/Richedit/ns-richedit-editstream) , которая задает буфер и функцию обратного вызова, определяемую приложением.

Чтобы считать данные в элемент управления Rich Edit (то есть поток в данных), используйте сообщение [**\_ Streaming EM**](em-streamin.md) . Элемент управления многократно вызывает функцию обратного вызова приложения, которая каждый раз передает часть данных в буфер.

Чтобы сохранить содержимое элемента управления Rich Edit (то есть потоковая передача данных), можно использовать сообщение о [**\_ потоке EM**](em-streamout.md) . Элемент управления многократно записывает данные в буфер, а затем вызывает функцию обратного вызова приложения. Для каждого вызова функция обратного вызова сохраняет содержимое буфера.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="use-a-stream"></a>Использование потока

В следующем примере кода показано, как прочитать RTF-файл в элементе управления Rich Edit. Этот файл передается функции обратного вызова через элемент **двкукие** структуры [**едитстреам**](/windows/desktop/api/Richedit/ns-richedit-editstream) .


```C++
DWORD CALLBACK EditStreamCallback(DWORD_PTR dwCookie, 
                                  LPBYTE lpBuff,
                                  LONG cb, 
                                  PLONG pcb)
{
    HANDLE hFile = (HANDLE)dwCookie;
    
    if (ReadFile(hFile, lpBuff, cb, (DWORD *)pcb, NULL)) 
    {
        return 0;
    }
    
    return -1;
}

BOOL FillRichEditFromFile(HWND hwnd, LPCTSTR pszFile)
{
    BOOL fSuccess = FALSE;
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, 
                              FILE_SHARE_READ, 0, OPEN_EXISTING,
                              FILE_FLAG_SEQUENTIAL_SCAN, NULL);
        
    if (hFile != INVALID_HANDLE_VALUE) 
    {
        EDITSTREAM es = { 0 };
        
        es.pfnCallback = EditStreamCallback;
        es.dwCookie    = (DWORD_PTR)hFile;
        
        if (SendMessage(hwnd, EM_STREAMIN, SF_RTF, (LPARAM)&es) && es.dwError == 0) 
        {
                fSuccess = TRUE;
        }
        
        CloseHandle(hFile);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




