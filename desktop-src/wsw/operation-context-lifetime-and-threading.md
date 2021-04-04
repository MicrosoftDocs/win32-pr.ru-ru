---
title: Время существования контекста операции и работа с потоками
description: Время существования контекста операции, представленного \_ \_ обработчиком контекста операции WS, определяет время существования содержащихся в нем свойств.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Время существования контекста операции и веб-службы потоковой обработки для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea27b0b1dc41ccd029df7d726fe92631adc1ee4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797310"
---
# <a name="operation-context-lifetime-and-threading"></a><span data-ttu-id="1314f-106">Время существования контекста операции и работа с потоками</span><span class="sxs-lookup"><span data-stu-id="1314f-106">Operation Context Lifetime and Threading</span></span>

<span data-ttu-id="1314f-107">Время существования контекста операции, представленного обработчиком [ \_ \_ контекста операции WS](ws-operation-context.md) , определяет время существования содержащихся в нем свойств.</span><span class="sxs-lookup"><span data-stu-id="1314f-107">The lifetime of the operation context, represented by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) handle, determines the lifetime of the properties it contains.</span></span> <span data-ttu-id="1314f-108">Таким образом, контекст должен использоваться только в течение времени существования [операции службы](service-operation.md) или обратного вызова, для которого предоставлен.</span><span class="sxs-lookup"><span data-stu-id="1314f-108">Therefore, a context should only be used within the lifetime of the [service operation](service-operation.md) or the callback to which its provided.</span></span> <span data-ttu-id="1314f-109">Время существования синхронного вызова — это выполнение самой функции.</span><span class="sxs-lookup"><span data-stu-id="1314f-109">The lifetime of a synchronous call is the execution of function itself.</span></span> <span data-ttu-id="1314f-110">Для асинхронного вызова время существования завершается после завершения асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="1314f-110">For an asynchronous call the lifetime ends once the asynchronous call is completed.</span></span> <span data-ttu-id="1314f-111">Модель службы не дает никаких гарантий относительно контекста после завершения вызова.</span><span class="sxs-lookup"><span data-stu-id="1314f-111">The Service Model gives no guarantees about the context once the call is completed.</span></span> <span data-ttu-id="1314f-112">Поведение контекста операции или его свойств, которые выходят за пределы времени существования, не определено.</span><span class="sxs-lookup"><span data-stu-id="1314f-112">The behavior of relying on operation context or any of its properties beyond its lifetime is undefined.</span></span>


<span data-ttu-id="1314f-113">См. также пример калькулятора на основе сеанса, [сессионфуллкалкулаторсервицеексампле](sessionfullcalculatorserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="1314f-113">See also, the session based calculator example, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span></span>

## <a name="threading-model"></a><span data-ttu-id="1314f-114">Модель потоков</span><span class="sxs-lookup"><span data-stu-id="1314f-114">Threading Model</span></span>

<span data-ttu-id="1314f-115">Контекст операции поддерживает свободную работу с потоками, однако это верно для контекста операции и не применяется к содержащимся в нем свойствам.</span><span class="sxs-lookup"><span data-stu-id="1314f-115">The operation context supports free threading, however this is true of the operation context itself and does not apply to any of the properties it contains.</span></span>

<span data-ttu-id="1314f-116">При регистрации обратного вызова Cancel для операции службы с помощью функции [**всрегистероператионфорканцел**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) Обратите внимание, что первая регистрация будет выполнена. Однако при многократном задании обратного вызова отмены произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="1314f-116">When you register a cancel callback for a service operation through the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function, note that the first registration will succeed; setting the cancel callback multiple times, however, will fail.</span></span>

 

 




