---
description: Инфраструктура открытых ключей Windows (PKI) сохраняет сертификаты на сервере, на котором размещается центр сертификации (ЦС), на локальном компьютере или устройстве.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Каталог сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272930"
---
# <a name="certificate-directory"></a><span data-ttu-id="2838f-103">Каталог сертификатов</span><span class="sxs-lookup"><span data-stu-id="2838f-103">Certificate Directory</span></span>

<span data-ttu-id="2838f-104">Инфраструктура открытых ключей Windows (PKI) сохраняет сертификаты на сервере, на котором размещается центр сертификации (ЦС), на локальном компьютере или устройстве.</span><span class="sxs-lookup"><span data-stu-id="2838f-104">A Windows public key infrastructure (PKI) saves certificates on the server that hosts the certification authority (CA) and on the local computer or device.</span></span> <span data-ttu-id="2838f-105">Хранилище ЦС обычно называется базой данных сертификатов, а локальное хранилище называется хранилищем сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2838f-105">CA storage is typically referred to as the certificate database, and local storage is known as the certificate store.</span></span>

## <a name="certificate-database"></a><span data-ttu-id="2838f-106">База данных сертификатов</span><span class="sxs-lookup"><span data-stu-id="2838f-106">Certificate Database</span></span>

<span data-ttu-id="2838f-107">При добавлении служб сертификатов на сервере Windows Server и настройке центра сертификации создается база данных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2838f-107">When you add Certificate Services on a Windows server and configure a CA, a certificate database is created.</span></span> <span data-ttu-id="2838f-108">По умолчанию база данных находится в папке *% systemroot%* \\ system32 \\ цертлог, а имя — на имени ЦС с расширением. edb.</span><span class="sxs-lookup"><span data-stu-id="2838f-108">By default, the database is contained in the *%SystemRoot%*\\System32\\Certlog folder, and the name is based on the CA name with an .edb extension.</span></span> <span data-ttu-id="2838f-109">База данных может содержать:</span><span class="sxs-lookup"><span data-stu-id="2838f-109">The database can contain:</span></span>

-   <span data-ttu-id="2838f-110">Выданные сертификаты</span><span class="sxs-lookup"><span data-stu-id="2838f-110">Issued certificates</span></span>
-   <span data-ttu-id="2838f-111">Отозванные сертификаты</span><span class="sxs-lookup"><span data-stu-id="2838f-111">Revoked certificates</span></span>
-   <span data-ttu-id="2838f-112">Архивированные закрытые ключи</span><span class="sxs-lookup"><span data-stu-id="2838f-112">Archived private keys</span></span>
-   <span data-ttu-id="2838f-113">Запросы сертификатов</span><span class="sxs-lookup"><span data-stu-id="2838f-113">Certificate requests</span></span>

<span data-ttu-id="2838f-114">API регистрации сертификатов нельзя использовать для работы с базой данных.</span><span class="sxs-lookup"><span data-stu-id="2838f-114">You cannot use the Certificate Enrollment API to manipulate the database.</span></span> <span data-ttu-id="2838f-115">Процесс регистрации автоматически создает необходимые записи.</span><span class="sxs-lookup"><span data-stu-id="2838f-115">The enrollment process automatically creates the necessary entries.</span></span>

## <a name="certificate-stores"></a><span data-ttu-id="2838f-116">Хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="2838f-116">Certificate Stores</span></span>

<span data-ttu-id="2838f-117">Службы сертификации Майкрософт копируют выданные сертификаты и ожидающие или отклоненные запросы на локальные компьютеры и устройства.</span><span class="sxs-lookup"><span data-stu-id="2838f-117">Microsoft Certificate Services copies issued certificates and pending or rejected requests to local computers and devices.</span></span> <span data-ttu-id="2838f-118">Место хранения называется хранилищем сертификатов и состоит из следующих логических хранилищ.</span><span class="sxs-lookup"><span data-stu-id="2838f-118">The storage location is called the certificate store and consists of the following logical stores.</span></span>

