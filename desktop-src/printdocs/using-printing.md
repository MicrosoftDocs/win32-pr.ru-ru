---
description: В этом разделе описывается, как выполнить печать из встроенной программы Windows Desktop.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Настольное приложение для печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbecbac997d000f50e7c912e57be42cc8fe239b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664343"
---
# <a name="desktop-app-printing"></a><span data-ttu-id="cc1c6-103">Настольное приложение для печати</span><span class="sxs-lookup"><span data-stu-id="cc1c6-103">Desktop App Printing</span></span>

<span data-ttu-id="cc1c6-104">В этом разделе описывается, как выполнить печать из встроенной программы Windows Desktop.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-104">This section describes how to print from a native Windows desktop program.</span></span>

## <a name="overview"></a><span data-ttu-id="cc1c6-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="cc1c6-105">Overview</span></span>

<span data-ttu-id="cc1c6-106">Чтобы обеспечить оптимальное взаимодействие с пользователем при печати из собственной программы Windows, программа должна быть разработана для печати из выделенного потока.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-106">To provide the best user experience when you print from a native Windows program, the program must be designed to print from a dedicated thread.</span></span> <span data-ttu-id="cc1c6-107">В собственной программе Windows программа отвечает за управление событиями и сообщениями пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-107">In a native Windows program, the program is responsible for managing user interface events and messages.</span></span> <span data-ttu-id="cc1c6-108">Операции печати могут потребовать периодов интенсивных вычислений по мере подготовки содержимого приложения для принтера, что может помешать программе реагировать на взаимодействие с пользователем, если эта обработка выполняется в том же потоке, что и обработка событий пользователем.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-108">Printing operations can require periods of intense computation as the application content is rendered for the printer, which can prevent the program from responding to user interaction if this processing is performed in the same thread as event processing of the user interaction.</span></span>

<span data-ttu-id="cc1c6-109">Если вы уже знакомы с написанием многопоточной собственной программы Windows, вы сразу переходите к [способу печати из приложения Windows](how-to--print-from-a-windows-application.md) и научитесь добавлять в программу функции печати.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-109">If you are already familiar with how to write a multi-threaded native Windows program, you go directly to [How to print from a Windows application](how-to--print-from-a-windows-application.md) and learn how to add printing functionality to your program.</span></span>

### <a name="basic-windows-program-requirements"></a><span data-ttu-id="cc1c6-110">Основные требования к программе Windows</span><span class="sxs-lookup"><span data-stu-id="cc1c6-110">Basic Windows Program Requirements</span></span>

<span data-ttu-id="cc1c6-111">Для лучшей производительности и скорости реагирования программы не следует выполнять обработку задания печати программы в потоке, обрабатывающем взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-111">For best performance and program responsiveness, do not perform a program's print job processing in the thread that processes user interaction.</span></span>

<span data-ttu-id="cc1c6-112">Такое разделение печати от взаимодействия с пользователем влияет на то, как программа управляет данными приложения.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-112">This separation of printing from user interaction will influence how the program manages the application data.</span></span> <span data-ttu-id="cc1c6-113">Прежде чем приступить к написанию приложения, необходимо тщательно разобраться с этими последствиями.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-113">You should thoroughly understand these implications before you start writing the application.</span></span> <span data-ttu-id="cc1c6-114">В следующих разделах описаны основные требования к обработке печати в отдельном потоке программы.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-114">The following topics describe the basic requirements of handling printing in a separate thread of a program.</span></span>

### <a name="windows-program-basics"></a><span data-ttu-id="cc1c6-115">Основные сведения о программе Windows</span><span class="sxs-lookup"><span data-stu-id="cc1c6-115">Windows Program Basics</span></span>

<span data-ttu-id="cc1c6-116">Собственная программа Windows должна предоставить главную процедуру окна для обработки сообщений окна, получаемых от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-116">A native Windows program must provide the main window procedure to process the window messages that it receives from the operating system.</span></span> <span data-ttu-id="cc1c6-117">Каждое окно в программе Windows имеет соответствующую функцию **WndProc** , которая обрабатывает эти сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-117">Every window in a Windows program has a corresponding **WndProc** function that processes these window messages.</span></span> <span data-ttu-id="cc1c6-118">Поток, в котором выполняется эта функция, называется пользовательским интерфейсом или потоком интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-118">The thread in which this function runs is called the user interface, or UI, thread.</span></span>

