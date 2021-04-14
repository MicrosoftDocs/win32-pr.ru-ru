---
title: Функции распределенная файловая система
description: Ниже перечислены функции распределенная файловая система (DFS).
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496578"
---
# <a name="distributed-file-system-functions"></a><span data-ttu-id="551bd-103">Функции распределенная файловая система</span><span class="sxs-lookup"><span data-stu-id="551bd-103">Distributed File System Functions</span></span>

<span data-ttu-id="551bd-104">Ниже перечислены функции распределенная файловая система (DFS).</span><span class="sxs-lookup"><span data-stu-id="551bd-104">The following are the Distributed File System (DFS) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="551bd-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="551bd-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="551bd-106">нетдфсадд</span><span class="sxs-lookup"><span data-stu-id="551bd-106">NetDfsAdd</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
<span data-ttu-id="551bd-107">Создает новую ссылку распределенная файловая система (DFS) или добавляет целевые объекты к существующей ссылке в пространстве имен DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-107">Creates a new Distributed File System (DFS) link or adds targets to an existing link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-108">нетдфсаддфтрут</span><span class="sxs-lookup"><span data-stu-id="551bd-108">NetDfsAddFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
<span data-ttu-id="551bd-109">Создает новое пространство имен распределенная файловая система на основе домена (DFS).</span><span class="sxs-lookup"><span data-stu-id="551bd-109">Creates a new domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="551bd-110">Если пространство имен уже существует, функция добавляет в нее указанную корневую целевую папку.</span><span class="sxs-lookup"><span data-stu-id="551bd-110">If the namespace already exists, the function adds the specified root target to it.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-111">нетдфсаддруттаржет</span><span class="sxs-lookup"><span data-stu-id="551bd-111">NetDfsAddRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
<span data-ttu-id="551bd-112">Создает доменное или изолированное пространство имен DFS или добавляет новую корневую целевую папку к существующему пространству имен на основе домена.</span><span class="sxs-lookup"><span data-stu-id="551bd-112">Creates a domain-based or stand-alone DFS namespace or adds a new root target to an existing domain-based namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-113">нетдфсаддстдрут</span><span class="sxs-lookup"><span data-stu-id="551bd-113">NetDfsAddStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
<span data-ttu-id="551bd-114">Создает новое изолированное распределенная файловая системаое пространство имен (DFS).</span><span class="sxs-lookup"><span data-stu-id="551bd-114">Creates a new stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-115">нетдфсенум</span><span class="sxs-lookup"><span data-stu-id="551bd-115">NetDfsEnum</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
<span data-ttu-id="551bd-116">Перечисляет пространства имен распределенная файловая система (DFS), размещенные на сервере или в ссылках DFS пространства имен, размещенного на сервере.</span><span class="sxs-lookup"><span data-stu-id="551bd-116">Enumerates the Distributed File System (DFS) namespaces hosted on a server or DFS links of a namespace hosted by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-117">нетдфсжетклиентинфо</span><span class="sxs-lookup"><span data-stu-id="551bd-117">NetDfsGetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
<span data-ttu-id="551bd-118">Извлекает сведения о корне (DFS) или ссылке распределенная файловая система из кэша, поддерживаемого клиентом DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-118">Retrieves information about a Distributed File System (DFS) root or link from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-119">нетдфсжетфтконтаинерсекурити</span><span class="sxs-lookup"><span data-stu-id="551bd-119">NetDfsGetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="551bd-120">Возвращает дескриптор безопасности объекта контейнера для пространств имен DFS на основе домена в указанном домене Active Directory.</span><span class="sxs-lookup"><span data-stu-id="551bd-120">Retrieves the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-121">нетдфсжетинфо</span><span class="sxs-lookup"><span data-stu-id="551bd-121">NetDfsGetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
<span data-ttu-id="551bd-122">Извлекает сведения об распределенная файловая система указанном корне или ссылке DFS в пространстве имен DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-122">Retrieves information about a specified Distributed File System (DFS) root or link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-123">нетдфсжетсекурити</span><span class="sxs-lookup"><span data-stu-id="551bd-123">NetDfsGetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
<span data-ttu-id="551bd-124">Возвращает дескриптор безопасности для корневого объекта указанного пространства имен DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-124">Retrieves the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-125">нетдфсжетстдконтаинерсекурити</span><span class="sxs-lookup"><span data-stu-id="551bd-125">NetDfsGetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="551bd-126">Извлекает дескриптор безопасности для объекта-контейнера указанного изолированного пространства имен DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-126">Retrieves the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-127">нетдфсжетсуппортеднамеспацеверсион</span><span class="sxs-lookup"><span data-stu-id="551bd-127">NetDfsGetSupportedNamespaceVersion</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
<span data-ttu-id="551bd-128">Определяет поддерживаемый номер версии метаданных.</span><span class="sxs-lookup"><span data-stu-id="551bd-128">Determines the supported metadata version number.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-129">нетдфсмове</span><span class="sxs-lookup"><span data-stu-id="551bd-129">NetDfsMove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
<span data-ttu-id="551bd-130">Переименовывает или перемещает ссылку DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-130">Renames or moves a DFS link.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-131">нетдфсремове</span><span class="sxs-lookup"><span data-stu-id="551bd-131">NetDfsRemove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
<span data-ttu-id="551bd-132">Удаляет ссылку на распределенная файловая система (DFS) или определенную цель ссылки на ссылку DFS в пространстве имен DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-132">Removes a Distributed File System (DFS) link or a specific link target of a DFS link in a DFS namespace.</span></span> <span data-ttu-id="551bd-133">При удалении определенной цели ссылки сама ссылка удаляется, если удаляется последняя ссылка на ссылку.</span><span class="sxs-lookup"><span data-stu-id="551bd-133">When removing a specific link target, the link itself is removed if the last link target of the link is removed.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-134">нетдфсремовефтрут</span><span class="sxs-lookup"><span data-stu-id="551bd-134">NetDfsRemoveFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
<span data-ttu-id="551bd-135">Удаляет указанную корневую целевую папку из пространства имен распределенная файловая система на основе домена (DFS).</span><span class="sxs-lookup"><span data-stu-id="551bd-135">Removes the specified root target from a domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="551bd-136">Если удаляется последняя корневая папка пространства имен DFS, она также удаляет пространство имен DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-136">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="551bd-137">Пространство имен DFS может быть удалено без предварительного удаления всех ссылок в нем.</span><span class="sxs-lookup"><span data-stu-id="551bd-137">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-138">нетдфсремовефтрутфорцед</span><span class="sxs-lookup"><span data-stu-id="551bd-138">NetDfsRemoveFtRootForced</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
<span data-ttu-id="551bd-139">Удаляет указанную корневую целевую папку из пространства имен распределенная файловая система домена (DFS), даже если корневой целевой сервер находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="551bd-139">Removes the specified root target from a domain-based Distributed File System (DFS) namespace, even if the root target server is offline.</span></span> <span data-ttu-id="551bd-140">Если удаляется последняя корневая папка пространства имен DFS, она также удаляет пространство имен DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-140">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="551bd-141">Пространство имен DFS может быть удалено без предварительного удаления всех ссылок в нем.</span><span class="sxs-lookup"><span data-stu-id="551bd-141">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

