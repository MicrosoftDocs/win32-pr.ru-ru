---
title: Элемент DisplayName (ПринЦипалтипе)
description: Указывает имя участника, отображаемого в пользовательском интерфейсе планировщик задач.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- Элемент DisplayName планировщик задач
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535501"
---
# <a name="displayname-principaltype-element"></a><span data-ttu-id="9966d-104">Элемент DisplayName (ПринЦипалтипе)</span><span class="sxs-lookup"><span data-stu-id="9966d-104">DisplayName (principalType) Element</span></span>

<span data-ttu-id="9966d-105">Указывает имя участника, отображаемого в пользовательском интерфейсе планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="9966d-105">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span>

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

<span data-ttu-id="9966d-106">Элемент **DisplayName** определяется сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9966d-106">The **DisplayName** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9966d-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="9966d-107">Parent element</span></span>



| <span data-ttu-id="9966d-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="9966d-108">Element</span></span>                                                                  | <span data-ttu-id="9966d-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="9966d-109">Derived from</span></span>                                                           | <span data-ttu-id="9966d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9966d-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9966d-111">**Основного**</span><span class="sxs-lookup"><span data-stu-id="9966d-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="9966d-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="9966d-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="9966d-113">Указывает учетные данные безопасности для участника.</span><span class="sxs-lookup"><span data-stu-id="9966d-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9966d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9966d-114">Remarks</span></span>

<span data-ttu-id="9966d-115">Для разработки сценариев отображаемое имя участника указывается с помощью свойства [**Principal. DisplayName**](principal-displayname.md) .</span><span class="sxs-lookup"><span data-stu-id="9966d-115">For scripting development, the display name of the principal is specified using the [**Principal.DisplayName**](principal-displayname.md) property.</span></span>

<span data-ttu-id="9966d-116">Для разработки на C++ отображаемое имя участника указывается с помощью свойства [**IPrincipal::D исплайнаме**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) .</span><span class="sxs-lookup"><span data-stu-id="9966d-116">For C++ development, the display name of the principal is specified using the [**IPrincipal::DisplayName**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) property.</span></span>

## <a name="examples"></a><span data-ttu-id="9966d-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="9966d-117">Examples</span></span>

<span data-ttu-id="9966d-118">Следующий XML-код определяет, используя идентификатор группы и отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="9966d-118">The following XML defines a using a group identifier and a display name.</span></span>


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



<span data-ttu-id="9966d-119">Следующий код XML определяет субъект, используя идентификатор пользователя и отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="9966d-119">The following XML defines a principal using a user identifier and a display name.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="9966d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9966d-120">Requirements</span></span>



| <span data-ttu-id="9966d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9966d-121">Requirement</span></span> | <span data-ttu-id="9966d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9966d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9966d-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9966d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9966d-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9966d-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9966d-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9966d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9966d-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9966d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9966d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9966d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9966d-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="9966d-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