<span data-ttu-id="cc1c6-119">**Используйте ресурсы для строк.**</span><span class="sxs-lookup"><span data-stu-id="cc1c6-119">**Use resources for strings.**</span></span>  
<span data-ttu-id="cc1c6-120">Используйте строковые ресурсы из файла ресурсов программы, а не строковые константы для строк, которые могут потребоваться изменить при поддержке другого языка.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-120">Use string resources from the program's resource file instead of string constants for strings that might need to be changed when you support another language.</span></span> <span data-ttu-id="cc1c6-121">Чтобы программа могла использовать строковый ресурс в качестве строки, программа должна извлечь ресурс из файла ресурсов и скопировать его в буфер локальной памяти.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-121">Before a program can use a string resource as a string, the program must retrieve the resource from the resource file and copy it to a local memory buffer.</span></span> <span data-ttu-id="cc1c6-122">Это требует дополнительного программирования в начале, но позволяет упростить изменение, перевод и локализацию программы в будущем.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-122">This requires some additional programming in the beginning, but allows for easier modification, translation, and localization of the program in the future.</span></span>  
<span data-ttu-id="cc1c6-123">**Обработка данных по шагам.**</span><span class="sxs-lookup"><span data-stu-id="cc1c6-123">**Process data in steps.**</span></span>  
<span data-ttu-id="cc1c6-124">Обработайте задание печати на шагах, которые могут быть прерваны.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-124">Process the print job in steps that can be interrupted.</span></span> <span data-ttu-id="cc1c6-125">Такая схема позволяет пользователю отменить длительную операцию обработки до ее завершения и помешает программе блокировать другие программы, которые могут выполняться одновременно.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-125">This design makes it possible for the user to cancel a long processing operation before it completes and prevents the program from blocking other programs that might be running at the same time.</span></span>  
<span data-ttu-id="cc1c6-126">**Используйте данные пользователя Window.**</span><span class="sxs-lookup"><span data-stu-id="cc1c6-126">**Use window user data.**</span></span>  
<span data-ttu-id="cc1c6-127">Для печати приложений часто используются несколько окон и потоков.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-127">Printing applications often have several windows and threads.</span></span> <span data-ttu-id="cc1c6-128">Чтобы обеспечить доступность данных между потоками и шагами обработки без использования статических, глобальных переменных, сослаться на структуры данных по указателю на данные, который является частью окна, в котором они используются.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-128">To keep the data available between threads and processing steps without using static, global variables, reference the data structures by a data pointer that is part of the window in which they are used.</span></span>  


<span data-ttu-id="cc1c6-129">В следующем примере кода показана Главная точка входа для приложения печати.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-129">The following code example shows a main entry point for a printing application.</span></span> <span data-ttu-id="cc1c6-130">В этом примере показано, как использовать строковые ресурсы вместо строковых констант, а также показан основной цикл обработки сообщений, который обрабатывает сообщения окна программы.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-130">This example shows how to use string resources instead of string constants and also shows the main message loop that processes the program's window messages.</span></span>


```C++
int APIENTRY 
wWinMain(
        HINSTANCE hInstance, 
        HINSTANCE hPrevInstance, 
        LPWSTR lpCmdLine, 
        int nCmdShow
)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG msg;
    HACCEL hAccelTable;
    HRESULT hr = S_OK;

    // Register the main window class name
    WCHAR szWindowClass[MAXIMUM_RESOURCE_STRING_LENGTH];            
    LoadString(
        hInstance, 
        IDC_PRINTSAMPLE, 
        szWindowClass, 
        MAXIMUM_RESOURCE_STRING_LENGTH);
    MyRegisterClass(hInstance, szWindowClass);

    // Perform application initialization:
    if (!InitInstance (hInstance, nCmdShow))
    {
        // Unable to initialize this instance of the application
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_INSTINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }    
    
    // Init COM for printing interfaces
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        // Unable to initialize COM
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_COMINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }

    hAccelTable = LoadAccelerators(
                    hInstance, 
                    MAKEINTRESOURCE(IDC_PRINTSAMPLE));

    // Main message handling loop
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    // Uninitialize (close) the COM interface
    CoUninitialize();

    return (int) msg.wParam;
}
```



### <a name="document-information"></a><span data-ttu-id="cc1c6-131">Сведения о документе</span><span class="sxs-lookup"><span data-stu-id="cc1c6-131">Document Information</span></span>

