---
title: Элемент Principal (ПринЦипалтипе)
description: Указывает учетные данные безопасности для участника.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Основной элемент планировщик задач
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681788"
---
# <a name="principal-principaltype-element"></a><span data-ttu-id="cd342-104">Элемент Principal (ПринЦипалтипе)</span><span class="sxs-lookup"><span data-stu-id="cd342-104">Principal (principalType) Element</span></span>

<span data-ttu-id="cd342-105">Указывает учетные данные безопасности для участника.</span><span class="sxs-lookup"><span data-stu-id="cd342-105">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="cd342-106">Эти учетные данные определяют контекст безопасности, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="cd342-106">These credentials define the security context that a task runs under.</span></span>

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

<span data-ttu-id="cd342-107">Элемент **Principal** определяется сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cd342-107">The **Principal** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cd342-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="cd342-108">Parent element</span></span>



| <span data-ttu-id="cd342-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="cd342-109">Element</span></span>                                                               | <span data-ttu-id="cd342-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="cd342-110">Derived from</span></span>                                                             | <span data-ttu-id="cd342-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cd342-111">Description</span></span>                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="cd342-112">**Субъекты**</span><span class="sxs-lookup"><span data-stu-id="cd342-112">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md) | [<span data-ttu-id="cd342-113">**принЦипалстипе**</span><span class="sxs-lookup"><span data-stu-id="cd342-113">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md) | <span data-ttu-id="cd342-114">Указывает субъекты безопасности, связанные с задачей.</span><span class="sxs-lookup"><span data-stu-id="cd342-114">Specifies the security principals associated with the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="cd342-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cd342-115">Child elements</span></span>



| <span data-ttu-id="cd342-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="cd342-116">Element</span></span>                                                                      | <span data-ttu-id="cd342-117">Тип</span><span class="sxs-lookup"><span data-stu-id="cd342-117">Type</span></span>                                                          | <span data-ttu-id="cd342-118">Описание</span><span class="sxs-lookup"><span data-stu-id="cd342-118">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd342-119">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="cd342-119">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md) | <span data-ttu-id="cd342-120">**string**</span><span class="sxs-lookup"><span data-stu-id="cd342-120">**string**</span></span>                                                    | <span data-ttu-id="cd342-121">Указывает имя участника, отображаемого в пользовательском интерфейсе планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="cd342-121">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                 |
| [<span data-ttu-id="cd342-122">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="cd342-122">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)         | <span data-ttu-id="cd342-123">**string**</span><span class="sxs-lookup"><span data-stu-id="cd342-123">**string**</span></span>                                                    | <span data-ttu-id="cd342-124">Указывает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="cd342-124">Specifies the identifier of the user group required to run tasks associated with the principal.</span></span><br/> |
| [<span data-ttu-id="cd342-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="cd342-125">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)     | [<span data-ttu-id="cd342-126">**logonType**</span><span class="sxs-lookup"><span data-stu-id="cd342-126">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md) | <span data-ttu-id="cd342-127">Указывает метод входа в систему безопасности, необходимый для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="cd342-127">Specifies the security logon method required to run those tasks associated with the principal.</span></span><br/>  |
| [<span data-ttu-id="cd342-128">**UserId**</span><span class="sxs-lookup"><span data-stu-id="cd342-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)           | <span data-ttu-id="cd342-129">**string**</span><span class="sxs-lookup"><span data-stu-id="cd342-129">**string**</span></span>                                                    | <span data-ttu-id="cd342-130">Указывает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="cd342-130">Specifies the user identifier required to run tasks associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="cd342-131">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cd342-131">Attributes</span></span>



| <span data-ttu-id="cd342-132">Имя</span><span class="sxs-lookup"><span data-stu-id="cd342-132">Name</span></span> | <span data-ttu-id="cd342-133">Тип</span><span class="sxs-lookup"><span data-stu-id="cd342-133">Type</span></span> | <span data-ttu-id="cd342-134">Описание</span><span class="sxs-lookup"><span data-stu-id="cd342-134">Description</span></span>                                        |
|------|------|----------------------------------------------------|
| <span data-ttu-id="cd342-135">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="cd342-135">Id</span></span>   | <span data-ttu-id="cd342-136">ID</span><span class="sxs-lookup"><span data-stu-id="cd342-136">ID</span></span>   | <span data-ttu-id="cd342-137">Идентификатор определения участника.</span><span class="sxs-lookup"><span data-stu-id="cd342-137">Identifier of the principal definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cd342-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd342-138">Remarks</span></span>

<span data-ttu-id="cd342-139">Для разработки сценариев учетные данные безопасности участника указываются с помощью объекта [**Principal**](principal.md) .</span><span class="sxs-lookup"><span data-stu-id="cd342-139">For scripting development, the security credentials for a principal are specified using the [**Principal**](principal.md) object.</span></span>

<span data-ttu-id="cd342-140">Для разработки на C++ учетные данные безопасности для субъекта задаются с помощью интерфейса [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) .</span><span class="sxs-lookup"><span data-stu-id="cd342-140">For C++ development, the security credentials for a principal are specified using the [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) interface.</span></span>

<span data-ttu-id="cd342-141">Перечисленные выше дочерние элементы определяются сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cd342-141">The child elements listed above are defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span> <span data-ttu-id="cd342-142">Сведения о последовательности для этих дочерних элементов см. в разделе [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md).</span><span class="sxs-lookup"><span data-stu-id="cd342-142">For sequencing information for these child elements, see [**principalType**](taskschedulerschema-principaltype-complextype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cd342-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="cd342-143">Examples</span></span>

<span data-ttu-id="cd342-144">Следующий XML-код определяет участника с идентификатором пользователя.</span><span class="sxs-lookup"><span data-stu-id="cd342-144">The following XML defines a principal with a user identifier.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



<span data-ttu-id="cd342-145">Следующий XML-код определяет участника с идентификатором группы.</span><span class="sxs-lookup"><span data-stu-id="cd342-145">The following XML defines a principal with a group identifier.</span></span>


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="cd342-146">Требования</span><span class="sxs-lookup"><span data-stu-id="cd342-146">Requirements</span></span>



| <span data-ttu-id="cd342-147">Требование</span><span class="sxs-lookup"><span data-stu-id="cd342-147">Requirement</span></span> | <span data-ttu-id="cd342-148">Значение</span><span class="sxs-lookup"><span data-stu-id="cd342-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd342-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd342-149">Minimum supported client</span></span><br/> | <span data-ttu-id="cd342-150">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd342-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cd342-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd342-151">Minimum supported server</span></span><br/> | <span data-ttu-id="cd342-152">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd342-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd342-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd342-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd342-154">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="cd342-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





