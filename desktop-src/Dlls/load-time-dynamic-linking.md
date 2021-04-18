---
description: Когда система запускает программу, которая использует динамическую компоновку во время загрузки, она использует сведения, помещенные компоновщиком в файл, чтобы указать имена библиотек DLL, используемых процессом.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Load-Time динамическая компоновка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546711"
---
# <a name="load-time-dynamic-linking"></a><span data-ttu-id="e9784-103">Load-Time динамическая компоновка</span><span class="sxs-lookup"><span data-stu-id="e9784-103">Load-Time Dynamic Linking</span></span>

<span data-ttu-id="e9784-104">Когда система запускает программу, которая использует динамическую компоновку во время загрузки, она использует сведения, помещенные компоновщиком в файл, чтобы указать имена библиотек DLL, используемых процессом.</span><span class="sxs-lookup"><span data-stu-id="e9784-104">When the system starts a program that uses load-time dynamic linking, it uses the information the linker placed in the file to locate the names of the DLLs that are used by the process.</span></span> <span data-ttu-id="e9784-105">Затем система ищет библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="e9784-105">The system then searches for the DLLs.</span></span> <span data-ttu-id="e9784-106">Дополнительные сведения см. в статье [Порядок поиска библиотек динамической компоновки](dynamic-link-library-search-order.md).</span><span class="sxs-lookup"><span data-stu-id="e9784-106">For more information, see [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).</span></span>

<span data-ttu-id="e9784-107">Если системе не удается разместить требуемую библиотеку DLL, она завершает процесс и отображает диалоговое окно, которое сообщает пользователю об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e9784-107">If the system cannot locate a required DLL, it terminates the process and displays a dialog box that reports the error to the user.</span></span> <span data-ttu-id="e9784-108">В противном случае система сопоставляет библиотеку DLL с виртуальным адресным пространством процесса и увеличивает значение счетчика ссылок DLL.</span><span class="sxs-lookup"><span data-stu-id="e9784-108">Otherwise, the system maps the DLL into the virtual address space of the process and increments the DLL reference count.</span></span>

<span data-ttu-id="e9784-109">Система вызывает функцию точки входа.</span><span class="sxs-lookup"><span data-stu-id="e9784-109">The system calls the entry-point function.</span></span> <span data-ttu-id="e9784-110">Функция получает код, указывающий, что процесс загружает библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="e9784-110">The function receives a code indicating that the process is loading the DLL.</span></span> <span data-ttu-id="e9784-111">Если функция точки входа не возвращает значение TRUE, система завершает процесс и сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e9784-111">If the entry-point function does not return TRUE, the system terminates the process and reports the error.</span></span> <span data-ttu-id="e9784-112">Дополнительные сведения о функции точки входа см. в разделе [Библиотека динамической компоновки Entry-Point функция](dynamic-link-library-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="e9784-112">For more information about the entry-point function, see [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).</span></span>

<span data-ttu-id="e9784-113">Наконец, система изменяет таблицу адресов функций с начальными адресами для импортированных функций DLL.</span><span class="sxs-lookup"><span data-stu-id="e9784-113">Finally, the system modifies the function address table with the starting addresses for the imported DLL functions.</span></span>

<span data-ttu-id="e9784-114">Библиотека DLL сопоставляется с виртуальным адресным пространством процесса во время его инициализации и загружается в физическую память только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="e9784-114">The DLL is mapped into the virtual address space of the process during its initialization and is loaded into physical memory only when needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9784-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e9784-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9784-116">Использование Load-Time динамической компоновки</span><span class="sxs-lookup"><span data-stu-id="e9784-116">Using Load-Time Dynamic Linking</span></span>](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



