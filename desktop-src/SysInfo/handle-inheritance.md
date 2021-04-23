---
description: Дочерний процесс может наследовать дескрипторы родительского процесса. Унаследованный обработчик допустим только в контексте дочернего процесса. Чтобы разрешить дочернему процессу наследовать открытые дескрипторы родительского процесса, выполните следующие действия.
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: Наследование в обработке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664354"
---
# <a name="handle-inheritance"></a><span data-ttu-id="fd010-105">Наследование в обработке</span><span class="sxs-lookup"><span data-stu-id="fd010-105">Handle Inheritance</span></span>

<span data-ttu-id="fd010-106">Дочерний процесс может наследовать дескрипторы родительского процесса.</span><span class="sxs-lookup"><span data-stu-id="fd010-106">A child process can inherit handles from its parent process.</span></span> <span data-ttu-id="fd010-107">Унаследованный обработчик допустим только в контексте дочернего процесса.</span><span class="sxs-lookup"><span data-stu-id="fd010-107">An inherited handle is valid only in the context of the child process.</span></span> <span data-ttu-id="fd010-108">Чтобы разрешить дочернему процессу наследовать открытые дескрипторы родительского процесса, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fd010-108">To enable a child process to inherit open handles from its parent process, use the following steps.</span></span>

1.  <span data-ttu-id="fd010-109">Создайте маркер с элементом **бинхерисандле** структуры [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="fd010-109">Create the handle with the **bInheritHandle** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure set to **TRUE**.</span></span>
2.  <span data-ttu-id="fd010-110">Создайте дочерний процесс с помощью функции [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , если для параметра *бинхерисандлес* задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="fd010-110">Create the child process using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, with the *bInheritHandles* parameter set to **TRUE**.</span></span>

<span data-ttu-id="fd010-111">Функция [**дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) дублирует маркер, который будет использоваться в текущем процессе или в другом процессе.</span><span class="sxs-lookup"><span data-stu-id="fd010-111">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function duplicates a handle to be used in the current process or in another process.</span></span> <span data-ttu-id="fd010-112">Если приложение дублирует один из его дескрипторов для другого процесса, дублирование дескриптора допустимо только в контексте другого процесса.</span><span class="sxs-lookup"><span data-stu-id="fd010-112">If an application duplicates one of its handles for another process, the duplicated handle is valid only in the context of the other process.</span></span>

<span data-ttu-id="fd010-113">Повторяющийся или унаследованный обработчик — это уникальное значение, но оно ссылается на тот же объект, что и исходный маркер.</span><span class="sxs-lookup"><span data-stu-id="fd010-113">A duplicated or inherited handle is a unique value, but it refers to the same object as the original handle.</span></span> <span data-ttu-id="fd010-114">Процессы могут наследовать или дублировать дескрипторы следующих типов объектов:</span><span class="sxs-lookup"><span data-stu-id="fd010-114">Processes can inherit or duplicate handles to the following types of objects:</span></span>

-   <span data-ttu-id="fd010-115">Маркер доступа</span><span class="sxs-lookup"><span data-stu-id="fd010-115">Access Token</span></span>
-   <span data-ttu-id="fd010-116">Коммуникационное устройство</span><span class="sxs-lookup"><span data-stu-id="fd010-116">Communications device</span></span>
-   <span data-ttu-id="fd010-117">Входные данные консоли</span><span class="sxs-lookup"><span data-stu-id="fd010-117">Console input</span></span>
-   <span data-ttu-id="fd010-118">Буфер экрана консоли</span><span class="sxs-lookup"><span data-stu-id="fd010-118">Console screen buffer</span></span>
-   <span data-ttu-id="fd010-119">Персональный компьютер</span><span class="sxs-lookup"><span data-stu-id="fd010-119">Desktop</span></span>
-   <span data-ttu-id="fd010-120">Каталог</span><span class="sxs-lookup"><span data-stu-id="fd010-120">Directory</span></span>
-   <span data-ttu-id="fd010-121">Событие</span><span class="sxs-lookup"><span data-stu-id="fd010-121">Event</span></span>
-   <span data-ttu-id="fd010-122">Файл</span><span class="sxs-lookup"><span data-stu-id="fd010-122">File</span></span>
-   <span data-ttu-id="fd010-123">Сопоставление файлов</span><span class="sxs-lookup"><span data-stu-id="fd010-123">File mapping</span></span>
-   <span data-ttu-id="fd010-124">Задание</span><span class="sxs-lookup"><span data-stu-id="fd010-124">Job</span></span>
-   <span data-ttu-id="fd010-125">Ящик</span><span class="sxs-lookup"><span data-stu-id="fd010-125">Mailslot</span></span>
-   <span data-ttu-id="fd010-126">Mutex</span><span class="sxs-lookup"><span data-stu-id="fd010-126">Mutex</span></span>
-   <span data-ttu-id="fd010-127">канал</span><span class="sxs-lookup"><span data-stu-id="fd010-127">Pipe</span></span>
-   <span data-ttu-id="fd010-128">Процесс</span><span class="sxs-lookup"><span data-stu-id="fd010-128">Process</span></span>
-   <span data-ttu-id="fd010-129">Раздел реестра</span><span class="sxs-lookup"><span data-stu-id="fd010-129">Registry key</span></span>
-   <span data-ttu-id="fd010-130">Semaphore</span><span class="sxs-lookup"><span data-stu-id="fd010-130">Semaphore</span></span>
-   <span data-ttu-id="fd010-131">Розетка</span><span class="sxs-lookup"><span data-stu-id="fd010-131">Socket</span></span>
-   <span data-ttu-id="fd010-132">Thread</span><span class="sxs-lookup"><span data-stu-id="fd010-132">Thread</span></span>
-   <span data-ttu-id="fd010-133">Таймер</span><span class="sxs-lookup"><span data-stu-id="fd010-133">Timer</span></span>
-   <span data-ttu-id="fd010-134">Оконная станция</span><span class="sxs-lookup"><span data-stu-id="fd010-134">Window station</span></span>

<span data-ttu-id="fd010-135">Все остальные объекты являются частными для создавшего их процесса; их дескрипторы объектов не могут дублироваться или наследоваться.</span><span class="sxs-lookup"><span data-stu-id="fd010-135">All other objects are private to the process that created them; their object handles cannot be duplicated or inherited.</span></span>

<span data-ttu-id="fd010-136">Дополнительные сведения см. в разделе [Наследование](/windows/desktop/ProcThread/inheritance).</span><span class="sxs-lookup"><span data-stu-id="fd010-136">For more information, see [Inheritance](/windows/desktop/ProcThread/inheritance).</span></span>

 

 
