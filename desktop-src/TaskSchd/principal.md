---
title: Объект Principal
description: Объект скрипта, предоставляющий учетные данные безопасности участника.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Основной объект планировщик задач
- Объект Principal планировщик задач, описание
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891677"
---
# <a name="principal-object"></a><span data-ttu-id="99cfa-105">Объект Principal</span><span class="sxs-lookup"><span data-stu-id="99cfa-105">Principal object</span></span>

<span data-ttu-id="99cfa-106">Объект скрипта, предоставляющий учетные данные безопасности участника.</span><span class="sxs-lookup"><span data-stu-id="99cfa-106">Scripting object that provides the security credentials for a principal.</span></span> <span data-ttu-id="99cfa-107">Эти учетные данные безопасности определяют контекст безопасности для задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="99cfa-107">These security credentials define the security context for the tasks that are associated with the principal.</span></span>

## <a name="members"></a><span data-ttu-id="99cfa-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="99cfa-108">Members</span></span>

<span data-ttu-id="99cfa-109">Объект **Principal** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="99cfa-109">The **Principal** object has these types of members:</span></span>

-   [<span data-ttu-id="99cfa-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="99cfa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99cfa-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="99cfa-111">Properties</span></span>

<span data-ttu-id="99cfa-112">Объект **Principal** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="99cfa-112">The **Principal** object has these properties.</span></span>



| <span data-ttu-id="99cfa-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="99cfa-113">Property</span></span>                                                | <span data-ttu-id="99cfa-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="99cfa-114">Access type</span></span>           | <span data-ttu-id="99cfa-115">Описание</span><span class="sxs-lookup"><span data-stu-id="99cfa-115">Description</span></span>                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99cfa-116">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="99cfa-116">**DisplayName**</span></span>](principal-displayname.md)<br/> | <span data-ttu-id="99cfa-117">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="99cfa-117">Read/write</span></span><br/> | <span data-ttu-id="99cfa-118">Возвращает или задает имя участника, отображаемого в пользовательском интерфейсе планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="99cfa-118">Gets or sets the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                                                                |
| [<span data-ttu-id="99cfa-119">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="99cfa-119">**GroupId**</span></span>](principal-groupid.md)<br/>         | <span data-ttu-id="99cfa-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="99cfa-120">Read/write</span></span><br/> | <span data-ttu-id="99cfa-121">Возвращает или задает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="99cfa-121">Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span><br/>                           |
| [<span data-ttu-id="99cfa-122">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="99cfa-122">**Id**</span></span>](principal-id.md)<br/>                   | <span data-ttu-id="99cfa-123">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="99cfa-123">Read/write</span></span><br/> | <span data-ttu-id="99cfa-124">Возвращает или задает идентификатор участника.</span><span class="sxs-lookup"><span data-stu-id="99cfa-124">Gets or sets the identifier of the principal.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="99cfa-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="99cfa-125">**LogonType**</span></span>](principal-logontype.md)<br/>     | <span data-ttu-id="99cfa-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="99cfa-126">Read/write</span></span><br/> | <span data-ttu-id="99cfa-127">Возвращает или задает метод входа в систему безопасности, необходимый для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="99cfa-127">Gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span><br/>                                  |
| [<span data-ttu-id="99cfa-128">**RunLevel**</span><span class="sxs-lookup"><span data-stu-id="99cfa-128">**RunLevel**</span></span>](principal-runlevel.md)<br/>       | <span data-ttu-id="99cfa-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="99cfa-129">Read/write</span></span><br/> | <span data-ttu-id="99cfa-130">Возвращает или задает идентификатор, который используется для указания уровня привилегий, необходимого для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="99cfa-130">Gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="99cfa-131">**UserId**</span><span class="sxs-lookup"><span data-stu-id="99cfa-131">**UserId**</span></span>](principal-userid.md)<br/>           | <span data-ttu-id="99cfa-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="99cfa-132">Read/write</span></span><br/> | <span data-ttu-id="99cfa-133">Возвращает или задает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="99cfa-133">Gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="99cfa-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99cfa-134">Remarks</span></span>

<span data-ttu-id="99cfa-135">При указании учетной записи не забывайте правильно использовать двойную обратную косую черту в коде, чтобы указать домен и имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="99cfa-135">When specifying an account, remember to properly use the double backslash in code to specify the domain and user name.</span></span> <span data-ttu-id="99cfa-136">Например, используйте домен \\ \\ имя_пользователя, чтобы указать значение для свойства [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="99cfa-136">For example, use DOMAIN\\\\UserName to specify a value for the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

<span data-ttu-id="99cfa-137">При чтении или записи XML для задачи учетные данные безопасности участника указываются в элементе [**Principal**](taskschedulerschema-principal-principaltype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="99cfa-137">When reading or writing XML for a task, the security credentials for a principal are specified in the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="99cfa-138">Если задача зарегистрирована с помощью средства командной строки at.exe и этот объект используется для получения сведений о задаче, свойство [**LogonType**](principal-logontype.md) возвратит 0, [**а свойство**](principal-runlevel.md) [**UserID**](principal-userid.md) возвратит значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="99cfa-138">If a task is registered using the at.exe command line tool, and this object is used to retrieve information about the task, then the [**LogonType**](principal-logontype.md) property will return 0, the [**RunLevel**](principal-runlevel.md) property will return 0, and the [**UserId**](principal-userid.md) property will return Nothing.</span></span>

## <a name="examples"></a><span data-ttu-id="99cfa-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="99cfa-139">Examples</span></span>

<span data-ttu-id="99cfa-140">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="99cfa-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99cfa-141">Требования</span><span class="sxs-lookup"><span data-stu-id="99cfa-141">Requirements</span></span>



| <span data-ttu-id="99cfa-142">Требование</span><span class="sxs-lookup"><span data-stu-id="99cfa-142">Requirement</span></span> | <span data-ttu-id="99cfa-143">Значение</span><span class="sxs-lookup"><span data-stu-id="99cfa-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99cfa-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99cfa-144">Minimum supported client</span></span><br/> | <span data-ttu-id="99cfa-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99cfa-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="99cfa-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99cfa-146">Minimum supported server</span></span><br/> | <span data-ttu-id="99cfa-147">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99cfa-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99cfa-148">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="99cfa-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="99cfa-149"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="99cfa-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="99cfa-150">DLL</span><span class="sxs-lookup"><span data-stu-id="99cfa-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99cfa-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99cfa-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





