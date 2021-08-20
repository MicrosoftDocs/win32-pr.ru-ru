---
title: Списки куч и проход по куче
description: Моментальный снимок, включающий список куч для указанного процесса, содержит идентификационную информацию для каждой кучи, связанной с указанным процессом, и подробные сведения о каждой куче.
ms.assetid: 631096fd-cb2c-4b19-aa71-d47060e2715c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cc1eaa2093715e3f42fd52cc5191bedf5a0ac137cf93df57daa5ef590e2471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058232"
---
# <a name="heap-lists-and-heap-walking"></a>Списки куч и проход по куче

Моментальный снимок, включающий список куч для указанного процесса, содержит идентификационную информацию для каждой кучи, связанной с указанным процессом, и подробные сведения о каждой куче. Идентификатор для первой кучи списка кучи можно получить с помощью функции [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) . После получения первой кучи в списке можно просмотреть список куч для последующих куч, связанных с процессом, с помощью функции [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) . **Heap32ListFirst** и **Heap32ListNext** заполняют структуру [**HEAPLIST32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heaplist32) идентификатором процесса, идентификатором кучи и флагами, описывающими кучу.

Сведения о первом блоке кучи можно получить с помощью функции [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) . После получения первого блока кучи можно получить сведения о последующих блоках той же кучи с помощью функции [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) . **Heap32First** и **Heap32Next** заполняют структуру [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) информацией для соответствующего блока кучи.

Код расширенного состояния ошибки для [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst), [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext), [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)и [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) можно получить с помощью функции [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> Идентификатор кучи, указанный в элементе **th32HeapID** структуры [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) , имеет значение только для функций справки средства. Он не является обработчиком и не может использоваться другими функциями.

 

 

 