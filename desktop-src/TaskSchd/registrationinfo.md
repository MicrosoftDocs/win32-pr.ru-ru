---
title: Объект Регистратионинфо
description: Объект скрипта, предоставляющий административные данные, которые можно использовать для описания задачи.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- сведения о регистрации планировщик задач, объект
- планировщик задач объекта Регистратионинфо
- Планировщик задач объекта Регистратионинфо, описание
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071354"
---
# <a name="registrationinfo-object"></a><span data-ttu-id="639cb-106">Объект Регистратионинфо</span><span class="sxs-lookup"><span data-stu-id="639cb-106">RegistrationInfo object</span></span>

<span data-ttu-id="639cb-107">Объект скрипта, предоставляющий административные данные, которые можно использовать для описания задачи.</span><span class="sxs-lookup"><span data-stu-id="639cb-107">Scripting object that provides the administrative information that can be used to describe the task.</span></span> <span data-ttu-id="639cb-108">Эти сведения включают в себя такие сведения, как описание задачи, автора задачи, Дата регистрации задачи и дескриптор безопасности задачи.</span><span class="sxs-lookup"><span data-stu-id="639cb-108">This information includes details such as a description of the task, the author of the task, the date the task is registered, and the security descriptor of the task.</span></span>

## <a name="members"></a><span data-ttu-id="639cb-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="639cb-109">Members</span></span>

<span data-ttu-id="639cb-110">Объект **регистратионинфо** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="639cb-110">The **RegistrationInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="639cb-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="639cb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="639cb-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="639cb-112">Properties</span></span>

<span data-ttu-id="639cb-113">Объект **регистратионинфо** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="639cb-113">The **RegistrationInfo** object has these properties.</span></span>



