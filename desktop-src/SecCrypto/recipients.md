---
description: Представляет коллекцию объектов Certificate.
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Объект Recipients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c68ca0217631970f35680160b71841f758b13fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685091"
---
# <a name="recipients-object"></a><span data-ttu-id="28cd1-103">Объект Recipients</span><span class="sxs-lookup"><span data-stu-id="28cd1-103">Recipients object</span></span>

<span data-ttu-id="28cd1-104">\[Объект **Recipients** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="28cd1-104">\[The **Recipients** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="28cd1-105">Вместо этого используйте [**класс кмсреЦипиентколлектион**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="28cd1-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="28cd1-106">Объект **Recipients** представляет коллекцию объектов [**Certificate**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="28cd1-106">The **Recipients** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="28cd1-107">Каждый объект представляет предполагаемого получателя сообщения, переданного в оболочке.</span><span class="sxs-lookup"><span data-stu-id="28cd1-107">Each object represents an intended recipient of the enveloped message.</span></span> <span data-ttu-id="28cd1-108">Данные в объекте [**енвелопеддата**](envelopeddata.md) шифруются с помощью [*симметричного*](../secgloss/s-gly.md) ключа сеанса, и этот симметричный ключ сеанса затем шифруется для каждого получателя с помощью открытого ключа из этого предполагаемого сертификата получателя.</span><span class="sxs-lookup"><span data-stu-id="28cd1-108">Data in an [**EnvelopedData**](envelopeddata.md) object is encrypted with a [*symmetric*](../secgloss/s-gly.md) session key, and that symmetric session key is then itself encrypted for each recipient by using the public key from that intended recipient's certificate.</span></span> <span data-ttu-id="28cd1-109">Получатель с доступом к [*закрытому ключу*](../secgloss/p-gly.md) , связанному с [*открытым ключом*](../secgloss/p-gly.md) сертификата, может расшифровать [*ключ сеанса*](../secgloss/s-gly.md) и использовать расшифрованный ключ сеанса для расшифровки фактических данных.</span><span class="sxs-lookup"><span data-stu-id="28cd1-109">A recipient with access to the [*private key*](../secgloss/p-gly.md) associated with a certificate's [*public key*](../secgloss/p-gly.md) can decrypt the [*session key*](../secgloss/s-gly.md) and use the decrypted session key to decrypt the actual data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="28cd1-110">Назначение</span><span class="sxs-lookup"><span data-stu-id="28cd1-110">When to use</span></span>

<span data-ttu-id="28cd1-111">Объект **Recipients** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="28cd1-111">The **Recipients** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="28cd1-112">Добавьте или удалите объект [**сертификата**](certificate.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="28cd1-112">Add or remove a [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="28cd1-113">Получение числа сертификатов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="28cd1-113">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="28cd1-114">Извлечение конкретного объекта **получателей** из коллекции.</span><span class="sxs-lookup"><span data-stu-id="28cd1-114">Retrieve a specific **Recipients** object from the collection.</span></span>
-   <span data-ttu-id="28cd1-115">Выполните итерацию по коллекции.</span><span class="sxs-lookup"><span data-stu-id="28cd1-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="28cd1-116">Элементы</span><span class="sxs-lookup"><span data-stu-id="28cd1-116">Members</span></span>

<span data-ttu-id="28cd1-117">Объекты **получателей** имеют следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="28cd1-117">The **Recipients** object has these types of members:</span></span>

-   [<span data-ttu-id="28cd1-118">Методы</span><span class="sxs-lookup"><span data-stu-id="28cd1-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="28cd1-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="28cd1-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="28cd1-120">Методы</span><span class="sxs-lookup"><span data-stu-id="28cd1-120">Methods</span></span>

<span data-ttu-id="28cd1-121">Объект **Recipients** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="28cd1-121">The **Recipients** object has these methods.</span></span>



| <span data-ttu-id="28cd1-122">Метод</span><span class="sxs-lookup"><span data-stu-id="28cd1-122">Method</span></span>                              | <span data-ttu-id="28cd1-123">Описание</span><span class="sxs-lookup"><span data-stu-id="28cd1-123">Description</span></span>                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="28cd1-124">**Включить**</span><span class="sxs-lookup"><span data-stu-id="28cd1-124">**Add**</span></span>](recipients-add.md)       | <span data-ttu-id="28cd1-125">Добавляет объект [**сертификата**](certificate.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="28cd1-125">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/>         |
| [<span data-ttu-id="28cd1-126">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="28cd1-126">**Clear**</span></span>](recipients-clear.md)   | <span data-ttu-id="28cd1-127">Удаляет все объекты [**сертификата**](certificate.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="28cd1-127">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="28cd1-128">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="28cd1-128">**Remove**</span></span>](recipients-remove.md) | <span data-ttu-id="28cd1-129">Удаляет объект [**сертификата**](certificate.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="28cd1-129">Removes a [**Certificate**](certificate.md) object from the collection.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="28cd1-130">Свойства</span><span class="sxs-lookup"><span data-stu-id="28cd1-130">Properties</span></span>

<span data-ttu-id="28cd1-131">Объект **Recipients** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="28cd1-131">The **Recipients** object has these properties.</span></span>



| <span data-ttu-id="28cd1-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="28cd1-132">Property</span></span>                                           | <span data-ttu-id="28cd1-133">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="28cd1-133">Access type</span></span>          | <span data-ttu-id="28cd1-134">Описание</span><span class="sxs-lookup"><span data-stu-id="28cd1-134">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28cd1-135">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="28cd1-135">**\_NewEnum**</span></span>](recipients-newenum.md)<br/> | <span data-ttu-id="28cd1-136">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28cd1-136">Read-only</span></span><br/> | <span data-ttu-id="28cd1-137">Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="28cd1-137">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="28cd1-138">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="28cd1-138">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="28cd1-139">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="28cd1-139">**Count**</span></span>](recipients-count.md)<br/>       |                      | <span data-ttu-id="28cd1-140">Число объектов в коллекции **получателей** .</span><span class="sxs-lookup"><span data-stu-id="28cd1-140">The number of objects in the **Recipients** collection.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="28cd1-141">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="28cd1-141">**Item**</span></span>](recipients-item.md)<br/>         |                      | <span data-ttu-id="28cd1-142">Индексированный объект в коллекции.</span><span class="sxs-lookup"><span data-stu-id="28cd1-142">An indexed object in the collection.</span></span> <span data-ttu-id="28cd1-143">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="28cd1-143">This is the default property.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="28cd1-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28cd1-144">Remarks</span></span>

<span data-ttu-id="28cd1-145">Не удается создать объект **получателей** .</span><span class="sxs-lookup"><span data-stu-id="28cd1-145">The **Recipients** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="28cd1-146">Требования</span><span class="sxs-lookup"><span data-stu-id="28cd1-146">Requirements</span></span>



| <span data-ttu-id="28cd1-147">Требование</span><span class="sxs-lookup"><span data-stu-id="28cd1-147">Requirement</span></span> | <span data-ttu-id="28cd1-148">Значение</span><span class="sxs-lookup"><span data-stu-id="28cd1-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28cd1-149">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="28cd1-149">Redistributable</span></span><br/> | <span data-ttu-id="28cd1-150">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="28cd1-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="28cd1-151">DLL</span><span class="sxs-lookup"><span data-stu-id="28cd1-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="28cd1-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28cd1-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28cd1-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28cd1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28cd1-154">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="28cd1-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
