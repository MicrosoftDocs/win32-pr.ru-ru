---
title: Создание поставщика протокол удаленного рабочего стола
description: Сведения о создании поставщика протокол удаленного рабочего стола. Диспетчер протоколов реализуется как сервер COM и регистрируется в расположении, которое выполняется при запуске службы службы удаленных рабочих столов.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41265a350b4d5c559731a09abc21aa4c81b9b29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681376"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a><span data-ttu-id="e68db-104">Создание поставщика протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="e68db-104">Creating a Remote Desktop Protocol Provider</span></span>

<span data-ttu-id="e68db-105">В следующих разделах содержатся сведения о создании поставщика протокол удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="e68db-105">The following sections contain information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="e68db-106">Диспетчер протоколов реализуется как сервер COM и регистрируется в расположении, которое выполняется при запуске службы службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e68db-106">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e68db-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="e68db-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="e68db-108">Регистрация диспетчера протокола</span><span class="sxs-lookup"><span data-stu-id="e68db-108">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
</dt> <dd>

<span data-ttu-id="e68db-109">Необходимо создать хотя бы одну запись значения реестра для диспетчера протоколов, чтобы служба службы удаленных рабочих столов могла создать ее экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e68db-109">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

</dd> <dt>

[<span data-ttu-id="e68db-110">Последовательность вызовов методов</span><span class="sxs-lookup"><span data-stu-id="e68db-110">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dd>

<span data-ttu-id="e68db-111">Служба службы удаленных рабочих столов и поставщик протокола вызывают друг друга в четко определенных последовательностях.</span><span class="sxs-lookup"><span data-stu-id="e68db-111">The Remote Desktop Services service and your protocol provider call each other in clearly defined sequences.</span></span>

</dd> </dl>

-   [<span data-ttu-id="e68db-112">Регистрация диспетчера протокола</span><span class="sxs-lookup"><span data-stu-id="e68db-112">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
-   [<span data-ttu-id="e68db-113">Последовательность вызовов методов</span><span class="sxs-lookup"><span data-stu-id="e68db-113">Method Call Sequence</span></span>](method-call-sequence.md)

## <a name="related-topics"></a><span data-ttu-id="e68db-114">См. также</span><span class="sxs-lookup"><span data-stu-id="e68db-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e68db-115">API поставщика протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="e68db-115">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dt>

[<span data-ttu-id="e68db-116">Использование службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="e68db-116">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> </dl>

 

 




