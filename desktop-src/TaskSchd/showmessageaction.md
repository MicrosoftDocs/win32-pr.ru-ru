---
title: Объект Шовмессажеактион
description: Для сценариев представляет действие, которое отображает окно сообщения при активации задачи.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- планировщик задач объекта Шовмессажеактион
- Планировщик задач объекта Шовмессажеактион, описание
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415105"
---
# <a name="showmessageaction-object"></a><span data-ttu-id="2b1e4-105">Объект Шовмессажеактион</span><span class="sxs-lookup"><span data-stu-id="2b1e4-105">ShowMessageAction object</span></span>

<span data-ttu-id="2b1e4-106">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2b1e4-106">\[This object is no longer supported.</span></span> <span data-ttu-id="2b1e4-107">Для отображения сообщения в сеансе пользователя можно использовать Иексекактион с функцией Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) .\]</span><span class="sxs-lookup"><span data-stu-id="2b1e4-107">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="2b1e4-108">Для сценариев представляет действие, которое отображает окно сообщения при активации задачи.</span><span class="sxs-lookup"><span data-stu-id="2b1e4-108">For scripting, represents an action that shows a message box when a task is activated.</span></span>

## <a name="members"></a><span data-ttu-id="2b1e4-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="2b1e4-109">Members</span></span>

<span data-ttu-id="2b1e4-110">Объект **шовмессажеактион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2b1e4-110">The **ShowMessageAction** object has these types of members:</span></span>

-   [<span data-ttu-id="2b1e4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b1e4-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b1e4-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b1e4-112">Properties</span></span>

<span data-ttu-id="2b1e4-113">Объект **шовмессажеактион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2b1e4-113">The **ShowMessageAction** object has these properties.</span></span>



| <span data-ttu-id="2b1e4-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="2b1e4-114">Property</span></span>                                                        | <span data-ttu-id="2b1e4-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="2b1e4-115">Access type</span></span>           | <span data-ttu-id="2b1e4-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2b1e4-116">Description</span></span>                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b1e4-117">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="2b1e4-117">**Id**</span></span>](action-id.md)<br/>                              | <span data-ttu-id="2b1e4-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2b1e4-118">Read/write</span></span><br/> | <span data-ttu-id="2b1e4-119">Наследуется от объекта [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="2b1e4-119">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="2b1e4-120">Возвращает или задает идентификатор действия.</span><span class="sxs-lookup"><span data-stu-id="2b1e4-120">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="2b1e4-121">**MessageBody**</span><span class="sxs-lookup"><span data-stu-id="2b1e4-121">**MessageBody**</span></span>](showmessageaction-messagebody.md)<br/> | <span data-ttu-id="2b1e4-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2b1e4-122">Read/write</span></span><br/> | <span data-ttu-id="2b1e4-123">Возвращает или задает текст сообщения, отображаемого в тексте окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="2b1e4-123">Gets or sets the message text that is displayed in the body of the message box.</span></span><br/>                |
| [<span data-ttu-id="2b1e4-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="2b1e4-124">**Title**</span></span>](showmessageaction-title.md)<br/>             | <span data-ttu-id="2b1e4-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2b1e4-125">Read/write</span></span><br/> | <span data-ttu-id="2b1e4-126">Возвращает или задает заголовок окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="2b1e4-126">Gets or sets the title of the message box.</span></span><br/>                                                     |
| [<span data-ttu-id="2b1e4-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2b1e4-127">**Type**</span></span>](action-type.md)<br/>                          | <span data-ttu-id="2b1e4-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e4-128">Read-only</span></span><br/>  | <span data-ttu-id="2b1e4-129">Наследуется от объекта [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="2b1e4-129">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="2b1e4-130">Возвращает тип действия.</span><span class="sxs-lookup"><span data-stu-id="2b1e4-130">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="2b1e4-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b1e4-131">Remarks</span></span>

<span data-ttu-id="2b1e4-132">Для задачи, которая содержит действие «окно сообщения», появится окно сообщения, если задача активирована, а задача имеет интерактивный тип входа в систему.</span><span class="sxs-lookup"><span data-stu-id="2b1e4-132">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="2b1e4-133">Чтобы установить для параметра Тип входа в интерактивный режим, укажите значение 3 (**\_ \_ Интерактивный \_ маркер входа в систему**) или 4 (**\_ \_ Группа входа** в систему) в свойстве [**LogonType**](principal-logontype.md) участника задачи или в параметре *LogonType* [**таскфолдер. регистертаск**](taskfolder-registertask.md) или [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="2b1e4-133">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="2b1e4-134">При чтении или записи собственного XML-кода для задачи действие окна сообщения указывается с помощью элемента [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="2b1e4-134">When reading or writing your own XML for a task, a message box action is specified using the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="2b1e4-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="2b1e4-135">Examples</span></span>

<span data-ttu-id="2b1e4-136">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [Пример окна сообщения (сценарии)](/previous-versions//aa381916(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b1e4-136">For more information and example code for this scripting object, see [Message Box Example (Scripting)](/previous-versions//aa381916(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b1e4-137">Требования</span><span class="sxs-lookup"><span data-stu-id="2b1e4-137">Requirements</span></span>



| <span data-ttu-id="2b1e4-138">Требование</span><span class="sxs-lookup"><span data-stu-id="2b1e4-138">Requirement</span></span> | <span data-ttu-id="2b1e4-139">Значение</span><span class="sxs-lookup"><span data-stu-id="2b1e4-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1e4-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b1e4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2b1e4-141">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b1e4-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2b1e4-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b1e4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2b1e4-143">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2b1e4-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b1e4-144">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2b1e4-144">End of client support</span></span><br/>    | <span data-ttu-id="2b1e4-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b1e4-145">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="2b1e4-146">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="2b1e4-146">End of server support</span></span><br/>    | <span data-ttu-id="2b1e4-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2b1e4-147">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="2b1e4-148">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="2b1e4-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b1e4-149"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2b1e4-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2b1e4-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2b1e4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b1e4-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b1e4-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

