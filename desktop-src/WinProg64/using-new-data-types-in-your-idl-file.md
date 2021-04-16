---
title: Использование новых типов данных в IDL-файле
description: Файл заголовка Басетсд. h определяет новые типы данных, необходимые для написания приложений, которые работают как в 32, так и в 64-разрядной версии Windows.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Файл заголовка басетсд. h, 64-разрядное программирование для Windows
- типы данных в IDL-файле — программирование для Windows 64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff1add2d70c99069911ac76ad168b7d31c3365f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710309"
---
# <a name="using-new-data-types-in-your-idl-file"></a><span data-ttu-id="66cd2-105">Использование новых типов данных в IDL-файле</span><span class="sxs-lookup"><span data-stu-id="66cd2-105">Using New Data Types in Your IDL File</span></span>

<span data-ttu-id="66cd2-106">Файл заголовка Басетсд. h определяет новые типы данных, необходимые для написания приложений, которые работают как в 32, так и в 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="66cd2-106">The Basetsd.h header file defines the new data types needed for writing applications that run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="66cd2-107">Чтобы использовать эти типы данных в интерфейсах, импортируйте Басетсд. h в IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="66cd2-107">To use these data types in your interfaces, import Basetsd.h into your IDL file.</span></span> <span data-ttu-id="66cd2-108">Не \# Включайте файл, или вы получите несколько определений во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="66cd2-108">Do not \#include the file or you will end up with multiple definitions at compile time.</span></span>

<span data-ttu-id="66cd2-109">Кроме того, можно включить или импортировать файл Басетсд. idl в IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="66cd2-109">Alternatively, you can include or import the Basetsd.idl file into your IDL file.</span></span>

<span data-ttu-id="66cd2-110">Дополнительные сведения о добавлении системных файлов заголовков в IDL-файл см. в разделе [Импорт файлов и библиотек типов](/windows/desktop/Midl/importing-files-and-type-libraries) и [Импорт системных файлов заголовков](/windows/desktop/Midl/importing-system-header-files).</span><span class="sxs-lookup"><span data-stu-id="66cd2-110">For more information on adding system header files to your IDL file, see [Importing Files and Type Libraries](/windows/desktop/Midl/importing-files-and-type-libraries) and [Importing System Header Files](/windows/desktop/Midl/importing-system-header-files).</span></span>

 

 