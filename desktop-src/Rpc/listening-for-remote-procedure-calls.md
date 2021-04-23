---
title: Прослушивание удаленных вызовов процедур
description: После того как серверная программа регистрирует сведения о привязке и объявляет о своем присутствии в базе данных службы имен, она может начать прослушивание конечной точки для удаленных вызовов процедур.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067260"
---
# <a name="listening-for-remote-procedure-calls"></a><span data-ttu-id="002bc-103">Прослушивание удаленных вызовов процедур</span><span class="sxs-lookup"><span data-stu-id="002bc-103">Listening for Remote Procedure Calls</span></span>

<span data-ttu-id="002bc-104">После того как серверная программа регистрирует сведения о привязке и объявляет о своем присутствии в базе данных службы имен, она может начать прослушивание конечной точки для удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="002bc-104">After a server program registers its binding information and advertises its presence in a name service database, it can begin listening to the endpoint for remote procedure calls.</span></span> <span data-ttu-id="002bc-105">Серверные программы вызывают функцию [**рпксерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) для отслеживания конечных точек клиентских вызовов удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="002bc-105">Server programs call the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to monitor endpoints for client invocations of remote procedures.</span></span>

<span data-ttu-id="002bc-106">Спецификация DCE [**рпксерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) указывает, что она не должна возвращаться до тех пор, пока функция в серверной программе не вызовет [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span><span class="sxs-lookup"><span data-stu-id="002bc-106">The DCE specification of [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indicates that it should not return until a function in the server program calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span></span> <span data-ttu-id="002bc-107">В реализации Microsoft RPC **рпксерверлистен** используются два параметра, которые не отображаются в спецификации DCE: *донтваит* и *минимумкаллсреадс*.</span><span class="sxs-lookup"><span data-stu-id="002bc-107">The Microsoft RPC implementation of **RpcServerListen** uses two parameters that do not appear in the DCE specification: *DontWait* and *MinimumCallThreads*.</span></span> <span data-ttu-id="002bc-108">Серверная программа может передать ненулевое значение параметра *донтваит* .</span><span class="sxs-lookup"><span data-stu-id="002bc-108">Your server program can pass a nonzero value for the *DontWait* parameter.</span></span> <span data-ttu-id="002bc-109">Если это так, функция **рпксерверлистен** будет возвращаться немедленно.</span><span class="sxs-lookup"><span data-stu-id="002bc-109">If it does, the **RpcServerListen** function will return immediately.</span></span> <span data-ttu-id="002bc-110">Используйте подпрограммы [**рпкмгмтваитсерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) для выполнения операции ожидания, обычно связанной с **рпксерверлистен**.</span><span class="sxs-lookup"><span data-stu-id="002bc-110">Use the [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) routine to perform the wait operation usually associated with **RpcServerListen**.</span></span>

 

 




