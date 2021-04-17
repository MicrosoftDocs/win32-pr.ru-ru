---
title: Указанный пользователь
description: Указанный пользователь
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700516"
---
# <a name="specified-user"></a><span data-ttu-id="91bb8-103">Указанный пользователь</span><span class="sxs-lookup"><span data-stu-id="91bb8-103">Specified User</span></span>

<span data-ttu-id="91bb8-104">Указание конкретного пользователя (и пароля пользователя) является предпочтительным идентификатором для серверов COM.</span><span class="sxs-lookup"><span data-stu-id="91bb8-104">Specifying a particular user (and the user's password) is the preferred identity for COM servers.</span></span> <span data-ttu-id="91bb8-105">Причиной этого удостоверения является то, что никто не должен быть зарегистрирован на компьютере, на котором запущен сервер, и каждый клиент обращается к одному и тому же экземпляру сервера, если сервер регистрирует свою фабрику классов как многофакторную.</span><span class="sxs-lookup"><span data-stu-id="91bb8-105">The reason this identity is preferred is that no one has to be logged on the machine where the server is running for the server to run, and every client talks to the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="91bb8-106">Если на сервере имеется графический интерфейс пользователя, это удостоверение выбирать не следует. в противном случае пользователь не сможет увидеть пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="91bb8-106">If the server has a GUI, you should not choose this identity; if you do, the user will not be able to see the user interface.</span></span>

<span data-ttu-id="91bb8-107">Этот тип сервера имеет основной маркер и может обращаться к удаленным ресурсам, когда сервер с удостоверением запуска пользователя может не иметь возможности.</span><span class="sxs-lookup"><span data-stu-id="91bb8-107">This type of server has a primary token and can access remote resources where a server that has the launching-user identity might not be able to.</span></span> <span data-ttu-id="91bb8-108">Дополнительные сведения об маркерах олицетворения и доступа см. в разделе [уровни олицетворения](impersonation-levels.md) и [маскировка](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="91bb8-108">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="91bb8-109">Работа в качестве фиксированной учетной записи пользователя более безопасна, чем удостоверение интерактивного пользователя, поскольку это удостоверение может быть назначено приложению только тем, кто имеет пароль конкретного пользователя.</span><span class="sxs-lookup"><span data-stu-id="91bb8-109">Running as a fixed user account is more secure than the interactive user identity because this identity can be assigned to the application only by someone who has the specific user's password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91bb8-110">См. также</span><span class="sxs-lookup"><span data-stu-id="91bb8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91bb8-111">Служба удостоверений приложения</span><span class="sxs-lookup"><span data-stu-id="91bb8-111">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="91bb8-112">Интерактивный пользователь</span><span class="sxs-lookup"><span data-stu-id="91bb8-112">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="91bb8-113">Запуск пользователя</span><span class="sxs-lookup"><span data-stu-id="91bb8-113">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="91bb8-114">Удостоверение службы</span><span class="sxs-lookup"><span data-stu-id="91bb8-114">Service Identity</span></span>](service-identity.md)
</dt> </dl>

 

 




