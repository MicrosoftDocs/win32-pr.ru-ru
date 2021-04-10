---
title: Проход по модулю
description: Моментальный снимок, включающий список модулей для указанного процесса, содержит сведения о каждом модуле, исполняемом файле или библиотеке динамической компоновки (DLL), используемой указанным процессом.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- библиотеки динамической компоновки
- библиотеки динамической компоновки, перечисление библиотек DLL
- перечисление
- Перечисление, библиотеки DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133987"
---
# <a name="module-walking"></a>Проход по модулю

Моментальный снимок, включающий список модулей для указанного процесса, содержит сведения о каждом модуле, исполняемом файле или библиотеке динамической компоновки (DLL), используемой указанным процессом. Сведения для первого модуля в списке можно получить с помощью функции [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) . После получения первого модуля из списка можно получить сведения о последующих модулях в списке с помощью функции [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) . **Module32First** и **Module32Next** заполняют структуру [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) информацией о модуле.

Код расширенного состояния ошибки для [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) и [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) можно получить с помощью функции [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> Идентификатор модуля, указанный в элементе **th32ModuleID** элемента [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), имеет значение только в 16-разрядной версии Windows.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обход списка модулей](traversing-the-module-list.md)
</dt> </dl>

 

 