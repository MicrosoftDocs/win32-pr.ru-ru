---
description: В следующем коде показано, как вызвать функцию Симфромнаме.
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: Получение символьной информации по имени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f5f4477be4f494383c7d9c1ca462f3beb69690
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141271"
---
# <a name="retrieving-symbol-information-by-name"></a><span data-ttu-id="86659-103">Получение символьной информации по имени</span><span class="sxs-lookup"><span data-stu-id="86659-103">Retrieving Symbol Information by Name</span></span>

<span data-ttu-id="86659-104">В следующем коде показано, как вызвать функцию [**симфромнаме**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) .</span><span class="sxs-lookup"><span data-stu-id="86659-104">The following code demonstrates how to call the [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) function.</span></span> <span data-ttu-id="86659-105">Эта функция заполняет структуру [**\_ сведений о символах**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) .</span><span class="sxs-lookup"><span data-stu-id="86659-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="86659-106">Так как имя переменной имеет длину, необходимо предоставить буфер, достаточно большой для хранения имени, хранящегося в конце структуры **\_ сведений о символах** .</span><span class="sxs-lookup"><span data-stu-id="86659-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="86659-107">Кроме того, элемент **макснамелен** должен иметь значение, равное количеству байтов, зарезервированных для имени.</span><span class="sxs-lookup"><span data-stu-id="86659-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="86659-108">В этом примере Сзсимболнаме — это буфер, в котором хранится имя запрошенного символа.</span><span class="sxs-lookup"><span data-stu-id="86659-108">In this example, szSymbolName is a buffer that stores the name of the requested symbol.</span></span> <span data-ttu-id="86659-109">В примере предполагается, что обработчик символов инициализирован с помощью кода при [инициализации обработчика символов](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="86659-109">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
TCHAR szSymbolName[MAX_SYM_NAME];
ULONG64 buffer[(sizeof(SYMBOL_INFO) +
    MAX_SYM_NAME * sizeof(TCHAR) +
    sizeof(ULONG64) - 1) /
    sizeof(ULONG64)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

_tcscpy_s(szSymbolName, MAX_SYM_NAME, TEXT("WinMain"));
pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromName(hProcess, szSymbolName, pSymbol))
{
    // SymFromName returned success
}
else
{
    // SymFromName failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymFromName returned error : %d\n"), error);
}
```



<span data-ttu-id="86659-110">Если в приложении есть имя модуля или исходного файла, а также сведения о номере строки, он может использовать [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) для получения виртуального адреса кода.</span><span class="sxs-lookup"><span data-stu-id="86659-110">If an application has a module or source file name as well as line number information, it can use [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) to retrieve a virtual code address.</span></span> <span data-ttu-id="86659-111">Эта функция требует указатель на структуру [**\_ LINE64 Imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) , чтобы получить адрес виртуального кода.</span><span class="sxs-lookup"><span data-stu-id="86659-111">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the virtual code address.</span></span> <span data-ttu-id="86659-112">Обратите внимание, что обработчик символов может извлекать сведения о номере строки только в том случае \_ , если параметр симопт Load \_ Lines установлен с помощью функции [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="86659-112">Note that the symbol handler can retrieve line number information only when SYMOPT\_LOAD\_LINES option is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="86659-113">Этот параметр необходимо задать перед загрузкой модуля.</span><span class="sxs-lookup"><span data-stu-id="86659-113">This option must be set before loading the module.</span></span> <span data-ttu-id="86659-114">Параметр Сзмодуленаме содержит имя исходного модуля; Он является необязательным и может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="86659-114">The szModuleName parameter contains the source module name; it is optional and can be **NULL**.</span></span> <span data-ttu-id="86659-115">Параметр Сзфиленаме должен содержать имя исходного файла, а параметр Двлиненумбер должен содержать номер строки, для которой будет получен виртуальный адрес.</span><span class="sxs-lookup"><span data-stu-id="86659-115">The szFileName parameter should contain the source file name, and dwLineNumber parameter should contain the line number for which the virtual address will be retrieved.</span></span>


```C++
TCHAR  szModuleName[MAX_PATH];
TCHAR  szFileName[MAX_PATH];
DWORD  dwLineNumber;
LONG   lDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
_tcscpy_s(szModuleName, MAX_PATH, TEXT("MyApp"));
_tcscpy_s(szFileName, MAX_PATH, TEXT("main.c"));
dwLineNumber = 248;

if (SymGetLineFromName64(hProcess, szModuleName, szFileName,
    dwLineNumber, &lDisplacement, &line))
{
    // SymGetLineFromName64 returned success
}
else
{
    // SymGetLineFromName64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromName64 returned error : %d\n"), error);
}
```



 

 



