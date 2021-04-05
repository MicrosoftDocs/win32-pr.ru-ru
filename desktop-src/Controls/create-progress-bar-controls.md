---
title: Использование элементов управления "индикатор выполнения"
description: В этом разделе объясняется, как использовать индикатор выполнения для указания хода выполнения длительной операции синтаксического анализа файлов.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c71ff33a14f2d2af5fa8735c5197c50acaa948b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987936"
---
# <a name="how-to-use-progress-bar-controls"></a><span data-ttu-id="4aada-103">Использование элементов управления "индикатор выполнения"</span><span class="sxs-lookup"><span data-stu-id="4aada-103">How to Use Progress Bar Controls</span></span>

<span data-ttu-id="4aada-104">В этом разделе объясняется, как использовать индикатор выполнения для указания хода выполнения длительной операции синтаксического анализа файлов.</span><span class="sxs-lookup"><span data-stu-id="4aada-104">This topic explains how to use a progress bar to indicate the progress of a lengthy file-parsing operation.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4aada-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="4aada-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4aada-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="4aada-106">Technologies</span></span>

-   [<span data-ttu-id="4aada-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="4aada-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="4aada-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="4aada-108">Prerequisites</span></span>

-   <span data-ttu-id="4aada-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="4aada-109">C/C++</span></span>
-   <span data-ttu-id="4aada-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="4aada-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="4aada-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="4aada-111">Instructions</span></span>

### <a name="create-a-progress-bar-control"></a><span data-ttu-id="4aada-112">Создание элемента управления "индикатор выполнения"</span><span class="sxs-lookup"><span data-stu-id="4aada-112">Create a Progress Bar Control</span></span>

<span data-ttu-id="4aada-113">В следующем примере кода создается индикатор выполнения, который размещается в нижней части клиентской области родительского окна.</span><span class="sxs-lookup"><span data-stu-id="4aada-113">The following example code creates a progress bar and positions it along the bottom of the parent window's client area.</span></span> <span data-ttu-id="4aada-114">Высота индикатора выполнения зависит от высоты растровой стрелки, используемой в полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="4aada-114">The height of the progress bar is based on the height of the arrow bitmap used in a scroll bar.</span></span> <span data-ttu-id="4aada-115">Диапазон основан на размере файла, деленном на 2 048. это размер каждого фрагмента данных, считываемых из файла.</span><span class="sxs-lookup"><span data-stu-id="4aada-115">The range is based on the size of the file divided by 2,048, which is the size of each "chunk" of data that is read from the file.</span></span> <span data-ttu-id="4aada-116">Этот пример также задает приращение и перемещает текущую позицию индикатора выполнения на шаг после анализа каждого фрагмента.</span><span class="sxs-lookup"><span data-stu-id="4aada-116">The example also sets an increment and advances the current position of the progress bar by the increment after parsing each chunk.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="4aada-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4aada-117">Remarks</span></span>

<span data-ttu-id="4aada-118">Необходимо правильно использовать функцию [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) , чтобы обеспечить безопасность приложения.</span><span class="sxs-lookup"><span data-stu-id="4aada-118">You must make sure to use the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function correctly, to ensure the security of your application.</span></span> <span data-ttu-id="4aada-119">Например, в примере кода следует проверить, чтобы убедиться, что `ReadFile` считывает все запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="4aada-119">For instance, in the example code, you should check to make sure that `ReadFile` actually reads all of the requested data.</span></span>

<span data-ttu-id="4aada-120">Также обратите внимание, что четвертый параметр [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)— (лпсекурити \_ Attributes)**null**— задает значения безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4aada-120">Also notice that the fourth parameter of [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)—(LPSECURITY\_ATTRIBUTES)**NULL**—sets default security values.</span></span> <span data-ttu-id="4aada-121">Если требуются определенные параметры безопасности, необходимо задать соответствующие значения в элементах структуры.</span><span class="sxs-lookup"><span data-stu-id="4aada-121">If you need specific security settings, you must set the appropriate values in the structure's members.</span></span> <span data-ttu-id="4aada-122">Вызовите **sizeof** , чтобы задать правильный размер структуры **\_ атрибутов лпсекурити** .</span><span class="sxs-lookup"><span data-stu-id="4aada-122">Call **sizeof** to set the correct size of the **LPSECURITY\_ATTRIBUTES** structure.</span></span>

<span data-ttu-id="4aada-123">Дополнительные сведения см. в разделе [вопросы безопасности: элементы управления Microsoft Windows](sec-comctls.md).</span><span class="sxs-lookup"><span data-stu-id="4aada-123">For more information, see [Security Considerations: Microsoft Windows Controls](sec-comctls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4aada-124">См. также</span><span class="sxs-lookup"><span data-stu-id="4aada-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aada-125">Использование элементов управления "индикатор выполнения"</span><span class="sxs-lookup"><span data-stu-id="4aada-125">Using Progress Bar Controls</span></span>](using-progress-bar-controls.md)
</dt> <dt>

[<span data-ttu-id="4aada-126">Вопросы безопасности: элементы управления Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="4aada-126">Security Considerations: Microsoft Windows Controls</span></span>](sec-comctls.md)
</dt> </dl>

 

 