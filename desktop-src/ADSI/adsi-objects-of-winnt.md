---
title: Объекты ADSI в WinNT
description: Поставщик ADSI WinNT реализует следующие COM-объекты для поддержки функций и служб различных интерфейсов ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- Службы WinNT Service Provider ADSI, объекты ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d0c9e5c486d07e1e392a9f307ecd9af4509ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132814"
---
# <a name="adsi-objects-of-winnt"></a><span data-ttu-id="1b54e-104">Объекты ADSI в WinNT</span><span class="sxs-lookup"><span data-stu-id="1b54e-104">ADSI Objects of WinNT</span></span>

<span data-ttu-id="1b54e-105">Поставщик ADSI WinNT реализует следующие COM-объекты для поддержки функций и служб различных интерфейсов ADSI.</span><span class="sxs-lookup"><span data-stu-id="1b54e-105">The ADSI WinNT provider implement the following COM objects to support features and services of various ADSI interfaces.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b54e-106">Объект ADSI</span><span class="sxs-lookup"><span data-stu-id="1b54e-106">ADSI Object</span></span></th>
<th><span data-ttu-id="1b54e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1b54e-107">Description</span></span></th>
<th><span data-ttu-id="1b54e-108">Поддерживаемые интерфейсы</span><span class="sxs-lookup"><span data-stu-id="1b54e-108">Supported Interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b54e-109"><strong>Класс</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-109"><strong>Class</strong></span></span></td>
<td><span data-ttu-id="1b54e-110">Объект ADSI, представляющий определение класса.</span><span class="sxs-lookup"><span data-stu-id="1b54e-110">An ADSI object that represents a class definition.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong>иадскласс</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>IADsClass</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-112"><strong>Компьютер</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-112"><strong>Computer</strong></span></span></td>
<td><span data-ttu-id="1b54e-113">Объект ADSI, представляющий компьютер.</span><span class="sxs-lookup"><span data-stu-id="1b54e-113">An ADSI object that represents a computer.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>иадскомпутер</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>иадскомпутероператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-115"><strong>Доменная</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-115"><strong>Domain</strong></span></span></td>
<td><span data-ttu-id="1b54e-116">Объект ADSI, представляющий домен по сети.</span><span class="sxs-lookup"><span data-stu-id="1b54e-116">An ADSI object that represents a domain over the network.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>иадсдомаин</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-118"><strong>FileService</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-118"><strong>FileService</strong></span></span></td>
<td><span data-ttu-id="1b54e-119">Объект ADSI, представляющий файловую службу.</span><span class="sxs-lookup"><span data-stu-id="1b54e-119">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>иадсфилесервице</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>иадсфилесервицеоператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-121"><strong>FileShare</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-121"><strong>FileShare</strong></span></span></td>
<td><span data-ttu-id="1b54e-122">Объект ADSI, представляющий общую папку.</span><span class="sxs-lookup"><span data-stu-id="1b54e-122">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>иадсфилешаре</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-124"><strong>фпнвфилесервице</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-124"><strong>FPNWFileService</strong></span></span></td>
<td><span data-ttu-id="1b54e-125">Объект ADSI, представляющий файловую службу.</span><span class="sxs-lookup"><span data-stu-id="1b54e-125">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>иадсфилесервице</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>иадсфилесервицеоператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-127"><strong>фпнвфилешаре</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-127"><strong>FPNWFileShare</strong></span></span></td>
<td><span data-ttu-id="1b54e-128">Объект ADSI, представляющий общую папку.</span><span class="sxs-lookup"><span data-stu-id="1b54e-128">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>иадсфилешаре</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-130"><strong>фпнвресаурце</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-130"><strong>FPNWResource</strong></span></span></td>
<td><span data-ttu-id="1b54e-131">Объект ADSI, представляющий ресурс.</span><span class="sxs-lookup"><span data-stu-id="1b54e-131">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>иадсресаурце</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-133"><strong>фпнвресаурцесколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-133"><strong>FPNWResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="1b54e-134">Объект ADSI, представляющий коллекцию ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b54e-134">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="1b54e-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b54e-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-136"><strong>фпнвсессион</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-136"><strong>FPNWSession</strong></span></span></td>
<td><span data-ttu-id="1b54e-137">Объект ADSI, представляющий сеанс.</span><span class="sxs-lookup"><span data-stu-id="1b54e-137">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>иадссессион</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-139"><strong>фпнвсессионсколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-139"><strong>FPNWSessionsCollection</strong></span></span></td>
<td><span data-ttu-id="1b54e-140">Объект ADSI, представляющий коллекцию сеансов.</span><span class="sxs-lookup"><span data-stu-id="1b54e-140">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="1b54e-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b54e-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-142"><strong>Группа</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-142"><strong>Group</strong></span></span></td>
<td><span data-ttu-id="1b54e-143">Объект ADSI, представляющий группу.</span><span class="sxs-lookup"><span data-stu-id="1b54e-143">An ADSI object that represents a group.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>иадсграуп</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl>
<blockquote>
[!Note]<br />
<span data-ttu-id="1b54e-145">Параметр-info не может использоваться для групп, содержащих члены, которые являются wellKnown субъектами безопасности в области WinNT.</span><span class="sxs-lookup"><span data-stu-id="1b54e-145">GetInfo cannot be used for groups that contain members that are wellKnown security principals in the WinNT scope.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-146"><strong>GroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-146"><strong>GroupCollection</strong></span></span></td>
<td><span data-ttu-id="1b54e-147">Объект ADSI, представляющий коллекцию групп.</span><span class="sxs-lookup"><span data-stu-id="1b54e-147">An ADSI object that represents a collection of groups.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>иадсмемберс</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-149"><strong>Локальная группа</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-149"><strong>LocalGroup</strong></span></span></td>
<td><span data-ttu-id="1b54e-150">Объект ADSI, представляющий локальную группу.</span><span class="sxs-lookup"><span data-stu-id="1b54e-150">An ADSI object that represents a local group.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>иадсграуп</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-152"><strong>локалграупколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-152"><strong>LocalgroupCollection</strong></span></span></td>
<td><span data-ttu-id="1b54e-153">Объект ADSI, представляющий коллекцию локальных групп.</span><span class="sxs-lookup"><span data-stu-id="1b54e-153">An ADSI object that represents a collection of local groups.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>иадсмемберс</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-155"><strong>Пространство имен</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-155"><strong>Namespace</strong></span></span></td>
<td><span data-ttu-id="1b54e-156">Объект ADSI, представляющий пространство имен WinNT.</span><span class="sxs-lookup"><span data-stu-id="1b54e-156">An ADSI object that represents the WinNT namespace.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>иадсконтаинер</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>иадсопендсобжект</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-158"><strong>PrintJob</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-158"><strong>PrintJob</strong></span></span></td>
<td><span data-ttu-id="1b54e-159">Объект ADSI, представляющий задание печати.</span><span class="sxs-lookup"><span data-stu-id="1b54e-159">An ADSI object that represents a print job.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>иадспринтжоб</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>иадспринтжобоператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-161"><strong>принтжобсколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-161"><strong>PrintJobsCollection</strong></span></span></td>
<td><span data-ttu-id="1b54e-162">Объект ADSI, представляющий коллекцию заданий печати.</span><span class="sxs-lookup"><span data-stu-id="1b54e-162">An ADSI object that represents a collection of print jobs.</span></span></td>
<td><span data-ttu-id="1b54e-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b54e-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-164"><strong>PrintQueue</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-164"><strong>PrintQueue</strong></span></span></td>
<td><span data-ttu-id="1b54e-165">Объект ADSI, представляющий очередь печати.</span><span class="sxs-lookup"><span data-stu-id="1b54e-165">An ADSI object that represents a print queue.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>иадспринткуеуе</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>иадспринткуеуеоператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-167"><strong>Свойство</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-167"><strong>Property</strong></span></span></td>
<td><span data-ttu-id="1b54e-168">Объект ADSI, представляющий определение атрибута.</span><span class="sxs-lookup"><span data-stu-id="1b54e-168">An ADSI object that represents an attribute definition.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>иадспроперти</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>IADsProperty</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-170"><strong>Ресурс</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-170"><strong>Resource</strong></span></span></td>
<td><span data-ttu-id="1b54e-171">Объект ADSI, представляющий ресурс.</span><span class="sxs-lookup"><span data-stu-id="1b54e-171">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>иадсресаурце</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-173"><strong>ресаурцесколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-173"><strong>ResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="1b54e-174">Объект ADSI, представляющий коллекцию ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b54e-174">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="1b54e-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b54e-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-176"><strong>Схема</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-176"><strong>Schema</strong></span></span></td>
<td><span data-ttu-id="1b54e-177">Объект ADSI, представляющий контейнер схемы.</span><span class="sxs-lookup"><span data-stu-id="1b54e-177">An ADSI object that represents the schema container.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>иадсконтаинер</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-179"><strong>Служба</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-179"><strong>Service</strong></span></span></td>
<td><span data-ttu-id="1b54e-180">Объект ADSI, представляющий службу.</span><span class="sxs-lookup"><span data-stu-id="1b54e-180">An ADSI object that represents a service.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>иадссервице</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>иадссервицеоператионс</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-182"><strong>Session</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-182"><strong>Session</strong></span></span></td>
<td><span data-ttu-id="1b54e-183">Объект ADSI, представляющий сеанс.</span><span class="sxs-lookup"><span data-stu-id="1b54e-183">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>иадссессион</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-185"><strong>сессионсколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-185"><strong>SessionsCollection</strong></span></span></td>
<td><span data-ttu-id="1b54e-186">Объект ADSI, представляющий коллекцию сеансов.</span><span class="sxs-lookup"><span data-stu-id="1b54e-186">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="1b54e-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>иадсколлектион</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b54e-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-188"><strong>Синтаксис</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-188"><strong>Syntax</strong></span></span></td>
<td><span data-ttu-id="1b54e-189">Объект ADSI, представляющий синтаксис атрибута.</span><span class="sxs-lookup"><span data-stu-id="1b54e-189">An ADSI object that represents the syntax of an attribute.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>иадссинтакс</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>IADsSyntax</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b54e-191"><strong>Пользователь</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-191"><strong>User</strong></span></span></td>
<td><span data-ttu-id="1b54e-192">Объект ADSI, представляющий учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="1b54e-192">An ADSI object that represents a user account.</span></span></td>
<td><dl> <span data-ttu-id="1b54e-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IAds</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>иадспропертилист</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="1b54e-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b54e-194"><strong>усерграупколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="1b54e-194"><strong>UserGroupCollection</strong></span></span></td>
<td><span data-ttu-id="1b54e-195">Объект ADSI, представляющий коллекцию групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="1b54e-195">An ADSI object that represents a collection of user groups.</span></span></td>
<td><span data-ttu-id="1b54e-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>иадсмемберс</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b54e-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





