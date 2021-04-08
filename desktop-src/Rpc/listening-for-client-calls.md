---
title: Ожидание вызовов клиента
description: После того как серверное приложение зарегистрировало интерфейсы, создало необходимые сведения о привязке и зарегистрировало свои конечные точки, он готов начать прослушивание удаленных вызовов процедур из клиентских программ.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- Удаленный вызов процедур RPC, задачи, прослушивание вызовов клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f375a4620e301f59d168bf5f7a4dbeedc0fb89f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888979"
---
# <a name="listening-for-client-calls"></a><span data-ttu-id="06dee-104">Ожидание вызовов клиента</span><span class="sxs-lookup"><span data-stu-id="06dee-104">Listening for Client Calls</span></span>

<span data-ttu-id="06dee-105">После того как серверное приложение зарегистрировало интерфейсы, создало необходимые сведения о привязке и зарегистрировало свои конечные точки, он готов начать прослушивание удаленных вызовов процедур из клиентских программ.</span><span class="sxs-lookup"><span data-stu-id="06dee-105">After your server application has registered its interfaces, created the necessary binding information, and registered its endpoints, it is ready to begin listening for remote procedure calls from client programs.</span></span>

<span data-ttu-id="06dee-106">Чтобы прослушивать удаленные вызовы процедур, серверная программа должна вызвать [**рпксерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), как показано в следующем фрагменте кода:</span><span class="sxs-lookup"><span data-stu-id="06dee-106">To listen for remote procedure calls, your server program must call [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



<span data-ttu-id="06dee-107">Сервер RPC имеет один или несколько потоков, которые выбирают клиентские вызовы и доставляют их в процедуры в зарегистрированных интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="06dee-107">An RPC Server has one or more threads that pick up client calls and deliver them to the routines in the registered interfaces.</span></span> <span data-ttu-id="06dee-108">Первым параметром функции [**рпксерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) является минимальное число создаваемых потоков.</span><span class="sxs-lookup"><span data-stu-id="06dee-108">The first parameter to the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function is the minimum number of threads to create.</span></span> <span data-ttu-id="06dee-109">Параметр является только подсказкой; время выполнения RPC может игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="06dee-109">The parameter is only a hint; the RPC run time may chose to ignore it.</span></span>

<span data-ttu-id="06dee-110">Вторым параметром для [**рпксерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) является максимальное число одновременных вызовов удаленных процедур для обработки.</span><span class="sxs-lookup"><span data-stu-id="06dee-110">The second parameter to [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) is the maximum number of concurrent remote procedure calls to handle.</span></span> <span data-ttu-id="06dee-111">Если вы хотите, чтобы в приложении использовалось максимальное значение по умолчанию, передайте \_ \_ \_ \_ \_ для этого параметра значение по умолчанию, равное Max RPC C Listening.</span><span class="sxs-lookup"><span data-stu-id="06dee-111">If you want your application to use the default maximum value, pass RPC\_C\_LISTEN\_MAX\_CALLS\_DEFAULT as the value for this parameter.</span></span>

<span data-ttu-id="06dee-112">Спецификация DCE вызывает функцию [**рпксерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) , чтобы она продолжала работать, пока не получит сигнал на завершение.</span><span class="sxs-lookup"><span data-stu-id="06dee-112">The DCE specification calls for [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) to keep running until it receives a signal to stop.</span></span> <span data-ttu-id="06dee-113">Одной из расширений Майкрософт для этой функции является обеспечение немедленного запуска прослушивания и возврата.</span><span class="sxs-lookup"><span data-stu-id="06dee-113">One Microsoft extension to this function is to enable it to begin listening and return immediately.</span></span> <span data-ttu-id="06dee-114">Если вы хотите, чтобы приложение использовало поведение DCE по умолчанию, задайте для третьего параметра значение 0.</span><span class="sxs-lookup"><span data-stu-id="06dee-114">If you want your application to use the default DCE behavior, set the third parameter to zero.</span></span> <span data-ttu-id="06dee-115">Дополнительные сведения см. в разделе [**рпксерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)и [**рпкмгмтваитсерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) .</span><span class="sxs-lookup"><span data-stu-id="06dee-115">See [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), and [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) for details.</span></span>

 

 




