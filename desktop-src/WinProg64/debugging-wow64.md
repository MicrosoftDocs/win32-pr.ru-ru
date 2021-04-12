---
title: Отладка WOW64
description: Приложения, выполняемые в WOW64, можно отлаживать с помощью отладчика, размещенного на x86, или собственного отладчика.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- WOW64 64-разрядное программирование Windows, отладка
- отладка WOW64 64-разрядного программирования Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413522"
---
# <a name="debugging-wow64"></a><span data-ttu-id="c2c5d-105">Отладка WOW64</span><span class="sxs-lookup"><span data-stu-id="c2c5d-105">Debugging WOW64</span></span>

<span data-ttu-id="c2c5d-106">Приложения, выполняемые в эмуляторе WOW64, можно отлаживать двумя способами:</span><span class="sxs-lookup"><span data-stu-id="c2c5d-106">Applications running under WOW64 can be debugged two ways:</span></span>

-   <span data-ttu-id="c2c5d-107">Используйте отладчик, размещенный на x86, например NTSD, WinDbg или Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-107">Use an x86-hosted debugger such as NTSD, WinDbg, or Visual Studio.</span></span> <span data-ttu-id="c2c5d-108">32-бит NTSD устанавливается в папку% SystemRoot% \\ SysWOW64 в розничных установках.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-108">The 32-bit NTSD is installed to %systemroot%\\syswow64 on retail installations.</span></span> <span data-ttu-id="c2c5d-109">Обратите внимание, что отладчики x86 можно использовать для отладки кода на платформе x86, но не могут использоваться для разгруппирования или установки точек останова в пределах слоя преобразователя WOW64, поскольку это 64-разрядный машинный код.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-109">Note that x86 debuggers can be used to debug x86 code, but cannot be used to disassemble or set breakpoints within the WOW64 thunk layer because it is 64-bit native code.</span></span>
-   <span data-ttu-id="c2c5d-110">Используйте собственный отладчик, например CDB, NTSD или WinDbg, и расширение отладчика WOW64 Wow64exts.dll.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-110">Use a native debugger such as CDB, NTSD, or WinDbg and the WOW64 debugger extension, Wow64exts.dll.</span></span> <span data-ttu-id="c2c5d-111">Если отладчик машинного кода прерывает работу, пока процессор находится в режиме x86, отладчик представляет процесс как процесс x86.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-111">If the native debugger breaks while the processor is in x86 mode, the debugger presents the process as an x86 process.</span></span> <span data-ttu-id="c2c5d-112">Если процессор работает в собственном режиме, отладчик представляет процесс как собственный.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-112">If the processor is in native mode, the debugger presents the process as native.</span></span>

<span data-ttu-id="c2c5d-113">CDB, NTSD и WinDbg включены в средства отладки для Windows.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-113">CDB, NTSD, and WinDbg are included in Debugging Tools for Windows.</span></span> <span data-ttu-id="c2c5d-114">Дополнительные сведения см. в документации по [средствам отладки для Windows](/windows-hardware/drivers/debugger/) .</span><span class="sxs-lookup"><span data-stu-id="c2c5d-114">For more information, see the [Debugging Tools for Windows](/windows-hardware/drivers/debugger/) documentation.</span></span>

<span data-ttu-id="c2c5d-115">Расширение отладчика Wow64exts устанавливается с WinDbg.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-115">The Wow64exts debugger extension is installed with WinDbg.</span></span> <span data-ttu-id="c2c5d-116">Чтобы загрузить расширение отладчика, используйте команду! Load wow64exts.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-116">Use the !load wow64exts command to load the debugger extension.</span></span> <span data-ttu-id="c2c5d-117">В следующей таблице перечислены команды расширения отладчика! wow64exts.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-117">The following table lists the !wow64exts debugger extension commands.</span></span>



| <span data-ttu-id="c2c5d-118">Get-Help</span><span class="sxs-lookup"><span data-stu-id="c2c5d-118">Command</span></span>                | <span data-ttu-id="c2c5d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="c2c5d-119">Description</span></span>                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c5d-120">! wow64exts. SW</span><span class="sxs-lookup"><span data-stu-id="c2c5d-120">!wow64exts.sw</span></span>          | <span data-ttu-id="c2c5d-121">Переключение между режимами x86 и Native.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-121">Switches between x86 and native mode.</span></span>                                                                                                    |
| <span data-ttu-id="c2c5d-122">! wow64exts. k, *число*</span><span class="sxs-lookup"><span data-stu-id="c2c5d-122">!wow64exts.k *count*</span></span>   | <span data-ttu-id="c2c5d-123">Создает дамп общей 32-разрядной или 64-разрядной трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-123">Dumps a combined 32-bit/64-bit stack trace.</span></span> <span data-ttu-id="c2c5d-124">Если указано *Count* , команда выводит первый *Счетчик* адресов в каждой трассировке стека.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-124">If *count* is specified, the command dumps the first *count* addresses in each stack trace.</span></span>  |
| <span data-ttu-id="c2c5d-125">! wow64exts.info</span><span class="sxs-lookup"><span data-stu-id="c2c5d-125">!wow64exts.info</span></span>        | <span data-ttu-id="c2c5d-126">Выводит основные сведения о ПЕБ процесса, ТЕБ текущего потока и слотах локального хранилища потока (TLS), используемые WOW64.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-126">Dumps basic information about the PEB of the process, the TEB of the current thread, and thread local storage (TLS) slots used by WOW64.</span></span> |
| <span data-ttu-id="c2c5d-127">! wow64exts. r *адрес*</span><span class="sxs-lookup"><span data-stu-id="c2c5d-127">!wow64exts.r *address*</span></span> | <span data-ttu-id="c2c5d-128">Создает дамп контекста для указанного адреса.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-128">Dumps context for the specified address.</span></span> <span data-ttu-id="c2c5d-129">Если параметр *Address* не указан, команда выводит контекст для процессора.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-129">If *address* is not specified, the command dumps context for the processor.</span></span>                     |



 

 

 