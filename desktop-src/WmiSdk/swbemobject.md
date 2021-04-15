---
description: Методы и свойства объекта SWbemObject можно использовать для представления одного определения класса инструментарий управления Windows (WMI) (WMI) или экземпляра объекта.
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: Объект SWbemObject (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701955"
---
# <a name="swbemobject-object"></a><span data-ttu-id="e264e-103">Объект SWbemObject</span><span class="sxs-lookup"><span data-stu-id="e264e-103">SWbemObject object</span></span>

<span data-ttu-id="e264e-104">Методы и свойства объекта **SWbemObject** можно использовать для представления одного определения класса инструментарий управления Windows (WMI) (WMI) или экземпляра объекта.</span><span class="sxs-lookup"><span data-stu-id="e264e-104">You can use the methods and properties of the **SWbemObject** object to represent one Windows Management Instrumentation (WMI) class definition or object instance.</span></span> <span data-ttu-id="e264e-105">Не удается создать этот объект с [помощью вызова функции](/previous-versions//xzysf6hc(v=vs.85)) VBScript.</span><span class="sxs-lookup"><span data-stu-id="e264e-105">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

<span data-ttu-id="e264e-106">Этот объект поддерживает два типа свойств и методов.</span><span class="sxs-lookup"><span data-stu-id="e264e-106">This object supports two types of properties and methods.</span></span> <span data-ttu-id="e264e-107">Те, которые определены в этом разделе, являются универсальными свойствами и методами, применяемыми ко всем объектам WMI.</span><span class="sxs-lookup"><span data-stu-id="e264e-107">Those defined in this section are generic properties and methods that apply to all WMI objects.</span></span> <span data-ttu-id="e264e-108">Кроме того, этот объект предоставляет свойства и методы базового объекта в виде динамических свойств автоматизации и методов **SWbemObject**.</span><span class="sxs-lookup"><span data-stu-id="e264e-108">In addition, this object exposes the properties and methods of the underlying object as dynamic automation properties and methods of **SWbemObject**.</span></span> <span data-ttu-id="e264e-109">Имена и типы этих свойств и методов зависят от базового объекта WMI.</span><span class="sxs-lookup"><span data-stu-id="e264e-109">The names and types of these properties and methods depend on the underlying WMI object.</span></span> <span data-ttu-id="e264e-110">Дополнительные сведения о том, как предоставляются эти динамические свойства и методы, см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="e264e-110">For more information about how these dynamic properties and methods are exposed, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="e264e-111">С точки зрения клиента WMI этот объект всегда находится внутри процесса.</span><span class="sxs-lookup"><span data-stu-id="e264e-111">From the WMI client perspective, this object is always in-process.</span></span> <span data-ttu-id="e264e-112">Операции записи затрагивают только локальную копию объекта, а операции чтения всегда извлекают значения из локальной копии.</span><span class="sxs-lookup"><span data-stu-id="e264e-112">Write operations only affect the local copy of the object, and read operations always retrieve values from the local copy.</span></span> <span data-ttu-id="e264e-113">Обновления WMI выполняются только при написании целых объектов с помощью вызова метода [**SWbemObject. постановки \_**](swbemobject-put-.md) .</span><span class="sxs-lookup"><span data-stu-id="e264e-113">Updates to WMI are performed only when entire objects are written using a call to the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span> <span data-ttu-id="e264e-114">При изменении свойств или методов в объекте **SWbemObject** изменения не записываются в WMI, пока не будет вызван метод **SWbemObject \_ .** WHERE.</span><span class="sxs-lookup"><span data-stu-id="e264e-114">If you modify the properties or methods in an **SWbemObject** object, your changes are not written to WMI until you call **SWbemObject.Put\_**.</span></span>

<span data-ttu-id="e264e-115">Универсальный метод и имена свойств, определенные в этом разделе, всегда заканчиваются завершающим символом подчеркивания (" \_ "), чтобы отличать их от динамических методов и свойств WMI базового объекта.</span><span class="sxs-lookup"><span data-stu-id="e264e-115">The generic method and property names defined in this section always end with a trailing underscore ("\_") to differentiate them from the dynamic WMI methods and properties of the underlying object.</span></span>

<span data-ttu-id="e264e-116">Обратите внимание, что **SWbemObject** не может быть создано с помощью VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). Method.</span><span class="sxs-lookup"><span data-stu-id="e264e-116">Note that **SWbemObject** cannot be created using the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).method.</span></span> <span data-ttu-id="e264e-117">Если вы хотите создать новый пустой класс, используйте [**SwbemServices. Get**](swbemservices-get.md) с пустым параметром пути.</span><span class="sxs-lookup"><span data-stu-id="e264e-117">If you want to create a new, empty class use [**SWbemServices.Get**](swbemservices-get.md) with an empty path parameter.</span></span> <span data-ttu-id="e264e-118">Этот вызов возвращает пустой объект **SWbemObject** , который может стать классом.</span><span class="sxs-lookup"><span data-stu-id="e264e-118">This call returns an empty **SWbemObject** object that can become a class.</span></span> <span data-ttu-id="e264e-119">Затем можно указать имя класса для свойства [**класса**](swbemobjectpath-class.md) объекта [**свбемобжектпас**](swbemobjectpath.md) , возвращаемого вызовом [**path \_**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="e264e-119">You can then supply a class name for the [**Class**](swbemobjectpath-class.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the [**Path\_**](swbemobject-path-.md) call.</span></span> <span data-ttu-id="e264e-120">Добавьте свойства в новый класс с помощью метода [**Properties \_**](swbemobject-properties-.md) .</span><span class="sxs-lookup"><span data-stu-id="e264e-120">Add properties to the new class by the [**Properties\_**](swbemobject-properties-.md) method.</span></span> <span data-ttu-id="e264e-121">Чтобы создать экземпляр, вызовите **GetObject** для нового класса.</span><span class="sxs-lookup"><span data-stu-id="e264e-121">To create an instance, call **GetObject** on the new class.</span></span>

<span data-ttu-id="e264e-122">В следующем примере кода показано, как получить новый класс и добавить в него свойство.</span><span class="sxs-lookup"><span data-stu-id="e264e-122">The following code example shows how to obtain a new class and add a property to it.</span></span> <span data-ttu-id="e264e-123">Объект **SWbemObject** , представляющий класс, должен быть записан обратно в репозиторий WMI с помощью вызова метода " [**поставить \_**](swbemobject-put-.md)".</span><span class="sxs-lookup"><span data-stu-id="e264e-123">The **SWbemObject** object that represents the class must be written back to the WMI repository by a call to [**Put\_**](swbemobject-put-.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



<span data-ttu-id="e264e-124">Вы можете проверить репозиторий с помощью средства просмотра, такого как [CIM Studio](further-information.md) , чтобы убедиться, что появился новый класс и экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e264e-124">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="e264e-125">Пример удаления класса и экземпляра из репозитория см. в разделе [**SwbemServices. Delete**](swbemservices-delete.md) или [**\_ SWbemObject. Delete**](swbemobject-delete-.md).</span><span class="sxs-lookup"><span data-stu-id="e264e-125">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="members"></a><span data-ttu-id="e264e-126">Элементы</span><span class="sxs-lookup"><span data-stu-id="e264e-126">Members</span></span>

<span data-ttu-id="e264e-127">Объект **SWbemObject** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e264e-127">The **SWbemObject** object has these types of members:</span></span>

-   [<span data-ttu-id="e264e-128">Методы</span><span class="sxs-lookup"><span data-stu-id="e264e-128">Methods</span></span>](#methods)
-   [<span data-ttu-id="e264e-129">Свойства</span><span class="sxs-lookup"><span data-stu-id="e264e-129">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e264e-130">Методы</span><span class="sxs-lookup"><span data-stu-id="e264e-130">Methods</span></span>

<span data-ttu-id="e264e-131">Объект **SWbemObject** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="e264e-131">The **SWbemObject** object has these methods.</span></span>



| <span data-ttu-id="e264e-132">Метод</span><span class="sxs-lookup"><span data-stu-id="e264e-132">Method</span></span>                                                        | <span data-ttu-id="e264e-133">Описание</span><span class="sxs-lookup"><span data-stu-id="e264e-133">Description</span></span>                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e264e-134">**ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-134">**Associators\_**</span></span>](swbemobject-associators-.md)             | <span data-ttu-id="e264e-135">Получает соединители объекта.</span><span class="sxs-lookup"><span data-stu-id="e264e-135">Retrieves the associators of the object.</span></span><br/>                                                     |
| [<span data-ttu-id="e264e-136">**ассоЦиаторсасинк\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-136">**AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)   | <span data-ttu-id="e264e-137">Асинхронно извлекает соединители объекта.</span><span class="sxs-lookup"><span data-stu-id="e264e-137">Asynchronously retrieves the associators of the object.</span></span><br/>                                      |
| [<span data-ttu-id="e264e-138">**Клонировать\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-138">**Clone\_**</span></span>](swbemobject-clone-.md)                         | <span data-ttu-id="e264e-139">Создает копию текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="e264e-139">Makes a copy of the current object.</span></span><br/>                                                          |
| [<span data-ttu-id="e264e-140">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-140">**CompareTo\_**</span></span>](swbemobject-compareto-.md)                 | <span data-ttu-id="e264e-141">Проверяет два объекта на равенство.</span><span class="sxs-lookup"><span data-stu-id="e264e-141">Tests two objects for equality.</span></span><br/>                                                              |
| [<span data-ttu-id="e264e-142">**Удалить\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-142">**Delete\_**</span></span>](swbemobject-delete-.md)                       | <span data-ttu-id="e264e-143">Удаляет объект из WMI.</span><span class="sxs-lookup"><span data-stu-id="e264e-143">Deletes the object from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="e264e-144">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-144">**DeleteAsync\_**</span></span>](swbemobject-deleteasync-.md)             | <span data-ttu-id="e264e-145">Асинхронно удаляет объект из WMI.</span><span class="sxs-lookup"><span data-stu-id="e264e-145">Asynchronously deletes the object from WMI.</span></span><br/>                                                  |
| [<span data-ttu-id="e264e-146">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-146">**ExecMethod\_**</span></span>](swbemobject-execmethod-.md)               | <span data-ttu-id="e264e-147">Выполняет метод, экспортированный поставщиком метода.</span><span class="sxs-lookup"><span data-stu-id="e264e-147">Executes a method exported by a method provider.</span></span><br/>                                             |
| [<span data-ttu-id="e264e-148">**ексекмесодасинк\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-148">**ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)     | <span data-ttu-id="e264e-149">Асинхронно выполняет метод, экспортированный поставщиком метода.</span><span class="sxs-lookup"><span data-stu-id="e264e-149">Asynchronously executes a method exported by a method provider.</span></span><br/>                              |
| [<span data-ttu-id="e264e-150">**жетобжекттекст\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-150">**GetObjectText\_**</span></span>](swbemobject-getobjecttext-.md)         | <span data-ttu-id="e264e-151">Извлекает текстовое представление объекта (синтаксис MOF).</span><span class="sxs-lookup"><span data-stu-id="e264e-151">Retrieves the textual representation of the object (MOF syntax).</span></span><br/>                             |
| [<span data-ttu-id="e264e-152">**Экземпляры\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-152">**Instances\_**</span></span>](swbemobject-instances-.md)                 | <span data-ttu-id="e264e-153">Возвращает коллекцию экземпляров объекта (который должен быть классом WMI).</span><span class="sxs-lookup"><span data-stu-id="e264e-153">Returns a collection of instances of the object (which must be a WMI class).</span></span><br/>                 |
| [<span data-ttu-id="e264e-154">**инстанцесасинк\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-154">**InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)       | <span data-ttu-id="e264e-155">Асинхронно возвращает коллекцию экземпляров объекта (который должен быть классом WMI).</span><span class="sxs-lookup"><span data-stu-id="e264e-155">Asynchronously returns a collection of instances of the object (which must be a WMI class).</span></span><br/>  |
| [<span data-ttu-id="e264e-156">**PUT\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-156">**Put\_**</span></span>](swbemobject-put-.md)                             | <span data-ttu-id="e264e-157">Создает или обновляет объект в WMI.</span><span class="sxs-lookup"><span data-stu-id="e264e-157">Creates or updates the object in WMI.</span></span><br/>                                                        |
| [<span data-ttu-id="e264e-158">**путасинк\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-158">**PutAsync\_**</span></span>](swbemobject-putasync-.md)                   | <span data-ttu-id="e264e-159">Асинхронно создает или обновляет объект в WMI.</span><span class="sxs-lookup"><span data-stu-id="e264e-159">Asynchronously creates or updates the object in WMI.</span></span><br/>                                         |
| [<span data-ttu-id="e264e-160">**Ссылки\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-160">**References\_**</span></span>](swbemobject-references-.md)               | <span data-ttu-id="e264e-161">Возвращает ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="e264e-161">Returns references to the object.</span></span><br/>                                                            |
| [<span data-ttu-id="e264e-162">**референцесасинк\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-162">**ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)     | <span data-ttu-id="e264e-163">Асинхронно возвращает ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="e264e-163">Asynchronously returns references to the object.</span></span><br/>                                             |
| [<span data-ttu-id="e264e-164">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-164">**SpawnDerivedClass\_**</span></span>](swbemobject-spawnderivedclass-.md) | <span data-ttu-id="e264e-165">Создает новый производный класс из текущего объекта (который должен быть классом WMI).</span><span class="sxs-lookup"><span data-stu-id="e264e-165">Creates a new derived class from the current object (which must be a WMI class).</span></span><br/>             |
| [<span data-ttu-id="e264e-166">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-166">**SpawnInstance\_**</span></span>](swbemobject-spawninstance-.md)         | <span data-ttu-id="e264e-167">Создает новый экземпляр из текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="e264e-167">Creates a new instance from the current object.</span></span><br/>                                              |
| [<span data-ttu-id="e264e-168">**Подклассы\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-168">**Subclasses\_**</span></span>](swbemobject-subclasses-.md)               | <span data-ttu-id="e264e-169">Возвращает коллекцию подклассов объекта (который должен быть классом WMI).</span><span class="sxs-lookup"><span data-stu-id="e264e-169">Returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/>                |
| [<span data-ttu-id="e264e-170">**субклассесасинк\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-170">**SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)     | <span data-ttu-id="e264e-171">Асинхронно возвращает коллекцию подклассов объекта (который должен быть классом WMI).</span><span class="sxs-lookup"><span data-stu-id="e264e-171">Asynchronously returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e264e-172">Свойства</span><span class="sxs-lookup"><span data-stu-id="e264e-172">Properties</span></span>

<span data-ttu-id="e264e-173">Объект **SWbemObject** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e264e-173">The **SWbemObject** object has these properties.</span></span>



| <span data-ttu-id="e264e-174">Свойство</span><span class="sxs-lookup"><span data-stu-id="e264e-174">Property</span></span>                                                   | <span data-ttu-id="e264e-175">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="e264e-175">Access type</span></span>          | <span data-ttu-id="e264e-176">Описание</span><span class="sxs-lookup"><span data-stu-id="e264e-176">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e264e-177">**Наследование\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-177">**Derivation\_**</span></span>](swbemobject-derivation-.md)<br/> | <span data-ttu-id="e264e-178">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e264e-178">Read-only</span></span><br/> | <span data-ttu-id="e264e-179">Содержит массив строк, описывающих производную иерархию для класса.</span><span class="sxs-lookup"><span data-stu-id="e264e-179">Contains an array of strings that describes the derivation hierarchy for the class.</span></span><br/>                                             |
| [<span data-ttu-id="e264e-180">**Методы\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-180">**Methods\_**</span></span>](swbemobject-methods-.md)<br/>       | <span data-ttu-id="e264e-181">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e264e-181">Read-only</span></span><br/> | <span data-ttu-id="e264e-182">Объект [**свбеммесодсет**](swbemmethodset.md) , являющийся коллекцией методов для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="e264e-182">An [**SWbemMethodSet**](swbemmethodset.md) object that is the collection of methods for this object.</span></span><br/>                           |
| [<span data-ttu-id="e264e-183">**Путь\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-183">**Path\_**</span></span>](swbemobject-path-.md)<br/>             | <span data-ttu-id="e264e-184">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e264e-184">Read-only</span></span><br/> | <span data-ttu-id="e264e-185">Содержит объект [**свбемобжектпас**](swbemobjectpath.md) , представляющий путь к объекту текущего класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e264e-185">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/> |
| [<span data-ttu-id="e264e-186">**Свойства\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-186">**Properties\_**</span></span>](swbemobject-properties-.md)<br/> | <span data-ttu-id="e264e-187">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e264e-187">Read-only</span></span><br/> | <span data-ttu-id="e264e-188">Объект [**SWbemPropertySet**](swbempropertyset.md) , являющийся коллекцией свойств для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="e264e-188">An [**SWbemPropertySet**](swbempropertyset.md) object that is the collection of properties for this object.</span></span><br/>                    |
| [<span data-ttu-id="e264e-189">**Квалификаторы\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-189">**Qualifiers\_**</span></span>](swbemobject-qualifiers-.md)<br/> | <span data-ttu-id="e264e-190">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e264e-190">Read-only</span></span><br/> | <span data-ttu-id="e264e-191">Объект [**свбемкуалифиерсет**](swbemqualifierset.md) , являющийся коллекцией квалификаторов для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="e264e-191">An [**SWbemQualifierSet**](swbemqualifierset.md) object that is the collection of qualifiers for this object.</span></span><br/>                  |
| [<span data-ttu-id="e264e-192">**Безопасность\_**</span><span class="sxs-lookup"><span data-stu-id="e264e-192">**Security\_**</span></span>](swbemobject-security-.md)<br/>     | <span data-ttu-id="e264e-193">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e264e-193">Read-only</span></span><br/> | <span data-ttu-id="e264e-194">Содержит объект [**свбемсекурити**](swbemsecurity.md) , используемый для чтения или изменения параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="e264e-194">Contains an [**SWbemSecurity**](swbemsecurity.md) object used to read or change the security settings.</span></span><br/>                         |



 

## <a name="examples"></a><span data-ttu-id="e264e-195">Примеры</span><span class="sxs-lookup"><span data-stu-id="e264e-195">Examples</span></span>

<span data-ttu-id="e264e-196">[Список всех свойств и методов для](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) примера кода VBScript класса WMI в коллекции TechNet использует SWbemObject для перечисления всех методов и свойств для УКАЗАННОГО класса WMI.</span><span class="sxs-lookup"><span data-stu-id="e264e-196">The [List All the Properties and Methods for a WMI Class](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) VBScript code sample on TechNet Gallery uses the SWbemObject to list all of the methods and properties for a specified WMI class.</span></span>

## <a name="requirements"></a><span data-ttu-id="e264e-197">Требования</span><span class="sxs-lookup"><span data-stu-id="e264e-197">Requirements</span></span>



| <span data-ttu-id="e264e-198">Требование</span><span class="sxs-lookup"><span data-stu-id="e264e-198">Requirement</span></span> | <span data-ttu-id="e264e-199">Значение</span><span class="sxs-lookup"><span data-stu-id="e264e-199">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e264e-200">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e264e-200">Minimum supported client</span></span><br/> | <span data-ttu-id="e264e-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e264e-201">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e264e-202">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e264e-202">Minimum supported server</span></span><br/> | <span data-ttu-id="e264e-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e264e-203">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e264e-204">Header</span><span class="sxs-lookup"><span data-stu-id="e264e-204">Header</span></span><br/>                   | <dl> <span data-ttu-id="e264e-205"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e264e-205"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e264e-206">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e264e-206">Type library</span></span><br/>             | <dl> <span data-ttu-id="e264e-207"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e264e-207"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e264e-208">DLL</span><span class="sxs-lookup"><span data-stu-id="e264e-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e264e-209"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e264e-209"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e264e-210">CLSID</span><span class="sxs-lookup"><span data-stu-id="e264e-210">CLSID</span></span><br/>                    | <span data-ttu-id="e264e-211">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="e264e-211">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="e264e-212">IID</span><span class="sxs-lookup"><span data-stu-id="e264e-212">IID</span></span><br/>                      | <span data-ttu-id="e264e-213">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="e264e-213">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="e264e-214">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e264e-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e264e-215">**свбемобжектекс**</span><span class="sxs-lookup"><span data-stu-id="e264e-215">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="e264e-216">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="e264e-216">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

