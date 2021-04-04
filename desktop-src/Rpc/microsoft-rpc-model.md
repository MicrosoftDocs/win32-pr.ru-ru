---
title: Модель RPC
description: Удаленный вызов процедур (RPC) для языков программирования C и C++ разработан для удовлетворения потребностей разработчиков, работающих над программным обеспечением следующего поколения для операционных систем Windows.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- Удаленный вызов процедур RPC, описание, модель RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793212"
---
# <a name="the-rpc-model"></a><span data-ttu-id="51c14-104">Модель RPC</span><span class="sxs-lookup"><span data-stu-id="51c14-104">The RPC Model</span></span>

<span data-ttu-id="51c14-105">Удаленный вызов процедур (RPC) для языков программирования C и C++ разработан для удовлетворения потребностей разработчиков, работающих над программным обеспечением следующего поколения для операционных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="51c14-105">Remote Procedure Call (RPC) for the C and C++ programming languages is designed to help meet the needs of developers working on the next generation of software for Windows operating systems.</span></span>

<span data-ttu-id="51c14-106">RPC — это мощный, надежный, эффективный и безопасный механизм межпроцессного взаимодействия (IPC), обеспечивающий обмен данными и вызов функций, размещенных в другом процессе.</span><span class="sxs-lookup"><span data-stu-id="51c14-106">RPC is a powerful, robust, efficient, and secure interprocess communication (IPC) mechanism that enables data exchange and invocation of functionality residing in a different process.</span></span> <span data-ttu-id="51c14-107">Этот процесс может находиться на одном компьютере, в локальной сети или через Интернет.</span><span class="sxs-lookup"><span data-stu-id="51c14-107">That different process can be on the same machine, on the local area network, or across the Internet.</span></span> <span data-ttu-id="51c14-108">В этом разделе описывается модель программирования RPC и модель для распределенных систем, которые можно реализовать с помощью RPC.</span><span class="sxs-lookup"><span data-stu-id="51c14-108">This section explains the RPC programming model and the model for distributed systems that can be implemented using RPC.</span></span>

<span data-ttu-id="51c14-109">RPC полностью поддерживает 64-разрядную версию Windows.</span><span class="sxs-lookup"><span data-stu-id="51c14-109">RPC fully supports 64-bit Windows.</span></span> <span data-ttu-id="51c14-110">Существует три типа процессов: собственные 32-разрядные процессы, собственные 64-разрядные процессы и 32-разрядные процессы, выполняющиеся в эмуляторе 32-разрядного процесса в 64-разрядной системе (часто называются процессами WOW64).</span><span class="sxs-lookup"><span data-stu-id="51c14-110">There are three types of processes: native 32-bit processes, native 64-bit processes, and 32-bit processes running under the 32-bit process emulator on a 64-bit system (often referred to as WOW64 processes).</span></span> <span data-ttu-id="51c14-111">Дополнительные сведения о WOW64 см. в разделе [выполнение 32-разрядных приложений](/windows/desktop/WinProg64/running-32-bit-applications).</span><span class="sxs-lookup"><span data-stu-id="51c14-111">For more information about WOW64, see [Running 32-bit Applications](/windows/desktop/WinProg64/running-32-bit-applications).</span></span> <span data-ttu-id="51c14-112">С помощью RPC разработчики могут прозрачно взаимодействовать между разными типами процессов. RPC автоматически управляет различиями в процессах в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="51c14-112">Using RPC, developers can transparently communicate between different types of process; RPC automatically manages process differences behind the scenes.</span></span>

<span data-ttu-id="51c14-113">Изначально RPC был разработан как расширение для использование RPC.</span><span class="sxs-lookup"><span data-stu-id="51c14-113">RPC was initially developed as an extension to OSF RPC.</span></span> <span data-ttu-id="51c14-114">За исключением некоторых дополнительных функций, RPC работает с реализациями использование RPC других поставщиков.</span><span class="sxs-lookup"><span data-stu-id="51c14-114">With the exception of some of its advanced features, RPC is interoperable with other vendors' implementations of OSF RPC.</span></span>

<span data-ttu-id="51c14-115">В этом разделе также приводятся общие сведения о компонентах RPC и их работе.</span><span class="sxs-lookup"><span data-stu-id="51c14-115">This section also provides an overview of RPC components and their operation.</span></span> <span data-ttu-id="51c14-116">Сведения представлены в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="51c14-116">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="51c14-117">Модель программирования</span><span class="sxs-lookup"><span data-stu-id="51c14-117">The Programming Model</span></span>](the-programming-model.md)
-   [<span data-ttu-id="51c14-118">Модель для распределенных систем</span><span class="sxs-lookup"><span data-stu-id="51c14-118">The Model for Distributed Systems</span></span>](the-model-for-distributed-systems.md)
-   [<span data-ttu-id="51c14-119">Как работает RPC</span><span class="sxs-lookup"><span data-stu-id="51c14-119">How RPC Works</span></span>](how-rpc-works.md)
-   [<span data-ttu-id="51c14-120">Компоненты Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="51c14-120">Microsoft RPC Components</span></span>](microsoft-rpc-components.md)

 

 