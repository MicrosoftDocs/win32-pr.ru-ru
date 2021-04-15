---
description: Перечисляет и описывает типы доступа объекта политики.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Права доступа к объектам политики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662304"
---
# <a name="policy-object-access-rights"></a><span data-ttu-id="6b562-103">Права доступа к объектам политики</span><span class="sxs-lookup"><span data-stu-id="6b562-103">Policy Object Access Rights</span></span>

<span data-ttu-id="6b562-104">Объект [**политики**](policy-object.md) имеет следующие типы доступа для конкретного объекта:</span><span class="sxs-lookup"><span data-stu-id="6b562-104">The [**Policy**](policy-object.md) object has the following object-specific access types:</span></span>



| <span data-ttu-id="6b562-105">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="6b562-105">Access type</span></span>                         | <span data-ttu-id="6b562-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6b562-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b562-107">\_ \_ Локальная информация представления политики \_</span><span class="sxs-lookup"><span data-stu-id="6b562-107">POLICY\_VIEW\_LOCAL\_INFORMATION</span></span>    | <span data-ttu-id="6b562-108">Этот тип доступа необходим для чтения сведений о различных политиках безопасности целевой системы.</span><span class="sxs-lookup"><span data-stu-id="6b562-108">This access type is needed to read the target system's miscellaneous security policy information.</span></span> <span data-ttu-id="6b562-109">К ним относятся квота по умолчанию, аудит, сведения о состоянии сервера и роли, а также сведения о доверии.</span><span class="sxs-lookup"><span data-stu-id="6b562-109">This includes the default quota, auditing, server state and role information, and trust information.</span></span> <span data-ttu-id="6b562-110">Этот тип доступа также необходим для перечисления доверенных доменов, учетных записей и [*привилегий*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="6b562-110">This access type is also needed to enumerate trusted domains, accounts, and [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> |
| <span data-ttu-id="6b562-111">ПОЛИТИКА \_ получения \_ частной \_ информации</span><span class="sxs-lookup"><span data-stu-id="6b562-111">POLICY\_GET\_PRIVATE\_INFORMATION</span></span>   | <span data-ttu-id="6b562-112">Этот тип доступа необходим для просмотра конфиденциальной информации, например имен учетных записей, установленных для отношений доверенных доменов.</span><span class="sxs-lookup"><span data-stu-id="6b562-112">This access type is needed to view sensitive information, such as the names of accounts established for trusted domain relationships.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="6b562-113">\_Администратор доверия \_ политики</span><span class="sxs-lookup"><span data-stu-id="6b562-113">POLICY\_TRUST\_ADMIN</span></span>                | <span data-ttu-id="6b562-114">Этот тип доступа необходим для изменения сведений о домене учетной записи или основном домене.</span><span class="sxs-lookup"><span data-stu-id="6b562-114">This access type is needed to change the account domain or primary domain information.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="6b562-115">\_ \_ \_ ограничение квоты по умолчанию для набора политик \_</span><span class="sxs-lookup"><span data-stu-id="6b562-115">POLICY\_SET\_DEFAULT\_QUOTA\_LIMITS</span></span> | <span data-ttu-id="6b562-116">Задайте системные квоты по умолчанию, применяемые к учетным записям пользователей.</span><span class="sxs-lookup"><span data-stu-id="6b562-116">Set the default system quotas that are applied to user accounts.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="6b562-117">ПОЛИТИКА \_ создания \_ секрета</span><span class="sxs-lookup"><span data-stu-id="6b562-117">POLICY\_CREATE\_SECRET</span></span>              | <span data-ttu-id="6b562-118">Этот тип доступа необходим для создания нового закрытого объекта данных.</span><span class="sxs-lookup"><span data-stu-id="6b562-118">This access type is needed to create a new Private Data object.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6b562-119">ПОЛИТИКА \_ создания \_ учетной записи</span><span class="sxs-lookup"><span data-stu-id="6b562-119">POLICY\_CREATE\_ACCOUNT</span></span>             | <span data-ttu-id="6b562-120">Этот тип доступа необходим для создания нового объекта [**учетной записи**](account-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6b562-120">This access type is needed to create a new [**Account**](account-object.md) object.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="6b562-121">\_ \_ требования к аудиту для набора политик \_</span><span class="sxs-lookup"><span data-stu-id="6b562-121">POLICY\_SET\_AUDIT\_REQUIREMENTS</span></span>    | <span data-ttu-id="6b562-122">Этот тип доступа необходим для обновления требований аудита системы.</span><span class="sxs-lookup"><span data-stu-id="6b562-122">This access type is needed to update the auditing requirements of the system.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6b562-123">\_ \_ Администратор журнала аудита \_ политики</span><span class="sxs-lookup"><span data-stu-id="6b562-123">POLICY\_AUDIT\_LOG\_ADMIN</span></span>           | <span data-ttu-id="6b562-124">Этот тип доступа необходим для изменения характеристик журнала аудита, например его максимального размера или срока хранения записей аудита, а также для очистки журналов.</span><span class="sxs-lookup"><span data-stu-id="6b562-124">This access type is needed to change the characteristics of the audit trail such as its maximum size or the retention period for audit records, or to clear the log.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="6b562-125">\_Просмотр политики \_ \_ сведения о аудите</span><span class="sxs-lookup"><span data-stu-id="6b562-125">POLICY\_VIEW\_AUDIT\_INFORMATION</span></span>    | <span data-ttu-id="6b562-126">Этот тип доступа необходим для просмотра сведений о требованиях аудита или аудита.</span><span class="sxs-lookup"><span data-stu-id="6b562-126">This access type is needed to view audit trail or audit requirements information.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6b562-127">\_Администратор сервера \_ политики</span><span class="sxs-lookup"><span data-stu-id="6b562-127">POLICY\_SERVER\_ADMIN</span></span>               | <span data-ttu-id="6b562-128">Этот тип доступа необходим для изменения сведений о состоянии сервера или роли (главной или реплике).</span><span class="sxs-lookup"><span data-stu-id="6b562-128">This access type is needed to modify the server state or role (master/replica) information.</span></span> <span data-ttu-id="6b562-129">Также необходимо изменить сведения об источнике реплики и имени учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6b562-129">It is also needed to change the replica source and account name information.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="6b562-130">\_имена уточняющего запроса политики \_</span><span class="sxs-lookup"><span data-stu-id="6b562-130">POLICY\_LOOKUP\_NAMES</span></span>               | <span data-ttu-id="6b562-131">Этот тип доступа необходим для преобразования между именами и идентификаторами безопасности.</span><span class="sxs-lookup"><span data-stu-id="6b562-131">This access type is needed to translate between names and SIDs.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6b562-132">\_привилегия создания \_ политики</span><span class="sxs-lookup"><span data-stu-id="6b562-132">POLICY\_CREATE\_PRIVILEGE</span></span>           | <span data-ttu-id="6b562-133">Пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6b562-133">Not yet supported.</span></span>                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a><span data-ttu-id="6b562-134">Универсальные маски доступа</span><span class="sxs-lookup"><span data-stu-id="6b562-134">Generic Access Masks</span></span>

<span data-ttu-id="6b562-135">Объект [**политики**](policy-object.md) публикует следующие сопоставления из универсальных типов доступа в определенные типы доступа:</span><span class="sxs-lookup"><span data-stu-id="6b562-135">The [**Policy**](policy-object.md) object publishes the following mappings from generic access types to specific access types:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a><span data-ttu-id="6b562-136">Стандартные типы доступа</span><span class="sxs-lookup"><span data-stu-id="6b562-136">Standard Access Types</span></span>

<span data-ttu-id="6b562-137">Этот объект не поддерживает (необязательно) СИНХРОНИЗАЦИю стандартного типа доступа.</span><span class="sxs-lookup"><span data-stu-id="6b562-137">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="6b562-138">Поддерживаются все необходимые типы доступа.</span><span class="sxs-lookup"><span data-stu-id="6b562-138">All required access types are supported.</span></span> <span data-ttu-id="6b562-139">Маска всех поддерживаемых типов доступа для этого типа объектов:</span><span class="sxs-lookup"><span data-stu-id="6b562-139">The mask of all supported access types for this object type is:</span></span>

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 