> [!Note]
> <span data-ttu-id="551bd-142">Функция [**нетдфсремовефтрутфорцед**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) не обновляет реестр на корневом целевом сервере DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-142">The [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) function does not update the registry on the DFS root target server.</span></span> <span data-ttu-id="551bd-143">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="551bd-143">For more information, see the Remarks section.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-144">нетдфсремоверуттаржет</span><span class="sxs-lookup"><span data-stu-id="551bd-144">NetDfsRemoveRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
<span data-ttu-id="551bd-145">Удаляет корневую целевую папку DFS из пространства имен DFS на основе домена.</span><span class="sxs-lookup"><span data-stu-id="551bd-145">Removes a DFS root target from a domain-based DFS namespace.</span></span> <span data-ttu-id="551bd-146">Если корневой целевой объект является последней корневой целью в пространстве имен DFS, эта функция удаляет пространство имен DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-146">If the root target is the last root target in the DFS namespace, this function removes the DFS namespace.</span></span> <span data-ttu-id="551bd-147">Эта функция также может использоваться для удаления изолированного пространства имен DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-147">This function can also be used to remove a stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-148">нетдфсремовестдрут</span><span class="sxs-lookup"><span data-stu-id="551bd-148">NetDfsRemoveStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
<span data-ttu-id="551bd-149">Удаляет изолированное распределенная файловая системаое пространство имен (DFS).</span><span class="sxs-lookup"><span data-stu-id="551bd-149">Deletes a stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-150">нетдфссетклиентинфо</span><span class="sxs-lookup"><span data-stu-id="551bd-150">NetDfsSetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
<span data-ttu-id="551bd-151">Изменяет сведения о корне распределенная файловая система (DFS) или ссылке в кэше, поддерживаемом клиентом DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-151">Modifies information about a Distributed File System (DFS) root or link in the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-152">нетдфссетфтконтаинерсекурити</span><span class="sxs-lookup"><span data-stu-id="551bd-152">NetDfsSetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="551bd-153">Задает дескриптор безопасности объекта контейнера для пространств имен DFS на основе домена в указанном домене Active Directory.</span><span class="sxs-lookup"><span data-stu-id="551bd-153">Sets the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-154">нетдфссетинфо</span><span class="sxs-lookup"><span data-stu-id="551bd-154">NetDfsSetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
<span data-ttu-id="551bd-155">Задает или изменяет сведения о конкретном корне распределенная файловая система (DFS), корневой целевой объект, ссылке или целевом объекте ссылки.</span><span class="sxs-lookup"><span data-stu-id="551bd-155">Sets or modifies information about a specific Distributed File System (DFS) root, root target, link, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-156">нетдфссетсекурити</span><span class="sxs-lookup"><span data-stu-id="551bd-156">NetDfsSetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
<span data-ttu-id="551bd-157">Задает дескриптор безопасности для корневого объекта указанного пространства имен DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-157">Sets the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="551bd-158">нетдфссетстдконтаинерсекурити</span><span class="sxs-lookup"><span data-stu-id="551bd-158">NetDfsSetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="551bd-159">Задает дескриптор безопасности для объекта-контейнера указанного изолированного пространства имен DFS.</span><span class="sxs-lookup"><span data-stu-id="551bd-159">Sets the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> </dl>

<span data-ttu-id="551bd-160">Обратите внимание, что приложение, вызывающее какие-либо функции, может быть косвенно приводит к тому, что локальный сервер пространства имен DFS, обслуживающий вызов функции, выполняет полную синхронизацию связанных метаданных пространства имен из хозяина эмулятора PDC для этого домена.</span><span class="sxs-lookup"><span data-stu-id="551bd-160">Note that an application invoking any of the functions may indirectly cause the local DFS Namespace server servicing the function call to perform a full synchronization of the related namespace metadata from the PDC emulator master for that domain.</span></span> <span data-ttu-id="551bd-161">Такая полная синхронизация может произойти даже в том случае, если для этого пространства имен настроен корневой режим масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="551bd-161">This full synchronization could happen even when root scalability mode is configured for that namespace.</span></span>