| <span data-ttu-id="2838f-119">Логическое хранилище</span><span class="sxs-lookup"><span data-stu-id="2838f-119">Logical store</span></span>                                         | <span data-ttu-id="2838f-120">Описание</span><span class="sxs-lookup"><span data-stu-id="2838f-120">Description</span></span>                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2838f-121">Персональный</span><span class="sxs-lookup"><span data-stu-id="2838f-121">Personal</span></span><br/>                                   | <span data-ttu-id="2838f-122">Содержит сертификаты, связанные с закрытым ключом, управляемым пользователем или компьютером.</span><span class="sxs-lookup"><span data-stu-id="2838f-122">Contains certificates associated with a private key controlled by the user or computer.</span></span><br/>                     |
| <span data-ttu-id="2838f-123">Доверенные корневые центры сертификации</span><span class="sxs-lookup"><span data-stu-id="2838f-123">Trusted Root Certification Authorities</span></span><br/>     | <span data-ttu-id="2838f-124">Содержит сертификаты из неявных доверенных центров сертификации (CAs).</span><span class="sxs-lookup"><span data-stu-id="2838f-124">Contains certificates from implicitly trusted certification authorities (CAs).</span></span><br/>                              |
| <span data-ttu-id="2838f-125">Доверительные отношения в предприятии</span><span class="sxs-lookup"><span data-stu-id="2838f-125">Enterprise Trust</span></span><br/>                           | <span data-ttu-id="2838f-126">Содержит списки доверия сертификатов, которые обычно используются для доверия самозаверяющих сертификатов из других организаций.</span><span class="sxs-lookup"><span data-stu-id="2838f-126">Contains certificate trust lists typically used to trust self-signed certificates from other organizations.</span></span><br/> |
| <span data-ttu-id="2838f-127">Промежуточные центры сертификации</span><span class="sxs-lookup"><span data-stu-id="2838f-127">Intermediate Certification Authorities</span></span><br/>     | <span data-ttu-id="2838f-128">Содержит сертификаты, выданные подчиненным ЦС в иерархии сертификации.</span><span class="sxs-lookup"><span data-stu-id="2838f-128">Contains certificates issued to subordinate CAs in the certification hierarchy.</span></span><br/>                             |
| <span data-ttu-id="2838f-129">Объект пользователя Active Directory</span><span class="sxs-lookup"><span data-stu-id="2838f-129">Active Directory User Object</span></span><br/>               | <span data-ttu-id="2838f-130">Содержит сертификат объекта пользователя или сертификаты, опубликованные в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2838f-130">Contains the user object certificate or certificates published in Active Directory.</span></span><br/>                         |
| <span data-ttu-id="2838f-131">Доверенные издатели</span><span class="sxs-lookup"><span data-stu-id="2838f-131">Trusted Publishers</span></span><br/>                         | <span data-ttu-id="2838f-132">Содержит сертификаты из доверенных ЦС.</span><span class="sxs-lookup"><span data-stu-id="2838f-132">Contains certificates from trusted CAs.</span></span><br/>                                                                     |
| <span data-ttu-id="2838f-133">Недоверенные сертификаты</span><span class="sxs-lookup"><span data-stu-id="2838f-133">Untrusted Certificates</span></span><br/>                     | <span data-ttu-id="2838f-134">Содержит сертификаты, которые были явно идентифицированы как ненадежные.</span><span class="sxs-lookup"><span data-stu-id="2838f-134">Contains certificates that have been explicitly identified as untrusted.</span></span><br/>                                    |
| <span data-ttu-id="2838f-135">cторонние корневые центры сертификации.</span><span class="sxs-lookup"><span data-stu-id="2838f-135">Third-Party Root Certification Authorities</span></span><br/> | <span data-ttu-id="2838f-136">Содержит доверенные корневые сертификаты из центров сертификации, находящихся за пределами внутренней иерархии сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2838f-136">Contains trusted root certificates from CAs outside the internal certificate hierarchy.</span></span><br/>                     |
| <span data-ttu-id="2838f-137">Доверенные лица</span><span class="sxs-lookup"><span data-stu-id="2838f-137">Trusted People</span></span><br/>                             | <span data-ttu-id="2838f-138">Содержит сертификаты, выданные пользователям или сущностям, которые были явно доверенными.</span><span class="sxs-lookup"><span data-stu-id="2838f-138">Contains certificates issued to users or entities that have been explicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="2838f-139">Другие люди</span><span class="sxs-lookup"><span data-stu-id="2838f-139">Other People</span></span><br/>                               | <span data-ttu-id="2838f-140">Содержит сертификаты, выданные пользователям или сущностям, которые были неявно доверенными.</span><span class="sxs-lookup"><span data-stu-id="2838f-140">Contains certificates issued to users or entities that have been implicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="2838f-141">Запросы регистрации сертификата</span><span class="sxs-lookup"><span data-stu-id="2838f-141">Certificate Enrollment Requests</span></span><br/>            | <span data-ttu-id="2838f-142">Содержит ожидающие или отклоненные запросы сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2838f-142">Contains pending or rejected certificate requests.</span></span><br/>                                                          |



 

<span data-ttu-id="2838f-143">API регистрации сертификатов нельзя использовать для указания или получения свойств хранилища или копирования сертификатов в определенные хранилища.</span><span class="sxs-lookup"><span data-stu-id="2838f-143">You cannot use the Certificate Enrollment API to specify or retrieve store properties or copy certificates to specific stores.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2838f-144">См. также</span><span class="sxs-lookup"><span data-stu-id="2838f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2838f-145">Элементы PKI</span><span class="sxs-lookup"><span data-stu-id="2838f-145">PKI Elements</span></span>](about-pki-components.md)
</dt> </dl>

 

 




