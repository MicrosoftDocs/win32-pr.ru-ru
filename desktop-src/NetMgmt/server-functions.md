---
title: Функции сервера (Управление сетью)
description: Функции сервера управления сетью выполняют задачи администрирования на локальном или удаленном сервере. Ниже перечислены функции сервера.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43758fa822ce60d484418431941a386681bb77d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104071024"
---
# <a name="server-functions-network-management"></a><span data-ttu-id="4f59a-104">Функции сервера (Управление сетью)</span><span class="sxs-lookup"><span data-stu-id="4f59a-104">Server Functions (Network Management)</span></span>

<span data-ttu-id="4f59a-105">Функции сервера управления сетью выполняют задачи администрирования на локальном или удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="4f59a-105">The network management server functions perform administrative tasks on a local or remote server.</span></span> <span data-ttu-id="4f59a-106">Ниже перечислены функции сервера.</span><span class="sxs-lookup"><span data-stu-id="4f59a-106">The server functions are listed following.</span></span>



| <span data-ttu-id="4f59a-107">Функция</span><span class="sxs-lookup"><span data-stu-id="4f59a-107">Function</span></span>                                       | <span data-ttu-id="4f59a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4f59a-108">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f59a-109">**нетсервердискенум**</span><span class="sxs-lookup"><span data-stu-id="4f59a-109">**NetServerDiskEnum**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | <span data-ttu-id="4f59a-110">Возвращает список локальных дисков на сервере.</span><span class="sxs-lookup"><span data-stu-id="4f59a-110">Returns a list of local disk drives on a server.</span></span>                                   |
| [<span data-ttu-id="4f59a-111">**нетсерверенум**</span><span class="sxs-lookup"><span data-stu-id="4f59a-111">**NetServerEnum**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | <span data-ttu-id="4f59a-112">Список всех видимых серверов определенного типа (или типов) в указанном домене.</span><span class="sxs-lookup"><span data-stu-id="4f59a-112">Lists all visible servers of a particular type (or types) in the specified domain.</span></span> |
| [<span data-ttu-id="4f59a-113">**нетсервержетинфо**</span><span class="sxs-lookup"><span data-stu-id="4f59a-113">**NetServerGetInfo**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | <span data-ttu-id="4f59a-114">Возвращает сведения о конфигурации указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="4f59a-114">Returns configuration information about a specified server.</span></span>                        |
| [<span data-ttu-id="4f59a-115">**нетсерверсетинфо**</span><span class="sxs-lookup"><span data-stu-id="4f59a-115">**NetServerSetInfo**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | <span data-ttu-id="4f59a-116">Задает параметры операционной системы для сервера.</span><span class="sxs-lookup"><span data-stu-id="4f59a-116">Sets the operating parameters for a server.</span></span>                                        |



 

<span data-ttu-id="4f59a-117">Только пользователь или приложение с членством в административной группе на локальном или удаленном сервере может выполнять административные задачи на этом сервере для управления работой сервера, доступом пользователей и предоставлением общего доступа к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="4f59a-117">Only a user or application with admin group membership on a local or remote server can perform administrative tasks on that server to control the server's operation, user access, and resource sharing.</span></span> <span data-ttu-id="4f59a-118">Параметры низкого уровня, влияющие на работу сервера, можно просмотреть и изменить, вызвав функции [**нетсервержетинфо**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) и [**нетсерверсетинфо**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) .</span><span class="sxs-lookup"><span data-stu-id="4f59a-118">The low-level parameters that affect a server's operation can be examined and modified by calling the [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) and [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) functions.</span></span> <span data-ttu-id="4f59a-119">Эти параметры определяются в файле LANMAN.INI сервера.</span><span class="sxs-lookup"><span data-stu-id="4f59a-119">These parameters are defined in the server's LANMAN.INI file.</span></span>

<span data-ttu-id="4f59a-120">Большинство функций сервера управления сетью выполняются только на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="4f59a-120">Most network management server functions execute only on a remote server.</span></span> <span data-ttu-id="4f59a-121">Функция [**нетсерверенум**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) выполняется как на локальной рабочей станции, так и на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="4f59a-121">The [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) function executes on either a local workstation or a remote server.</span></span> <span data-ttu-id="4f59a-122">При попытке выполнения других серверных функций на локальной рабочей станции функции возвращают ошибку НЕРР \_ RemoteOnly.</span><span class="sxs-lookup"><span data-stu-id="4f59a-122">If you attempt to execute other server functions on a local workstation, the functions return the error NERR\_RemoteOnly.</span></span>

<span data-ttu-id="4f59a-123">Сведения, относящиеся к серверу, доступны на следующих уровнях:</span><span class="sxs-lookup"><span data-stu-id="4f59a-123">Server-specific information is available at the following levels:</span></span>

-   [<span data-ttu-id="4f59a-124">**\_Сведения о сервере \_ 100**</span><span class="sxs-lookup"><span data-stu-id="4f59a-124">**SERVER\_INFO\_100**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [<span data-ttu-id="4f59a-125">**\_Сведения о сервере \_ 101**</span><span class="sxs-lookup"><span data-stu-id="4f59a-125">**SERVER\_INFO\_101**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [<span data-ttu-id="4f59a-126">**\_Сведения о сервере \_ 102**</span><span class="sxs-lookup"><span data-stu-id="4f59a-126">**SERVER\_INFO\_102**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [<span data-ttu-id="4f59a-127">**\_Сведения о сервере \_ 402**</span><span class="sxs-lookup"><span data-stu-id="4f59a-127">**SERVER\_INFO\_402**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [<span data-ttu-id="4f59a-128">**\_Сведения о сервере \_ 403**</span><span class="sxs-lookup"><span data-stu-id="4f59a-128">**SERVER\_INFO\_403**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [<span data-ttu-id="4f59a-129">**\_Сведения о сервере \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="4f59a-129">**SERVER\_INFO\_1501**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [<span data-ttu-id="4f59a-130">**\_Сведения о сервере \_ 1502**</span><span class="sxs-lookup"><span data-stu-id="4f59a-130">**SERVER\_INFO\_1502**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [<span data-ttu-id="4f59a-131">**\_Сведения о сервере \_ 1503**</span><span class="sxs-lookup"><span data-stu-id="4f59a-131">**SERVER\_INFO\_1503**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [<span data-ttu-id="4f59a-132">**\_Сведения о сервере \_ 1506**</span><span class="sxs-lookup"><span data-stu-id="4f59a-132">**SERVER\_INFO\_1506**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [<span data-ttu-id="4f59a-133">**\_Сведения о сервере \_ 1509**</span><span class="sxs-lookup"><span data-stu-id="4f59a-133">**SERVER\_INFO\_1509**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [<span data-ttu-id="4f59a-134">**\_Сведения о сервере \_ 1510**</span><span class="sxs-lookup"><span data-stu-id="4f59a-134">**SERVER\_INFO\_1510**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [<span data-ttu-id="4f59a-135">**\_Сведения о сервере \_ 1511**</span><span class="sxs-lookup"><span data-stu-id="4f59a-135">**SERVER\_INFO\_1511**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [<span data-ttu-id="4f59a-136">**\_Сведения о сервере \_ 1512**</span><span class="sxs-lookup"><span data-stu-id="4f59a-136">**SERVER\_INFO\_1512**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [<span data-ttu-id="4f59a-137">**\_Сведения о сервере \_ 1513**</span><span class="sxs-lookup"><span data-stu-id="4f59a-137">**SERVER\_INFO\_1513**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [<span data-ttu-id="4f59a-138">**\_Сведения о сервере \_ 1515**</span><span class="sxs-lookup"><span data-stu-id="4f59a-138">**SERVER\_INFO\_1515**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [<span data-ttu-id="4f59a-139">**\_Сведения о сервере \_ 1516**</span><span class="sxs-lookup"><span data-stu-id="4f59a-139">**SERVER\_INFO\_1516**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [<span data-ttu-id="4f59a-140">**\_Сведения о сервере \_ 1518**</span><span class="sxs-lookup"><span data-stu-id="4f59a-140">**SERVER\_INFO\_1518**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [<span data-ttu-id="4f59a-141">**\_Сведения о сервере \_ 1523**</span><span class="sxs-lookup"><span data-stu-id="4f59a-141">**SERVER\_INFO\_1523**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [<span data-ttu-id="4f59a-142">**\_Сведения о сервере \_ 1528**</span><span class="sxs-lookup"><span data-stu-id="4f59a-142">**SERVER\_INFO\_1528**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [<span data-ttu-id="4f59a-143">**\_Сведения о сервере \_ 1529**</span><span class="sxs-lookup"><span data-stu-id="4f59a-143">**SERVER\_INFO\_1529**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [<span data-ttu-id="4f59a-144">**\_Сведения о сервере \_ 1530**</span><span class="sxs-lookup"><span data-stu-id="4f59a-144">**SERVER\_INFO\_1530**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [<span data-ttu-id="4f59a-145">**\_Сведения о сервере \_ 1533**</span><span class="sxs-lookup"><span data-stu-id="4f59a-145">**SERVER\_INFO\_1533**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [<span data-ttu-id="4f59a-146">**\_Сведения о сервере \_ 1536**</span><span class="sxs-lookup"><span data-stu-id="4f59a-146">**SERVER\_INFO\_1536**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [<span data-ttu-id="4f59a-147">**\_Сведения о сервере \_ 1538**</span><span class="sxs-lookup"><span data-stu-id="4f59a-147">**SERVER\_INFO\_1538**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [<span data-ttu-id="4f59a-148">**\_Сведения о сервере \_ 1539**</span><span class="sxs-lookup"><span data-stu-id="4f59a-148">**SERVER\_INFO\_1539**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [<span data-ttu-id="4f59a-149">**\_Сведения о сервере \_ 1540**</span><span class="sxs-lookup"><span data-stu-id="4f59a-149">**SERVER\_INFO\_1540**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [<span data-ttu-id="4f59a-150">**\_Сведения о сервере \_ 1541**</span><span class="sxs-lookup"><span data-stu-id="4f59a-150">**SERVER\_INFO\_1541**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [<span data-ttu-id="4f59a-151">**\_Сведения о сервере \_ 1542**</span><span class="sxs-lookup"><span data-stu-id="4f59a-151">**SERVER\_INFO\_1542**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [<span data-ttu-id="4f59a-152">**\_Сведения о сервере \_ 1544**</span><span class="sxs-lookup"><span data-stu-id="4f59a-152">**SERVER\_INFO\_1544**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [<span data-ttu-id="4f59a-153">**\_Сведения о сервере \_ 1550**</span><span class="sxs-lookup"><span data-stu-id="4f59a-153">**SERVER\_INFO\_1550**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [<span data-ttu-id="4f59a-154">**\_Сведения о сервере \_ 1552**</span><span class="sxs-lookup"><span data-stu-id="4f59a-154">**SERVER\_INFO\_1552**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

<span data-ttu-id="4f59a-155">При программировании для Active Directory можно вызвать определенные методы интерфейса Active Directory (ADSI) для достижения тех же функций, которые можно достичь, вызвав функции сервера управления сетью.</span><span class="sxs-lookup"><span data-stu-id="4f59a-155">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management server functions.</span></span> <span data-ttu-id="4f59a-156">Дополнительные сведения см. в разделе [**иадскомпутер**](/windows/desktop/api/iads/nn-iads-iadscomputer).</span><span class="sxs-lookup"><span data-stu-id="4f59a-156">For more information, see [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).</span></span>

<span data-ttu-id="4f59a-157">Дополнительные сведения см. в статье [транспортная функция сервера и рабочей станции](server-and-workstation-transport-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4f59a-157">For more information, see the [Server and Workstation Transport Functions](server-and-workstation-transport-functions.md).</span></span>

 

 
