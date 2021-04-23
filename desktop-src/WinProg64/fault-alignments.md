---
title: Ошибки выравнивания
description: Ошибки выравнивания
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- ошибки выравнивания в 64-разрядном программировании для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a7a55010ac148354d000ece32c91a8652f821
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710335"
---
# <a name="alignment-faults"></a><span data-ttu-id="11164-104">Ошибки выравнивания</span><span class="sxs-lookup"><span data-stu-id="11164-104">Alignment Faults</span></span>

<span data-ttu-id="11164-105">В системах на базе процессоров Itanium по умолчанию отключен обработчик ошибок выравнивания системы.</span><span class="sxs-lookup"><span data-stu-id="11164-105">The system alignment-fault handler is turned off by default on Itanium-based systems.</span></span> <span data-ttu-id="11164-106">Таким образом, любой невыравниваемая доступ к данным создает исключение, которое не будет автоматически исправлено системой, если только приложение не перехватывает исключение в [обработчике исключений на основе кадров](/windows/desktop/Debug/frame-based-exception-handling).</span><span class="sxs-lookup"><span data-stu-id="11164-106">Therefore, any unaligned data access generates an exception that will not automatically be fixed by the system unless the application catches the exception in a [frame-based exception handler](/windows/desktop/Debug/frame-based-exception-handling).</span></span> <span data-ttu-id="11164-107">Чтобы включить обработчик ошибок выравнивания системы, вызовите функцию [**функцию SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) с **SEM \_ ноалигнментфаултексцепт**.</span><span class="sxs-lookup"><span data-stu-id="11164-107">To enable the system alignment-fault hander, call the [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with **SEM\_NOALIGNMENTFAULTEXCEPT**.</span></span> <span data-ttu-id="11164-108">Однако обратите внимание, что процессы могут столкнуться с серьезным снижением производительности, если включен обработчик ошибок выравнивания системы, и процесс создает ошибки выравнивания.</span><span class="sxs-lookup"><span data-stu-id="11164-108">However, note that processes may experience severe performance degradation if the system alignment-fault handler is enabled and the process generates alignment faults.</span></span>

<span data-ttu-id="11164-109">Если отладчик WinDbg был установлен в качестве системного отладчика, WinDbg будет автоматически запущен, если любой процесс в системе создаст необработанное исключение.</span><span class="sxs-lookup"><span data-stu-id="11164-109">If the WinDbg debugger has been installed as the system debugger, WinDbg will automatically be launched if any process on the system generates an unhandled exception.</span></span> <span data-ttu-id="11164-110">Если отладчик не установлен в качестве системного отладчика, система отображает диалоговое окно с сообщением о том, что приложение обнаружило ошибку и предоставляло возможность сообщить о проблеме в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="11164-110">If you do not have a debugger installed as your system debugger, the system displays a dialog box stating that your application has encountered an error and providing the opportunity to report the problem to Microsoft.</span></span>

<span data-ttu-id="11164-111">В системах x64 и ARM64 все ошибки выравнивания обрабатываются сочетанием оборудования и программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="11164-111">On x64 and ARM64 systems, any alignment faults are handled by a combination of hardware and software.</span></span> <span data-ttu-id="11164-112">Для оптимальной производительности весь доступ к памяти должен быть правильно согласован.</span><span class="sxs-lookup"><span data-stu-id="11164-112">For best performance, all access to memory should be properly aligned.</span></span> <span data-ttu-id="11164-113">Кроме того, в ARM64 следует избегать несогласованного [доступа к переменным с блокировкой](/windows/desktop/Sync/interlocked-variable-access) , так как эти операции не являются атомарными.</span><span class="sxs-lookup"><span data-stu-id="11164-113">In addition, unaligned [interlocked variable access](/windows/desktop/Sync/interlocked-variable-access) should be avoided on ARM64, as these operations are not atomic-safe.</span></span>

 

 