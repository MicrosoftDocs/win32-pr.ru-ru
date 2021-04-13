---
title: Регистратионинфо (taskType), элемент
description: Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- планировщик задач сведения о регистрации, XML-элемент
- планировщик задач элемента Регистратионинфо
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491676"
---
# <a name="registrationinfo-tasktype-element"></a><span data-ttu-id="65d9d-105">Регистратионинфо (taskType), элемент</span><span class="sxs-lookup"><span data-stu-id="65d9d-105">RegistrationInfo (taskType) Element</span></span>

<span data-ttu-id="65d9d-106">Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="65d9d-106">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

<span data-ttu-id="65d9d-107">Элемент **регистратионинфо** определяется сложным типом [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="65d9d-107">The **RegistrationInfo** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="65d9d-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="65d9d-108">Parent element</span></span>



| <span data-ttu-id="65d9d-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="65d9d-109">Element</span></span>                                          | <span data-ttu-id="65d9d-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="65d9d-110">Derived from</span></span>                                                 | <span data-ttu-id="65d9d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="65d9d-111">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="65d9d-112">**Задача**</span><span class="sxs-lookup"><span data-stu-id="65d9d-112">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="65d9d-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="65d9d-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="65d9d-114">Определяет задачу, выполняемую службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="65d9d-114">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="65d9d-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="65d9d-115">Child elements</span></span>



| <span data-ttu-id="65d9d-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="65d9d-116">Element</span></span>                                                                                                                  | <span data-ttu-id="65d9d-117">Тип</span><span class="sxs-lookup"><span data-stu-id="65d9d-117">Type</span></span>     | <span data-ttu-id="65d9d-118">Описание</span><span class="sxs-lookup"><span data-stu-id="65d9d-118">Description</span></span>                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65d9d-119">**Автор (Регистратионинфотипе)**</span><span class="sxs-lookup"><span data-stu-id="65d9d-119">**Author (registrationInfoType)**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="65d9d-120">строка</span><span class="sxs-lookup"><span data-stu-id="65d9d-120">string</span></span>   | <span data-ttu-id="65d9d-121">Указывает автора задачи.</span><span class="sxs-lookup"><span data-stu-id="65d9d-121">Specifies the author of the task.</span></span><br/>                                                                              |
| [<span data-ttu-id="65d9d-122">**Дата (Регистратионинфотипе)**</span><span class="sxs-lookup"><span data-stu-id="65d9d-122">**Date (registrationInfoType)**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="65d9d-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="65d9d-123">dateTime</span></span> | <span data-ttu-id="65d9d-124">Указывает дату и время регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="65d9d-124">Specifies the date and time when the task is registered.</span></span><br/>                                                       |
| [<span data-ttu-id="65d9d-125">**Описание (Регистратионинфотипе)**</span><span class="sxs-lookup"><span data-stu-id="65d9d-125">**Description (registrationInfoType)**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="65d9d-126">строка</span><span class="sxs-lookup"><span data-stu-id="65d9d-126">string</span></span>   | <span data-ttu-id="65d9d-127">Указание описания задачи.</span><span class="sxs-lookup"><span data-stu-id="65d9d-127">Specifies the description of the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="65d9d-128">**Документация (Регистратионинфотипе)**</span><span class="sxs-lookup"><span data-stu-id="65d9d-128">**Documentation (registrationInfoType)**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="65d9d-129">строка</span><span class="sxs-lookup"><span data-stu-id="65d9d-129">string</span></span>   | <span data-ttu-id="65d9d-130">Указывает любую дополнительную документацию для задачи.</span><span class="sxs-lookup"><span data-stu-id="65d9d-130">Specifies any additional documentation for the task.</span></span><br/>                                                           |
| [<span data-ttu-id="65d9d-131">**SecurityDescriptor (Регистратионинфотипе)**</span><span class="sxs-lookup"><span data-stu-id="65d9d-131">**SecurityDescriptor (registrationInfoType)**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="65d9d-132">строка</span><span class="sxs-lookup"><span data-stu-id="65d9d-132">string</span></span>   | <span data-ttu-id="65d9d-133">Указывает дескриптор безопасности задачи.</span><span class="sxs-lookup"><span data-stu-id="65d9d-133">Specifies the security descriptor of the task.</span></span><br/>                                                                 |
| [<span data-ttu-id="65d9d-134">**Источник (Регистратионинфотипе)**</span><span class="sxs-lookup"><span data-stu-id="65d9d-134">**Source (registrationInfoType)**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="65d9d-135">строка</span><span class="sxs-lookup"><span data-stu-id="65d9d-135">string</span></span>   | <span data-ttu-id="65d9d-136">Указывает, откуда поступила задача.</span><span class="sxs-lookup"><span data-stu-id="65d9d-136">Specifies where the task originated from.</span></span> <span data-ttu-id="65d9d-137">Например, из компонента, службы, приложения или пользователя.</span><span class="sxs-lookup"><span data-stu-id="65d9d-137">For example, from a component, a service, an application, or a user.</span></span><br/> |
| [<span data-ttu-id="65d9d-138">**URI (Регистратионинфотипе)**</span><span class="sxs-lookup"><span data-stu-id="65d9d-138">**URI (registrationInfoType)**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="65d9d-139">anyURI</span><span class="sxs-lookup"><span data-stu-id="65d9d-139">anyURI</span></span>   | <span data-ttu-id="65d9d-140">Указывает универсальный код ресурса (URI) задачи.</span><span class="sxs-lookup"><span data-stu-id="65d9d-140">Specifies the URI of the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="65d9d-141">**Версия (Регистратионинфотипе)**</span><span class="sxs-lookup"><span data-stu-id="65d9d-141">**Version (registrationInfoType)**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="65d9d-142">строка</span><span class="sxs-lookup"><span data-stu-id="65d9d-142">string</span></span>   | <span data-ttu-id="65d9d-143">Указывает номер версии задачи.</span><span class="sxs-lookup"><span data-stu-id="65d9d-143">Specifies the version number of the task.</span></span><br/>                                                                      |



## <a name="remarks"></a><span data-ttu-id="65d9d-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65d9d-144">Remarks</span></span>

<span data-ttu-id="65d9d-145">Для разработки сценариев сведения о регистрации задачи указываются с помощью свойства [**таскдефинитион. регистратионинфо**](taskdefinition-registrationinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="65d9d-145">For scripting development, the registration information of a task is specified using the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property.</span></span>

<span data-ttu-id="65d9d-146">Для разработки на C++ сведения о регистрации задачи указываются с помощью [**Свойства регистратионинфо объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span><span class="sxs-lookup"><span data-stu-id="65d9d-146">For C++ development, the registration information of a task is specified using the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="65d9d-147">Требования</span><span class="sxs-lookup"><span data-stu-id="65d9d-147">Requirements</span></span>



| <span data-ttu-id="65d9d-148">Требование</span><span class="sxs-lookup"><span data-stu-id="65d9d-148">Requirement</span></span> | <span data-ttu-id="65d9d-149">Значение</span><span class="sxs-lookup"><span data-stu-id="65d9d-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65d9d-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65d9d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="65d9d-151">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65d9d-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65d9d-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65d9d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="65d9d-153">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65d9d-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65d9d-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65d9d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d9d-155">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="65d9d-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="65d9d-156">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="65d9d-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





