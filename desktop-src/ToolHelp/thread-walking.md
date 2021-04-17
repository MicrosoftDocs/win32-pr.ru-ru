---
title: Потоковый проход
description: Моментальный снимок, включающий список потоков, содержит сведения о каждом потоке каждого выполняющегося процесса.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- перечисление
- Перечисление, потоки
- потоки
- потоки, перечисление потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681665"
---
# <a name="thread-walking"></a>Потоковый проход

Моментальный снимок, включающий список потоков, содержит сведения о каждом потоке каждого выполняющегося процесса. Сведения для первого потока в списке можно получить с помощью функции [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) . После получения первого потока в списке можно получить сведения для последующих потоков с помощью функции [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) . **Thread32First** и **Thread32Next** заполняют структуру [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) информацией об отдельных потоках в моментальном снимке.

Вы можете перечислить потоки определенного процесса, используя моментальный снимок, включающий потоки, а затем продвигаясь по списку потоков, сохранив сведения о потоках, имеющих тот же идентификатор процесса, что и указанный процесс.

Код расширенного состояния ошибки для [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) и [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) можно получить с помощью функции [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> Содержимое элемента **th32ThreadID** объекта [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) является идентификатором потока и может использоваться любыми функциями, которым требуется идентификатор потока.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обход списка потоков](traversing-the-thread-list.md)
</dt> </dl>

 

 