---
description: Описывает соглашения о документе для чтения разделов API сценариев WMI.
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: Соглашения о документе для API скриптов
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346742"
---
# <a name="document-conventions-for-the-scripting-api"></a><span data-ttu-id="a9677-103">Соглашения о документе для API скриптов</span><span class="sxs-lookup"><span data-stu-id="a9677-103">Document Conventions for the Scripting API</span></span>

<span data-ttu-id="a9677-104">[API скриптов для WMI](scripting-api-for-wmi.md) Reference использует следующие соглашения о документе:</span><span class="sxs-lookup"><span data-stu-id="a9677-104">The [Scripting API for WMI](scripting-api-for-wmi.md) reference uses the following document conventions:</span></span>

-   <span data-ttu-id="a9677-105">Типы параметров определяются с помощью префикса: b (логическое значение), str (строка), I (целое число), obj (объект автоматизации), var (Variant).</span><span class="sxs-lookup"><span data-stu-id="a9677-105">Parameter types are defined using a prefix: b (Boolean), str (string), I (integer), obj (Automation object), var (Variant).</span></span>
-   <span data-ttu-id="a9677-106">Необязательные параметры помещаются в квадратные скобки со значениями по умолчанию, которые отображаются по назначению.</span><span class="sxs-lookup"><span data-stu-id="a9677-106">Optional parameters are placed in square brackets with their default values shown by assignment.</span></span>
-   <span data-ttu-id="a9677-107">В случае с параметрами объекта символы после префикса "obj" указывают тип ожидаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="a9677-107">In the case of object parameters, the characters after the "obj" prefix indicate the type of object expected.</span></span>



