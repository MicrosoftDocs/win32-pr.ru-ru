---
title: Синтаксис и NDR64 для перемещения
description: Транспортный протокол NDR, также называемый синтаксисом передачи, позволяет выполнять вызовы RPC для обхода сети.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dfec9bc1569ef9a42d0bc844c3b098736f714ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070041"
---
# <a name="transfer-syntax-and-ndr64"></a><span data-ttu-id="a09bd-103">Синтаксис и NDR64 для перемещения</span><span class="sxs-lookup"><span data-stu-id="a09bd-103">Transfer Syntax and NDR64</span></span>

<span data-ttu-id="a09bd-104">Транспортный протокол NDR, также называемый синтаксисом передачи, позволяет выполнять вызовы RPC для обхода сети.</span><span class="sxs-lookup"><span data-stu-id="a09bd-104">The NDR wire protocol, also referred to as transfer syntax, enables RPC calls to traverse the network.</span></span> <span data-ttu-id="a09bd-105">Протокол проводной связи определяет сетевое представление вызова RPC, например порядок, в котором выполняется маршалирование элементов данных, выравнивание данных по сети, дополнительные сведения, включенные в данные, и другие проблемы.</span><span class="sxs-lookup"><span data-stu-id="a09bd-105">The wire protocol defines the wire representation of an RPC call, such as the order in which data members are marshaled, alignment of data on the wire, additional information included with the data, and other issues.</span></span> <span data-ttu-id="a09bd-106">Протокол NDR64 — это расширение для синтаксиса, основанного на 32-разрядных отчетах о недоставке, созданном специально для того, чтобы разработчики, нацеленные на 64-разрядные системы, получили оптимальную производительность.</span><span class="sxs-lookup"><span data-stu-id="a09bd-106">The NDR64 protocol is an extension to the 32-bit based NDR transfer syntax, created specifically to enable developers targeting 64-bit systems to achieve optimized performance.</span></span>

<span data-ttu-id="a09bd-107">Различия между форматом пропускной связи ОНД и форматом сети NDR64 различного размера указателей в 64-разрядной среде, а также других проблем.</span><span class="sxs-lookup"><span data-stu-id="a09bd-107">The differences between the NDR wire format and the NDR64 wire format addresses the different size of pointers in a 64-bit environment, as well as other issues.</span></span> <span data-ttu-id="a09bd-108">Механизм NDR64 обрабатывается RPC.</span><span class="sxs-lookup"><span data-stu-id="a09bd-108">The mechanics of NDR64 is handled by RPC.</span></span> <span data-ttu-id="a09bd-109">Для получения преимуществ NDR64 на 64-разрядных платформах разработчикам необходимо использовать только параметр командной строки/[**Protocol**](/windows/desktop/Midl/-protocol)**ALL** MIDL.</span><span class="sxs-lookup"><span data-stu-id="a09bd-109">Developers need only use the /[**protocol**](/windows/desktop/Midl/-protocol)**all** MIDL command line switch to obtain the benefits of NDR64 on 64-bit platforms.</span></span> <span data-ttu-id="a09bd-110">NDR64 доступен только на 64-разрядных платформах.</span><span class="sxs-lookup"><span data-stu-id="a09bd-110">NDR64 is available only on 64-bit platforms.</span></span>

 

 