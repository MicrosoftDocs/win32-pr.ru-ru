---
title: Запуск пользователя
description: Запуск пользователя
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891117"
---
# <a name="launching-user"></a><span data-ttu-id="96a82-103">Запуск пользователя</span><span class="sxs-lookup"><span data-stu-id="96a82-103">Launching User</span></span>

<span data-ttu-id="96a82-104">Это значение по умолчанию для удостоверения приложения.</span><span class="sxs-lookup"><span data-stu-id="96a82-104">This is the default setting for the application identity.</span></span> <span data-ttu-id="96a82-105">При выборе запуска пользователя для удостоверения приложения каждая учетная запись клиента получает новый экземпляр сервера, а каждый сервер получает свою собственную [станцию](/windows/desktop/winstation/window-stations).</span><span class="sxs-lookup"><span data-stu-id="96a82-105">When the launching user is chosen for the application's identity, each client account gets a new instance of the server and each server gets its own [window station](/windows/desktop/winstation/window-stations).</span></span> <span data-ttu-id="96a82-106">Из-за наличия отдельных экземпляров сервера Запуск пользователя является параметром идентификатора защиты наивысшего уровня безопасности.</span><span class="sxs-lookup"><span data-stu-id="96a82-106">Because of the separate server instances, launching user is the highest-level security protection identity setting.</span></span> <span data-ttu-id="96a82-107">Однако существуют ограничения на потребление ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96a82-107">However, there are finite limits on resource consumption.</span></span> <span data-ttu-id="96a82-108">Кроме того, любой графический пользовательский интерфейс, отображаемый сервером, не будет виден клиенту.</span><span class="sxs-lookup"><span data-stu-id="96a82-108">Also, any GUI the server displays will not be seen by the client.</span></span>

<span data-ttu-id="96a82-109">Если приложение имеет удостоверение запускающего пользователя, оно выполняется с маркером олицетворения.</span><span class="sxs-lookup"><span data-stu-id="96a82-109">If the application has the identity of the launching user, it runs with an impersonation token.</span></span> <span data-ttu-id="96a82-110">Дополнительные сведения об маркерах олицетворения и доступа см. в разделе [уровни олицетворения](impersonation-levels.md) и [маскировка](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="96a82-110">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="96a82-111">См. также</span><span class="sxs-lookup"><span data-stu-id="96a82-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96a82-112">Служба удостоверений приложения</span><span class="sxs-lookup"><span data-stu-id="96a82-112">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="96a82-113">Интерактивный пользователь</span><span class="sxs-lookup"><span data-stu-id="96a82-113">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="96a82-114">Удостоверение службы</span><span class="sxs-lookup"><span data-stu-id="96a82-114">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="96a82-115">Указанный пользователь</span><span class="sxs-lookup"><span data-stu-id="96a82-115">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 