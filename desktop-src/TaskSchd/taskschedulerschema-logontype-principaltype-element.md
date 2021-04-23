---
title: LogonType (ПринЦипалтипе), элемент
description: Указывает метод входа в систему безопасности, необходимый для выполнения задач, связанных с участником.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- планировщик задач элемента LogonType
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a382225f526f18731b8b9f0541e617cb31dfb4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681814"
---
# <a name="logontype-principaltype-element"></a><span data-ttu-id="cd857-104">LogonType (ПринЦипалтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="cd857-104">LogonType (principalType) Element</span></span>

<span data-ttu-id="cd857-105">Указывает метод входа в систему безопасности, необходимый для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="cd857-105">Specifies the security logon method required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

<span data-ttu-id="cd857-106">Элемент **LogonType** определяется сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cd857-106">The **LogonType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cd857-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="cd857-107">Parent element</span></span>



| <span data-ttu-id="cd857-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="cd857-108">Element</span></span>                                                                  | <span data-ttu-id="cd857-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="cd857-109">Derived from</span></span>                                                           | <span data-ttu-id="cd857-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cd857-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="cd857-111">**Основного**</span><span class="sxs-lookup"><span data-stu-id="cd857-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="cd857-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="cd857-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="cd857-113">Указывает учетные данные безопасности для участника.</span><span class="sxs-lookup"><span data-stu-id="cd857-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cd857-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd857-114">Remarks</span></span>

<span data-ttu-id="cd857-115">Элемент **LogonType** и элемент [**UserID**](taskschedulerschema-userid-principaltype-element.md) используются совместно для определения пользователя, необходимого для выполнения этих задач, использующих этот участник.</span><span class="sxs-lookup"><span data-stu-id="cd857-115">The **LogonType** element and the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="cd857-116">Для разработки сценариев тип входа для участника указывается свойством [**Principal. LogonType**](principal-logontype.md) .</span><span class="sxs-lookup"><span data-stu-id="cd857-116">For scripting development, the logon type for the principal is specified by the [**Principal.LogonType**](principal-logontype.md) property.</span></span>

<span data-ttu-id="cd857-117">Для разработки на C++ тип входа для участника указывается в свойстве [**IPrincipal:: LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) .</span><span class="sxs-lookup"><span data-stu-id="cd857-117">For C++ development, the logon type for the principal is specified by the [**IPrincipal::LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) property.</span></span>

<span data-ttu-id="cd857-118">Этот элемент (определяемый простым типом [**logonType**](taskschedulerschema-logontype-simpletype.md) ) должен иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cd857-118">This element (defined by the [**logonType**](taskschedulerschema-logontype-simpletype.md) simple type) must have one of the following values.</span></span>

-   <span data-ttu-id="cd857-119">S4U: пользователь должен войти в систему, используя службу для входа пользователя (S4U).</span><span class="sxs-lookup"><span data-stu-id="cd857-119">S4U: User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="cd857-120">При использовании имени входа S4U система не хранит пароль и не имеет доступа к сети или зашифрованным файлам.</span><span class="sxs-lookup"><span data-stu-id="cd857-120">When an S4U logon is used, no password is stored by the system and there is no access to the network or encrypted files.</span></span>
-   <span data-ttu-id="cd857-121">Пароль: пользователь должен войти в систему, используя пароль.</span><span class="sxs-lookup"><span data-stu-id="cd857-121">Password: User must log on using a password.</span></span>
-   <span data-ttu-id="cd857-122">Интерактиветокен: пользователь уже должен войти в систему.</span><span class="sxs-lookup"><span data-stu-id="cd857-122">InteractiveToken: User must already be logged on.</span></span> <span data-ttu-id="cd857-123">Задача будет запущена только в существующем интерактивном сеансе.</span><span class="sxs-lookup"><span data-stu-id="cd857-123">The task will be run only in an existing interactive session.</span></span>

<span data-ttu-id="cd857-124">Для задачи, которая содержит действие «окно сообщения», появится окно сообщения, если задача активирована, а задача имеет интерактивный тип входа в систему.</span><span class="sxs-lookup"><span data-stu-id="cd857-124">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="cd857-125">Чтобы задать тип входа "интерактивный" для задачи, укажите **интерактиветокен** в **<LogonType>** элементе участника задачи.</span><span class="sxs-lookup"><span data-stu-id="cd857-125">To set the task logon type to be interactive, specify **InteractiveToken** in the **<LogonType>** element of the task principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd857-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cd857-126">Requirements</span></span>



| <span data-ttu-id="cd857-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cd857-127">Requirement</span></span> | <span data-ttu-id="cd857-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cd857-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd857-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd857-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cd857-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd857-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cd857-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd857-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cd857-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd857-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd857-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd857-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd857-134">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="cd857-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





