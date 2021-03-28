---
description: API оболочки предоставляет функции, которые можно использовать для управления сетевыми принтерами. Если с файлом связана команда печати, для ее печати можно использовать команду ShellExecuteEx.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Управление принтерами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985637"
---
# <a name="managing-printers"></a><span data-ttu-id="05933-104">Управление принтерами</span><span class="sxs-lookup"><span data-stu-id="05933-104">Managing Printers</span></span>

<span data-ttu-id="05933-105">API оболочки предоставляет функции, которые можно использовать для управления сетевыми принтерами.</span><span class="sxs-lookup"><span data-stu-id="05933-105">The Shell API provides functions that you can use to manage networked printers.</span></span> <span data-ttu-id="05933-106">Если с файлом связана команда **печати** , для ее печати можно использовать команду [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="05933-106">If a file has the **print** verb associated with it, you can use the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) command to print it.</span></span>

-   [<span data-ttu-id="05933-107">Управление принтерами</span><span class="sxs-lookup"><span data-stu-id="05933-107">Printer Management</span></span>](#printer-management)
-   [<span data-ttu-id="05933-108">Печать файлов с помощью ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="05933-108">Printing Files with ShellExecuteEx</span></span>](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a><span data-ttu-id="05933-109">Управление принтерами</span><span class="sxs-lookup"><span data-stu-id="05933-109">Printer Management</span></span>

<span data-ttu-id="05933-110">Вы можете управлять принтерами в системе с помощью функции [**шинвокепринтеркомманд**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) .</span><span class="sxs-lookup"><span data-stu-id="05933-110">You can manage printers on a system with the [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) function.</span></span> <span data-ttu-id="05933-111">Эта функция позволяет выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="05933-111">This function allows you to:</span></span>

-   <span data-ttu-id="05933-112">Установка принтеров.</span><span class="sxs-lookup"><span data-stu-id="05933-112">Install printers.</span></span>
-   <span data-ttu-id="05933-113">Откройте принтеры.</span><span class="sxs-lookup"><span data-stu-id="05933-113">Open printers.</span></span>
-   <span data-ttu-id="05933-114">Получение свойств принтера.</span><span class="sxs-lookup"><span data-stu-id="05933-114">Get printer properties.</span></span>
-   <span data-ttu-id="05933-115">Создание ссылок на принтеры.</span><span class="sxs-lookup"><span data-stu-id="05933-115">Create printer links.</span></span>
-   <span data-ttu-id="05933-116">Напечатайте тестовую страницу.</span><span class="sxs-lookup"><span data-stu-id="05933-116">Print a test page.</span></span>

## <a name="printing-files-with-shellexecuteex"></a><span data-ttu-id="05933-117">Печать файлов с помощью ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="05933-117">Printing Files with ShellExecuteEx</span></span>

<span data-ttu-id="05933-118">Если с типом файла связана команда печати, можно напечатать файл, вызвав [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) с параметром **Print** в качестве команды.</span><span class="sxs-lookup"><span data-stu-id="05933-118">If a file type has a print command associated with it, you can print the file by calling [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) with **print** as the verb.</span></span> <span data-ttu-id="05933-119">Эта команда часто совпадает с той, которая используется для команды **Open** , с добавлением флага, указывающего приложению распечатать файл.</span><span class="sxs-lookup"><span data-stu-id="05933-119">This command is often the same as that used for the **open** verb, with the addition of a flag to tell the application to print the file.</span></span> <span data-ttu-id="05933-120">Например, файлы. txt могут быть распечатаны с помощью Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="05933-120">For instance, .txt files can be printed by Microsoft WordPad.</span></span> <span data-ttu-id="05933-121">Таким образом, команда **Open** для TXT-файла будет соответствовать примерно следующей команде:</span><span class="sxs-lookup"><span data-stu-id="05933-121">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



<span data-ttu-id="05933-122">При использовании [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для печати TXT-файла WordPad открывает файл, выводит его на печать, а затем закрывает, возвращая управление приложению.</span><span class="sxs-lookup"><span data-stu-id="05933-122">When you use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to print a .txt file, WordPad opens the file, prints it, and then closes, returning control to the application.</span></span> <span data-ttu-id="05933-123">Следующий пример функции принимает полный путь и использует **ShellExecuteEx** для печати, используя команду Print, связанную с расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="05933-123">The following sample function takes a fully qualified path, and uses **ShellExecuteEx** to print it, using the print command associated with its file name extension.</span></span>


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