| <span data-ttu-id="a9677-108">Параметр объекта</span><span class="sxs-lookup"><span data-stu-id="a9677-108">Object parameter</span></span>      | <span data-ttu-id="a9677-109">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="a9677-109">Object type</span></span>                                          |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="a9677-110">*вбемдатетиме*</span><span class="sxs-lookup"><span data-stu-id="a9677-110">*WbemDatetime*</span></span>        | [<span data-ttu-id="a9677-111">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="a9677-111">**SWbemDateTime**</span></span>](swbemdatetime.md)               |
| <span data-ttu-id="a9677-112">*вбемевентсаурце*</span><span class="sxs-lookup"><span data-stu-id="a9677-112">*WbemEventSource*</span></span>     | [<span data-ttu-id="a9677-113">**свбемевентсаурце**</span><span class="sxs-lookup"><span data-stu-id="a9677-113">**SWbemEventSource**</span></span>](swbemeventsource.md)         |
| <span data-ttu-id="a9677-114">*вбемлокатор*</span><span class="sxs-lookup"><span data-stu-id="a9677-114">*WbemLocator*</span></span>         | [<span data-ttu-id="a9677-115">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="a9677-115">**SWbemLocator**</span></span>](swbemlocator.md)                 |
| <span data-ttu-id="a9677-116">*вбеммесод*</span><span class="sxs-lookup"><span data-stu-id="a9677-116">*WbemMethod*</span></span>          | [<span data-ttu-id="a9677-117">**свбеммесод**</span><span class="sxs-lookup"><span data-stu-id="a9677-117">**SWbemMethod**</span></span>](swbemmethod.md)                   |
| <span data-ttu-id="a9677-118">*вбеммесодсет*</span><span class="sxs-lookup"><span data-stu-id="a9677-118">*WbemMethodSet*</span></span>       | [<span data-ttu-id="a9677-119">**свбеммесодсет**</span><span class="sxs-lookup"><span data-stu-id="a9677-119">**SWbemMethodSet**</span></span>](swbemmethodset.md)             |
| <span data-ttu-id="a9677-120">*вбемнамедвалуесет*</span><span class="sxs-lookup"><span data-stu-id="a9677-120">*WbemNamedValueSet*</span></span>   | [<span data-ttu-id="a9677-121">**свбемнамедвалуесет**</span><span class="sxs-lookup"><span data-stu-id="a9677-121">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)     |
| <span data-ttu-id="a9677-122">*вбемобжект*</span><span class="sxs-lookup"><span data-stu-id="a9677-122">*WbemObject*</span></span>          | [<span data-ttu-id="a9677-123">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="a9677-123">**SWbemObject**</span></span>](swbemobject.md)                   |
| <span data-ttu-id="a9677-124">*вбемобжектекс*</span><span class="sxs-lookup"><span data-stu-id="a9677-124">*WbemObjectEx*</span></span>        | [<span data-ttu-id="a9677-125">**свбемобжектекс**</span><span class="sxs-lookup"><span data-stu-id="a9677-125">**SWbemObjectEx**</span></span>](swbemobjectex.md)               |
| <span data-ttu-id="a9677-126">*вбемобжектпас*</span><span class="sxs-lookup"><span data-stu-id="a9677-126">*WbemObjectPath*</span></span>      | [<span data-ttu-id="a9677-127">**свбемобжектпас**</span><span class="sxs-lookup"><span data-stu-id="a9677-127">**SWbemObjectPath**</span></span>](swbemobjectpath.md)           |
| <span data-ttu-id="a9677-128">*вбемобжектсет*</span><span class="sxs-lookup"><span data-stu-id="a9677-128">*WbemObjectSet*</span></span>       | [<span data-ttu-id="a9677-129">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="a9677-129">**SWbemObjectSet**</span></span>](swbemobjectset.md)             |
| <span data-ttu-id="a9677-130">*вбемпривилеже*</span><span class="sxs-lookup"><span data-stu-id="a9677-130">*WbemPrivilege*</span></span>       | [<span data-ttu-id="a9677-131">**свбемпривилеже**</span><span class="sxs-lookup"><span data-stu-id="a9677-131">**SWbemPrivilege**</span></span>](swbemprivilege.md)             |
| <span data-ttu-id="a9677-132">*вбемпривилежесет*</span><span class="sxs-lookup"><span data-stu-id="a9677-132">*WbemPrivilegeSet*</span></span>    | [<span data-ttu-id="a9677-133">**свбемпривилежесет**</span><span class="sxs-lookup"><span data-stu-id="a9677-133">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)       |
| <span data-ttu-id="a9677-134">*вбемпроперти*</span><span class="sxs-lookup"><span data-stu-id="a9677-134">*WbemProperty*</span></span>        | [<span data-ttu-id="a9677-135">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="a9677-135">**SWbemProperty**</span></span>](swbemproperty.md)               |
| <span data-ttu-id="a9677-136">*вбемпропертисет*</span><span class="sxs-lookup"><span data-stu-id="a9677-136">*WbemPropertySet*</span></span>     | [<span data-ttu-id="a9677-137">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="a9677-137">**SWbemPropertySet**</span></span>](swbempropertyset.md)         |
| <span data-ttu-id="a9677-138">*вбемкуалифиер*</span><span class="sxs-lookup"><span data-stu-id="a9677-138">*WbemQualifier*</span></span>       | [<span data-ttu-id="a9677-139">**свбемкуалифиер**</span><span class="sxs-lookup"><span data-stu-id="a9677-139">**SWbemQualifier**</span></span>](swbemqualifier.md)             |
| <span data-ttu-id="a9677-140">*вбемкуалифиерсет*</span><span class="sxs-lookup"><span data-stu-id="a9677-140">*WbemQualifierSet*</span></span>    | [<span data-ttu-id="a9677-141">**свбемкуалифиерсет**</span><span class="sxs-lookup"><span data-stu-id="a9677-141">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)       |
| <span data-ttu-id="a9677-142">*вбемрефрешаблеитем*</span><span class="sxs-lookup"><span data-stu-id="a9677-142">*WbemRefreshableItem*</span></span> | [<span data-ttu-id="a9677-143">**свбемрефрешаблеитем**</span><span class="sxs-lookup"><span data-stu-id="a9677-143">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md) |
| <span data-ttu-id="a9677-144">*вбемрефрешер*</span><span class="sxs-lookup"><span data-stu-id="a9677-144">*WbemRefresher*</span></span>       | [<span data-ttu-id="a9677-145">**свбемрефрешер**</span><span class="sxs-lookup"><span data-stu-id="a9677-145">**SWbemRefresher**</span></span>](swbemrefresher.md)             |
| <span data-ttu-id="a9677-146">*вбемсервицес*</span><span class="sxs-lookup"><span data-stu-id="a9677-146">*WbemServices*</span></span>        | [<span data-ttu-id="a9677-147">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="a9677-147">**SWbemServices**</span></span>](swbemservices.md)               |
| <span data-ttu-id="a9677-148">*вбемсервицесекс*</span><span class="sxs-lookup"><span data-stu-id="a9677-148">*WbemServicesEx*</span></span>      | [<span data-ttu-id="a9677-149">**свбемсервицесекс**</span><span class="sxs-lookup"><span data-stu-id="a9677-149">**SWbemServicesEx**</span></span>](swbemservicesex.md)           |



 

<span data-ttu-id="a9677-150">Например, в следующем коде показано, как можно присвоить имена переменным для различных типов объектов:</span><span class="sxs-lookup"><span data-stu-id="a9677-150">For example, the following code shows how to name variables for different types of objects:</span></span>


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



