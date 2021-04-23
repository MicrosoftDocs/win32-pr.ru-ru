---
description: При обновлении компьютера или переносе компьютера на компьютер будут перенесены сертификаты в определенных хранилищах сертификатов.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Перенос хранилища сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31b42b83718aa1cab786ad79cc2df754b8fd9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081281"
---
# <a name="certificate-store-migration"></a><span data-ttu-id="995fe-103">Перенос хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="995fe-103">Certificate Store Migration</span></span>

<span data-ttu-id="995fe-104">При обновлении компьютера или переносе компьютера на компьютер будут перенесены сертификаты в определенных хранилищах сертификатов.</span><span class="sxs-lookup"><span data-stu-id="995fe-104">During a computer upgrade or a computer-to-computer migration, the certificates in certain certificate stores will be migrated.</span></span> <span data-ttu-id="995fe-105">В следующей таблице перечислены хранилища сертификатов, которые переносятся по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="995fe-105">The following table lists the certificate stores that are migrated by default.</span></span> <span data-ttu-id="995fe-106">Для хранилища параметров автоматического запроса сертификатов (записи контроля доступа) переносятся только [*списки доверия сертификатов*](../secgloss/c-gly.md) (CTL).</span><span class="sxs-lookup"><span data-stu-id="995fe-106">For the system Automatic Certificate Request Settings (ACRS) store, only the [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) are migrated.</span></span> <span data-ttu-id="995fe-107">Для всех остальных магазинов, перечисленных ниже, переносятся только сертификаты.</span><span class="sxs-lookup"><span data-stu-id="995fe-107">For all other stores listed below, only the certificates are migrated.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="995fe-108">Система или пользователь</span><span class="sxs-lookup"><span data-stu-id="995fe-108">System/user</span></span></th>
<th><span data-ttu-id="995fe-109">Магазин</span><span class="sxs-lookup"><span data-stu-id="995fe-109">Store</span></span></th>
<th><span data-ttu-id="995fe-110">Расположение хранения</span><span class="sxs-lookup"><span data-stu-id="995fe-110">Storage location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="995fe-111">$ {ROWSPAN8} $System $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="995fe-111">${ROWSPAN8}$System${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="995fe-112">ROOT</span><span class="sxs-lookup"><span data-stu-id="995fe-112">ROOT</span></span></td>
<td><span data-ttu-id="995fe-113"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Корневая папка</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-113"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="995fe-114">MY</span><span class="sxs-lookup"><span data-stu-id="995fe-114">MY</span></span></td>
<td><span data-ttu-id="995fe-115"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Мой</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-115"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>My</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="995fe-116">ПОЛУЧЕНИЯ</span><span class="sxs-lookup"><span data-stu-id="995fe-116">REQUEST</span></span></td>
<td><span data-ttu-id="995fe-117"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Запрос</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-117"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Request</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="995fe-118">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="995fe-118">TrustedPublisher</span></span></td>
<td><span data-ttu-id="995fe-119"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Трустедпублишер</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-119"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="995fe-120">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="995fe-120">TrustedPeople</span></span></td>
<td><span data-ttu-id="995fe-121"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>TrustedPeople</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-121"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="995fe-122">Запрещено</span><span class="sxs-lookup"><span data-stu-id="995fe-122">Disallowed</span></span></td>
<td><span data-ttu-id="995fe-123"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Запрещено</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-123"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="995fe-124">Целостности и доступности</span><span class="sxs-lookup"><span data-stu-id="995fe-124">CA</span></span></td>
<td><span data-ttu-id="995fe-125"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Центр сертификации</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-125"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="995fe-126">ЗАПИСИ контроля доступа</span><span class="sxs-lookup"><span data-stu-id="995fe-126">ACRS</span></span></td>
<td><span data-ttu-id="995fe-127"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Записи контроля доступа</strong> \ <strong>Списки CTL</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-127"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>ACRS</strong>\<strong>CTLs</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td rowspan="7"><span data-ttu-id="995fe-128">Пользователь $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="995fe-128">User${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="995fe-129">ROOT</span><span class="sxs-lookup"><span data-stu-id="995fe-129">ROOT</span></span></td>
<td><span data-ttu-id="995fe-130"><strong>HKEY_CURRENT_USER</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Корневая папка</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-130"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="995fe-131">MY</span><span class="sxs-lookup"><span data-stu-id="995fe-131">MY</span></span></td>
<td><span data-ttu-id="995fe-132">файл: \\ %аппдата%\микрософт\системцертификатес\ми\цертификатес</span><span class="sxs-lookup"><span data-stu-id="995fe-132">file:\\%APPDATA%\Microsoft\SystemCertificates\My\Certificates</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="995fe-133">ПОЛУЧЕНИЯ</span><span class="sxs-lookup"><span data-stu-id="995fe-133">REQUEST</span></span></td>
<td><span data-ttu-id="995fe-134">файл: \\ %аппдата%\микрософт\системцертификатес\рекуест\цертификатес</span><span class="sxs-lookup"><span data-stu-id="995fe-134">file:\\%APPDATA%\Microsoft\SystemCertificates\Request\Certificates</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="995fe-135">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="995fe-135">TrustedPublisher</span></span></td>
<td><span data-ttu-id="995fe-136"><strong>HKEY_CURRENT_USER</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Трустедпублишер</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-136"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="995fe-137">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="995fe-137">TrustedPeople</span></span></td>
<td><span data-ttu-id="995fe-138"><strong>HKEY_CURRENT_USER</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>TrustedPeople</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-138"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="995fe-139">Запрещено</span><span class="sxs-lookup"><span data-stu-id="995fe-139">Disallowed</span></span></td>
<td><span data-ttu-id="995fe-140"><strong>HKEY_CURRENT_USER</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Запрещено</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-140"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="995fe-141">Целостности и доступности</span><span class="sxs-lookup"><span data-stu-id="995fe-141">CA</span></span></td>
<td><span data-ttu-id="995fe-142"><strong>HKEY_CURRENT_USER</strong> \ <strong>Программное обеспечение</strong> \ <strong>Microsoft</strong> \ <strong>Системцертификатес</strong> \ <strong>Центр сертификации</strong> \ <strong>Сертификаты</strong></span><span class="sxs-lookup"><span data-stu-id="995fe-142"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="995fe-143">Другие хранилища сертификатов, созданные приложениями, не переносятся по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="995fe-143">Other certificate stores created by applications are not migrated by default.</span></span> <span data-ttu-id="995fe-144">Приложения, которые создают собственные магазины, отвечают за миграцию созданных ими магазинов.</span><span class="sxs-lookup"><span data-stu-id="995fe-144">Applications that create their own stores are responsible for migration of the stores that they create.</span></span> <span data-ttu-id="995fe-145">Для создания магазинов рекомендуется определить раздел реестра в параметрах приложения и создать хранилище в параметрах реестра с помощью поставщика **\_ хранилища сертификатов \_ Prov \_ reg** Store.</span><span class="sxs-lookup"><span data-stu-id="995fe-145">To create stores, we recommend that you define a registry key in the application settings and create a store within the registry settings by using the **CERT\_STORE\_PROV\_REG** store provider.</span></span> <span data-ttu-id="995fe-146">Дополнительные сведения о переносе параметров приложения см. в разделе *Создание пользовательского XML-файла* руководства по *использованию средства USMT 3,0* по адресу [средство миграции пользовательской среды 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span><span class="sxs-lookup"><span data-stu-id="995fe-146">For more information about migrating application settings, see the *How To Create a Custom .xml File* topic in the *Using USMT 3.0* guide at [User State Migration Tool 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span></span> <span data-ttu-id="995fe-147">(Этот ресурс может быть недоступен в некоторых языках и странах или регионах.)</span><span class="sxs-lookup"><span data-stu-id="995fe-147">(This resource may not be available in some languages and countries or regions.)</span></span>

 

 
