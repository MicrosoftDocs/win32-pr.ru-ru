---
description: В следующем коде показано, как вызвать функцию Симфромаддр.
ms.assetid: 63dfadea-b0c4-4050-add8-d1f3aef7a495
title: Получение символьной информации по адресу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ad9d2879dbfd5820c4aa6c2e7563a1575ebe1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141274"
---
# <a name="retrieving-symbol-information-by-address"></a><span data-ttu-id="3c33a-103">Получение символьной информации по адресу</span><span class="sxs-lookup"><span data-stu-id="3c33a-103">Retrieving Symbol Information by Address</span></span>

<span data-ttu-id="3c33a-104">В следующем коде показано, как вызвать функцию [**симфромаддр**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) .</span><span class="sxs-lookup"><span data-stu-id="3c33a-104">The following code demonstrates how to call the [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) function.</span></span> <span data-ttu-id="3c33a-105">Эта функция заполняет структуру [**\_ сведений о символах**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) .</span><span class="sxs-lookup"><span data-stu-id="3c33a-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="3c33a-106">Так как имя переменной имеет длину, необходимо предоставить буфер, достаточно большой для хранения имени, хранящегося в конце структуры **\_ сведений о символах** .</span><span class="sxs-lookup"><span data-stu-id="3c33a-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="3c33a-107">Кроме того, элемент **макснамелен** должен иметь значение, равное количеству байтов, зарезервированных для имени.</span><span class="sxs-lookup"><span data-stu-id="3c33a-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="3c33a-108">В этом примере *дваддресс* — это адрес, который должен быть сопоставлен с символом.</span><span class="sxs-lookup"><span data-stu-id="3c33a-108">In this example, *dwAddress* is the address to be mapped to a symbol.</span></span> <span data-ttu-id="3c33a-109">Функция **симфромаддр** сохранит смещение в начале символа на адрес в *двдисплацемент*.</span><span class="sxs-lookup"><span data-stu-id="3c33a-109">The **SymFromAddr** function will store an offset to the beginning of the symbol to the address in *dwDisplacement*.</span></span> <span data-ttu-id="3c33a-110">В примере предполагается, что обработчик символов инициализирован с помощью кода при [инициализации обработчика символов](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="3c33a-110">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
DWORD64  dwDisplacement = 0;
DWORD64  dwAddress = SOME_ADDRESS;

char buffer[sizeof(SYMBOL_INFO) + MAX_SYM_NAME * sizeof(TCHAR)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromAddr(hProcess, dwAddress, &dwDisplacement, pSymbol))
{
    // SymFromAddr returned success
}
else
{
    // SymFromAddr failed
    DWORD error = GetLastError();
    printf("SymFromAddr returned error : %d\n", error);
}
```



<span data-ttu-id="3c33a-111">Чтобы получить номер строки исходного кода для указанного адреса, приложение может использовать [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span><span class="sxs-lookup"><span data-stu-id="3c33a-111">To retrieve the source code line number for a specified address, an application can use [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span></span> <span data-ttu-id="3c33a-112">Эта функция требует указатель на структуру [**\_ LINE64 Imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) , чтобы получить имя исходного файла и номер строки, соответствующие указанному адресу кода.</span><span class="sxs-lookup"><span data-stu-id="3c33a-112">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the source file name and line number corresponding to a specified code address.</span></span> <span data-ttu-id="3c33a-113">Обратите внимание, что обработчик символов может извлекать сведения о номере строки только в том случае, если **симопт \_ \_ нагрузки** заданы с помощью функции [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="3c33a-113">Note that the symbol handler can retrieve line number information only when **SYMOPT\_LOAD\_LINES** is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="3c33a-114">Этот параметр необходимо задать перед загрузкой модуля.</span><span class="sxs-lookup"><span data-stu-id="3c33a-114">This option must be set before loading the module.</span></span> <span data-ttu-id="3c33a-115">Параметр Дваддресс содержит адрес кода, для которого будет располагаться имя исходного файла и номер строки.</span><span class="sxs-lookup"><span data-stu-id="3c33a-115">The dwAddress parameter contains the code address for which the source file name and line number will be located.</span></span>


```C++
DWORD64  dwAddress;
DWORD  dwDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
dwAddress = 0x1000000; // Address you want to check on.

if (SymGetLineFromAddr64(hProcess, dwAddress, &dwDisplacement, &line))
{
    // SymGetLineFromAddr64 returned success
}
else
{
    // SymGetLineFromAddr64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromAddr64 returned error : %d\n"), error);
}
```



 

 



