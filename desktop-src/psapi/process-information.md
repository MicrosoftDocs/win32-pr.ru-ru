---
title: Сведения о процессе
description: Система поддерживает список запущенных процессов. Идентификаторы для этих процессов можно получить, вызвав функцию EnumProcesses. Эта функция заполняет массив значений типа DWORD идентификаторами всех процессов в системе.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338033"
---
# <a name="process-information"></a><span data-ttu-id="c4e8c-105">Сведения о процессе</span><span class="sxs-lookup"><span data-stu-id="c4e8c-105">Process Information</span></span>

<span data-ttu-id="c4e8c-106">Система поддерживает список запущенных процессов.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-106">The system maintains a list of running processes.</span></span> <span data-ttu-id="c4e8c-107">Идентификаторы для этих процессов можно получить, вызвав функцию [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="c4e8c-107">You can retrieve the identifiers for these processes by calling the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="c4e8c-108">Эта функция заполняет массив значений **типа DWORD** идентификаторами всех процессов в системе.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-108">This function fills an array of **DWORD** values with the identifiers of all processes in the system.</span></span>

<span data-ttu-id="c4e8c-109">Многим функциям в PSAPI требуется обработчик процесса.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-109">Many functions in PSAPI require a process handle.</span></span> <span data-ttu-id="c4e8c-110">Чтобы получить обработчик процесса для выполняющегося процесса, передайте его идентификатор процесса (полученный из [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) в функцию [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) .</span><span class="sxs-lookup"><span data-stu-id="c4e8c-110">To obtain a process handle for a running process, pass its process identifier (obtained from [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) to the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function.</span></span> <span data-ttu-id="c4e8c-111">Не забудьте вызвать функцию [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) по завершении работы с обработчиком процесса.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-111">Remember to call the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function when you are finished with the process handle.</span></span>

 

 