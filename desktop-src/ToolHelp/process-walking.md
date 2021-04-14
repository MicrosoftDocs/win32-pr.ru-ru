---
title: Процесс прохода
description: Моментальный снимок, включающий список процессов, содержит сведения о каждом выполняющемся процессе.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- перечисление
- Перечисление, процессы
- процессы
- процессы, перечисление процессов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc95f0de4021ce3c355286376decbdecef2c883
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487937"
---
# <a name="process-walking"></a>Процесс прохода

Моментальный снимок, включающий список процессов, содержит сведения о каждом выполняющемся процессе. Сведения для первого процесса в списке можно получить с помощью функции [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) . После получения первого процесса в списке можно просмотреть список процессов для последующих записей с помощью функции [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) . **Process32First** и **Process32Next** заполняют структуру [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) информацией о процессе в моментальном снимке. Пример см. в разделе [Создание моментального снимка и Просмотр процессов](taking-a-snapshot-and-viewing-processes.md).

Код расширенного состояния ошибки для [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) и [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) можно получить с помощью функции [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Можно прочитать память в определенном процессе в буфер с помощью функции [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (или функции [**виртуалкуерекс**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) ).

> [!Note]  
> Содержимое элементов **th32ProcessID** и **th32ParentProcessID** в [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) являются идентификаторами процессов и могут использоваться любыми функциями, которым требуется идентификатор процесса.

 

 

 