---
title: Элемент SendEmail (actionGroup)
description: Представляет действие, которое отправляет сообщение электронной почты.
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- планировщик задач элемента SendEmail
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989107"
---
# <a name="sendemail-actiongroup-element"></a><span data-ttu-id="8c2a3-104">Элемент SendEmail (actionGroup)</span><span class="sxs-lookup"><span data-stu-id="8c2a3-104">SendEmail (actionGroup) Element</span></span>

<span data-ttu-id="8c2a3-105">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-105">Represents an action that sends an email message.</span></span>

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

<span data-ttu-id="8c2a3-106">Элемент **SendEmail** определяется параметром [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="8c2a3-106">The **SendEmail** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="8c2a3-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="8c2a3-107">Parent element</span></span>



| <span data-ttu-id="8c2a3-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="8c2a3-108">Element</span></span>                                                         | <span data-ttu-id="8c2a3-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="8c2a3-109">Derived from</span></span>                                                       | <span data-ttu-id="8c2a3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8c2a3-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="8c2a3-111">**Действия**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="8c2a3-112">**актионстипе**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="8c2a3-113">Содержит действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="8c2a3-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8c2a3-114">Child elements</span></span>



| <span data-ttu-id="8c2a3-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="8c2a3-115">Element</span></span>                                                                        | <span data-ttu-id="8c2a3-116">Тип</span><span class="sxs-lookup"><span data-stu-id="8c2a3-116">Type</span></span>                                                                         | <span data-ttu-id="8c2a3-117">Описание</span><span class="sxs-lookup"><span data-stu-id="8c2a3-117">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c2a3-118">**Вложения**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-118">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="8c2a3-119">**аттачментстипе**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-119">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="8c2a3-120">Указывает список вложений в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-120">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="8c2a3-121">**Скрытая копия**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-121">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="8c2a3-122">**string**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-122">**string**</span></span>                                                                   | <span data-ttu-id="8c2a3-123">Указывает адреса электронной почты, используемые в строке СК сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-123">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="8c2a3-124">**Текст**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-124">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="8c2a3-125">**string**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-125">**string**</span></span>                                                                   | <span data-ttu-id="8c2a3-126">Задает текст в тексте сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-126">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="8c2a3-127">**Кому**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-127">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="8c2a3-128">**string**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-128">**string**</span></span>                                                                   | <span data-ttu-id="8c2a3-129">Указывает адреса электронной почты, используемые в строке CC сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-129">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="8c2a3-130">**Исходный тип**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-130">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="8c2a3-131">**string**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-131">**string**</span></span>                                                                   | <span data-ttu-id="8c2a3-132">Указывает адрес электронной почты отправителя.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-132">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="8c2a3-133">**хеадерфиелдс**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-133">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="8c2a3-134">**хеадерфиелдстипе**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-134">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="8c2a3-135">Задает поля заголовка и их значения, используемые в заголовке сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-135">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="8c2a3-136">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-136">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="8c2a3-137">**string**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-137">**string**</span></span>                                                                   | <span data-ttu-id="8c2a3-138">Указывает адреса электронной почты, на которые вы ответили в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-138">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="8c2a3-139">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-139">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="8c2a3-140">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-140">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="8c2a3-141">Указывает сервер электронной почты, используемый для отправки сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-141">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="8c2a3-142">**Субъект**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-142">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="8c2a3-143">**string**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-143">**string**</span></span>                                                                   | <span data-ttu-id="8c2a3-144">Указывает тему сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-144">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="8c2a3-145">**Кому**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-145">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="8c2a3-146">**string**</span><span class="sxs-lookup"><span data-stu-id="8c2a3-146">**string**</span></span>                                                                   | <span data-ttu-id="8c2a3-147">Указывает адреса электронной почты, на которые будет отправлено сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-147">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="8c2a3-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c2a3-148">Remarks</span></span>

<span data-ttu-id="8c2a3-149">Сведения о разработке на языке C++ см. в разделе интерфейс [**иемаилактион**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) .</span><span class="sxs-lookup"><span data-stu-id="8c2a3-149">For C++ development, see the [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) interface.</span></span>

<span data-ttu-id="8c2a3-150">Сведения о разработке сценариев см. в разделе объект [**емаилактион**](emailaction.md) .</span><span class="sxs-lookup"><span data-stu-id="8c2a3-150">For script development, see the [**EmailAction**](emailaction.md) object.</span></span>

<span data-ttu-id="8c2a3-151">**Windows 8 и Windows Server 2012:** Этот элемент был удален.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-151">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="8c2a3-152">Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.</span><span class="sxs-lookup"><span data-stu-id="8c2a3-152">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.</span></span>

## <a name="examples"></a><span data-ttu-id="8c2a3-153">Примеры</span><span class="sxs-lookup"><span data-stu-id="8c2a3-153">Examples</span></span>

<span data-ttu-id="8c2a3-154">Полный пример XML-кода для задачи, указывающей действие электронной почты, см. в разделе [пример триггера события (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8c2a3-154">For a complete example of the XML for a task that specifies an email action, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c2a3-155">Требования</span><span class="sxs-lookup"><span data-stu-id="8c2a3-155">Requirements</span></span>



| <span data-ttu-id="8c2a3-156">Требование</span><span class="sxs-lookup"><span data-stu-id="8c2a3-156">Requirement</span></span> | <span data-ttu-id="8c2a3-157">Значение</span><span class="sxs-lookup"><span data-stu-id="8c2a3-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8c2a3-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c2a3-158">Minimum supported client</span></span><br/> | <span data-ttu-id="8c2a3-159">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c2a3-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8c2a3-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c2a3-160">Minimum supported server</span></span><br/> | <span data-ttu-id="8c2a3-161">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c2a3-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8c2a3-162">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8c2a3-162">End of client support</span></span><br/>    | <span data-ttu-id="8c2a3-163">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c2a3-163">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="8c2a3-164">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8c2a3-164">End of server support</span></span><br/>    | <span data-ttu-id="8c2a3-165">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8c2a3-165">Windows Server 2008 R2</span></span><br/>                    |



 

