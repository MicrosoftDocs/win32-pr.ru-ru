---
title: Безопасность и расширенные сведения об ошибках
description: Расширенные сведения об ошибках предлагают полезные данные при устранении неполадок RPC, но такие данные во многом считаются конфиденциальными для организаций, имеющих повышенный уровень безопасности.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779088"
---
# <a name="security-and-extended-error-information"></a><span data-ttu-id="17b33-103">Безопасность и расширенные сведения об ошибках</span><span class="sxs-lookup"><span data-stu-id="17b33-103">Security and Extended Error Information</span></span>

<span data-ttu-id="17b33-104">Расширенные сведения об ошибках предлагают полезные данные при устранении неполадок RPC, но такие данные во многом считаются конфиденциальными для организаций, имеющих повышенный уровень безопасности.</span><span class="sxs-lookup"><span data-stu-id="17b33-104">Extended error information offers very useful data when troubleshooting an RPC problem, but such data many be considered confidential by security-conscious organizations.</span></span> <span data-ttu-id="17b33-105">Учитывая такие проблемы безопасности, расширенные сведения об ошибках по умолчанию отключены.</span><span class="sxs-lookup"><span data-stu-id="17b33-105">In consideration of such security issues, extended error information is turned off by default.</span></span>

<span data-ttu-id="17b33-106">Расширенные сведения об ошибках по-прежнему создаются, когда расширенные сведения об ошибках отключены, но данные никогда не передаются через границы процессов или компьютеров.</span><span class="sxs-lookup"><span data-stu-id="17b33-106">Extended error information is still generated when extended error information is disabled, but the information is never transmitted across process or computer boundaries.</span></span> <span data-ttu-id="17b33-107">Такой подход позволяет использовать сведения об ошибках средствами, имеющими доступ к адресному пространству процесса, например отладчикам.</span><span class="sxs-lookup"><span data-stu-id="17b33-107">This approach enables error information to be used by tools that have access to the process address space, such as debuggers.</span></span> <span data-ttu-id="17b33-108">Если этот ключ включен, расширенные сведения об ошибках формируются и могут быть отправлены через границы процессов и компьютеров.</span><span class="sxs-lookup"><span data-stu-id="17b33-108">When turned on, extended error information is generated and can be sent across process and computer boundaries.</span></span> <span data-ttu-id="17b33-109">В настоящее время расширенные сведения об ошибках используются для последовательностей протоколов подключения и локальных RPC (ЛРПК).</span><span class="sxs-lookup"><span data-stu-id="17b33-109">Currently, extended error information is used for connection oriented protocol sequences and local RPC (LRPC).</span></span> <span data-ttu-id="17b33-110">Он частично реализован для датаграмм.</span><span class="sxs-lookup"><span data-stu-id="17b33-110">It is partially implemented for datagrams.</span></span>

 

 




