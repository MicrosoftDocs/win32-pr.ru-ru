---
description: Представляет коллекцию объектов Attribute.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Объект Attributes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665422"
---
# <a name="attributes-object"></a><span data-ttu-id="15c8d-103">Объект Attributes</span><span class="sxs-lookup"><span data-stu-id="15c8d-103">Attributes object</span></span>

<span data-ttu-id="15c8d-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="15c8d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="15c8d-105">Вместо этого используйте [**класс криптографикаттрибутеобжектколлектион**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="15c8d-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="15c8d-106">Объект **Attributes** представляет коллекцию объектов [**Attribute**](attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="15c8d-106">The **Attributes** object represents a collection of [**Attribute**](attribute.md) objects.</span></span> <span data-ttu-id="15c8d-107">Каждый объект [**атрибута**](attribute.md) представляет один атрибут сообщения.</span><span class="sxs-lookup"><span data-stu-id="15c8d-107">Each [**Attribute**](attribute.md) object represents a single attribute of a message.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="15c8d-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="15c8d-108">When to use</span></span>

<span data-ttu-id="15c8d-109">Объект **Attributes** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="15c8d-109">The **Attributes** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="15c8d-110">Добавление или удаление определенного объекта [**атрибута**](attribute.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="15c8d-110">Add or remove a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="15c8d-111">Очистите коллекцию.</span><span class="sxs-lookup"><span data-stu-id="15c8d-111">Clear the collection.</span></span>
-   <span data-ttu-id="15c8d-112">Получение числа атрибутов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="15c8d-112">Retrieve the number of attributes in the collection.</span></span>
-   <span data-ttu-id="15c8d-113">Извлечение определенного объекта [**атрибута**](attribute.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="15c8d-113">Retrieve a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="15c8d-114">Выполните итерацию по коллекции.</span><span class="sxs-lookup"><span data-stu-id="15c8d-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="15c8d-115">Элементы</span><span class="sxs-lookup"><span data-stu-id="15c8d-115">Members</span></span>

<span data-ttu-id="15c8d-116">Объект **Attributes** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="15c8d-116">The **Attributes** object has these types of members:</span></span>

-   [<span data-ttu-id="15c8d-117">Методы</span><span class="sxs-lookup"><span data-stu-id="15c8d-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="15c8d-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="15c8d-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="15c8d-119">Методы</span><span class="sxs-lookup"><span data-stu-id="15c8d-119">Methods</span></span>

<span data-ttu-id="15c8d-120">Объект **Attributes** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="15c8d-120">The **Attributes** object has these methods.</span></span>



| <span data-ttu-id="15c8d-121">Метод</span><span class="sxs-lookup"><span data-stu-id="15c8d-121">Method</span></span>                              | <span data-ttu-id="15c8d-122">Описание</span><span class="sxs-lookup"><span data-stu-id="15c8d-122">Description</span></span>                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="15c8d-123">**Включить**</span><span class="sxs-lookup"><span data-stu-id="15c8d-123">**Add**</span></span>](attributes-add.md)       | <span data-ttu-id="15c8d-124">Добавляет объект [**атрибута**](attribute.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="15c8d-124">Adds an [**Attribute**](attribute.md) object to the collection.</span></span><br/>       |
| [<span data-ttu-id="15c8d-125">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="15c8d-125">**Clear**</span></span>](attributes-clear.md)   | <span data-ttu-id="15c8d-126">Удаляет все объекты [**атрибутов**](attribute.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="15c8d-126">Clears all [**Attribute**](attribute.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="15c8d-127">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="15c8d-127">**Remove**</span></span>](attributes-remove.md) | <span data-ttu-id="15c8d-128">Удаляет объект [**атрибута**](attribute.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="15c8d-128">Removes an [**Attribute**](attribute.md) object from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="15c8d-129">Свойства</span><span class="sxs-lookup"><span data-stu-id="15c8d-129">Properties</span></span>

<span data-ttu-id="15c8d-130">Объект **Attributes** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="15c8d-130">The **Attributes** object has these properties.</span></span>



| <span data-ttu-id="15c8d-131">Свойство</span><span class="sxs-lookup"><span data-stu-id="15c8d-131">Property</span></span>                                           | <span data-ttu-id="15c8d-132">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="15c8d-132">Access type</span></span>          | <span data-ttu-id="15c8d-133">Описание</span><span class="sxs-lookup"><span data-stu-id="15c8d-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15c8d-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="15c8d-134">**\_NewEnum**</span></span>](attributes-newenum.md)<br/> | <span data-ttu-id="15c8d-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="15c8d-135">Read-only</span></span><br/> | <span data-ttu-id="15c8d-136">Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="15c8d-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="15c8d-137">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="15c8d-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="15c8d-138">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="15c8d-138">**Count**</span></span>](attributes-count.md)<br/>       | <span data-ttu-id="15c8d-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="15c8d-139">Read-only</span></span><br/> | <span data-ttu-id="15c8d-140">Возвращает количество объектов [**атрибутов**](attribute.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="15c8d-140">Retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="15c8d-141">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="15c8d-141">**Item**</span></span>](attributes-item.md)<br/>         | <span data-ttu-id="15c8d-142">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="15c8d-142">Read-only</span></span><br/> | <span data-ttu-id="15c8d-143">Извлекает объект [**атрибута**](attribute.md) , представляющий индексированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="15c8d-143">Retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="15c8d-144">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15c8d-144">This is the default property.</span></span><br/>                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="15c8d-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15c8d-145">Remarks</span></span>

<span data-ttu-id="15c8d-146">Не удается создать объект **атрибутов** .</span><span class="sxs-lookup"><span data-stu-id="15c8d-146">The **Attributes** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="15c8d-147">Требования</span><span class="sxs-lookup"><span data-stu-id="15c8d-147">Requirements</span></span>



| <span data-ttu-id="15c8d-148">Требование</span><span class="sxs-lookup"><span data-stu-id="15c8d-148">Requirement</span></span> | <span data-ttu-id="15c8d-149">Значение</span><span class="sxs-lookup"><span data-stu-id="15c8d-149">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15c8d-150">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="15c8d-150">End of client support</span></span><br/> | <span data-ttu-id="15c8d-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15c8d-151">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="15c8d-152">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="15c8d-152">End of server support</span></span><br/> | <span data-ttu-id="15c8d-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15c8d-153">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="15c8d-154">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="15c8d-154">Redistributable</span></span><br/>       | <span data-ttu-id="15c8d-155">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="15c8d-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="15c8d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="15c8d-156">DLL</span></span><br/>                   | <dl> <span data-ttu-id="15c8d-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15c8d-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15c8d-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15c8d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c8d-159">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="15c8d-159">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
