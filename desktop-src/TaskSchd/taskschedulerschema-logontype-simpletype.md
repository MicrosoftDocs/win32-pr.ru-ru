---
title: Простой тип logonType
description: Определяет возможные значения элемента LogonType.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- планировщик задач простого типа logonType
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136922"
---
# <a name="logontype-simple-type"></a><span data-ttu-id="8717a-104">Простой тип logonType</span><span class="sxs-lookup"><span data-stu-id="8717a-104">logonType Simple Type</span></span>

<span data-ttu-id="8717a-105">Определяет возможные значения элемента [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8717a-105">Defines the possible values of the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="8717a-106">Значения перечисления</span><span class="sxs-lookup"><span data-stu-id="8717a-106">Enumeration values</span></span>

<span data-ttu-id="8717a-107">Простой тип **logonType** определяет следующие значения.</span><span class="sxs-lookup"><span data-stu-id="8717a-107">The **logonType** simple type defines the following values.</span></span>



| <span data-ttu-id="8717a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8717a-108">Value</span></span>                      | <span data-ttu-id="8717a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8717a-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8717a-110">S4U</span><span class="sxs-lookup"><span data-stu-id="8717a-110">S4U</span></span>                        | <span data-ttu-id="8717a-111">Пользователь должен войти в систему, используя службу для входа пользователя (S4U).</span><span class="sxs-lookup"><span data-stu-id="8717a-111">User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="8717a-112">При использовании имени входа S4U система не хранит пароль и не имеет доступа к сети или зашифрованным файлам.</span><span class="sxs-lookup"><span data-stu-id="8717a-112">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="8717a-113">Пароль</span><span class="sxs-lookup"><span data-stu-id="8717a-113">Password</span></span>                   | <span data-ttu-id="8717a-114">Пользователь должен войти в систему, используя пароль.</span><span class="sxs-lookup"><span data-stu-id="8717a-114">User must log on using a password.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8717a-115">интерактиветокен</span><span class="sxs-lookup"><span data-stu-id="8717a-115">InteractiveToken</span></span>           | <span data-ttu-id="8717a-116">Пользователь уже должен войти в систему.</span><span class="sxs-lookup"><span data-stu-id="8717a-116">User must already be logged on.</span></span> <span data-ttu-id="8717a-117">Задача будет запущена только в существующем интерактивном сеансе.</span><span class="sxs-lookup"><span data-stu-id="8717a-117">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="8717a-118">интерактиветокенорпассворд</span><span class="sxs-lookup"><span data-stu-id="8717a-118">InteractiveTokenOrPassword</span></span> | <span data-ttu-id="8717a-119">Больше не используется; в настоящее время совпадает с паролем.</span><span class="sxs-lookup"><span data-stu-id="8717a-119">No longer in use; currently identical to Password.</span></span><br/> <span data-ttu-id="8717a-120">**Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows server 2012, Windows Vista и Windows server 2008:** Задача будет запущена в существующем интерактивном сеансе или пользователь должен войти в систему с помощью пароля.</span><span class="sxs-lookup"><span data-stu-id="8717a-120">**Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista and Windows Server 2008:** The task will be run in an existing interactive session or the user must log on using a password.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="8717a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8717a-121">Requirements</span></span>



| <span data-ttu-id="8717a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8717a-122">Requirement</span></span> | <span data-ttu-id="8717a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8717a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8717a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8717a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8717a-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8717a-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8717a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8717a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8717a-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8717a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8717a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8717a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8717a-129">Простые типы схемы планировщик задач</span><span class="sxs-lookup"><span data-stu-id="8717a-129">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="8717a-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="8717a-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





