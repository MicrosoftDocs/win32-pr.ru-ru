---
title: Удаленные вызовы протокола SAM RPC ограничиваются только локальными администраторами
description: Протокол SAM RPC ограничен. Это означает, что только члены локальной группы администраторов могут выполнять удаленные вызовы к методам этого протокола. Active Directory поведение контроллера домена не затрагивается.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133050"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a><span data-ttu-id="c6a04-105">Удаленные вызовы протокола SAM RPC ограничиваются только локальными администраторами</span><span class="sxs-lookup"><span data-stu-id="c6a04-105">Remote calls to the SAM RPC protocol are restricted to only local administrators</span></span>

<span data-ttu-id="c6a04-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="c6a04-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c6a04-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="c6a04-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c6a04-108">Протокол SAM RPC ограничен.</span><span class="sxs-lookup"><span data-stu-id="c6a04-108">The SAM RPC protocol is being restricted.</span></span> <span data-ttu-id="c6a04-109">Это означает, что только члены локальной группы администраторов могут выполнять удаленные вызовы к методам этого протокола.</span><span class="sxs-lookup"><span data-stu-id="c6a04-109">This means that only members of the local Administrator group can make remote calls against methods in this protocol.</span></span> <span data-ttu-id="c6a04-110">Active Directory поведение контроллера домена не затрагивается.</span><span class="sxs-lookup"><span data-stu-id="c6a04-110">Active Directory domain controller behavior is unaffected.</span></span>

## <a name="mitigations"></a><span data-ttu-id="c6a04-111">Устранение проблем</span><span class="sxs-lookup"><span data-stu-id="c6a04-111">Mitigations</span></span>

<span data-ttu-id="c6a04-112">Убедитесь, что нужные пользователи настроены как Администраторы на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c6a04-112">Ensure that the right users are set as administrators on the PC.</span></span> <span data-ttu-id="c6a04-113">Список управления доступом, используемый для проверки доступа, можно настроить с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="c6a04-113">The ACL used for the access check is configurable via group policy.</span></span>

 

 




