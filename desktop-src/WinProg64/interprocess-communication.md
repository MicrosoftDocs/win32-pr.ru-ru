---
title: Межпроцессное взаимодействие
description: Для обмена данными между 32-разрядными и 64-разрядными приложениями можно использовать следующие методы.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- межпроцессное взаимодействие 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2398174f011127973dfd0b1773e6eb040cdde898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413348"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a><span data-ttu-id="69765-104">Межпроцессное взаимодействие между 32-разрядными и 64-разрядными приложениями</span><span class="sxs-lookup"><span data-stu-id="69765-104">Interprocess Communication Between 32-bit and 64-bit Applications</span></span>

<span data-ttu-id="69765-105">Для обмена данными между 32-разрядными и 64-разрядными приложениями можно использовать следующие методы:</span><span class="sxs-lookup"><span data-stu-id="69765-105">The following techniques can be used for communication between 32-bit and 64-bit applications:</span></span>

-   <span data-ttu-id="69765-106">64-разрядные версии Windows используют 32-разрядные дескрипторы для взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="69765-106">64-bit versions of Windows use 32-bit handles for interoperability.</span></span> <span data-ttu-id="69765-107">При совместном использовании маркера между 32-разрядными и 64-разрядными приложениями значимыми являются только младшие биты 32, поэтому можно легко усечь этот маркер (при передаче его из 64-разрядного в 32-bit) или знак расширения (при передаче его из 32-bit в 64-bit).</span><span class="sxs-lookup"><span data-stu-id="69765-107">When sharing a handle between 32-bit and 64-bit applications, only the lower 32 bits are significant, so it is safe to truncate the handle (when passing it from 64-bit to 32-bit) or sign-extend the handle (when passing it from 32-bit to 64-bit).</span></span> <span data-ttu-id="69765-108">Дескрипторы, которые могут быть общими, включают дескрипторы для пользовательских объектов, таких как Windows (**HWND**), дескрипторы объектов GDI, таких как перья и кисти (**хбруш** и **Хпен**), а также дескрипторы именованных объектов, таких как мьютексы, семафоры и дескрипторы файлов.</span><span class="sxs-lookup"><span data-stu-id="69765-108">Handles that can be shared include handles to user objects such as windows (**HWND**), handles to GDI objects such as pens and brushes (**HBRUSH** and **HPEN**), and handles to named objects such as mutexes, semaphores, and file handles.</span></span>
-   <span data-ttu-id="69765-109">Можно использовать удаленные вызовы процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="69765-109">Remote procedure calls (RPC) can be used.</span></span>
-   <span data-ttu-id="69765-110">Локалсерверс COM можно использовать, если для всех используемых интерфейсов зарегистрированы как 32-разрядные, так и 64-битовые прокси-библиотеки.</span><span class="sxs-lookup"><span data-stu-id="69765-110">COM LocalServers can be used if both 32-bit and 64-bit proxy/stub DLLs are registered for all interfaces used.</span></span>
-   <span data-ttu-id="69765-111">Можно использовать общую память, если зависимые от указателя типы преобразовываются должным образом (или избегать).</span><span class="sxs-lookup"><span data-stu-id="69765-111">Shared memory can be used if pointer-dependent types are converted properly (or avoided).</span></span>
-   <span data-ttu-id="69765-112">Функции [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) и [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) могут запускать 32-разрядные и 64-разрядные процессы из 32-разрядных или 64-разрядных процессов с определенными ограничениями.</span><span class="sxs-lookup"><span data-stu-id="69765-112">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) and [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) functions can launch 32-bit and 64-bit processes from either 32-bit or 64-bit processes with certain limitations.</span></span>

<span data-ttu-id="69765-113">64-разрядный исполняемый файл, расположенный в папке% WINDIR% \\ System32, не может быть запущен из 32-разрядного процесса, так как перенаправитель файловой системы перенаправит путь.</span><span class="sxs-lookup"><span data-stu-id="69765-113">A 64-bit executable file located under %windir%\\System32 cannot be launched from a 32-bit process, because the file system redirector redirects the path.</span></span> <span data-ttu-id="69765-114">Для этого не следует отключать перенаправление. Используйте вместо него% WINDIR% \\ сиснативе.</span><span class="sxs-lookup"><span data-stu-id="69765-114">Do not disable redirection to accomplish this; use %windir%\\Sysnative instead.</span></span> <span data-ttu-id="69765-115">Дополнительные сведения см. в разделе [перенаправитель файловой системы](file-system-redirector.md).</span><span class="sxs-lookup"><span data-stu-id="69765-115">For more information, see [File System Redirector](file-system-redirector.md).</span></span>

 

 