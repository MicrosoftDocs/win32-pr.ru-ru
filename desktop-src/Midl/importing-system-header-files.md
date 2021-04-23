---
title: Импорт системных файлов заголовков
description: Хотя часто можно использовать директиву \ include для включения файлов заголовков в IDL-файл, делать это не рекомендуется.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- Импорт MIDL, файлы заголовков системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820476"
---
# <a name="importing-system-header-files"></a><span data-ttu-id="6ee30-104">Импорт системных файлов заголовков</span><span class="sxs-lookup"><span data-stu-id="6ee30-104">Importing System Header Files</span></span>

<span data-ttu-id="6ee30-105">Хотя часто можно использовать директиву **\# include** для включения файлов заголовков в IDL-файл, делать это не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6ee30-105">While it is often possible to use the **\#include** directive to include header files in your IDL file, it is not recommended.</span></span> <span data-ttu-id="6ee30-106">Компилятор MIDL создаст заглушки для всех функций, определенных в компилируемом файле IDL.</span><span class="sxs-lookup"><span data-stu-id="6ee30-106">The MIDL compiler will generate stubs for all functions defined in the IDL file being compiled.</span></span> <span data-ttu-id="6ee30-107">Как правило, файл заголовка содержит несколько прототипов, которые не нужно включать в файлы заглушки и, в своюмся, **\# содержат** все эти определения в основном файле IDL.</span><span class="sxs-lookup"><span data-stu-id="6ee30-107">Usually a header file contains a number of prototypes that you neither need nor want to include in your stub files, and a **\#include** effectively puts all those definitions into your main IDL file.</span></span> <span data-ttu-id="6ee30-108">Кроме того, если в файле заголовка определены типы, не поддерживающие удаленное взаимодействие, IDL-файл может не компилироваться.</span><span class="sxs-lookup"><span data-stu-id="6ee30-108">Furthermore, if there are nonremotable types defined in the header file, the IDL file may not compile.</span></span>

<span data-ttu-id="6ee30-109">Существует два способа включения определений типов из файлов заголовков в IDL-файл:</span><span class="sxs-lookup"><span data-stu-id="6ee30-109">There are two ways to include type definitions from header files in an IDL file:</span></span>

-   <span data-ttu-id="6ee30-110">Используйте директиву [**Import**](import.md) для включения типов данных, определенных в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="6ee30-110">Use the [**import**](import.md) directive to include data types defined in a header file.</span></span> <span data-ttu-id="6ee30-111">В отличие от директивы **\# include** языка C, Директива **Import** выбирает только определения типа и константы и игнорирует прототипы процедур.</span><span class="sxs-lookup"><span data-stu-id="6ee30-111">Unlike the C-language **\#include** directive, the **import** directive only picks up type and constant definitions and ignores procedure prototypes.</span></span> <span data-ttu-id="6ee30-112">Этот подход работает при условии, что основной IDL-файл не ссылается на типы, не поддерживающие удаленное взаимодействие, определенные в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="6ee30-112">This approach will work as long as your main IDL file does not reference any nonremotable types defined in the header file.</span></span>
-   <span data-ttu-id="6ee30-113">Создайте вспомогательный IDL-файл с фиктивным интерфейсом, который включает файлы заголовков.</span><span class="sxs-lookup"><span data-stu-id="6ee30-113">Create a helper IDL file with a dummy interface that includes the header files.</span></span> <span data-ttu-id="6ee30-114">Затем используйте директиву [**Import**](import.md) , чтобы включить вспомогательный файл.</span><span class="sxs-lookup"><span data-stu-id="6ee30-114">Then, use the [**import**](import.md) directive to include the helper file.</span></span> <span data-ttu-id="6ee30-115">Таким образом, в скомпилированных заглушках будет отображаться только [**typedef**](typedef.md).</span><span class="sxs-lookup"><span data-stu-id="6ee30-115">In this way, only the [**typedef**](typedef.md)s will appear in the compiled stubs.</span></span> <span data-ttu-id="6ee30-116">Пример:</span><span class="sxs-lookup"><span data-stu-id="6ee30-116">For example:</span></span>

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
