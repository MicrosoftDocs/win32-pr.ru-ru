---
description: Представляет коллекцию объектов OID.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: OID, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685176"
---
# <a name="oids-object"></a><span data-ttu-id="14591-103">OID, объект</span><span class="sxs-lookup"><span data-stu-id="14591-103">OIDs object</span></span>

<span data-ttu-id="14591-104">\[Объект **OID** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="14591-104">\[The **OIDs** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="14591-105">Вместо этого используйте [**класс оидколлектион**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="14591-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="14591-106">Объект **OID** представляет коллекцию объектов [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="14591-106">The **OIDs** object represents a collection of [**OID**](oid.md) objects.</span></span> <span data-ttu-id="14591-107">Каждый объект [**OID**](oid.md) представляет один идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="14591-107">Each [**OID**](oid.md) object represents a single object identifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="14591-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="14591-108">When to use</span></span>

<span data-ttu-id="14591-109">Объект **OID** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="14591-109">The **OIDs** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="14591-110">Добавьте или удалите объект [**OID**](oid.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="14591-110">Add or remove an [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="14591-111">Очистить все объекты [**OID**](oid.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="14591-111">Clear all the [**OID**](oid.md) objects from the collection.</span></span>
-   <span data-ttu-id="14591-112">Получение числа идентификаторов объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="14591-112">Retrieve the number of object identifiers in the collection.</span></span>
-   <span data-ttu-id="14591-113">Получение определенного объекта [**OID**](oid.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="14591-113">Retrieve a specific [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="14591-114">Выполните итерацию по коллекции.</span><span class="sxs-lookup"><span data-stu-id="14591-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="14591-115">Элементы</span><span class="sxs-lookup"><span data-stu-id="14591-115">Members</span></span>

<span data-ttu-id="14591-116">Объект **OID** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="14591-116">The **OIDs** object has these types of members:</span></span>

-   [<span data-ttu-id="14591-117">Методы</span><span class="sxs-lookup"><span data-stu-id="14591-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="14591-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="14591-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="14591-119">Методы</span><span class="sxs-lookup"><span data-stu-id="14591-119">Methods</span></span>

<span data-ttu-id="14591-120">Объект **OID** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="14591-120">The **OIDs** object has these methods.</span></span>



| <span data-ttu-id="14591-121">Метод</span><span class="sxs-lookup"><span data-stu-id="14591-121">Method</span></span>                        | <span data-ttu-id="14591-122">Описание</span><span class="sxs-lookup"><span data-stu-id="14591-122">Description</span></span>                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="14591-123">**Включить**</span><span class="sxs-lookup"><span data-stu-id="14591-123">**Add**</span></span>](oids-add.md)       | <span data-ttu-id="14591-124">Добавляет объект [**OID**](oid.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="14591-124">Adds an [**OID**](oid.md) object to the collection.</span></span><br/>              |
| [<span data-ttu-id="14591-125">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="14591-125">**Clear**</span></span>](oids-clear.md)   | <span data-ttu-id="14591-126">Удаляет все объекты [**OID**](oid.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="14591-126">Clears all [**OID**](oid.md) objects from the collection.</span></span><br/>        |
| [<span data-ttu-id="14591-127">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="14591-127">**Remove**</span></span>](oids-remove.md) | <span data-ttu-id="14591-128">Удаляет индексируемый объект [**OID**](oid.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="14591-128">Removes an indexed [**OID**](oid.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="14591-129">Свойства</span><span class="sxs-lookup"><span data-stu-id="14591-129">Properties</span></span>

<span data-ttu-id="14591-130">Объект **OID** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="14591-130">The **OIDs** object has these properties.</span></span>



| <span data-ttu-id="14591-131">Свойство</span><span class="sxs-lookup"><span data-stu-id="14591-131">Property</span></span>                                     | <span data-ttu-id="14591-132">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="14591-132">Access type</span></span>          | <span data-ttu-id="14591-133">Описание</span><span class="sxs-lookup"><span data-stu-id="14591-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14591-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="14591-134">**\_NewEnum**</span></span>](oids-newenum.md)<br/> | <span data-ttu-id="14591-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="14591-135">Read-only</span></span><br/> | <span data-ttu-id="14591-136">Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="14591-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="14591-137">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="14591-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="14591-138">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="14591-138">**Count**</span></span>](oids-count.md)<br/>       | <span data-ttu-id="14591-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="14591-139">Read-only</span></span><br/> | <span data-ttu-id="14591-140">Возвращает число объектов [**OID**](oid.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="14591-140">Retrieves the number of [**OID**](oid.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="14591-141">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="14591-141">**Item**</span></span>](oids-item.md)<br/>         | <span data-ttu-id="14591-142">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="14591-142">Read-only</span></span><br/> | <span data-ttu-id="14591-143">Извлекает индексируемый объект [**OID**](oid.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="14591-143">Retrieves an indexed [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="14591-144">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14591-144">This is the default property.</span></span><br/>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="14591-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14591-145">Remarks</span></span>

<span data-ttu-id="14591-146">Не удается создать объект **OID** .</span><span class="sxs-lookup"><span data-stu-id="14591-146">The **OIDs** object cannot be created.</span></span>

<span data-ttu-id="14591-147">Объект **OID** используется следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="14591-147">The **OIDs** object is used by the following properties:</span></span>

-   [<span data-ttu-id="14591-148">**Цертификатестатус. АппликатионполиЦиес**</span><span class="sxs-lookup"><span data-stu-id="14591-148">**CertificateStatus.ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md)
-   [<span data-ttu-id="14591-149">**Цертификатестатус. ЦертификатеполиЦиес**</span><span class="sxs-lookup"><span data-stu-id="14591-149">**CertificateStatus.CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a><span data-ttu-id="14591-150">Требования</span><span class="sxs-lookup"><span data-stu-id="14591-150">Requirements</span></span>



| <span data-ttu-id="14591-151">Требование</span><span class="sxs-lookup"><span data-stu-id="14591-151">Requirement</span></span> | <span data-ttu-id="14591-152">Значение</span><span class="sxs-lookup"><span data-stu-id="14591-152">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14591-153">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="14591-153">Redistributable</span></span><br/> | <span data-ttu-id="14591-154">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="14591-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="14591-155">DLL</span><span class="sxs-lookup"><span data-stu-id="14591-155">DLL</span></span><br/>             | <dl> <span data-ttu-id="14591-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14591-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
