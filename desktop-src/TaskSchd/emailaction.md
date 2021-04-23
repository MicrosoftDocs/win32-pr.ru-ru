---
title: Объект EmailAction
description: Объект скрипта, представляющий действие, которое отправляет сообщение электронной почты.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- планировщик задач объекта Емаилактион
- Планировщик задач объекта Емаилактион, описание
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a339a1549b76f61499b7192a48edc7c1b86a6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892509"
---
# <a name="emailaction-object"></a><span data-ttu-id="ec45f-105">Объект EmailAction</span><span class="sxs-lookup"><span data-stu-id="ec45f-105">EmailAction object</span></span>

<span data-ttu-id="ec45f-106">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ec45f-106">\[This object is no longer supported.</span></span> <span data-ttu-id="ec45f-107">Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.\]</span><span class="sxs-lookup"><span data-stu-id="ec45f-107">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="ec45f-108">Объект скрипта, представляющий действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ec45f-108">Scripting object that represents an action that sends an email message.</span></span>

## <a name="members"></a><span data-ttu-id="ec45f-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="ec45f-109">Members</span></span>

<span data-ttu-id="ec45f-110">Объект **емаилактион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ec45f-110">The **EmailAction** object has these types of members:</span></span>

-   [<span data-ttu-id="ec45f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec45f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec45f-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec45f-112">Properties</span></span>

<span data-ttu-id="ec45f-113">Объект **емаилактион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ec45f-113">The **EmailAction** object has these properties.</span></span>



| <span data-ttu-id="ec45f-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="ec45f-114">Property</span></span>                                                    | <span data-ttu-id="ec45f-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="ec45f-115">Access type</span></span>           | <span data-ttu-id="ec45f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ec45f-116">Description</span></span>                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec45f-117">**Вложения**</span><span class="sxs-lookup"><span data-stu-id="ec45f-117">**Attachments**</span></span>](emailaction-attachments.md)<br/>   | <span data-ttu-id="ec45f-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ec45f-118">Read/write</span></span><br/> | <span data-ttu-id="ec45f-119">Возвращает или задает массив вложений, отправляемых с сообщением электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ec45f-119">Gets or sets an array of attachments that is sent with the email message.</span></span><br/>                      |
| [<span data-ttu-id="ec45f-120">**Скрытая копия**</span><span class="sxs-lookup"><span data-stu-id="ec45f-120">**Bcc**</span></span>](emailaction-bcc.md)<br/>                   | <span data-ttu-id="ec45f-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ec45f-121">Read/write</span></span><br/> | <span data-ttu-id="ec45f-122">Возвращает или задает адрес электронной почты или адреса, которые нужно отправить в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ec45f-122">Gets or sets the email address or addresses that you want to Bcc in the email message.</span></span><br/>         |
| [<span data-ttu-id="ec45f-123">**Текст**</span><span class="sxs-lookup"><span data-stu-id="ec45f-123">**Body**</span></span>](emailaction-body.md)<br/>                 | <span data-ttu-id="ec45f-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ec45f-124">Read/write</span></span><br/> | <span data-ttu-id="ec45f-125">Возвращает или задает текст сообщения электронной почты, содержащего сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ec45f-125">Gets or sets the body of the email that contains the email message.</span></span><br/>                            |
| [<span data-ttu-id="ec45f-126">**Кому**</span><span class="sxs-lookup"><span data-stu-id="ec45f-126">**Cc**</span></span>](emailaction-cc.md)<br/>                     | <span data-ttu-id="ec45f-127">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ec45f-127">Read/write</span></span><br/> | <span data-ttu-id="ec45f-128">Возвращает или задает адрес электронной почты или адреса, которые вы хотите отправить в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ec45f-128">Gets or sets the email address or addresses that you want to Cc in the email message.</span></span><br/>          |
| [<span data-ttu-id="ec45f-129">**Исходный тип**</span><span class="sxs-lookup"><span data-stu-id="ec45f-129">**From**</span></span>](emailaction-from.md)<br/>                 | <span data-ttu-id="ec45f-130">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ec45f-130">Read/write</span></span><br/> | <span data-ttu-id="ec45f-131">Возвращает или задает адрес электронной почты, по которому вы хотите отправить электронное письмо.</span><span class="sxs-lookup"><span data-stu-id="ec45f-131">Gets or sets the email address that you want to send the email from.</span></span><br/>                           |
| [<span data-ttu-id="ec45f-132">**хеадерфиелдс**</span><span class="sxs-lookup"><span data-stu-id="ec45f-132">**HeaderFields**</span></span>](emailaction-headerfields.md)<br/> | <span data-ttu-id="ec45f-133">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ec45f-133">Read/write</span></span><br/> | <span data-ttu-id="ec45f-134">Возвращает или задает сведения о заголовке сообщения электронной почты, которое необходимо отправить.</span><span class="sxs-lookup"><span data-stu-id="ec45f-134">Gets or sets the header information in the email that you want to send.</span></span><br/>                        |
| [<span data-ttu-id="ec45f-135">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="ec45f-135">**Id**</span></span>](action-id.md)<br/>                          | <span data-ttu-id="ec45f-136">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ec45f-136">Read/write</span></span><br/> | <span data-ttu-id="ec45f-137">Наследуется от объекта [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="ec45f-137">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="ec45f-138">Возвращает или задает идентификатор действия.</span><span class="sxs-lookup"><span data-stu-id="ec45f-138">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="ec45f-139">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="ec45f-139">**ReplyTo**</span></span>](emailaction-replyto.md)<br/>           | <span data-ttu-id="ec45f-140">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ec45f-140">Read/write</span></span><br/> | <span data-ttu-id="ec45f-141">Возвращает или задает адрес электронной почты, на который вы хотите ответить.</span><span class="sxs-lookup"><span data-stu-id="ec45f-141">Gets or sets the email address that you want to reply to.</span></span><br/>                                      |
| [<span data-ttu-id="ec45f-142">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="ec45f-142">**Server**</span></span>](emailaction-server.md)<br/>             | <span data-ttu-id="ec45f-143">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ec45f-143">Read/write</span></span><br/> | <span data-ttu-id="ec45f-144">Возвращает или задает имя сервера, который используется для отправки электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ec45f-144">Gets or sets the name of the server that you use to send email from.</span></span><br/>                           |
| [<span data-ttu-id="ec45f-145">**Субъект**</span><span class="sxs-lookup"><span data-stu-id="ec45f-145">**Subject**</span></span>](emailaction-subject.md)<br/>           | <span data-ttu-id="ec45f-146">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ec45f-146">Read/write</span></span><br/> | <span data-ttu-id="ec45f-147">Возвращает или задает тему сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ec45f-147">Gets or sets the subject of the email message.</span></span><br/>                                                 |
| [<span data-ttu-id="ec45f-148">**Кому**</span><span class="sxs-lookup"><span data-stu-id="ec45f-148">**To**</span></span>](emailaction-to.md)<br/>                     | <span data-ttu-id="ec45f-149">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ec45f-149">Read/write</span></span><br/> | <span data-ttu-id="ec45f-150">Возвращает или задает адрес электронной почты или адреса, по которым необходимо отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="ec45f-150">Gets or sets the email address or addresses that you want to send the email to.</span></span><br/>                |
| [<span data-ttu-id="ec45f-151">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ec45f-151">**Type**</span></span>](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | <span data-ttu-id="ec45f-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec45f-152">Read-only</span></span><br/>  | <span data-ttu-id="ec45f-153">Наследуется от объекта [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="ec45f-153">Inherited from [**Action**](action.md) object.</span></span> <span data-ttu-id="ec45f-154">Возвращает тип действия.</span><span class="sxs-lookup"><span data-stu-id="ec45f-154">Gets the type of the action.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="ec45f-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec45f-155">Remarks</span></span>

<span data-ttu-id="ec45f-156">Действие электронной почты должно иметь допустимое значение для свойств [**сервера**](emailaction-server.md), [**из**](emailaction-from.md), и [**to**](emailaction-to.md) или [**CC**](emailaction-cc.md) , чтобы задача была зарегистрирована и выполнена правильно.</span><span class="sxs-lookup"><span data-stu-id="ec45f-156">The email action must have a valid value for the [**Server**](emailaction-server.md), [**From**](emailaction-from.md), and [**To**](emailaction-to.md) or [**Cc**](emailaction-cc.md) properties for the task to register and run correctly.</span></span>

<span data-ttu-id="ec45f-157">При чтении или записи собственного XML-кода для задачи действие электронной почты задается с помощью элемента [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="ec45f-157">When reading or writing your own XML for a task, an email action is specified using the [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="ec45f-158">Примеры</span><span class="sxs-lookup"><span data-stu-id="ec45f-158">Examples</span></span>

<span data-ttu-id="ec45f-159">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера события (создание сценариев)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ec45f-159">For more information and example code for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec45f-160">Требования</span><span class="sxs-lookup"><span data-stu-id="ec45f-160">Requirements</span></span>



| <span data-ttu-id="ec45f-161">Требование</span><span class="sxs-lookup"><span data-stu-id="ec45f-161">Requirement</span></span> | <span data-ttu-id="ec45f-162">Значение</span><span class="sxs-lookup"><span data-stu-id="ec45f-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec45f-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec45f-163">Minimum supported client</span></span><br/> | <span data-ttu-id="ec45f-164">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec45f-164">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ec45f-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec45f-165">Minimum supported server</span></span><br/> | <span data-ttu-id="ec45f-166">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ec45f-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec45f-167">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ec45f-167">End of client support</span></span><br/>    | <span data-ttu-id="ec45f-168">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ec45f-168">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="ec45f-169">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="ec45f-169">End of server support</span></span><br/>    | <span data-ttu-id="ec45f-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec45f-170">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="ec45f-171">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ec45f-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec45f-172"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec45f-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec45f-173">DLL</span><span class="sxs-lookup"><span data-stu-id="ec45f-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec45f-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec45f-174"><dt>Taskschd.dll</dt></span></span> </dl> |



 