| <span data-ttu-id="639cb-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="639cb-114">Property</span></span>                                                                     | <span data-ttu-id="639cb-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="639cb-115">Access type</span></span>           | <span data-ttu-id="639cb-116">Описание</span><span class="sxs-lookup"><span data-stu-id="639cb-116">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="639cb-117">**Автор**</span><span class="sxs-lookup"><span data-stu-id="639cb-117">**Author**</span></span>](registrationinfo-author.md)<br/>                         | <span data-ttu-id="639cb-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="639cb-118">Read/write</span></span><br/> | <span data-ttu-id="639cb-119">Возвращает или задает автора задачи.</span><span class="sxs-lookup"><span data-stu-id="639cb-119">Gets or sets the author of the task.</span></span><br/>                                                                                            |
| [<span data-ttu-id="639cb-120">**Дата**</span><span class="sxs-lookup"><span data-stu-id="639cb-120">**Date**</span></span>](registrationinfo-date.md)<br/>                             | <span data-ttu-id="639cb-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="639cb-121">Read/write</span></span><br/> | <span data-ttu-id="639cb-122">Возвращает или задает дату и время регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="639cb-122">Gets or sets the date and time when the task is registered.</span></span><br/>                                                                     |
| [<span data-ttu-id="639cb-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="639cb-123">**Description**</span></span>](registrationinfo-description.md)<br/>               | <span data-ttu-id="639cb-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="639cb-124">Read/write</span></span><br/> | <span data-ttu-id="639cb-125">Возвращает или задает описание задачи.</span><span class="sxs-lookup"><span data-stu-id="639cb-125">Gets or sets the description of the task.</span></span><br/>                                                                                       |
| [<span data-ttu-id="639cb-126">**Документация**</span><span class="sxs-lookup"><span data-stu-id="639cb-126">**Documentation**</span></span>](registrationinfo-documentation.md)<br/>           | <span data-ttu-id="639cb-127">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="639cb-127">Read/write</span></span><br/> | <span data-ttu-id="639cb-128">Возвращает или задает любую дополнительную документацию для задачи.</span><span class="sxs-lookup"><span data-stu-id="639cb-128">Gets or sets any additional documentation for the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="639cb-129">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="639cb-129">**SecurityDescriptor**</span></span>](registrationinfo-securitydescriptor.md)<br/> |                       | <span data-ttu-id="639cb-130">Возвращает или задает дескриптор безопасности задачи.</span><span class="sxs-lookup"><span data-stu-id="639cb-130">Gets or sets the security descriptor of the task.</span></span><br/>                                                                               |
| [<span data-ttu-id="639cb-131">**Источник**</span><span class="sxs-lookup"><span data-stu-id="639cb-131">**Source**</span></span>](registrationinfo-source.md)<br/>                         | <span data-ttu-id="639cb-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="639cb-132">Read/write</span></span><br/> | <span data-ttu-id="639cb-133">Возвращает или задает, откуда поступила задача.</span><span class="sxs-lookup"><span data-stu-id="639cb-133">Gets or sets where the task originated from.</span></span> <span data-ttu-id="639cb-134">Например, задача может исходить из компонента, службы, приложения или пользователя.</span><span class="sxs-lookup"><span data-stu-id="639cb-134">For example, a task may originate from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="639cb-135">**URI**</span><span class="sxs-lookup"><span data-stu-id="639cb-135">**URI**</span></span>](registrationinfo-uri.md)<br/>                               | <span data-ttu-id="639cb-136">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="639cb-136">Read/write</span></span><br/> | <span data-ttu-id="639cb-137">Возвращает или задает универсальный код ресурса (URI) задачи.</span><span class="sxs-lookup"><span data-stu-id="639cb-137">Gets or sets the URI of the task.</span></span><br/>                                                                                               |
| [<span data-ttu-id="639cb-138">**Версия**</span><span class="sxs-lookup"><span data-stu-id="639cb-138">**Version**</span></span>](registrationinfo-version.md)<br/>                       | <span data-ttu-id="639cb-139">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="639cb-139">Read/write</span></span><br/> | <span data-ttu-id="639cb-140">Возвращает или задает номер версии задачи.</span><span class="sxs-lookup"><span data-stu-id="639cb-140">Gets or sets the version number of the task.</span></span><br/>                                                                                    |
| [<span data-ttu-id="639cb-141">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="639cb-141">**XmlText**</span></span>](registrationinfo-xmltext.md)<br/>                       | <span data-ttu-id="639cb-142">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="639cb-142">Read/write</span></span><br/> | <span data-ttu-id="639cb-143">Возвращает или задает версию сведений о регистрации для задачи в формате XML.</span><span class="sxs-lookup"><span data-stu-id="639cb-143">Gets or sets an XML-formatted version of the registration information for the task.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="639cb-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="639cb-144">Remarks</span></span>

<span data-ttu-id="639cb-145">Сведения о регистрации можно использовать для указания задачи через пользовательский интерфейс планировщик задач или в качестве условий поиска при перечислении зарегистрированных задач.</span><span class="sxs-lookup"><span data-stu-id="639cb-145">Registration information can be used to identify a task through the Task Scheduler UI, or as search criteria when enumerating over the registered tasks.</span></span>

<span data-ttu-id="639cb-146">При чтении или записи XML для задачи сведения о регистрации для задачи задаются в элементе [**регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="639cb-146">When reading or writing XML for a task, registration information for the task is specified in the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="639cb-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="639cb-147">Examples</span></span>

<span data-ttu-id="639cb-148">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="639cb-148">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="639cb-149">Требования</span><span class="sxs-lookup"><span data-stu-id="639cb-149">Requirements</span></span>



| <span data-ttu-id="639cb-150">Требование</span><span class="sxs-lookup"><span data-stu-id="639cb-150">Requirement</span></span> | <span data-ttu-id="639cb-151">Значение</span><span class="sxs-lookup"><span data-stu-id="639cb-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="639cb-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="639cb-152">Minimum supported client</span></span><br/> | <span data-ttu-id="639cb-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="639cb-153">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="639cb-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="639cb-154">Minimum supported server</span></span><br/> | <span data-ttu-id="639cb-155">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="639cb-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="639cb-156">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="639cb-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="639cb-157"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="639cb-157"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="639cb-158">DLL</span><span class="sxs-lookup"><span data-stu-id="639cb-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="639cb-159"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="639cb-159"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





