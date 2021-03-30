---
title: Безопасность транспорта
description: Хотя это и не является предпочтительным способом, вы можете использовать параметры безопасности, предлагаемые транспортом именованных каналов, для добавления функций безопасности в распределенное приложение.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d129b5a373ed7304c142c66dd0e8b2d4e9035416
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331475"
---
# <a name="transport-security"></a><span data-ttu-id="2c1bf-103">Безопасность транспорта</span><span class="sxs-lookup"><span data-stu-id="2c1bf-103">Transport Security</span></span>

<span data-ttu-id="2c1bf-104">Хотя это и не является предпочтительным способом, вы можете использовать параметры безопасности, предлагаемые транспортом именованных каналов, для добавления функций безопасности в распределенное приложение.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-104">Although this is not the preferred method, you can use the security settings that the named-pipe transport offers to add security features to your distributed application.</span></span> <span data-ttu-id="2c1bf-105">Эти параметры безопасности используются с функциями Microsoft RPC, которые начинаются с префиксов [**рпксерверусепротсек**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) и [**рпксерверусеаллпротсекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), а также функций [**рпЦимперсонатеклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) и [**рпкреверттоселф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span><span class="sxs-lookup"><span data-stu-id="2c1bf-105">These security settings are used with the Microsoft RPC functions that start with the prefixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) and [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), and the functions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span></span>

> [!Note]  
> <span data-ttu-id="2c1bf-106">Если вы используете приложение, которое является службой и используете NTLM для обеспечения безопасности, необходимо добавить явную зависимость службы для приложения.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-106">If you are running an application that is a service and you are using NTLM for security, you must add an explicit service dependency for your application.</span></span> <span data-ttu-id="2c1bf-107">Secur32.dll будет вызывать диспетчер управления службами (SCM) для запуска службы пакета безопасности NTLM.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-107">The Secur32.dll will call the Service Control Manager (SCM) to begin the NTLM security package service.</span></span> <span data-ttu-id="2c1bf-108">Однако приложение RPC, которое является службой и работает в качестве системы, также должно обращаться к SC, если оно не подключается к другой службе на том же компьютере.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-108">However, an RPC application that is a service and is running as a system, must also contact the SC unless it is connecting to another service on the same computer.</span></span>

 

 

 




