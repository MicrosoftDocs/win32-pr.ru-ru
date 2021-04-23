---
description: Представляет коллекцию объектов ExtendedProperty.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: Объект расширенных свойств
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648821"
---
# <a name="extendedproperties-object"></a><span data-ttu-id="3139e-103">Объект расширенных свойств</span><span class="sxs-lookup"><span data-stu-id="3139e-103">ExtendedProperties object</span></span>

<span data-ttu-id="3139e-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3139e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3139e-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функции Win32 API [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) и получения свойств.</span><span class="sxs-lookup"><span data-stu-id="3139e-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="3139e-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="3139e-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="3139e-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="3139e-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="3139e-108">Объект **расширенных свойств** представляет коллекцию объектов [**ExtendedProperty**](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="3139e-108">The **ExtendedProperties** object represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span> <span data-ttu-id="3139e-109">Каждый объект представляет одно расширенное свойство.</span><span class="sxs-lookup"><span data-stu-id="3139e-109">Each object represents a single extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="3139e-110">Назначение</span><span class="sxs-lookup"><span data-stu-id="3139e-110">When to use</span></span>

<span data-ttu-id="3139e-111">Объект **расширенных свойств** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="3139e-111">The **ExtendedProperties** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="3139e-112">Добавьте или удалите объект [**ExtendedProperty**](extendedproperty.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="3139e-112">Add or remove an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="3139e-113">Получение числа расширенных свойств в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3139e-113">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="3139e-114">Извлечение конкретного объекта [**ExtendedProperty**](extendedproperty.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="3139e-114">Retrieve a specific [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="3139e-115">Выполните итерацию по коллекции.</span><span class="sxs-lookup"><span data-stu-id="3139e-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="3139e-116">Элементы</span><span class="sxs-lookup"><span data-stu-id="3139e-116">Members</span></span>

<span data-ttu-id="3139e-117">Объект **расширенных свойств** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3139e-117">The **ExtendedProperties** object has these types of members:</span></span>

-   [<span data-ttu-id="3139e-118">Методы</span><span class="sxs-lookup"><span data-stu-id="3139e-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="3139e-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="3139e-119">Properties</span></span>](#extendedproperties-object)

### <a name="methods"></a><span data-ttu-id="3139e-120">Методы</span><span class="sxs-lookup"><span data-stu-id="3139e-120">Methods</span></span>

<span data-ttu-id="3139e-121">Объект **расширенных свойств** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="3139e-121">The **ExtendedProperties** object has these methods.</span></span>



| <span data-ttu-id="3139e-122">Метод</span><span class="sxs-lookup"><span data-stu-id="3139e-122">Method</span></span>                                      | <span data-ttu-id="3139e-123">Описание</span><span class="sxs-lookup"><span data-stu-id="3139e-123">Description</span></span>                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3139e-124">**Включить**</span><span class="sxs-lookup"><span data-stu-id="3139e-124">**Add**</span></span>](extendedproperties-add.md)       | <span data-ttu-id="3139e-125">Добавляет объект [**ExtendedProperty**](extendedproperty.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="3139e-125">Adds an [**ExtendedProperty**](extendedproperty.md) object to the collection.</span></span><br/>      |
| [<span data-ttu-id="3139e-126">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="3139e-126">**Remove**</span></span>](extendedproperties-remove.md) | <span data-ttu-id="3139e-127">Удаляет объект [**ExtendedProperty**](extendedproperty.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="3139e-127">Removes an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3139e-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="3139e-128">Properties</span></span>

<span data-ttu-id="3139e-129">Объект **расширенных свойств** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3139e-129">The **ExtendedProperties** object has these properties.</span></span>



| <span data-ttu-id="3139e-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="3139e-130">Property</span></span>                                                   | <span data-ttu-id="3139e-131">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="3139e-131">Access type</span></span>          | <span data-ttu-id="3139e-132">Описание</span><span class="sxs-lookup"><span data-stu-id="3139e-132">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3139e-133">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="3139e-133">**\_NewEnum**</span></span>](extendedproperties-newenum.md)<br/> | <span data-ttu-id="3139e-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3139e-134">Read-only</span></span><br/> | <span data-ttu-id="3139e-135">Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="3139e-135">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="3139e-136">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="3139e-136">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="3139e-137">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="3139e-137">**Count**</span></span>](extendedproperties-count.md)<br/>       | <span data-ttu-id="3139e-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3139e-138">Read-only</span></span><br/> | <span data-ttu-id="3139e-139">Возвращает число объектов [**ExtendedProperty**](extendedproperty.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3139e-139">Retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="3139e-140">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3139e-140">**Item**</span></span>](extendedproperties-item.md)<br/>         | <span data-ttu-id="3139e-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3139e-141">Read-only</span></span><br/> | <span data-ttu-id="3139e-142">Извлекает объект [**ExtendedProperty**](extendedproperty.md) , представляющий индексированное расширенное свойство коллекции.</span><span class="sxs-lookup"><span data-stu-id="3139e-142">Retrieves an [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span> <span data-ttu-id="3139e-143">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3139e-143">This is the default property.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="3139e-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3139e-144">Remarks</span></span>

<span data-ttu-id="3139e-145">Не удается создать объект **расширенных свойств** .</span><span class="sxs-lookup"><span data-stu-id="3139e-145">The **ExtendedProperties** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="3139e-146">Требования</span><span class="sxs-lookup"><span data-stu-id="3139e-146">Requirements</span></span>



| <span data-ttu-id="3139e-147">Требование</span><span class="sxs-lookup"><span data-stu-id="3139e-147">Requirement</span></span> | <span data-ttu-id="3139e-148">Значение</span><span class="sxs-lookup"><span data-stu-id="3139e-148">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3139e-149">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3139e-149">End of client support</span></span><br/> | <span data-ttu-id="3139e-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3139e-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3139e-151">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="3139e-151">End of server support</span></span><br/> | <span data-ttu-id="3139e-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3139e-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3139e-153">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="3139e-153">Redistributable</span></span><br/>       | <span data-ttu-id="3139e-154">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="3139e-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3139e-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3139e-155">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3139e-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3139e-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
