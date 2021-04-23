---
title: Интерактивный пользователь
description: Интерактивным пользователем является пользователь, который в данный момент вошел в систему на компьютере, где работает сервер COM.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7fc8aeb5fd9674c09b40f6c46e4e173f5965a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339321"
---
# <a name="interactive-user"></a><span data-ttu-id="a2b6c-103">Интерактивный пользователь</span><span class="sxs-lookup"><span data-stu-id="a2b6c-103">Interactive User</span></span>

<span data-ttu-id="a2b6c-104">*Интерактивным пользователем* является пользователь, который в данный момент вошел в систему на компьютере, где работает сервер COM.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-104">The *interactive user* is the user that is currently logged on to the computer where the COM server is running.</span></span> <span data-ttu-id="a2b6c-105">Если удостоверение настроено как интерактивный пользователь, все клиенты используют один и тот же экземпляр сервера, если сервер регистрирует свою фабрику класса в качестве многофакторного использования.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-105">If the identity is set to be the interactive user, all clients use the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="a2b6c-106">Если ни один пользователь не вошел в систему, сервер не будет работать.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-106">If no user is logged on, the server will not run.</span></span> <span data-ttu-id="a2b6c-107">Если сервер имеет графический интерфейс пользователя (GUI), который должен видеть клиент, следует использовать для удостоверения сервера интерактивный пользователь.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-107">If the server has a graphical user interface (GUI) that the client needs to see, you should use interactive user for the server's identity.</span></span> <span data-ttu-id="a2b6c-108">Однако при выборе этого удостоверения происходит ряд угроз безопасности, так как сервер работает с удостоверением вошедшего в систему пользователя без ведома пользователя или его согласия.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-108">However, choosing this identity carries some security risks because the server runs under the identity of the logged on user without the logged on user's knowledge or consent.</span></span> <span data-ttu-id="a2b6c-109">Кроме того, приложение службы не может отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-109">In addition, a service application cannot display a user interface.</span></span> <span data-ttu-id="a2b6c-110">Дополнительные сведения см. в разделе [Интерактивные службы](/windows/desktop/Services/interactive-services).</span><span class="sxs-lookup"><span data-stu-id="a2b6c-110">For more information, see [Interactive Services](/windows/desktop/Services/interactive-services).</span></span>

<span data-ttu-id="a2b6c-111">Если сервер COM настроен для работы в качестве интерактивного пользователя, в среде служб терминалов сервер будет запущен в интерактивном сеансе, который соответствует удостоверению пользователя клиента.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-111">If a COM server is configured to run as the interactive user, in a terminal services environment, the server will be launched in the interactive session that matches the client's user identity.</span></span> <span data-ttu-id="a2b6c-112">Однако клиентское приложение может использовать моникер сеанса для ссылки на объект, предоставленный сервером в сеансе, который не соответствует удостоверению клиента.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-112">However, the client application can use the session moniker to reference an object provided by the server in a session that does not match the client identity.</span></span> <span data-ttu-id="a2b6c-113">При использовании этого приложения клиентское приложение может указать любой сеанс, в этом случае сервер будет работать от имени пользователя, владеющего сеансом, а не запускающего пользователя.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-113">When this is used, the client application can specify any session, in which case the server will run as the user who owns the session, not the launching user.</span></span> <span data-ttu-id="a2b6c-114">Разрешения на доступ по умолчанию в этом сценарии не позволяют запускающему пользователю вызывать методы на сервере.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-114">The default access permissions in this scenario would not allow the launching user to call methods on the server.</span></span> <span data-ttu-id="a2b6c-115">Однако остаются следующие риски безопасности:</span><span class="sxs-lookup"><span data-stu-id="a2b6c-115">However, the following security risks remain:</span></span>

-   <span data-ttu-id="a2b6c-116">Если COM-сервер предоставляет интерфейсы, которые не управляются COM, например TCP-порты, именованные каналы, порты LPC, разделы общей памяти и т. д., они могут использоваться запускающими пользователями для влияния на сервер.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-116">If the COM server exposes interfaces that are not controlled by COM, such as TCP ports, named pipes, LPC ports, shared memory sections, and so on, these could be used by the launching user to influence the server.</span></span> <span data-ttu-id="a2b6c-117">Объекты COM, настроенные для запуска от имени интерактивного пользователя, должны максимально сократить эту зону атак.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-117">COM objects configured to run as the interactive user should reduce this attack surface as much as possible.</span></span>
-   <span data-ttu-id="a2b6c-118">Объекты COM свободны для установки собственных разрешений на доступ.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-118">COM objects are free to set their own access permissions.</span></span> <span data-ttu-id="a2b6c-119">Если объект задает разрешения на доступ, либо в его регистрации AppID, либо путем вызова [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), чтобы разрешить запуск пользовательского доступа, пользователь сможет запустить сервер для запуска от имени другого пользователя, а затем получить доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="a2b6c-119">If the object sets access permissions, either in its AppID registration or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), to allow the launching user access, the user would be able to launch the server to run as another user, then access the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2b6c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a2b6c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2b6c-121">Служба удостоверений приложения</span><span class="sxs-lookup"><span data-stu-id="a2b6c-121">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="a2b6c-122">Запуск пользователя</span><span class="sxs-lookup"><span data-stu-id="a2b6c-122">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="a2b6c-123">Удостоверение службы</span><span class="sxs-lookup"><span data-stu-id="a2b6c-123">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="a2b6c-124">Указанный пользователь</span><span class="sxs-lookup"><span data-stu-id="a2b6c-124">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 