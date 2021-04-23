---
description: Сетевые общие функции управляют общими ресурсами. Общий ресурс — это локальный ресурс на сервере (например, каталог на диске, устройство печати или именованный канал), к которому могут обращаться пользователи и приложения в сети.
ms.assetid: 14886bb0-e597-4728-a64f-bc16e82874da
title: Функции сетевой папки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640dc877c9b482cb8ebdcef0d36e6dff562fcd8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683270"
---
# <a name="network-share-functions"></a><span data-ttu-id="7c5ee-104">Функции сетевой папки</span><span class="sxs-lookup"><span data-stu-id="7c5ee-104">Network Share Functions</span></span>

<span data-ttu-id="7c5ee-105">Сетевые общие функции управляют общими ресурсами.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-105">The network share functions control shared resources.</span></span> <span data-ttu-id="7c5ee-106">Общий ресурс — это локальный ресурс на сервере (например, каталог на диске, устройство печати или именованный канал), к которому могут обращаться пользователи и приложения в сети.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-106">A shared resource is a local resource on a server (for example, a disk directory, print device, or named pipe) that can be accessed by users and applications on the network.</span></span>

<span data-ttu-id="7c5ee-107">Функции общего доступа перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-107">The share functions are listed following.</span></span>



| <span data-ttu-id="7c5ee-108">Функция</span><span class="sxs-lookup"><span data-stu-id="7c5ee-108">Function</span></span>                                   | <span data-ttu-id="7c5ee-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7c5ee-109">Description</span></span>                                                          |
|--------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="7c5ee-110">**нетшареадд**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-110">**NetShareAdd**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)         | <span data-ttu-id="7c5ee-111">Предоставляет общий доступ к ресурсу на сервере.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-111">Shares a resource on a server.</span></span>                                       |
| [<span data-ttu-id="7c5ee-112">**нетшаречекк**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-112">**NetShareCheck**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharecheck)     | <span data-ttu-id="7c5ee-113">Запрашивает, является ли сервер общим для устройства.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-113">Queries whether a server is sharing a device.</span></span>                        |
| [<span data-ttu-id="7c5ee-114">**нетшаредел**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-114">**NetShareDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharedel)         | <span data-ttu-id="7c5ee-115">Удаляет имя общего ресурса из списка общих ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-115">Deletes a share name from a server's list of shared resources.</span></span>       |
| [<span data-ttu-id="7c5ee-116">**нетшаринум**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-116">**NetShareEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareenum)       | <span data-ttu-id="7c5ee-117">Возвращает общие сведения о каждом общем ресурсе на сервере.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-117">Retrieves share information about each shared resource on a server.</span></span>  |
| [<span data-ttu-id="7c5ee-118">**нетшарежетинфо**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-118">**NetShareGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharegetinfo) | <span data-ttu-id="7c5ee-119">Извлекает сведения об указанном общем ресурсе на сервере.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-119">Retrieves information about a specified shared resource on a server.</span></span> |
| [<span data-ttu-id="7c5ee-120">**нетшаресетинфо**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-120">**NetShareSetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) | <span data-ttu-id="7c5ee-121">Задает параметры общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-121">Sets a shared resource's parameters.</span></span>                                 |



 

<span data-ttu-id="7c5ee-122">Функция [**нетшареадд**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) позволяет пользователю или приложению совместно использовать ресурс определенного типа, используя указанное имя общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-122">The [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) function allows a user or application to share a resource of a specific type using the specified share name.</span></span> <span data-ttu-id="7c5ee-123">Для предоставления общего доступа к ресурсу функции **нетшареадд** требуется имя общего ресурса и имя локального устройства.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-123">The **NetShareAdd** function requires the share name and local device name to share the resource.</span></span> <span data-ttu-id="7c5ee-124">Для доступа к ресурсу пользователю или приложению должна быть назначена учетная запись на сервере.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-124">A user or application must have an account on the server to access the resource.</span></span>

<span data-ttu-id="7c5ee-125">Можно также указать дескриптор безопасности, который будет связан с общим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-125">You can also specify a security descriptor to be associated with a share.</span></span> <span data-ttu-id="7c5ee-126">Дескрипторы безопасности определяют, каким пользователям разрешен доступ к файлам через общую папку, а также к какому типу доступа.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-126">Security descriptors specify which users are allowed to access files through the share, and with what type of access.</span></span> <span data-ttu-id="7c5ee-127">При вызове [**нетшареадд**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) или [**Нетшаресетинфо**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo)укажите [**\_ дескриптор безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) со сведениями об [**общей информации \_ \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) .</span><span class="sxs-lookup"><span data-stu-id="7c5ee-127">Specify a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) with the [**SHARE\_INFO\_502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) information level when calling [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) or [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo).</span></span> <span data-ttu-id="7c5ee-128">**Нетшаресетинфо** поддерживает информационный [**уровень \_ \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) .</span><span class="sxs-lookup"><span data-stu-id="7c5ee-128">**NetShareSetInfo** supports the [**SHARE\_INFO\_1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) information level.</span></span> <span data-ttu-id="7c5ee-129">Дополнительные сведения о дескрипторах безопасности см. в разделе [Управление доступом](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="7c5ee-129">For more information about security descriptors, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="7c5ee-130">Функции управления сетью используют следующие специальные имена общих ресурсов для межпроцессного взаимодействия (IPC) и удаленного администрирования сервера.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-130">The network management functions use the following special share names for interprocess communication (IPC) and remote administration of the server:</span></span>

-   <span data-ttu-id="7c5ee-131">IPC $, зарезервировано для межпроцессного взаимодействия</span><span class="sxs-lookup"><span data-stu-id="7c5ee-131">IPC$, reserved for interprocess communication</span></span>
-   <span data-ttu-id="7c5ee-132">Администратор $, зарезервированный для удаленного администрирования</span><span class="sxs-lookup"><span data-stu-id="7c5ee-132">ADMIN$, reserved for remote administration</span></span>
-   <span data-ttu-id="7c5ee-133">A $, B $, C $ (и другие имена локальных дисков, за которыми следует знак доллара), назначенный для локальных дисковых устройств</span><span class="sxs-lookup"><span data-stu-id="7c5ee-133">A$, B$, C$ (and other local disk names followed by a dollar sign), assigned to local disk devices</span></span>

<span data-ttu-id="7c5ee-134">Чтобы получить список всех подключений к общему ресурсу на сервере или получить список всех соединений, установленных с определенного компьютера, вызовите функцию [**нетконнектионенум**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) .</span><span class="sxs-lookup"><span data-stu-id="7c5ee-134">To list all connections made to a shared resource on a server, or to list all connections established from a particular computer, call the [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) function.</span></span> <span data-ttu-id="7c5ee-135">Вы можете вызвать **нетконнектионенум** в сведениях о [**соединении \_ \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) и на уровнях информации о [**подключении \_ \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) .</span><span class="sxs-lookup"><span data-stu-id="7c5ee-135">You can call **NetConnectionEnum** at the [**CONNECTION\_INFO\_0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) and [**CONNECTION\_INFO\_1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) information levels.</span></span>

<span data-ttu-id="7c5ee-136">Функции общего доступа доступны на следующих уровнях информации:</span><span class="sxs-lookup"><span data-stu-id="7c5ee-136">Share functions are available at the following information levels:</span></span>

<dl>

[<span data-ttu-id="7c5ee-137">**ПОДЕЛИТЬСЯ \_ информацией \_ 0**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-137">**SHARE\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_0)  
[<span data-ttu-id="7c5ee-138">**Общие \_ сведения \_ 1**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-138">**SHARE\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1)  
[<span data-ttu-id="7c5ee-139">**Общие \_ сведения \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-139">**SHARE\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_2)  
[<span data-ttu-id="7c5ee-140">**Общие \_ сведения \_ 501**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-140">**SHARE\_INFO\_501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_501)  
[<span data-ttu-id="7c5ee-141">**Общие \_ сведения \_ 502**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-141">**SHARE\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)  
[<span data-ttu-id="7c5ee-142">**Общие \_ сведения \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-142">**SHARE\_INFO\_1005**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1005)  
</dl>

<span data-ttu-id="7c5ee-143">Следующие уровни информации допустимы только для [**нетшаресетинфо**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):</span><span class="sxs-lookup"><span data-stu-id="7c5ee-143">The following information levels are valid only for [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):</span></span>

<dl>

[<span data-ttu-id="7c5ee-144">**Общие \_ сведения \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-144">**SHARE\_INFO\_1004**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1004)  
[<span data-ttu-id="7c5ee-145">**Общие \_ сведения \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-145">**SHARE\_INFO\_1006**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1006)  
[<span data-ttu-id="7c5ee-146">**Общие \_ сведения \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="7c5ee-146">**SHARE\_INFO\_1501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501)  
</dl>

<span data-ttu-id="7c5ee-147">При программировании для Active Directory можно вызвать определенные методы интерфейса Active Directory (ADSI) для достижения тех же функций, которые можно достичь, вызвав функции общего доступа к управлению сетью.</span><span class="sxs-lookup"><span data-stu-id="7c5ee-147">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions.</span></span> <span data-ttu-id="7c5ee-148">Дополнительные сведения см. в разделе [**иадсфилешаре**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span><span class="sxs-lookup"><span data-stu-id="7c5ee-148">For more information, see [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span></span>

 

 
