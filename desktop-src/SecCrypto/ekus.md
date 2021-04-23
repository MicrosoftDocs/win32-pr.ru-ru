---
description: Представляет коллекцию объектов EKU.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: Объект EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669101"
---
# <a name="ekus-object"></a><span data-ttu-id="f71a9-103">Объект EKU</span><span class="sxs-lookup"><span data-stu-id="f71a9-103">EKUs object</span></span>

<span data-ttu-id="f71a9-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f71a9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f71a9-105">Вместо этого используйте [**класс X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f71a9-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f71a9-106">Объект **EKU** представляет коллекцию объектов [**EKU**](eku.md) .</span><span class="sxs-lookup"><span data-stu-id="f71a9-106">The **EKUs** object represents a collection of [**EKU**](eku.md) objects.</span></span> <span data-ttu-id="f71a9-107">Каждый объект [**EKU**](eku.md) представляет одно свойство расширенного использования ключа (EKU) сертификата.</span><span class="sxs-lookup"><span data-stu-id="f71a9-107">Each [**EKU**](eku.md) object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="f71a9-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="f71a9-108">When to use</span></span>

<span data-ttu-id="f71a9-109">Коллекция **EKU** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="f71a9-109">The **EKUs** collection is used to perform the following tasks:</span></span>

-   <span data-ttu-id="f71a9-110">Получение числа свойств EKU в коллекции.</span><span class="sxs-lookup"><span data-stu-id="f71a9-110">Retrieve the number of EKU properties in the collection.</span></span>
-   <span data-ttu-id="f71a9-111">Получение определенного объекта [**EKU**](eku.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="f71a9-111">Retrieve a specific [**EKU**](eku.md) object from the collection.</span></span>
-   <span data-ttu-id="f71a9-112">Выполните итерацию по коллекции.</span><span class="sxs-lookup"><span data-stu-id="f71a9-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="f71a9-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="f71a9-113">Members</span></span>

<span data-ttu-id="f71a9-114">Объект **EKU** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f71a9-114">The **EKUs** object has these types of members:</span></span>

-   [<span data-ttu-id="f71a9-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="f71a9-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f71a9-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="f71a9-116">Properties</span></span>

<span data-ttu-id="f71a9-117">Объект **EKU** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f71a9-117">The **EKUs** object has these properties.</span></span>



| <span data-ttu-id="f71a9-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="f71a9-118">Property</span></span>                                     | <span data-ttu-id="f71a9-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="f71a9-119">Access type</span></span>          | <span data-ttu-id="f71a9-120">Описание</span><span class="sxs-lookup"><span data-stu-id="f71a9-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f71a9-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="f71a9-121">**\_NewEnum**</span></span>](ekus-newenum.md)<br/> | <span data-ttu-id="f71a9-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f71a9-122">Read-only</span></span><br/> | <span data-ttu-id="f71a9-123">Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="f71a9-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="f71a9-124">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="f71a9-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="f71a9-125">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="f71a9-125">**Count**</span></span>](ekus-count.md)<br/>       | <span data-ttu-id="f71a9-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f71a9-126">Read-only</span></span><br/> | <span data-ttu-id="f71a9-127">Возвращает число объектов [**EKU**](eku.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="f71a9-127">Retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="f71a9-128">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f71a9-128">**Item**</span></span>](ekus-item.md)<br/>         | <span data-ttu-id="f71a9-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f71a9-129">Read-only</span></span><br/> | <span data-ttu-id="f71a9-130">Извлекает объект [**EKU**](eku.md) , представляющий свойство индексированного EKU.</span><span class="sxs-lookup"><span data-stu-id="f71a9-130">Retrieves the [**EKU**](eku.md) object that represents the indexed EKU property.</span></span> <span data-ttu-id="f71a9-131">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f71a9-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="f71a9-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f71a9-132">Remarks</span></span>

<span data-ttu-id="f71a9-133">Эта коллекция извлекается с помощью свойства [**екстендедкэйусаже. EKU**](extendedkeyusage-ekus.md) .</span><span class="sxs-lookup"><span data-stu-id="f71a9-133">This collection is retrieved by the [**ExtendedKeyUsage.EKUs**](extendedkeyusage-ekus.md) property.</span></span>

<span data-ttu-id="f71a9-134">Не удается создать объект **EKU** .</span><span class="sxs-lookup"><span data-stu-id="f71a9-134">The **EKUs** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="f71a9-135">Требования</span><span class="sxs-lookup"><span data-stu-id="f71a9-135">Requirements</span></span>



| <span data-ttu-id="f71a9-136">Требование</span><span class="sxs-lookup"><span data-stu-id="f71a9-136">Requirement</span></span> | <span data-ttu-id="f71a9-137">Значение</span><span class="sxs-lookup"><span data-stu-id="f71a9-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f71a9-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f71a9-138">End of client support</span></span><br/> | <span data-ttu-id="f71a9-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f71a9-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f71a9-140">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f71a9-140">End of server support</span></span><br/> | <span data-ttu-id="f71a9-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f71a9-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f71a9-142">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f71a9-142">Redistributable</span></span><br/>       | <span data-ttu-id="f71a9-143">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="f71a9-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f71a9-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f71a9-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f71a9-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f71a9-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
