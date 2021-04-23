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
# <a name="how-to-use-streams"></a><span data-ttu-id="8c9f9-104">Использование потоков</span><span class="sxs-lookup"><span data-stu-id="8c9f9-104">How to Use Streams</span></span>

<span data-ttu-id="8c9f9-105">Потоки можно использовать для перемещения данных в элемент управления Rich Edit или из него.</span><span class="sxs-lookup"><span data-stu-id="8c9f9-105">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="8c9f9-106">Поток определяется структурой [**едитстреам**](/windows/desktop/api/Richedit/ns-richedit-editstream) , которая задает буфер и функцию обратного вызова, определяемую приложением.</span><span class="sxs-lookup"><span data-stu-id="8c9f9-106">A stream is defined by an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure, which specifies a buffer and an application-defined callback function.</span></span>

<span data-ttu-id="8c9f9-107">Чтобы считать данные в элемент управления Rich Edit (то есть поток в данных), используйте сообщение [**\_ Streaming EM**](em-streamin.md) .</span><span class="sxs-lookup"><span data-stu-id="8c9f9-107">To read data into a rich edit control (that is, stream in the data), use the [**EM\_STREAMIN**](em-streamin.md) message.</span></span> <span data-ttu-id="8c9f9-108">Элемент управления многократно вызывает функцию обратного вызова приложения, которая каждый раз передает часть данных в буфер.</span><span class="sxs-lookup"><span data-stu-id="8c9f9-108">The control repeatedly calls the application's callback function, which transfers a portion of the data into the buffer each time.</span></span>

<span data-ttu-id="8c9f9-109">Чтобы сохранить содержимое элемента управления Rich Edit (то есть потоковая передача данных), можно использовать сообщение о [**\_ потоке EM**](em-streamout.md) .</span><span class="sxs-lookup"><span data-stu-id="8c9f9-109">To save the contents of a rich edit control (that is, stream out the data), you can use the [**EM\_STREAMOUT**](em-streamout.md) message.</span></span> <span data-ttu-id="8c9f9-110">Элемент управления многократно записывает данные в буфер, а затем вызывает функцию обратного вызова приложения.</span><span class="sxs-lookup"><span data-stu-id="8c9f9-110">The control repeatedly writes to the buffer and then calls the application's callback function.</span></span> <span data-ttu-id="8c9f9-111">Для каждого вызова функция обратного вызова сохраняет содержимое буфера.</span><span class="sxs-lookup"><span data-stu-id="8c9f9-111">For each call, the callback function saves the contents of the buffer.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8c9f9-112">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="8c9f9-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8c9f9-113">Технологии</span><span class="sxs-lookup"><span data-stu-id="8c9f9-113">Technologies</span></span>

-   [<span data-ttu-id="8c9f9-114">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="8c9f9-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8c9f9-115">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="8c9f9-115">Prerequisites</span></span>

-   <span data-ttu-id="8c9f9-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="8c9f9-116">C/C++</span></span>
-   <span data-ttu-id="8c9f9-117">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="8c9f9-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8c9f9-118">Инструкции</span><span class="sxs-lookup"><span data-stu-id="8c9f9-118">Instructions</span></span>

### <a name="use-a-stream"></a><span data-ttu-id="8c9f9-119">Использование потока</span><span class="sxs-lookup"><span data-stu-id="8c9f9-119">Use a Stream</span></span>

<span data-ttu-id="8c9f9-120">В следующем примере кода показано, как прочитать RTF-файл в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8c9f9-120">The following code example shows how to read an .rtf file into a rich edit control.</span></span> <span data-ttu-id="8c9f9-121">Этот файл передается функции обратного вызова через элемент **двкукие** структуры [**едитстреам**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="8c9f9-121">The file handle is passed to the callback function through the **dwCookie** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8c9f9-122">См. также</span><span class="sxs-lookup"><span data-stu-id="8c9f9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c9f9-123">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="8c9f9-123">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="8c9f9-124">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="8c9f9-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




