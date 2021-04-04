---
description: Системное хранилище — это коллекция, состоящая из одного или нескольких физических хранилищ на одном уровне.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Расположения системных хранилищ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998627"
---
# <a name="system-store-locations"></a><span data-ttu-id="91beb-103">Расположения системных хранилищ</span><span class="sxs-lookup"><span data-stu-id="91beb-103">System Store Locations</span></span>

<span data-ttu-id="91beb-104">Системное хранилище — это коллекция, состоящая из одного или нескольких физических хранилищ на одном уровне.</span><span class="sxs-lookup"><span data-stu-id="91beb-104">A system store is a collection that consists of one or more physical sibling stores.</span></span> <span data-ttu-id="91beb-105">Для каждого системного хранилища существуют стандартные физические хранилища на уровне элементов.</span><span class="sxs-lookup"><span data-stu-id="91beb-105">For each system store, there are predefined physical sibling stores.</span></span> <span data-ttu-id="91beb-106">После открытия системного хранилища, например MY в \_ системном \_ хранилище сертификатов \_ текущий \_ пользователь, поставщик услуг магазина вызывает [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) , чтобы открыть каждое из физических хранилищ в коллекции системных хранилищ.</span><span class="sxs-lookup"><span data-stu-id="91beb-106">After opening a system store such as MY at CERT\_SYSTEM\_STORE\_CURRENT\_USER, the store provider calls [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open each of the physical stores in the system store collection.</span></span> <span data-ttu-id="91beb-107">В открытом процессе каждое из этих физических хранилищ добавляется в коллекцию системного хранилища с помощью [**цертаддсторетоколлектион**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span><span class="sxs-lookup"><span data-stu-id="91beb-107">In the open process, each of these physical stores is added to the system store collection using [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span></span> <span data-ttu-id="91beb-108">Все сертификаты в этих физических хранилищах доступны через коллекцию логических хранилищ систем.</span><span class="sxs-lookup"><span data-stu-id="91beb-108">All certificates in those physical stores are available through the logical system store collection.</span></span>

<span data-ttu-id="91beb-109">Для каждого расположения системного хранилища предопределены следующие стандартные хранилища систем:</span><span class="sxs-lookup"><span data-stu-id="91beb-109">For each system store location, the predefined systems stores are:</span></span>

-   <span data-ttu-id="91beb-110">MY</span><span class="sxs-lookup"><span data-stu-id="91beb-110">MY</span></span>
-   <span data-ttu-id="91beb-111">Root</span><span class="sxs-lookup"><span data-stu-id="91beb-111">Root</span></span>
-   <span data-ttu-id="91beb-112">Доверие</span><span class="sxs-lookup"><span data-stu-id="91beb-112">Trust</span></span>
-   <span data-ttu-id="91beb-113">Целостности и доступности</span><span class="sxs-lookup"><span data-stu-id="91beb-113">CA</span></span>

<span data-ttu-id="91beb-114">В \_ системном \_ хранилище CERT \_ текущий \_ пользователь также имеется предопределенное хранилище усердс.</span><span class="sxs-lookup"><span data-stu-id="91beb-114">In CERT\_SYSTEM\_STORE\_CURRENT\_USER, there is also a predefined UserDS store.</span></span> <span data-ttu-id="91beb-115">Для этого расположения планируется хранилище смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="91beb-115">A smart card store is planned for this location.</span></span>

<span data-ttu-id="91beb-116">Ниже приведены системные хранилища, за которыми следуют дополнительные замечания.</span><span class="sxs-lookup"><span data-stu-id="91beb-116">Here are the system stores followed by further remarks:</span></span>

-   [<span data-ttu-id="91beb-117">\_ \_ \_ текущий \_ пользователь хранилища системы сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-117">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>](#cert_system_store_current_user)
-   [<span data-ttu-id="91beb-118">\_ \_ \_ локальный \_ компьютер хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-118">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>](#cert_system_store_local_machine)
-   [<span data-ttu-id="91beb-119">\_ \_ \_ Текущая \_ Служба хранилища сертификатов системы</span><span class="sxs-lookup"><span data-stu-id="91beb-119">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>](#cert_system_store_current_service)
-   [<span data-ttu-id="91beb-120">\_ \_ службы хранилища систем \_ сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-120">CERT\_SYSTEM\_STORE\_SERVICES</span></span>](#cert_system_store_services)
-   [<span data-ttu-id="91beb-121">\_Пользователи системного \_ хранилища \_ сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-121">CERT\_SYSTEM\_STORE\_USERS</span></span>](#cert_system_store_users)
-   [<span data-ttu-id="91beb-122">\_ \_ \_ \_ Групповая политика текущего пользователя системы CERT \_</span><span class="sxs-lookup"><span data-stu-id="91beb-122">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>](#cert_system_current_user_group_policy)
-   [<span data-ttu-id="91beb-123">\_системная \_ \_ Политика ЛОКАЛЬНОГО \_ компьютера \_ с сертификатом</span><span class="sxs-lookup"><span data-stu-id="91beb-123">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>](#cert_system_local_machine_group_policy)
-   [<span data-ttu-id="91beb-124">\_ \_ \_ Локальная машина хранилища \_ сертификатов \_ предприятия</span><span class="sxs-lookup"><span data-stu-id="91beb-124">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>](#cert_system_store_local_machine_enterprise)
-   [<span data-ttu-id="91beb-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="91beb-125">Remarks</span></span>](#remarks)

### <a name="cert_system_store_current_user"></a><span data-ttu-id="91beb-126">\_ \_ \_ текущий \_ пользователь хранилища системы сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-126">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>

<span data-ttu-id="91beb-127">\_Хранилище системы \_ сертификатов \_ текущие \_ пользовательские хранилища систем находятся в следующем расположении реестра:</span><span class="sxs-lookup"><span data-stu-id="91beb-127">CERT\_SYSTEM\_STORE\_CURRENT\_USER system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="91beb-128">Ниже приведены стандартные физические хранилища, связанные с этими системными хранилищами.</span><span class="sxs-lookup"><span data-stu-id="91beb-128">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="91beb-129">Системное хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-129">System store</span></span> | <span data-ttu-id="91beb-130">Физическое хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-130">Physical store</span></span>                                           |
|--------------|----------------------------------------------------------|
| <span data-ttu-id="91beb-131">MY</span><span class="sxs-lookup"><span data-stu-id="91beb-131">MY</span></span>           | <span data-ttu-id="91beb-132">. Параметры</span><span class="sxs-lookup"><span data-stu-id="91beb-132">.Default</span></span>                                                 |
| <span data-ttu-id="91beb-133">Root</span><span class="sxs-lookup"><span data-stu-id="91beb-133">Root</span></span>         | <span data-ttu-id="91beb-134">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-134">.Default.LocalMachine</span></span><br/> <span data-ttu-id="91beb-135">. Карте</span><span class="sxs-lookup"><span data-stu-id="91beb-135">.SmartCard</span></span><br/>   |
| <span data-ttu-id="91beb-136">Доверие</span><span class="sxs-lookup"><span data-stu-id="91beb-136">Trust</span></span>        | <span data-ttu-id="91beb-137">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="91beb-137">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="91beb-138">. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-138">.LocalMachine</span></span><br/> |
| <span data-ttu-id="91beb-139">Целостности и доступности</span><span class="sxs-lookup"><span data-stu-id="91beb-139">CA</span></span>           | <span data-ttu-id="91beb-140">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="91beb-140">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="91beb-141">. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-141">.LocalMachine</span></span><br/> |
| <span data-ttu-id="91beb-142">усердс</span><span class="sxs-lookup"><span data-stu-id="91beb-142">UserDS</span></span>       | <span data-ttu-id="91beb-143">. UserCertificate</span><span class="sxs-lookup"><span data-stu-id="91beb-143">.UserCertificate</span></span>                                         |



 

### <a name="cert_system_store_local_machine"></a><span data-ttu-id="91beb-144">\_ \_ \_ локальный \_ компьютер хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-144">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>

<span data-ttu-id="91beb-145">Хранилища \_ системы \_ сертификатов \_ локального \_ компьютера хранятся в следующем расположении реестра:</span><span class="sxs-lookup"><span data-stu-id="91beb-145">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="91beb-146">Стандартные физические хранилища связаны с этими системными хранилищами следующим образом.</span><span class="sxs-lookup"><span data-stu-id="91beb-146">The predefined physical stores are associated with those system stores are as follows.</span></span>



| <span data-ttu-id="91beb-147">Системное хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-147">System store</span></span> | <span data-ttu-id="91beb-148">Физическое хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-148">Physical store</span></span>                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91beb-149">MY</span><span class="sxs-lookup"><span data-stu-id="91beb-149">MY</span></span>           | <span data-ttu-id="91beb-150">. Параметры</span><span class="sxs-lookup"><span data-stu-id="91beb-150">.Default</span></span>                                                                                          |
| <span data-ttu-id="91beb-151">Root</span><span class="sxs-lookup"><span data-stu-id="91beb-151">Root</span></span>         | <span data-ttu-id="91beb-152">. Default. Аусрут</span><span class="sxs-lookup"><span data-stu-id="91beb-152">.Default.AuthRoot</span></span><br/> <span data-ttu-id="91beb-153">. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="91beb-153">.GroupPolicy</span></span><br/> <span data-ttu-id="91beb-154">. Компании</span><span class="sxs-lookup"><span data-stu-id="91beb-154">.Enterprise</span></span><br/> <span data-ttu-id="91beb-155">. Карте</span><span class="sxs-lookup"><span data-stu-id="91beb-155">.SmartCard</span></span><br/> |
| <span data-ttu-id="91beb-156">Доверие</span><span class="sxs-lookup"><span data-stu-id="91beb-156">Trust</span></span>        | <span data-ttu-id="91beb-157">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="91beb-157">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="91beb-158">. Компании</span><span class="sxs-lookup"><span data-stu-id="91beb-158">.Enterprise</span></span><br/>                                            |
| <span data-ttu-id="91beb-159">Целостности и доступности</span><span class="sxs-lookup"><span data-stu-id="91beb-159">CA</span></span>           | <span data-ttu-id="91beb-160">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="91beb-160">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="91beb-161">. Компании</span><span class="sxs-lookup"><span data-stu-id="91beb-161">.Enterprise</span></span> <br/>                                           |



 

### <a name="cert_system_store_current_service"></a><span data-ttu-id="91beb-162">\_ \_ \_ Текущая \_ Служба хранилища сертификатов системы</span><span class="sxs-lookup"><span data-stu-id="91beb-162">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>

<span data-ttu-id="91beb-163">\_Хранилище системы \_ сертификатов \_ \_ . текущие хранилища системных систем службы находятся в следующем расположении реестра:</span><span class="sxs-lookup"><span data-stu-id="91beb-163">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="91beb-164">Ниже приведены стандартные физические хранилища, связанные с этими системными хранилищами.</span><span class="sxs-lookup"><span data-stu-id="91beb-164">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="91beb-165">Системное хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-165">System store</span></span> | <span data-ttu-id="91beb-166">Физическое хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-166">Physical store</span></span>                   |
|--------------|----------------------------------|
| <span data-ttu-id="91beb-167">MY</span><span class="sxs-lookup"><span data-stu-id="91beb-167">MY</span></span>           | <span data-ttu-id="91beb-168">. Параметры</span><span class="sxs-lookup"><span data-stu-id="91beb-168">.Default</span></span>                         |
| <span data-ttu-id="91beb-169">Root</span><span class="sxs-lookup"><span data-stu-id="91beb-169">Root</span></span>         | <span data-ttu-id="91beb-170">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-170">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="91beb-171">Доверие</span><span class="sxs-lookup"><span data-stu-id="91beb-171">Trust</span></span>        | <span data-ttu-id="91beb-172">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-172">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="91beb-173">Целостности и доступности</span><span class="sxs-lookup"><span data-stu-id="91beb-173">CA</span></span>           | <span data-ttu-id="91beb-174">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-174">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_services"></a><span data-ttu-id="91beb-175">\_ \_ службы хранилища систем \_ сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-175">CERT\_SYSTEM\_STORE\_SERVICES</span></span>

<span data-ttu-id="91beb-176">Системные \_ хранилища служб сертификатов системы сертификации \_ \_ находятся в следующем расположении реестра:</span><span class="sxs-lookup"><span data-stu-id="91beb-176">CERT\_SYSTEM\_STORE\_SERVICES system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="91beb-177">Ниже приведены стандартные физические хранилища, связанные с этими системными хранилищами.</span><span class="sxs-lookup"><span data-stu-id="91beb-177">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="91beb-178">Системное хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-178">System store</span></span>       | <span data-ttu-id="91beb-179">Физическое хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-179">Physical store</span></span>                   |
|--------------------|----------------------------------|
| <span data-ttu-id="91beb-180">ServiceName \\ My</span><span class="sxs-lookup"><span data-stu-id="91beb-180">ServiceName\\MY</span></span>    | <span data-ttu-id="91beb-181">. Параметры</span><span class="sxs-lookup"><span data-stu-id="91beb-181">.Default</span></span>                         |
| <span data-ttu-id="91beb-182">\\Корневой каталог ServiceName</span><span class="sxs-lookup"><span data-stu-id="91beb-182">ServiceName\\Root</span></span>  | <span data-ttu-id="91beb-183">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-183">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="91beb-184">\\Доверие ServiceName</span><span class="sxs-lookup"><span data-stu-id="91beb-184">ServiceName\\Trust</span></span> | <span data-ttu-id="91beb-185">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-185">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="91beb-186">\\Центр сертификации ServiceName</span><span class="sxs-lookup"><span data-stu-id="91beb-186">ServiceName\\CA</span></span>    | <span data-ttu-id="91beb-187">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-187">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_users"></a><span data-ttu-id="91beb-188">\_Пользователи системного \_ хранилища \_ сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-188">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="91beb-189">\_Хранилище системы \_ сертификатов \_ Пользователи системы хранятся в следующем расположении реестра:</span><span class="sxs-lookup"><span data-stu-id="91beb-189">CERT\_SYSTEM\_STORE\_USERS system stores are at the following registry location:</span></span>

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

<span data-ttu-id="91beb-190">Ниже приведены стандартные физические хранилища, связанные с этими системными хранилищами.</span><span class="sxs-lookup"><span data-stu-id="91beb-190">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="91beb-191">Системное хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-191">System store</span></span>  | <span data-ttu-id="91beb-192">Физическое хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-192">Physical store</span></span>                   |
|---------------|----------------------------------|
| <span data-ttu-id="91beb-193">UserID \\ My</span><span class="sxs-lookup"><span data-stu-id="91beb-193">userid\\MY</span></span>    | <span data-ttu-id="91beb-194">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-194">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="91beb-195">\\корневой UserID</span><span class="sxs-lookup"><span data-stu-id="91beb-195">userid\\Root</span></span>  | <span data-ttu-id="91beb-196">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-196">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="91beb-197">\\доверие UserID</span><span class="sxs-lookup"><span data-stu-id="91beb-197">userid\\Trust</span></span> | <span data-ttu-id="91beb-198">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-198">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="91beb-199">\\ЦС UserID</span><span class="sxs-lookup"><span data-stu-id="91beb-199">userid\\CA</span></span>    | <span data-ttu-id="91beb-200">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="91beb-200">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_current_user_group_policy"></a><span data-ttu-id="91beb-201">\_ \_ \_ \_ Групповая политика текущего пользователя системы CERT \_</span><span class="sxs-lookup"><span data-stu-id="91beb-201">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>

<span data-ttu-id="91beb-202">\_Системные \_ \_ хранилища групповой политики системных политик текущего пользователя системы CERT \_ \_ находятся в следующем расположении реестра:</span><span class="sxs-lookup"><span data-stu-id="91beb-202">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a><span data-ttu-id="91beb-203">\_системная \_ \_ Политика ЛОКАЛЬНОГО \_ компьютера \_ с сертификатом</span><span class="sxs-lookup"><span data-stu-id="91beb-203">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>

<span data-ttu-id="91beb-204">Системные \_ \_ \_ \_ хранилища групповой политики локального компьютера с сертификатами \_ находятся в следующем расположении реестра:</span><span class="sxs-lookup"><span data-stu-id="91beb-204">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a><span data-ttu-id="91beb-205">\_ \_ \_ Локальная машина хранилища \_ сертификатов \_ предприятия</span><span class="sxs-lookup"><span data-stu-id="91beb-205">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>

<span data-ttu-id="91beb-206">\_ \_ \_ Локальная машина хранилища \_ сертификатов \_ на локальном компьютере содержит сертификаты, которые совместно используются в доменах предприятия и скачаны из глобального корпоративного каталога.</span><span class="sxs-lookup"><span data-stu-id="91beb-206">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE contains certificates shared across domains in the enterprise and downloaded from the global enterprise directory.</span></span> <span data-ttu-id="91beb-207">Чтобы синхронизировать корпоративное хранилище клиента, Каталог предприятия опрашивается каждые восемь часов, а сертификаты автоматически загружаются в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="91beb-207">To synchronize the client's enterprise store, the enterprise directory is polled every eight hours and certificates are downloaded automatically in the background.</span></span>

<span data-ttu-id="91beb-208">Ниже приведены стандартные физические хранилища, связанные с этими системными хранилищами.</span><span class="sxs-lookup"><span data-stu-id="91beb-208">The predefined physical stores associated with these system stores are as follows.</span></span>



| <span data-ttu-id="91beb-209">Системное хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-209">System store</span></span> | <span data-ttu-id="91beb-210">Физическое хранилище</span><span class="sxs-lookup"><span data-stu-id="91beb-210">Physical store</span></span> |
|--------------|----------------|
| <span data-ttu-id="91beb-211">MY</span><span class="sxs-lookup"><span data-stu-id="91beb-211">MY</span></span>           | <span data-ttu-id="91beb-212">. Параметры</span><span class="sxs-lookup"><span data-stu-id="91beb-212">.Default</span></span>       |
| <span data-ttu-id="91beb-213">Root</span><span class="sxs-lookup"><span data-stu-id="91beb-213">Root</span></span>         | <span data-ttu-id="91beb-214">. Параметры</span><span class="sxs-lookup"><span data-stu-id="91beb-214">.Default</span></span>       |
| <span data-ttu-id="91beb-215">Доверие</span><span class="sxs-lookup"><span data-stu-id="91beb-215">Trust</span></span>        | <span data-ttu-id="91beb-216">. Параметры</span><span class="sxs-lookup"><span data-stu-id="91beb-216">.Default</span></span>       |
| <span data-ttu-id="91beb-217">Целостности и доступности</span><span class="sxs-lookup"><span data-stu-id="91beb-217">CA</span></span>           | <span data-ttu-id="91beb-218">. Параметры</span><span class="sxs-lookup"><span data-stu-id="91beb-218">.Default</span></span>       |



 

### <a name="remarks"></a><span data-ttu-id="91beb-219">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91beb-219">Remarks</span></span>

<span data-ttu-id="91beb-220">Дополнительные физические хранилища могут быть связаны с системным хранилищем с помощью [**цертрегистерфисикалсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span><span class="sxs-lookup"><span data-stu-id="91beb-220">Additional physical stores can be associated with a system store by using [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span></span>

<span data-ttu-id="91beb-221">\_Хранилища системы \_ сертификатов \_ и хранилища \_ \_ пользователей в хранилище системы сертификатов \_ открываются путем добавления имени хранилища в строку, переданную в *пвпара* с помощью службы или имени пользователя, например *ServiceName* \\ **Trust** или **. По умолчанию** \\ **My**.</span><span class="sxs-lookup"><span data-stu-id="91beb-221">CERT\_SYSTEM\_STORE\_SERVICE and CERT\_SYSTEM\_STORE\_USERS stores are opened by prefixing the name of the store in the string passed to *pvPara* with the service or user name such as *ServiceName*\\**Trust** or **.Default**\\**MY**.</span></span> <span data-ttu-id="91beb-222">\_ \_ \_ Расположение пользователей службы хранилища системы сертификатов или \_ хранилища систем сертификатов \_ \_ может открыть то же хранилище в \_ \_ текущей службе системы сертификации \_ или в \_ системном \_ хранилище сертификатов \_ текущий пользователь с \_ помощью текстового [*идентификатора безопасности*](../secgloss/s-gly.md) (SID) текущей службы или пользователя.</span><span class="sxs-lookup"><span data-stu-id="91beb-222">The CERT\_SYSTEM\_STORE\_SERVICES or CERT\_SYSTEM\_STORE\_USERS location can open the same store in CERT\_SYSTEM\_CURRENT\_SERVICE or CERT\_SYSTEM\_STORE\_CURRENT\_USER by using the textual [*security identifier*](../secgloss/s-gly.md) (SID) of the current service or user.</span></span>

<span data-ttu-id="91beb-223">\_ \_ \_ \_ При загрузке компьютера или входе в систему на клиентском компьютере хранятся учетная запись групповая политика пользователя для хранилища систем сертификатов \_ и \_ \_ \_ \_ Групповая политика локального компьютера \_ Групповая политика с сертификатами в сети.</span><span class="sxs-lookup"><span data-stu-id="91beb-223">Stores in CERT\_SYSTEM\_STORE\_USER\_GROUP\_POLICY and CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY in a network setting are downloaded to the client computer from the Group Policy Template (GPT) during computer startup or user logon.</span></span> <span data-ttu-id="91beb-224">Эти магазины могут быть обновлены на клиентском компьютере после запуска или входа в систему при изменении GPT на сервере домена администратором.</span><span class="sxs-lookup"><span data-stu-id="91beb-224">These stores can be updated on the client computer after startup or logon when the GPT is changed on the domain server by an administrator.</span></span> <span data-ttu-id="91beb-225">Функция [**цертконтролсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) позволяет получать уведомления о приложении при изменении хранилищ в любом из этих расположений.</span><span class="sxs-lookup"><span data-stu-id="91beb-225">The [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) function allows an application to be notified when stores in either of these locations have changed.</span></span>

<span data-ttu-id="91beb-226">Следующие расположения системных хранилищ можно открыть удаленно:</span><span class="sxs-lookup"><span data-stu-id="91beb-226">The following system store locations can be opened remotely:</span></span>

-   <span data-ttu-id="91beb-227">\_ \_ \_ локальный \_ компьютер хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-227">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>
-   <span data-ttu-id="91beb-228">\_ \_ \_ \_ \_ Групповая политика локального компьютера хранилища \_ сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-228">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>
-   <span data-ttu-id="91beb-229">\_ \_ службы хранилища систем \_ сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-229">CERT\_SYSTEM\_STORE\_SERVICES</span></span>
-   <span data-ttu-id="91beb-230">\_Пользователи системного \_ хранилища \_ сертификатов</span><span class="sxs-lookup"><span data-stu-id="91beb-230">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="91beb-231">Расположения системных хранилищ открываются удаленно путем добавления имени хранилища в строку, переданную в *пвпара* , с именем компьютера.</span><span class="sxs-lookup"><span data-stu-id="91beb-231">System store locations are opened remotely by prefixing the store name in the string passed to *pvPara* with the computer name.</span></span> <span data-ttu-id="91beb-232">Примеры имен удаленных систем хранения:</span><span class="sxs-lookup"><span data-stu-id="91beb-232">Examples of remote system store names are:</span></span>

-   <span data-ttu-id="91beb-233">*Имя компьютера* \\ **Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="91beb-233">*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="91beb-234">\\\\*Имя компьютера* \\ **Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="91beb-234">\\\\*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="91beb-235">*Имя компьютера* \\ *ServiceName* \\ **Отношение доверия**</span><span class="sxs-lookup"><span data-stu-id="91beb-235">*ComputerName*\\*ServiceName*\\**Trust**</span></span>
-   <span data-ttu-id="91beb-236">\\\\*Имя компьютера* \\ *ServiceName* \\ **Отношение доверия**</span><span class="sxs-lookup"><span data-stu-id="91beb-236">\\\\*ComputerName*\\*ServiceName*\\**Trust**</span></span>

 

 