<span data-ttu-id="cc1c6-132">Встроенные программы Windows, предназначенные для печати, должны быть предназначены для многопоточной обработки.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-132">Native Windows programs that print should be designed for multi-threaded processing.</span></span> <span data-ttu-id="cc1c6-133">Одним из требований многопоточного проектирования является защита элементов данных программы, чтобы они были надежными для одновременного использования несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-133">One of the requirements of a multi-threaded design is to protect the program's data elements so that they are safe for multiple threads to use at the same time.</span></span> <span data-ttu-id="cc1c6-134">Можно защитить элементы данных с помощью объектов синхронизации и организовать данные, чтобы избежать конфликтов между потоками.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-134">You can protect data elements by using synchronization objects and organizing the data to avoid conflicts between the threads.</span></span> <span data-ttu-id="cc1c6-135">В то же время программа должна предотвращать изменения в данных программы во время ее печати.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-135">At the same time, the program must prevent changes to the program data while it is being printed.</span></span> <span data-ttu-id="cc1c6-136">Пример программы использует несколько различных многопоточных методик программирования.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-136">The sample program uses several different multi-threaded programming techniques.</span></span>

 <span data-ttu-id="cc1c6-137">**События синхронизации**</span><span class="sxs-lookup"><span data-stu-id="cc1c6-137">**Synchronization Events**</span></span>  
<span data-ttu-id="cc1c6-138">Пример программы использует события, дескрипторы потоков и функции ожидания для синхронизации обработки между потоком печати и основной программой, а также для указания того, что данные используются.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-138">The sample program uses events, thread handles, and wait functions to synchronize the processing between the print thread and the main program and to indicate that the data is in use.</span></span>  
<span data-ttu-id="cc1c6-139">**Сообщения Windows, относящиеся к приложению**</span><span class="sxs-lookup"><span data-stu-id="cc1c6-139">**Application-Specific Windows Messages**</span></span>  
<span data-ttu-id="cc1c6-140">Пример программы использует сообщения окна для конкретного приложения, чтобы сделать программу более совместимой с другими программами Windows.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-140">The sample program uses application-specific window messages to make the program more compatible with other native Windows programs.</span></span> <span data-ttu-id="cc1c6-141">Разбиение обработки на небольшие шаги и постановка в очередь этих шагов в цикле окон сообщений упрощает управление обработкой в Windows без блокировки других приложений, которые могут также выполняться на компьютере.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-141">Breaking the processing into smaller steps and queuing those steps in the window message loop makes it easier for Windows to manage the processing without blocking other applications that might also be running on the computer.</span></span>  
<span data-ttu-id="cc1c6-142">**Структуры данных**</span><span class="sxs-lookup"><span data-stu-id="cc1c6-142">**Data Structures**</span></span>  
<span data-ttu-id="cc1c6-143">Пример программы не написан на объектно-ориентированном стиле, использующем объекты и классы, хотя элементы данных группируются в структуры данных.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-143">The sample program is not written in an object-oriented style using objects and classes, although it does group data elements into data structures.</span></span> <span data-ttu-id="cc1c6-144">В примере не используется объектно-ориентированный подход, чтобы не допустить того, что один подход лучше или хуже другого.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-144">The sample does not use an object-oriented approach to avoid implying that one approach is better or worse than another.</span></span>  
<span data-ttu-id="cc1c6-145">Функции и структуры данных примера программы можно использовать в качестве отправной точки при проектировании программы.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-145">You can use the functions and data structures of the sample program as a starting point when you design your program.</span></span> <span data-ttu-id="cc1c6-146">Если вы решили спроектировать объектно-ориентированную программу или нет, важно помнить, что необходимо сгруппировать связанные элементы данных, чтобы их можно было безопасно использовать в разных потоках при необходимости.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-146">Whether you decide to design an object-oriented program or not, the important design consideration to remember is to group the related data elements so that you can use them safely in different threads as necessary.</span></span>  


### <a name="printer-device-context"></a><span data-ttu-id="cc1c6-147">Контекст устройства печати</span><span class="sxs-lookup"><span data-stu-id="cc1c6-147">Printer Device Context</span></span>

<span data-ttu-id="cc1c6-148">При печати может потребоваться отобразить содержимое, которое будет напечатано в контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-148">When printing, you might want to render the content to be printed to a device context.</span></span> <span data-ttu-id="cc1c6-149">[Инструкции. Извлечение контекста печатающего устройства](retrieving-a-printer-device-context.md) описание различных способов получения контекста устройства печати.</span><span class="sxs-lookup"><span data-stu-id="cc1c6-149">[How To: Retrieve a Printer Device Context](retrieving-a-printer-device-context.md) describes the different ways that you can obtain a printer device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc1c6-150">См. также</span><span class="sxs-lookup"><span data-stu-id="cc1c6-150">Related topics</span></span>



[<span data-ttu-id="cc1c6-151">Печать из приложения Windows</span><span class="sxs-lookup"><span data-stu-id="cc1c6-151">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)


 

 



