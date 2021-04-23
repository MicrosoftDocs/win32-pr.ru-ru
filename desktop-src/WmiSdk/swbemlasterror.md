---
description: Методы и свойства объекта Свбемластеррор содержат объекты ошибок и управляют ими.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Объект Свбемластеррор (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692704"
---
# <a name="swbemlasterror-object"></a><span data-ttu-id="48f71-103">Объект Свбемластеррор</span><span class="sxs-lookup"><span data-stu-id="48f71-103">SWbemLastError object</span></span>

<span data-ttu-id="48f71-104">Методы и свойства объекта **свбемластеррор** содержат объекты ошибок и управляют ими.</span><span class="sxs-lookup"><span data-stu-id="48f71-104">The methods and properties of the **SWbemLastError** object contain and manipulate error objects.</span></span> <span data-ttu-id="48f71-105">Методы и свойства этого объекта точно совпадают с методами объекта [**SWbemObject**](swbemobject.md) , но используются для хранения сведений об ошибках вместо сведений о классах WMI.</span><span class="sxs-lookup"><span data-stu-id="48f71-105">The methods and properties of this object are exactly the same as those of the [**SWbemObject**](swbemobject.md) object, but are used to contain error information instead of WMI class information.</span></span> <span data-ttu-id="48f71-106">Этот объект может быть создан вызовом метода **CreateObject** VBScript.</span><span class="sxs-lookup"><span data-stu-id="48f71-106">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="48f71-107">Можно создать объект ошибки **свбемластеррор** для проверки расширенных сведений об ошибке, связанных с предыдущим вызовом метода.</span><span class="sxs-lookup"><span data-stu-id="48f71-107">You can create an **SWbemLastError** error object to inspect the extended error information that is associated with a previous method call.</span></span> <span data-ttu-id="48f71-108">Если информация об ошибках недоступна, попытка создать объект ошибки завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="48f71-108">If error information is not available, an attempt to create an error object will fail.</span></span> <span data-ttu-id="48f71-109">Если вызов завершается с ошибкой и возвращается объект Error, состояние объекта сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="48f71-109">If the call succeeds and an error object returns, the status of the object is reset.</span></span> <span data-ttu-id="48f71-110">Дальнейшие попытки получить объект ошибки будут завершаться ошибкой, пока не произойдет новая ошибка.</span><span class="sxs-lookup"><span data-stu-id="48f71-110">Further attempts to retrieve an error object will fail until a new error occurs.</span></span> <span data-ttu-id="48f71-111">В случае сбоя асинхронного вызова в параметре *обжвбемерроробжект* может возвращаться объект **свбемластеррор** , вызываемый событием [**свбемсинк. OnComplete**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="48f71-111">If you make an asynchronous call that fails, an **SWbemLastError** object may be returned to you by the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event in the *objWbemErrorObject* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="48f71-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="48f71-112">Members</span></span>

<span data-ttu-id="48f71-113">Объект **свбемластеррор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="48f71-113">The **SWbemLastError** object has these types of members:</span></span>

-   [<span data-ttu-id="48f71-114">Методы</span><span class="sxs-lookup"><span data-stu-id="48f71-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="48f71-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="48f71-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="48f71-116">Методы</span><span class="sxs-lookup"><span data-stu-id="48f71-116">Methods</span></span>

<span data-ttu-id="48f71-117">Объект **свбемластеррор** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="48f71-117">The **SWbemLastError** object has these methods.</span></span>



| <span data-ttu-id="48f71-118">Метод</span><span class="sxs-lookup"><span data-stu-id="48f71-118">Method</span></span>                                                   | <span data-ttu-id="48f71-119">Описание</span><span class="sxs-lookup"><span data-stu-id="48f71-119">Description</span></span>                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f71-120">**ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-120">**Associators\_**</span></span>                                        | <span data-ttu-id="48f71-121">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-121">Not used.</span></span> <span data-ttu-id="48f71-122">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-122">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-123">**ассоЦиаторсасинк\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-123">**AssociatorsAsync\_**</span></span>                                   | <span data-ttu-id="48f71-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-124">Not used.</span></span> <span data-ttu-id="48f71-125">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-125">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="48f71-126">**Клонировать\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-126">**Clone\_**</span></span>](swbemlasterror-clone-.md)                 | <span data-ttu-id="48f71-127">Создает копию текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="48f71-127">Makes a copy of the current object.</span></span><br/>                                               |
| [<span data-ttu-id="48f71-128">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-128">**CompareTo\_**</span></span>](swbemlasterror-compareto-.md)         | <span data-ttu-id="48f71-129">Проверяет два объекта на равенство.</span><span class="sxs-lookup"><span data-stu-id="48f71-129">Tests two objects for equality.</span></span><br/>                                                   |
| <span data-ttu-id="48f71-130">**Удалить\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-130">**Delete\_**</span></span>                                             | <span data-ttu-id="48f71-131">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-131">Not used.</span></span> <span data-ttu-id="48f71-132">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-132">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-133">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-133">**DeleteAsync\_**</span></span>                                        | <span data-ttu-id="48f71-134">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-134">Not used.</span></span> <span data-ttu-id="48f71-135">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-135">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-136">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-136">**ExecMethod\_**</span></span>                                         | <span data-ttu-id="48f71-137">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-137">Not used.</span></span> <span data-ttu-id="48f71-138">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-138">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-139">**ексекмесодасинк\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-139">**ExecMethodAsync\_**</span></span>                                    | <span data-ttu-id="48f71-140">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-140">Not used.</span></span> <span data-ttu-id="48f71-141">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-141">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="48f71-142">**жетобжекттекст\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-142">**GetObjectText\_**</span></span>](swbemlasterror-getobjecttext-.md) | <span data-ttu-id="48f71-143">Извлекает текстовое представление объекта, написанного с помощью синтаксиса MOF.</span><span class="sxs-lookup"><span data-stu-id="48f71-143">Retrieves the textual representation of the object written with MOF syntax.</span></span><br/>       |
| <span data-ttu-id="48f71-144">**Экземпляры\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-144">**Instances\_**</span></span>                                          | <span data-ttu-id="48f71-145">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-145">Not used.</span></span> <span data-ttu-id="48f71-146">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-146">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-147">**инстанцесасинк\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-147">**InstancesAsync\_**</span></span>                                     | <span data-ttu-id="48f71-148">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-148">Not used.</span></span> <span data-ttu-id="48f71-149">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-149">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-150">**PUT\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-150">**Put\_**</span></span>                                                | <span data-ttu-id="48f71-151">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-151">Not used.</span></span> <span data-ttu-id="48f71-152">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-152">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-153">**путасинк\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-153">**PutAsync\_**</span></span>                                           | <span data-ttu-id="48f71-154">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-154">Not used.</span></span> <span data-ttu-id="48f71-155">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-155">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-156">**Ссылки\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-156">**References\_**</span></span>                                         | <span data-ttu-id="48f71-157">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-157">Not used.</span></span> <span data-ttu-id="48f71-158">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-158">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-159">**референцесасинк\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-159">**ReferencesAsync\_**</span></span>                                    | <span data-ttu-id="48f71-160">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-160">Not used.</span></span> <span data-ttu-id="48f71-161">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-161">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-162">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-162">**SpawnDerivedClass\_**</span></span>                                  | <span data-ttu-id="48f71-163">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-163">Not used.</span></span> <span data-ttu-id="48f71-164">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-164">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-165">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-165">**SpawnInstance\_**</span></span>                                      | <span data-ttu-id="48f71-166">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-166">Not used.</span></span> <span data-ttu-id="48f71-167">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-167">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-168">**Подклассы\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-168">**Subclasses\_**</span></span>                                         | <span data-ttu-id="48f71-169">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-169">Not used.</span></span> <span data-ttu-id="48f71-170">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-170">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="48f71-171">**субклассесасинк\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-171">**SubclassesAsync\_**</span></span>                                    | <span data-ttu-id="48f71-172">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-172">Not used.</span></span> <span data-ttu-id="48f71-173">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-173">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="48f71-174">Свойства</span><span class="sxs-lookup"><span data-stu-id="48f71-174">Properties</span></span>

<span data-ttu-id="48f71-175">Объект **свбемластеррор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="48f71-175">The **SWbemLastError** object has these properties.</span></span>



| <span data-ttu-id="48f71-176">Свойство</span><span class="sxs-lookup"><span data-stu-id="48f71-176">Property</span></span>                                                      | <span data-ttu-id="48f71-177">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="48f71-177">Access type</span></span>          | <span data-ttu-id="48f71-178">Описание</span><span class="sxs-lookup"><span data-stu-id="48f71-178">Description</span></span>                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f71-179">**Наследование\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-179">**Derivation\_**</span></span><br/>                                   | <span data-ttu-id="48f71-180">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="48f71-180">Read-only</span></span><br/> | <span data-ttu-id="48f71-181">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-181">Not used.</span></span> <span data-ttu-id="48f71-182">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-182">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="48f71-183">**Методы\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-183">**Methods\_**</span></span> <br/>                                     | <span data-ttu-id="48f71-184">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="48f71-184">Read-only</span></span><br/> | <span data-ttu-id="48f71-185">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-185">Not used.</span></span> <span data-ttu-id="48f71-186">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-186">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| [<span data-ttu-id="48f71-187">**Путь\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-187">**Path\_**</span></span>](swbemlasterror-path-.md)<br/>             | <span data-ttu-id="48f71-188">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="48f71-188">Read-only</span></span><br/> | <span data-ttu-id="48f71-189">Содержит объект [**свбемобжектпас**](swbemobjectpath.md) , представляющий путь к объекту текущего класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="48f71-189">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/>                    |
| [<span data-ttu-id="48f71-190">**Свойства\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-190">**Properties\_**</span></span>](swbemlasterror-properties-.md)<br/> | <span data-ttu-id="48f71-191">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="48f71-191">Read-only</span></span><br/> | <span data-ttu-id="48f71-192">Представляет коллекцию свойств объекта **свбемластеррор** .</span><span class="sxs-lookup"><span data-stu-id="48f71-192">Represents the collection of properties of the **SWbemLastError** object.</span></span> <span data-ttu-id="48f71-193">Это свойство является объектом [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="48f71-193">This property is an [**SWbemPropertySet**](swbempropertyset.md) object.</span></span><br/> |
| <span data-ttu-id="48f71-194">**Квалификаторы\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-194">**Qualifiers\_**</span></span><br/>                                   | <span data-ttu-id="48f71-195">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="48f71-195">Read-only</span></span><br/> | <span data-ttu-id="48f71-196">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-196">Not used.</span></span> <span data-ttu-id="48f71-197">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-197">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="48f71-198">**Безопасность\_**</span><span class="sxs-lookup"><span data-stu-id="48f71-198">**Security\_**</span></span><br/>                                     | <span data-ttu-id="48f71-199">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="48f71-199">Read-only</span></span><br/> | <span data-ttu-id="48f71-200">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f71-200">Not used.</span></span> <span data-ttu-id="48f71-201">Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.</span><span class="sxs-lookup"><span data-stu-id="48f71-201">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |



 

## <a name="examples"></a><span data-ttu-id="48f71-202">Примеры</span><span class="sxs-lookup"><span data-stu-id="48f71-202">Examples</span></span>

<span data-ttu-id="48f71-203">В следующем примере сценария VBScript показано, как проверить сведения об объекте Error и Error.</span><span class="sxs-lookup"><span data-stu-id="48f71-203">The following VBScript sample demonstrates how to inspect error and error object information.</span></span>


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



<span data-ttu-id="48f71-204">В следующем образце Perl показано, как проверить сведения об объекте Error и Error.</span><span class="sxs-lookup"><span data-stu-id="48f71-204">The following Perl sample demonstrates how to inspect error and error object information.</span></span>


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
}
```



## <a name="requirements"></a><span data-ttu-id="48f71-205">Требования</span><span class="sxs-lookup"><span data-stu-id="48f71-205">Requirements</span></span>



| <span data-ttu-id="48f71-206">Требование</span><span class="sxs-lookup"><span data-stu-id="48f71-206">Requirement</span></span> | <span data-ttu-id="48f71-207">Значение</span><span class="sxs-lookup"><span data-stu-id="48f71-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48f71-208">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48f71-208">Minimum supported client</span></span><br/> | <span data-ttu-id="48f71-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48f71-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48f71-210">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48f71-210">Minimum supported server</span></span><br/> | <span data-ttu-id="48f71-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48f71-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48f71-212">Header</span><span class="sxs-lookup"><span data-stu-id="48f71-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="48f71-213"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="48f71-213"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="48f71-214">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="48f71-214">Type library</span></span><br/>             | <dl> <span data-ttu-id="48f71-215"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="48f71-215"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="48f71-216">DLL</span><span class="sxs-lookup"><span data-stu-id="48f71-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48f71-217"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48f71-217"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="48f71-218">CLSID</span><span class="sxs-lookup"><span data-stu-id="48f71-218">CLSID</span></span><br/>                    | <span data-ttu-id="48f71-219">\_СВБЕМЛАСТЕРРОР CLSID</span><span class="sxs-lookup"><span data-stu-id="48f71-219">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="48f71-220">IID</span><span class="sxs-lookup"><span data-stu-id="48f71-220">IID</span></span><br/>                      | <span data-ttu-id="48f71-221">IID \_ исвбемластеррор</span><span class="sxs-lookup"><span data-stu-id="48f71-221">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="48f71-222">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48f71-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f71-223">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="48f71-223">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




