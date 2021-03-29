---
title: Обновление динамического объекта
description: Клиент может обновить срок жизни (TTL) заданной записи каталога, чтобы она оставалась в рабочем состоянии одним из двух способов выполнить обновление LDAP до значения его атрибута Ентриттл, прежде чем запись будет собрана в мусор.
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7866c423fcb715289793a7beefa564150954257
ms.sourcegitcommit: 4d6ff888fd5825e78bc8fd5cdb21d4b542205039
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "105654399"
---
# <a name="refreshing-a-dynamic-object"></a><span data-ttu-id="8321d-103">Обновление динамического объекта</span><span class="sxs-lookup"><span data-stu-id="8321d-103">Refreshing a Dynamic Object</span></span>

<span data-ttu-id="8321d-104">Клиент может обновить срок жизни (TTL) заданной записи каталога, чтобы он оставался активным, одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="8321d-104">A client can refresh the Time To Live (TTL) of a given directory entry to keep it alive in one of two ways:</span></span>

-   <span data-ttu-id="8321d-105">Выполнение обновления LDAP до значения его атрибута **ентриттл** до того, как запись будет собрана в мусор.</span><span class="sxs-lookup"><span data-stu-id="8321d-105">Performing an LDAP update to the value of its **entryTTL** attribute before the entry is garbage collected.</span></span> <span data-ttu-id="8321d-106">Этот метод обновления динамической записи в каталоге является дополнительной (необязательной) функцией служб домен Active Directory Services, которая не указана в RFC 2589.</span><span class="sxs-lookup"><span data-stu-id="8321d-106">This method of refreshing a dynamic entry in the directory is an additional (optional) feature of Active Directory Domain Services that is not specified by RFC 2589.</span></span>
-   <span data-ttu-id="8321d-107">Выполнение расширенной операции LDAP с идентификатором OID 1.3.6.1.4.1.1466.101.119.1 для обновления TTL, как было оговорено в RFC 2589.</span><span class="sxs-lookup"><span data-stu-id="8321d-107">Performing an LDAP extended operation with an OID of 1.3.6.1.4.1.1466.101.119.1 for TTL refresh, as stipulated in the RFC 2589.</span></span> <span data-ttu-id="8321d-108">Этот OID определяется как **LDAP \_ TTL \_ Extended \_ Op \_** в винлдап. H.</span><span class="sxs-lookup"><span data-stu-id="8321d-108">This OID is defined as **LDAP\_TTL\_EXTENDED\_OP\_OID** in WINLDAP.H.</span></span>

 
<span data-ttu-id="8321d-109">\* \* Замечание \* \* \*: динамические объекты удаляются сборщиком мусора по истечении срока действия объекта, если срок его действия истек.</span><span class="sxs-lookup"><span data-stu-id="8321d-109">\*\*Remark\*\*\*: Dynamic objects are removed by Garbage Collector when they have expired, there is no phase of the object being a tombstone when it has expired.</span></span> <span data-ttu-id="8321d-110">При обновлении объектов необходимо соблюдать осторожность при использовании задержки репликации Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8321d-110">You need to be careful with the AD replication latency when you refresh objects.</span></span> <span data-ttu-id="8321d-111">Необходимо убедиться, что обновление для обновления TTL поступает на ранних этапах, поэтому все реплики контекста именования (полный и глобальный каталоги) видят транзакцию обновления, прежде чем срок действия объекта закончится локально.</span><span class="sxs-lookup"><span data-stu-id="8321d-111">You have to ensure that the update to refresh the TTL arrives early enough so all replicas of the naming context (full and global catalog) see the refresh transaction before the object expires locally.</span></span>

 




