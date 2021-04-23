---
description: Предоставляет свойства и методы, которые можно использовать для выбора, управления и использования хранилищ сертификатов и сертификатов в этих хранилищах.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Объект Store
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648859"
---
# <a name="store-object"></a><span data-ttu-id="4315c-103">Объект Store</span><span class="sxs-lookup"><span data-stu-id="4315c-103">Store object</span></span>

<span data-ttu-id="4315c-104">\[Объект **Store** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4315c-104">\[The **Store** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4315c-105">Вместо этого используйте [**класс X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4315c-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4315c-106">Объект **Store** предоставляет свойства и методы, которые можно использовать для выбора, управления и использования [*хранилищ сертификатов*](../secgloss/c-gly.md) и сертификатов в этих хранилищах.</span><span class="sxs-lookup"><span data-stu-id="4315c-106">The **Store** object provides properties and methods that you can use to choose, manage, and use [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="4315c-107">CAPICOM может использовать хранилища текущего пользователя, локального компьютера, памяти и Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4315c-107">CAPICOM can use Current-User, Local-Machine, memory, and Active Directory stores.</span></span> <span data-ttu-id="4315c-108">Кроме того, хранит поддержку хранилищ сертификатов на основе смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="4315c-108">Also, stores support smart card–based certificate stores.</span></span> <span data-ttu-id="4315c-109">Разработчики должны иметь в виду, что некоторые методы могут завершаться с ошибками в некоторых магазинах, если попытаются выполнить операции, для которых у пользователя нет прав.</span><span class="sxs-lookup"><span data-stu-id="4315c-109">Developers should be aware that some methods may fail with some stores if operations are attempted for which the user does not have rights.</span></span>

## <a name="members"></a><span data-ttu-id="4315c-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="4315c-110">Members</span></span>

<span data-ttu-id="4315c-111">Объект **Store** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4315c-111">The **Store** object has these types of members:</span></span>

-   [<span data-ttu-id="4315c-112">Методы</span><span class="sxs-lookup"><span data-stu-id="4315c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4315c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4315c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4315c-114">Методы</span><span class="sxs-lookup"><span data-stu-id="4315c-114">Methods</span></span>

<span data-ttu-id="4315c-115">Объект **Store** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="4315c-115">The **Store** object has these methods.</span></span>



| <span data-ttu-id="4315c-116">Метод</span><span class="sxs-lookup"><span data-stu-id="4315c-116">Method</span></span>                         | <span data-ttu-id="4315c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4315c-117">Description</span></span>                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4315c-118">**Включить**</span><span class="sxs-lookup"><span data-stu-id="4315c-118">**Add**</span></span>](store-add.md)       | <span data-ttu-id="4315c-119">Добавляет объект [**сертификата**](certificate.md) в открытое хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="4315c-119">Adds a [**Certificate**](certificate.md) object to the open certificate store.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="4315c-120">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="4315c-120">**Close**</span></span>](store-close.md)   | <span data-ttu-id="4315c-121">Закрывает открытое хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="4315c-121">Closes an open certificate store.</span></span><br/> <span data-ttu-id="4315c-122">**CAPICOM 2.0.0.3 и более ранние версии:** Метод [**Close**](store-close.md) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4315c-122">**CAPICOM 2.0.0.3 and earlier:** The [**Close**](store-close.md) method is not supported.</span></span><br/>                                                               |
| [<span data-ttu-id="4315c-123">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="4315c-123">**Delete**</span></span>](store-delete.md) | <span data-ttu-id="4315c-124">Удаляет хранилище сертификатов, представленное текущим объектом [**хранилища**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="4315c-124">Deletes the certificate store represented by the current [**Store**](certificate.md) object.</span></span><br/> <span data-ttu-id="4315c-125">**CAPICOM 2.0.0.3 и более ранние версии:** Метод [**Delete**](store-delete.md) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4315c-125">**CAPICOM 2.0.0.3 and earlier:** The [**Delete**](store-delete.md) method is not supported.</span></span><br/> |
| [<span data-ttu-id="4315c-126">**Экспорт**</span><span class="sxs-lookup"><span data-stu-id="4315c-126">**Export**</span></span>](store-export.md) | <span data-ttu-id="4315c-127">Экспортирует хранилище закодированного [*большого двоичного объекта*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4315c-127">Exports the store of an encoded [*BLOB*](../secgloss/b-gly.md).</span></span><br/>                                                                                                       |
| [<span data-ttu-id="4315c-128">**Импорт**</span><span class="sxs-lookup"><span data-stu-id="4315c-128">**Import**</span></span>](store-import.md) | <span data-ttu-id="4315c-129">Импортирует ранее экспортированное хранилище.</span><span class="sxs-lookup"><span data-stu-id="4315c-129">Imports a previously exported store.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="4315c-130">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="4315c-130">**Load**</span></span>](store-load.md)     | <span data-ttu-id="4315c-131">Импортирует объекты [**сертификата**](certificate.md) из файла в хранилище.</span><span class="sxs-lookup"><span data-stu-id="4315c-131">Imports [**Certificate**](certificate.md) objects from a file into the store.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="4315c-132">**Открыт**</span><span class="sxs-lookup"><span data-stu-id="4315c-132">**Open**</span></span>](store-open.md)     | <span data-ttu-id="4315c-133">Открывает хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="4315c-133">Opens a certificate store.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="4315c-134">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="4315c-134">**Remove**</span></span>](store-remove.md) | <span data-ttu-id="4315c-135">Удаляет объект [**сертификата**](certificate.md) из открытого хранилища.</span><span class="sxs-lookup"><span data-stu-id="4315c-135">Removes a [**Certificate**](certificate.md) object from an open store.</span></span><br/>                                                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="4315c-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="4315c-136">Properties</span></span>

<span data-ttu-id="4315c-137">Объект **Store** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="4315c-137">The **Store** object has these properties.</span></span>



| <span data-ttu-id="4315c-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="4315c-138">Property</span></span>                                              | <span data-ttu-id="4315c-139">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="4315c-139">Access type</span></span>          | <span data-ttu-id="4315c-140">Описание</span><span class="sxs-lookup"><span data-stu-id="4315c-140">Description</span></span>                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4315c-141">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="4315c-141">**Certificates**</span></span>](store-certificates.md)<br/> | <span data-ttu-id="4315c-142">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4315c-142">Read-only</span></span><br/> | <span data-ttu-id="4315c-143">Извлекает коллекцию [**сертификатов**](certificates.md) хранилища.</span><span class="sxs-lookup"><span data-stu-id="4315c-143">Retrieves the [**Certificates**](certificates.md) collection of the store.</span></span> <span data-ttu-id="4315c-144">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4315c-144">This is the default property.</span></span><br/>                                                                                  |
| [<span data-ttu-id="4315c-145">**Расположение**</span><span class="sxs-lookup"><span data-stu-id="4315c-145">**Location**</span></span>](store-location.md)<br/>         | <span data-ttu-id="4315c-146">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4315c-146">Read-only</span></span><br/> | <span data-ttu-id="4315c-147">Извлекает расположение хранилища сертификатов, которое представляет этот объект.</span><span class="sxs-lookup"><span data-stu-id="4315c-147">Retrieves the location of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="4315c-148">**CAPICOM 2.0.0.3 и более ранние версии:** Свойство [**Location**](store-location.md) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4315c-148">**CAPICOM 2.0.0.3 and earlier:** The [**Location**](store-location.md) property is not supported.</span></span><br/> |
| [<span data-ttu-id="4315c-149">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4315c-149">**Name**</span></span>](store-name.md)<br/>                 | <span data-ttu-id="4315c-150">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4315c-150">Read-only</span></span><br/> | <span data-ttu-id="4315c-151">Возвращает имя хранилища сертификатов, которое представляет этот объект.</span><span class="sxs-lookup"><span data-stu-id="4315c-151">Retrieves the name of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="4315c-152">**CAPICOM 2.0.0.3 и более ранние версии:** Свойство [**Name**](store-name.md) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4315c-152">**CAPICOM 2.0.0.3 and earlier:** The [**Name**](store-name.md) property is not supported.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="4315c-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4315c-153">Remarks</span></span>

<span data-ttu-id="4315c-154">Объект **Store** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="4315c-154">The **Store** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="4315c-155">Идентификатор ProgID для объекта **Store** — CAPICOM. Store. 2.</span><span class="sxs-lookup"><span data-stu-id="4315c-155">The ProgID for the **Store** object is CAPICOM.Store.2.</span></span>

<span data-ttu-id="4315c-156">**CAPICOM 1. *x*:** идентификатор ProgID для объекта **Store** — CAPICOM. Store. 1.</span><span class="sxs-lookup"><span data-stu-id="4315c-156">**CAPICOM 1.*x*:** The ProgID for the **Store** object is CAPICOM.Store.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="4315c-157">Требования</span><span class="sxs-lookup"><span data-stu-id="4315c-157">Requirements</span></span>



| <span data-ttu-id="4315c-158">Требование</span><span class="sxs-lookup"><span data-stu-id="4315c-158">Requirement</span></span> | <span data-ttu-id="4315c-159">Значение</span><span class="sxs-lookup"><span data-stu-id="4315c-159">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4315c-160">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="4315c-160">Redistributable</span></span><br/> | <span data-ttu-id="4315c-161">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="4315c-161">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4315c-162">DLL</span><span class="sxs-lookup"><span data-stu-id="4315c-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="4315c-163"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4315c-163"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4315c-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4315c-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4315c-165">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="4315c-165">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
