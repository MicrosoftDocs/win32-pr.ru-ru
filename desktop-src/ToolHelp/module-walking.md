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
# <a name="module-walking"></a><span data-ttu-id="7d29a-107">Проход по модулю</span><span class="sxs-lookup"><span data-stu-id="7d29a-107">Module Walking</span></span>

<span data-ttu-id="7d29a-108">Моментальный снимок, включающий список модулей для указанного процесса, содержит сведения о каждом модуле, исполняемом файле или библиотеке динамической компоновки (DLL), используемой указанным процессом.</span><span class="sxs-lookup"><span data-stu-id="7d29a-108">A snapshot that includes the module list for a specified process contains information about each module, executable file, or dynamic-link library (DLL), used by the specified process.</span></span> <span data-ttu-id="7d29a-109">Сведения для первого модуля в списке можно получить с помощью функции [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) .</span><span class="sxs-lookup"><span data-stu-id="7d29a-109">You can retrieve information for the first module in the list by using the [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) function.</span></span> <span data-ttu-id="7d29a-110">После получения первого модуля из списка можно получить сведения о последующих модулях в списке с помощью функции [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) .</span><span class="sxs-lookup"><span data-stu-id="7d29a-110">After retrieving the first module in the list, you can retrieve information for subsequent modules in the list by using the [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) function.</span></span> <span data-ttu-id="7d29a-111">**Module32First** и **Module32Next** заполняют структуру [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) информацией о модуле.</span><span class="sxs-lookup"><span data-stu-id="7d29a-111">**Module32First** and **Module32Next** fill a [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) structure with information about the module.</span></span>

<span data-ttu-id="7d29a-112">Код расширенного состояния ошибки для [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) и [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) можно получить с помощью функции [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="7d29a-112">You can retrieve an extended error status code for [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) and [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="7d29a-113">Идентификатор модуля, указанный в элементе **th32ModuleID** элемента [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), имеет значение только в 16-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="7d29a-113">The module identifier, which is specified in the **th32ModuleID** member of [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), only has meaning in 16-bit Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7d29a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="7d29a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d29a-115">Обход списка модулей</span><span class="sxs-lookup"><span data-stu-id="7d29a-115">Traversing the Module List</span></span>](traversing-the-module-list.md)
</dt> </dl>

 

 