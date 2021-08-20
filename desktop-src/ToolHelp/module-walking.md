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
ms.openlocfilehash: a61e72fcdbcae52a78e62465b12845077572b6b4669e1b0744c26d50ddfd2a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126494"
---
# <a name="module-walking"></a>Проход по модулю

Моментальный снимок, включающий список модулей для указанного процесса, содержит сведения о каждом модуле, исполняемом файле или библиотеке динамической компоновки (DLL), используемой указанным процессом. Сведения для первого модуля в списке можно получить с помощью функции [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) . После получения первого модуля из списка можно получить сведения о последующих модулях в списке с помощью функции [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) . **Module32First** и **Module32Next** заполняют структуру [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) информацией о модуле.

Код расширенного состояния ошибки для [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) и [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) можно получить с помощью функции [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> Идентификатор модуля, указанный в элементе **th32ModuleID** элемента [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), имеет значение только в 16-разрядном Windows.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Обход списка модулей](traversing-the-module-list.md)
</dt> </dl>

 

 