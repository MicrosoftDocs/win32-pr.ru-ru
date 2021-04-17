---
description: Динамическая компоновка имеет следующие преимущества по сравнению со статической компоновкой.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Преимущества динамической компоновки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663539"
---
# <a name="advantages-of-dynamic-linking"></a><span data-ttu-id="6645c-103">Преимущества динамической компоновки</span><span class="sxs-lookup"><span data-stu-id="6645c-103">Advantages of Dynamic Linking</span></span>

<span data-ttu-id="6645c-104">Динамическая компоновка имеет следующие преимущества по сравнению со статической компоновкой:</span><span class="sxs-lookup"><span data-stu-id="6645c-104">Dynamic linking has the following advantages over static linking:</span></span>

-   <span data-ttu-id="6645c-105">Несколько процессов, которые загружают одну и ту же библиотеку DLL на одном базовом адресе, совместно используют единственную копию библиотеки DLL в физической памяти.</span><span class="sxs-lookup"><span data-stu-id="6645c-105">Multiple processes that load the same DLL at the same base address share a single copy of the DLL in physical memory.</span></span> <span data-ttu-id="6645c-106">Это экономит системную память и сокращает количество переключений.</span><span class="sxs-lookup"><span data-stu-id="6645c-106">Doing this saves system memory and reduces swapping.</span></span>
-   <span data-ttu-id="6645c-107">При изменении функций в библиотеке DLL приложения, использующие их, не нуждаются в повторной компиляции или повторной компоновке при условии, что аргументы функции, соглашения о вызове и возвращаемые значения не изменяются.</span><span class="sxs-lookup"><span data-stu-id="6645c-107">When the functions in a DLL change, the applications that use them do not need to be recompiled or relinked as long as the function arguments, calling conventions, and return values do not change.</span></span> <span data-ttu-id="6645c-108">В отличие от этого статически связываемый объектный код требует, чтобы приложение было повторно связано при изменении функций.</span><span class="sxs-lookup"><span data-stu-id="6645c-108">In contrast, statically linked object code requires that the application be relinked when the functions change.</span></span>
-   <span data-ttu-id="6645c-109">Библиотека DLL может предоставлять поддержку по окончании рынка.</span><span class="sxs-lookup"><span data-stu-id="6645c-109">A DLL can provide after-market support.</span></span> <span data-ttu-id="6645c-110">Например, библиотеку DLL видеодрайверов можно изменить для поддержки дисплея, недоступного при первоначальной отгрузке приложения.</span><span class="sxs-lookup"><span data-stu-id="6645c-110">For example, a display driver DLL can be modified to support a display that was not available when the application was initially shipped.</span></span>
-   <span data-ttu-id="6645c-111">Программы, написанные на разных языках программирования, могут вызывать одну и ту же функцию DLL, если программы соответствуют тому же соглашению о вызовах, которое использует функция.</span><span class="sxs-lookup"><span data-stu-id="6645c-111">Programs written in different programming languages can call the same DLL function as long as the programs follow the same calling convention that the function uses.</span></span> <span data-ttu-id="6645c-112">Соглашение о вызовах (например, C, Pascal или стандартный вызов) управляет порядком, в котором вызывающая функция должна передать аргументы в стек, будь то функция или вызывающая функция отвечает за очистку стека, а также передаются ли какие-либо аргументы в регистры.</span><span class="sxs-lookup"><span data-stu-id="6645c-112">The calling convention (such as C, Pascal, or standard call) controls the order in which the calling function must push the arguments onto the stack, whether the function or the calling function is responsible for cleaning up the stack, and whether any arguments are passed in registers.</span></span> <span data-ttu-id="6645c-113">Дополнительные сведения см. в документации, прилагаемой к компилятору.</span><span class="sxs-lookup"><span data-stu-id="6645c-113">For more information, see the documentation included with your compiler.</span></span>

<span data-ttu-id="6645c-114">Потенциальные недостатки использования библиотек DLL заключается в том, что приложение не является автономным; Это зависит от существования отдельного модуля DLL.</span><span class="sxs-lookup"><span data-stu-id="6645c-114">A potential disadvantage to using DLLs is that the application is not self-contained; it depends on the existence of a separate DLL module.</span></span> <span data-ttu-id="6645c-115">Система прерывает процессы, используя динамическую компоновку во время загрузки, если требуется библиотека DLL, не найденная при запуске процесса, и выдает пользователю сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6645c-115">The system terminates processes using load-time dynamic linking if they require a DLL that is not found at process startup and gives an error message to the user.</span></span> <span data-ttu-id="6645c-116">В этой ситуации система не завершает процесс, использующий динамическую компоновку времени выполнения, но функции, экспортированные отсутствующими библиотеками DLL, недоступны для программы.</span><span class="sxs-lookup"><span data-stu-id="6645c-116">The system does not terminate a process using run-time dynamic linking in this situation, but functions exported by the missing DLL are not available to the program.</span></span>

 

 



