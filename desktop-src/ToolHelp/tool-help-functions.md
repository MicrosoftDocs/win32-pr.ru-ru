---
title: Функции справки средства
description: Содержит список функций библиотеки справки по средствам.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068479"
---
# <a name="tool-help-functions"></a>Функции справки средства

Следующие функции являются частью библиотеки справки по средствам.



| Функция                                                           | Описание                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | Создает моментальный снимок указанных процессов, а также кучи, модули и потоки, используемые этими процессами. |
| [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | Извлекает сведения о первом блоке кучи, выделенной процессом.                      |
| [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | Извлекает сведения о первой куче, выделенной указанным процессом.                       |
| [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | Извлекает сведения о следующей куче, выделенной процессом.                                  |
| [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | Извлекает сведения о следующем блоке кучи, выделенной процессом.                       |
| [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | Извлекает сведения о первом модуле, связанном с процессом.                                          |
| [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | Извлекает сведения о следующем модуле, связанном с процессом или потоком.                                 |
| [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | Извлекает сведения о первом процессе, обнаруженном в системном снимке.                                  |
| [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | Извлекает сведения о следующем процессе, записанном в системном снимке.                                      |
| [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | Извлекает сведения о первом потоке любого процесса, обнаруженного в системном снимке.                    |
| [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | Извлекает сведения о следующем потоке любого процесса, обнаруженного в снимке системной памяти.            |
| [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | Копирует память, выделенную для другого процесса, в буфер, предоставленный приложением.                                  |



 

 

 




