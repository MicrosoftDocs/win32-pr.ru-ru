---
description: Общие сведения о функциях сеанса в управлении сетевыми ресурсами. Эти функции управляют сетевыми сеансами, установленными между рабочими станциями и серверами.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Функции сеанса (Управление сетевыми ресурсами)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdde451eb2942171569b24c36aae5d5742208e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409727"
---
# <a name="session-functions-network-share-management"></a><span data-ttu-id="c6f66-104">Функции сеанса (Управление сетевыми ресурсами)</span><span class="sxs-lookup"><span data-stu-id="c6f66-104">Session Functions (Network Share Management)</span></span>

<span data-ttu-id="c6f66-105">Функции сеанса управления сетью управляют сетевыми сеансами, установленными между рабочими станциями и серверами.</span><span class="sxs-lookup"><span data-stu-id="c6f66-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="c6f66-106">Функция требует, чтобы служба сервера была запущена на сервере.</span><span class="sxs-lookup"><span data-stu-id="c6f66-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="c6f66-107">Функции сеанса перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="c6f66-107">The session functions are listed following.</span></span>



| <span data-ttu-id="c6f66-108">Функция</span><span class="sxs-lookup"><span data-stu-id="c6f66-108">Function</span></span>                                       | <span data-ttu-id="c6f66-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c6f66-109">Description</span></span>                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6f66-110">**нетсессиондел**</span><span class="sxs-lookup"><span data-stu-id="c6f66-110">**NetSessionDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="c6f66-111">Удаляет текущие подключения между рабочей станцией и сервером. завершает сетевой сеанс.</span><span class="sxs-lookup"><span data-stu-id="c6f66-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="c6f66-112">**нетсессионенум**</span><span class="sxs-lookup"><span data-stu-id="c6f66-112">**NetSessionEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="c6f66-113">Возвращает сведения обо всех текущих сеансах, установленных для сервера.</span><span class="sxs-lookup"><span data-stu-id="c6f66-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="c6f66-114">**нетсессионжетинфо**</span><span class="sxs-lookup"><span data-stu-id="c6f66-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="c6f66-115">Возвращает сведения о конкретном сеансе.</span><span class="sxs-lookup"><span data-stu-id="c6f66-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="c6f66-116">*Сеанс* — это связь между рабочей станцией и сервером.</span><span class="sxs-lookup"><span data-stu-id="c6f66-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="c6f66-117">Сеанс устанавливается в первый раз, когда Рабочая станция устанавливает подключение к общему ресурсу на сервере.</span><span class="sxs-lookup"><span data-stu-id="c6f66-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="c6f66-118">Пока сеанс не завершится, все дальнейшие подключения между рабочей станцией и сервером будут входить в один сеанс.</span><span class="sxs-lookup"><span data-stu-id="c6f66-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="c6f66-119">Чтобы завершить сеанс, приложение на стороне сервера соединения вызывает функцию [**нетсессиондел**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) .</span><span class="sxs-lookup"><span data-stu-id="c6f66-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="c6f66-120">Функции сеанса управления сетью управляют сведениями для отдельных пользователей с помощью параметра *username* .</span><span class="sxs-lookup"><span data-stu-id="c6f66-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="c6f66-121">Так как в сеансе может быть несколько пользователей, этот параметр необходим для доступа к сведениям о конкретном пользователе для сеанса.</span><span class="sxs-lookup"><span data-stu-id="c6f66-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="c6f66-122">Функции сеанса доступны на пяти уровнях информации:</span><span class="sxs-lookup"><span data-stu-id="c6f66-122">Session functions are available at five information levels:</span></span>

<dl>

[<span data-ttu-id="c6f66-123">**\_Сведения о сеансе \_ 0**</span><span class="sxs-lookup"><span data-stu-id="c6f66-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[<span data-ttu-id="c6f66-124">**\_Сведения о сеансе \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c6f66-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[<span data-ttu-id="c6f66-125">**\_Сведения о сеансе \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c6f66-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[<span data-ttu-id="c6f66-126">**\_Сведения о сеансе \_ 10**</span><span class="sxs-lookup"><span data-stu-id="c6f66-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[<span data-ttu-id="c6f66-127">**\_Сведения о сеансе \_ 502**</span><span class="sxs-lookup"><span data-stu-id="c6f66-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

<span data-ttu-id="c6f66-128">При программировании для Active Directory можно вызвать определенные методы интерфейса Active Directory (ADSI) для достижения тех же функций, которые можно достичь, вызвав функции сеанса управления сетью.</span><span class="sxs-lookup"><span data-stu-id="c6f66-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="c6f66-129">Дополнительные сведения см. в разделе [**иадссессион**](/windows/desktop/api/iads/nn-iads-iadssession) и [**иадсфилесервицеоператионс**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="c6f66-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
