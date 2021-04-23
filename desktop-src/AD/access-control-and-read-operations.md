---
title: Операции контроля доступа и чтения
description: Безопасность — это неявный фильтр для поиска, перечисления контейнеров или чтения свойств.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Управление доступом и операции чтения AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067277"
---
# <a name="access-control-and-read-operations"></a><span data-ttu-id="602f4-104">Операции контроля доступа и чтения</span><span class="sxs-lookup"><span data-stu-id="602f4-104">Access Control and Read Operations</span></span>

<span data-ttu-id="602f4-105">Безопасность — это неявный фильтр для поиска, перечисления контейнеров или чтения свойств.</span><span class="sxs-lookup"><span data-stu-id="602f4-105">Security is an implicit filter for searching, enumerating containers, or reading properties.</span></span> <span data-ttu-id="602f4-106">Если у вас нет необходимых прав доступа, попытки перечисления объектов или чтения свойств могут завершиться со следующими кодами ошибок, даже если объект или свойство существует.</span><span class="sxs-lookup"><span data-stu-id="602f4-106">If you do not have the necessary access rights, attempts to list objects or read properties can fail with the following error codes even thought the object or property exists:</span></span>

-   <span data-ttu-id="602f4-107">**E \_ ADS \_ Недопустимый \_ \_ объект домена**</span><span class="sxs-lookup"><span data-stu-id="602f4-107">**E\_ADS\_INVALID\_DOMAIN\_OBJECT**</span></span>
-   <span data-ttu-id="602f4-108">**\_свойство E \_ ADS \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="602f4-108">**E\_ADS\_PROPERTY\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="602f4-109">**\_ \_ \_ не \_ найдено свойство E ADS**</span><span class="sxs-lookup"><span data-stu-id="602f4-109">**E\_ADS\_PROPERTY\_NOT\_FOUND**</span></span>

<span data-ttu-id="602f4-110">Имейте в виду, что вызывающая сторона с **AD \_ справа \_ актрл \_ DS \_ List** имеет доступ к контейнеру, который может перечислить дочерние объекты в контейнере.</span><span class="sxs-lookup"><span data-stu-id="602f4-110">Be aware that a caller with **ADS\_RIGHT\_ACTRL\_DS\_LIST** access to a container can enumerate the child objects in the container.</span></span> <span data-ttu-id="602f4-111">Но попытка доступа к дочернему объекту по-прежнему может завершиться ошибкой, например с **\_ \_ неизвестным \_ объектом E ADS** , если у вызывающего объекта нет ads, актрл доступ к **\_ \_ \_ \_ \_ объекту списка DS** с дочерним объектом.</span><span class="sxs-lookup"><span data-stu-id="602f4-111">But an attempt to access a child object can still fail with an error such as **E\_ADS\_UNKNOWN\_OBJECT** if the caller does not have **ADS\_RIGHT\_ACTRL\_DS\_LIST\_OBJECT** access to the child object.</span></span>

<span data-ttu-id="602f4-112">Влияние безопасности на операции чтения не обязательно является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="602f4-112">The impact of security on read operations is not necessarily manifested as an error.</span></span> <span data-ttu-id="602f4-113">Например, операция поиска может выполняться успешно, но результаты поиска не включают объекты или свойства, к которым вызывающий объект не имеет доступа.</span><span class="sxs-lookup"><span data-stu-id="602f4-113">For example, a search operation can succeed, but the search results do not include objects or properties to which the caller does not have access.</span></span>

 

 




