---
description: Примеры ограничений программы
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Примеры ограничений программы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663937"
---
# <a name="example-program-limitations"></a><span data-ttu-id="76edb-103">Примеры ограничений программы</span><span class="sxs-lookup"><span data-stu-id="76edb-103">Example Program Limitations</span></span>

<span data-ttu-id="76edb-104">Принципы хорошей практики программирования не всегда следуют в этих примерах программ, чтобы предоставить более краткий и удобочитаемый код.</span><span class="sxs-lookup"><span data-stu-id="76edb-104">Principles of good programming practice are not always followed in these sample programs in order to provide more concise, more readable code.</span></span> <span data-ttu-id="76edb-105">В частности:</span><span class="sxs-lookup"><span data-stu-id="76edb-105">In particular:</span></span>

-   <span data-ttu-id="76edb-106">Отображаются только ограниченные ответы на ошибки.</span><span class="sxs-lookup"><span data-stu-id="76edb-106">Only limited error responses are shown.</span></span> <span data-ttu-id="76edb-107">Работающие программы должны всегда проверять возвращенные коды ошибок и выполнять соответствующие действия при обнаружении ошибки.</span><span class="sxs-lookup"><span data-stu-id="76edb-107">Working programs should always check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="76edb-108">Выполняется только ограниченное управление памятью и ресурсами.</span><span class="sxs-lookup"><span data-stu-id="76edb-108">Only limited memory and resource management is done.</span></span> <span data-ttu-id="76edb-109">В Work Programs все ключи и [*хэши*](../secgloss/h-gly.md) должны быть уничтожены, вся выделенная память должна быть освобождена, все файлы должны быть закрыты и все дескрипторы должны быть освобождены.</span><span class="sxs-lookup"><span data-stu-id="76edb-109">In working programs, all keys and [*hashes*](../secgloss/h-gly.md) should be destroyed, all allocated memory should be freed, all files should be closed, and all handles should be released.</span></span> <span data-ttu-id="76edb-110">Эти примеры программ предоставляют только ограниченные демонстрации использования функций, выполняющих эти задачи.</span><span class="sxs-lookup"><span data-stu-id="76edb-110">These example programs provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="76edb-111">Эти примеры программ не выполняют задачи по управлению ресурсами памяти или ресурсов в случае завершения программы из-за ошибок.</span><span class="sxs-lookup"><span data-stu-id="76edb-111">These example programs perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

 

 
