---
title: Сигнал о нестандартном канале
description: Совместно работающие приложения с общими данными, использующие каталог, могут использовать нестандартный сигнал, чтобы избежать рассогласованности версий и частичных обновлений.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067363"
---
# <a name="out-of-band-signaling"></a><span data-ttu-id="21b84-103">Сигнал о нестандартном канале</span><span class="sxs-lookup"><span data-stu-id="21b84-103">Out-of-Band Signaling</span></span>

<span data-ttu-id="21b84-104">Совместно работающие приложения с общими данными, использующие каталог, могут использовать нестандартный сигнал, чтобы избежать рассогласованности версий и частичных обновлений.</span><span class="sxs-lookup"><span data-stu-id="21b84-104">Cooperating applications that share common data using the directory can use out-of-band signaling to avoid both version skew and partial updates.</span></span> <span data-ttu-id="21b84-105">Говоря просто, совместно используемые приложения используют механизм, отличный от репликации каталога, чтобы информировать друг друга об изменениях в общих общих данных.</span><span class="sxs-lookup"><span data-stu-id="21b84-105">Put simply, the cooperating applications use a mechanism separate from directory replication to inform each other of changes in the shared common data.</span></span> <span data-ttu-id="21b84-106">Получение сигнала по внешнему каналу наиболее эффективно при использовании в сочетании с механизмом управления версиями. Это позволяет участнику, который обнаруживает изменение, уведомлять удаленных партнеров, какие версии общих данных следует ожидать.</span><span class="sxs-lookup"><span data-stu-id="21b84-106">Out-of-band signaling is most effective when used in combination with a versioning mechanism—this allows the partner detecting the change to notify remote partners what version of the shared data to wait for.</span></span>

<span data-ttu-id="21b84-107">При возврате к примеру RPC, указанному в разделе "отклонение версий" [поведения репликации в службах домен Active Directory Services](replication-behavior-in-active-directory-domain-services.md), сервер RPC может выполнить обратный вызов к подключенным клиентам, чтобы сообщить им о переходе на новый сервер: "я собираюсь переместить".</span><span class="sxs-lookup"><span data-stu-id="21b84-107">Returning to the RPC example given in the "Version Skew" section of [Replication Behavior in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), the RPC server could call back into connected clients to inform them of the move to a new server: "I am going to move.</span></span> <span data-ttu-id="21b84-108">В ближайшее время репликация поместит новый адрес вскоре, чтобы клиент мог управлять периодом перехода.</span><span class="sxs-lookup"><span data-stu-id="21b84-108">Please stand by, replication will bring you the new address shortly" so that the client can handle the transition period.</span></span>

<span data-ttu-id="21b84-109">Приложения, для которых требуется выполнение идентичных политик для взаимодействия друг с другом, могут использовать нестандартную сигнализацию, чтобы гарантировать, что новая политика не будет использоваться, пока она не получит все вовлеченные стороны.</span><span class="sxs-lookup"><span data-stu-id="21b84-109">Applications that require identical policies to be in force in order to communicate with each other can use out-of-band signaling to ensure that a new policy is not employed until all involved parties have received it.</span></span> <span data-ttu-id="21b84-110">Например, если изменилась политика IPsec между двумя компьютерами, агент на исходном компьютере может связаться с агентом на целевом компьютере для согласования применения измененной политики, при этом приложение задерживает работу исходного компьютера до тех пор, пока конечный компьютер не получит новую политику.</span><span class="sxs-lookup"><span data-stu-id="21b84-110">For example, if the Internet Protocol security (IPsec) policy between two machines is changed, an agent on the source machine could contact an agent on the destination machine to negotiate the application of the changed policy, with the source machine delaying application until the destination machine has received the new policy as well.</span></span>

 

 




