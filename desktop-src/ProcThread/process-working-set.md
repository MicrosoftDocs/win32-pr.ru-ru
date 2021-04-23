---
description: Рабочий набор программы представляет собой коллекцию страниц в своем виртуальном адресном пространстве, на которые недавно ссылались.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Рабочий набор процесса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900b5d8a19c756a9087a9b2c006259857691dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264490"
---
# <a name="process-working-set"></a><span data-ttu-id="1db99-103">Рабочий набор процесса</span><span class="sxs-lookup"><span data-stu-id="1db99-103">Process Working Set</span></span>

<span data-ttu-id="1db99-104">*Рабочий набор* программы представляет собой коллекцию страниц в своем виртуальном адресном пространстве, на которые недавно ссылались.</span><span class="sxs-lookup"><span data-stu-id="1db99-104">The *working set* of a program is a collection of those pages in its virtual address space that have been recently referenced.</span></span> <span data-ttu-id="1db99-105">Он включает как общие, так и частные данные.</span><span class="sxs-lookup"><span data-stu-id="1db99-105">It includes both shared and private data.</span></span> <span data-ttu-id="1db99-106">Общие данные включают страницы, содержащие все инструкции, выполняемые приложением, включая файлы в библиотеках DLL и системные библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="1db99-106">The shared data includes pages that contain all instructions your application executes, including those in your DLLs and the system DLLs.</span></span> <span data-ttu-id="1db99-107">По мере увеличения размера рабочего набора увеличивается потребность в памяти.</span><span class="sxs-lookup"><span data-stu-id="1db99-107">As the working set size increases, memory demand increases.</span></span>

<span data-ttu-id="1db99-108">Процесс имеет связанный минимальный размер рабочего набора и максимальный размер рабочего множества.</span><span class="sxs-lookup"><span data-stu-id="1db99-108">A process has an associated minimum working set size and maximum working set size.</span></span> <span data-ttu-id="1db99-109">Каждый раз, когда вызывается [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), он резервирует минимальный размер рабочего множества для процесса.</span><span class="sxs-lookup"><span data-stu-id="1db99-109">Each time you call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), it reserves the minimum working set size for the process.</span></span> <span data-ttu-id="1db99-110">Диспетчер виртуальной памяти пытается сохранить достаточно памяти для минимального рабочего набора, резидентного, если процесс активен, но не поддерживает максимальный размер.</span><span class="sxs-lookup"><span data-stu-id="1db99-110">The virtual memory manager attempts to keep enough memory for the minimum working set resident when the process is active, but keeps no more than the maximum size.</span></span>

<span data-ttu-id="1db99-111">Чтобы получить требуемый минимальный и максимальный размеры рабочего набора для приложения, вызовите функцию [**жетпроцессворкингсетсизе**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) .</span><span class="sxs-lookup"><span data-stu-id="1db99-111">To get the requested minimum and maximum sizes of the working set for your application, call the [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) function.</span></span>

<span data-ttu-id="1db99-112">Система устанавливает размеры рабочего набора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1db99-112">The system sets the default working set sizes.</span></span> <span data-ttu-id="1db99-113">Размеры рабочих наборов также можно изменить с помощью функции [**сетпроцессворкингсетсизе**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) .</span><span class="sxs-lookup"><span data-stu-id="1db99-113">You can also modify the working set sizes using the [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) function.</span></span> <span data-ttu-id="1db99-114">Установка этих значений не гарантирует, что память будет зарезервированной или резидентной.</span><span class="sxs-lookup"><span data-stu-id="1db99-114">Setting these values is not a guarantee that the memory will be reserved or resident.</span></span> <span data-ttu-id="1db99-115">Будьте внимательны при запросе слишком большого объема минимального или максимального размера рабочего множества, так как это может привести к снижению производительности системы.</span><span class="sxs-lookup"><span data-stu-id="1db99-115">Be careful about requesting too large a minimum or maximum working set size, because doing so can degrade system performance.</span></span>

<span data-ttu-id="1db99-116">Чтобы получить текущий или пиковый размер рабочего набора для процесса, используйте функцию [**жетпроцессмеморинфо**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) .</span><span class="sxs-lookup"><span data-stu-id="1db99-116">To obtain the current or peak size of the working set for your process, use the [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1db99-117">См. также</span><span class="sxs-lookup"><span data-stu-id="1db99-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1db99-118">[Сведения о производительности памяти](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1db99-118">[Memory Performance Information](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1db99-119">Рабочий набор</span><span class="sxs-lookup"><span data-stu-id="1db99-119">Working Set</span></span>](../memory/working-set.md)
</dt> </dl>

 

 
