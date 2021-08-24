---
description: В следующем коде показано, как вызвать функцию Симфромнаме.
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: Получение символьной информации по имени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ec0a04ef2cac9dcd8256f8d00ff59b00bec449cdb4b5661566e7087e782cdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076368"
---
# <a name="retrieving-symbol-information-by-name"></a>Получение символьной информации по имени

В следующем коде показано, как вызвать функцию [**симфромнаме**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) . Эта функция заполняет структуру [**\_ сведений о символах**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Так как имя переменной имеет длину, необходимо предоставить буфер, достаточно большой для хранения имени, хранящегося в конце структуры **\_ сведений о символах** . Кроме того, элемент **макснамелен** должен иметь значение, равное количеству байтов, зарезервированных для имени. В этом примере Сзсимболнаме — это буфер, в котором хранится имя запрошенного символа. В примере предполагается, что обработчик символов инициализирован с помощью кода при [инициализации обработчика символов](initializing-the-symbol-handler.md).


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



Если в приложении есть имя модуля или исходного файла, а также сведения о номере строки, он может использовать [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) для получения виртуального адреса кода. Эта функция требует указатель на структуру [**\_ LINE64 Imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) , чтобы получить адрес виртуального кода. Обратите внимание, что обработчик символов может извлекать сведения о номере строки только в том случае \_ , если параметр симопт Load \_ Lines установлен с помощью функции [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Этот параметр необходимо задать перед загрузкой модуля. Параметр Сзмодуленаме содержит имя исходного модуля; Он является необязательным и может иметь **значение NULL**. Параметр Сзфиленаме должен содержать имя исходного файла, а параметр Двлиненумбер должен содержать номер строки, для которой будет получен виртуальный адрес.


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



 

 



