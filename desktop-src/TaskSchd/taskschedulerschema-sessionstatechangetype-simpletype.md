---
title: Простой тип Сессионстатечанжетипе
description: Определяет значения для типа изменения состояния сеанса сервера терминалов, которые можно использовать для запуска задачи.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- планировщик задач простого типа Сессионстатечанжетипе
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492270"
---
# <a name="sessionstatechangetype-simple-type"></a><span data-ttu-id="0c21d-104">Простой тип Сессионстатечанжетипе</span><span class="sxs-lookup"><span data-stu-id="0c21d-104">sessionStateChangeType Simple Type</span></span>

<span data-ttu-id="0c21d-105">Определяет значения для типа изменения состояния сеанса сервера терминалов, которые можно использовать для запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="0c21d-105">Defines values for the kind of Terminal Server session state change you can use to trigger a task to start.</span></span>

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="0c21d-106">Значения перечисления</span><span class="sxs-lookup"><span data-stu-id="0c21d-106">Enumeration values</span></span>

<span data-ttu-id="0c21d-107">Простой тип **сессионстатечанжетипе** определяет следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0c21d-107">The **sessionStateChangeType** simple type defines the following values.</span></span>



| <span data-ttu-id="0c21d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0c21d-108">Value</span></span>             | <span data-ttu-id="0c21d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0c21d-109">Description</span></span>                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c21d-110">консолеконнект</span><span class="sxs-lookup"><span data-stu-id="0c21d-110">ConsoleConnect</span></span>    | <span data-ttu-id="0c21d-111">Изменение состояния подключения к консоли сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="0c21d-111">Terminal Server console connection state change.</span></span> <span data-ttu-id="0c21d-112">Например, при подключении к сеансу пользователя на локальном компьютере путем переключения пользователей на компьютер.</span><span class="sxs-lookup"><span data-stu-id="0c21d-112">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                            |
| <span data-ttu-id="0c21d-113">консоледисконнект</span><span class="sxs-lookup"><span data-stu-id="0c21d-113">ConsoleDisconnect</span></span> | <span data-ttu-id="0c21d-114">Изменение состояния отключения консоли сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="0c21d-114">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="0c21d-115">Например, при отключении сеанса пользователя на локальном компьютере путем переключения пользователей на компьютер.</span><span class="sxs-lookup"><span data-stu-id="0c21d-115">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span> <br/>                      |
| <span data-ttu-id="0c21d-116">ремотеконнект</span><span class="sxs-lookup"><span data-stu-id="0c21d-116">RemoteConnect</span></span>     | <span data-ttu-id="0c21d-117">Изменение состояния удаленного подключения сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="0c21d-117">Terminal Server remote connection state change.</span></span> <span data-ttu-id="0c21d-118">Например, когда пользователь подключается к сеансу пользователя с помощью подключение к удаленному рабочему столу программы с удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="0c21d-118">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span> <br/>            |
| <span data-ttu-id="0c21d-119">ремотедисконнект</span><span class="sxs-lookup"><span data-stu-id="0c21d-119">RemoteDisconnect</span></span>  | <span data-ttu-id="0c21d-120">Изменение состояния удаленного отключения сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="0c21d-120">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="0c21d-121">Например, когда пользователь отключается от сеанса пользователя при использовании подключение к удаленному рабочему столу программы с удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="0c21d-121">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span> <br/> |
| <span data-ttu-id="0c21d-122">сессионлокк</span><span class="sxs-lookup"><span data-stu-id="0c21d-122">SessionLock</span></span>       | <span data-ttu-id="0c21d-123">Изменение состояния блокировки сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="0c21d-123">Terminal Server session locked state change.</span></span> <span data-ttu-id="0c21d-124">Например, это изменение состояния приводит к запуску задачи при блокировке компьютера.</span><span class="sxs-lookup"><span data-stu-id="0c21d-124">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                       |
| <span data-ttu-id="0c21d-125">сессионунлокк</span><span class="sxs-lookup"><span data-stu-id="0c21d-125">SessionUnlock</span></span>     | <span data-ttu-id="0c21d-126">Изменение состояния разблокировки сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="0c21d-126">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="0c21d-127">Например, это изменение состояния приводит к выполнению задачи при разблокировании компьютера.</span><span class="sxs-lookup"><span data-stu-id="0c21d-127">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                    |



## <a name="requirements"></a><span data-ttu-id="0c21d-128">Требования</span><span class="sxs-lookup"><span data-stu-id="0c21d-128">Requirements</span></span>



| <span data-ttu-id="0c21d-129">Требование</span><span class="sxs-lookup"><span data-stu-id="0c21d-129">Requirement</span></span> | <span data-ttu-id="0c21d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="0c21d-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c21d-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c21d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0c21d-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c21d-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c21d-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c21d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0c21d-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c21d-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





