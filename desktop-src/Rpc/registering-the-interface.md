---
title: Регистрация интерфейса
description: Регистрация интерфейса, поддерживаемого серверной программой, позволяет отправлять удаленные вызовы процедур из клиентских программ в соответствующую серверную процедуру.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- Удаленный вызов процедур RPC, задачи, регистрация интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252748"
---
# <a name="registering-the-interface"></a><span data-ttu-id="0c665-104">Регистрация интерфейса</span><span class="sxs-lookup"><span data-stu-id="0c665-104">Registering the Interface</span></span>

<span data-ttu-id="0c665-105">Регистрация интерфейса, поддерживаемого серверной программой, позволяет отправлять удаленные вызовы процедур из клиентских программ в соответствующую серверную процедуру.</span><span class="sxs-lookup"><span data-stu-id="0c665-105">Registering the interface that a server program supports enables remote procedure calls from client programs to be dispatched to the proper server routine.</span></span> <span data-ttu-id="0c665-106">Серверные программы вызывают [**рпксерверрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) для регистрации своих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="0c665-106">Server programs call [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to register their interfaces.</span></span> <span data-ttu-id="0c665-107">В следующем фрагменте кода демонстрируется его использование:</span><span class="sxs-lookup"><span data-stu-id="0c665-107">The following code fragment demonstrates its use:</span></span>


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



<span data-ttu-id="0c665-108">Первым параметром функции [**рпксерверрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) является структура, которую компилятор MIDL создает из IDL-файла, определяющего интерфейс (или интерфейсы) для сервера.</span><span class="sxs-lookup"><span data-stu-id="0c665-108">The first parameter to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is a structure the MIDL compiler generates from the IDL file that defines the interface (or interfaces) for the server.</span></span> <span data-ttu-id="0c665-109">Второй и третий параметры — это UUID и вектор точки входа соответственно.</span><span class="sxs-lookup"><span data-stu-id="0c665-109">The second and third parameters are a UUID and an entry-point vector, respectively.</span></span> <span data-ttu-id="0c665-110">В этом примере для них задано **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="0c665-110">They are set to **NULL** in this example.</span></span> <span data-ttu-id="0c665-111">Во многих случаях серверная программа установит для этих параметров значения **null**.</span><span class="sxs-lookup"><span data-stu-id="0c665-111">In many instances, your server program will set these parameter values to **NULL**.</span></span> <span data-ttu-id="0c665-112">Серверные программы используют второй и третий параметры, если они предоставляют несколько реализаций одних и тех же процедур в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="0c665-112">Server programs use the second and third parameters when they provide multiple implementations of the same procedures in an interface.</span></span> <span data-ttu-id="0c665-113">Дополнительные сведения см. в разделе [векторы точки входа](registering-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="0c665-113">For more information, see [Entry-Point Vectors](registering-interfaces.md).</span></span>

<span data-ttu-id="0c665-114">Серверные программы также могут использовать [**рпксерверрегистерифекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) для регистрации интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0c665-114">Server programs can also use [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) to register an interface.</span></span> <span data-ttu-id="0c665-115">Одно из преимуществ использования этой функции заключается в том, что она предоставляет приложению возможность установить функцию обратного вызова безопасности.</span><span class="sxs-lookup"><span data-stu-id="0c665-115">One advantage of using this function is that it provides your application with the ability to set a security-callback function.</span></span> <span data-ttu-id="0c665-116">Использование функций обратного вызова безопасности является рекомендуемым подходом к обеспечению безопасности интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0c665-116">Using security-callback functions is the recommended approach to securing an interface.</span></span>

> [!Note]  
> <span data-ttu-id="0c665-117">MIDL создает две очень похожие структуры: одну для клиента и одну для сервера.</span><span class="sxs-lookup"><span data-stu-id="0c665-117">MIDL produces two very similar structures, one for the client and one for the server.</span></span> <span data-ttu-id="0c665-118">Структура, передаваемая функции [**рпксерверрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) , является серверной версией структуры, созданной с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="0c665-118">The structure passed to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is the server version of the MIDL-produced structure.</span></span>

 

 

 




