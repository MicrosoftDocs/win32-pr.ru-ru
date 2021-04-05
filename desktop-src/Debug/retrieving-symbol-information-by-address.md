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
# <a name="retrieving-symbol-information-by-address"></a>Получение символьной информации по адресу

В следующем коде показано, как вызвать функцию [**симфромаддр**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) . Эта функция заполняет структуру [**\_ сведений о символах**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Так как имя переменной имеет длину, необходимо предоставить буфер, достаточно большой для хранения имени, хранящегося в конце структуры **\_ сведений о символах** . Кроме того, элемент **макснамелен** должен иметь значение, равное количеству байтов, зарезервированных для имени. В этом примере *дваддресс* — это адрес, который должен быть сопоставлен с символом. Функция **симфромаддр** сохранит смещение в начале символа на адрес в *двдисплацемент*. В примере предполагается, что обработчик символов инициализирован с помощью кода при [инициализации обработчика символов](initializing-the-symbol-handler.md).


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



Чтобы получить номер строки исходного кода для указанного адреса, приложение может использовать [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr). Эта функция требует указатель на структуру [**\_ LINE64 Imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) , чтобы получить имя исходного файла и номер строки, соответствующие указанному адресу кода. Обратите внимание, что обработчик символов может извлекать сведения о номере строки только в том случае, если **симопт \_ \_ нагрузки** заданы с помощью функции [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Этот параметр необходимо задать перед загрузкой модуля. Параметр Дваддресс содержит адрес кода, для которого будет располагаться имя исходного файла и номер строки.


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



 

 



