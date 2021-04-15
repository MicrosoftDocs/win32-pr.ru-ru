---
title: UserId (ПринЦипалтипе), элемент
description: Указывает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
keywords:
- Элемент UserId планировщик задач
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416149"
---
# <a name="userid-principaltype-element"></a><span data-ttu-id="ede2a-104">UserId (ПринЦипалтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="ede2a-104">UserId (principalType) Element</span></span>

<span data-ttu-id="ede2a-105">Указывает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="ede2a-105">Specifies the user identifier required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="ede2a-106">Элемент **UserID** определяется сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ede2a-106">The **UserId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ede2a-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="ede2a-107">Parent element</span></span>



| <span data-ttu-id="ede2a-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="ede2a-108">Element</span></span>                                                                  | <span data-ttu-id="ede2a-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="ede2a-109">Derived from</span></span>                                                           | <span data-ttu-id="ede2a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ede2a-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ede2a-111">**Основного**</span><span class="sxs-lookup"><span data-stu-id="ede2a-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="ede2a-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="ede2a-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="ede2a-113">Указывает учетные данные безопасности для участника.</span><span class="sxs-lookup"><span data-stu-id="ede2a-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ede2a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ede2a-114">Remarks</span></span>

<span data-ttu-id="ede2a-115">Элемент **UserID** и элемент [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) используются вместе для определения пользователя, необходимого для выполнения этих задач, использующих этот участник.</span><span class="sxs-lookup"><span data-stu-id="ede2a-115">The **UserId** element and the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="ede2a-116">Нельзя одновременно указать идентификатор пользователя и идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="ede2a-116">You cannot specify a user identifier and a group identifier at the same time.</span></span> <span data-ttu-id="ede2a-117">Укажите либо **идентификатор UserID** , либо элемент [**groupId**](taskschedulerschema-groupid-principaltype-element.md) , но не оба.</span><span class="sxs-lookup"><span data-stu-id="ede2a-117">Specify either the **UserId** or the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element, but not both.</span></span>

<span data-ttu-id="ede2a-118">Для разработки сценариев идентификатор пользователя указывается с помощью свойства [**Principal. UserID**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="ede2a-118">For scripting development, the user identifier is specified using the [**Principal.UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="ede2a-119">Для разработки на C++ идентификатор пользователя указывается с помощью свойства [**IPrincipal:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="ede2a-119">For C++ development, the user identifier is specified using the [**IPrincipal::UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ede2a-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="ede2a-120">Examples</span></span>

<span data-ttu-id="ede2a-121">Следующий XML-код определяет принцип, используя идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="ede2a-121">The following XML defines a principle using a user identifier.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="ede2a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ede2a-122">Requirements</span></span>



| <span data-ttu-id="ede2a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ede2a-123">Requirement</span></span> | <span data-ttu-id="ede2a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ede2a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ede2a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ede2a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ede2a-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ede2a-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ede2a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ede2a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ede2a-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ede2a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ede2a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ede2a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede2a-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="ede2a-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





