---
description: Представляет коллекцию объектов Extension.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Объект Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668691"
---
# <a name="extensions-object"></a><span data-ttu-id="4d48d-103">Объект Extensions</span><span class="sxs-lookup"><span data-stu-id="4d48d-103">Extensions object</span></span>

<span data-ttu-id="4d48d-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4d48d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4d48d-105">Вместо этого используйте [**класс X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4d48d-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4d48d-106">Объект **Extensions** представляет коллекцию объектов [**Extension**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="4d48d-106">The **Extensions** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="4d48d-107">Каждый объект [**расширения**](extension.md) представляет одно расширение сертификата.</span><span class="sxs-lookup"><span data-stu-id="4d48d-107">Each [**Extension**](extension.md) object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4d48d-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="4d48d-108">When to use</span></span>

<span data-ttu-id="4d48d-109">Объект **Extensions** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="4d48d-109">The **Extensions** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="4d48d-110">Получение числа расширений сертификата в коллекции.</span><span class="sxs-lookup"><span data-stu-id="4d48d-110">Retrieve the number of certificate extensions in the collection.</span></span>
-   <span data-ttu-id="4d48d-111">Извлечение указанного объекта [**расширения**](extension.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="4d48d-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="4d48d-112">Выполните итерацию по коллекции.</span><span class="sxs-lookup"><span data-stu-id="4d48d-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="4d48d-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="4d48d-113">Members</span></span>

<span data-ttu-id="4d48d-114">Объект **Extensions** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4d48d-114">The **Extensions** object has these types of members:</span></span>

-   [<span data-ttu-id="4d48d-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="4d48d-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d48d-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="4d48d-116">Properties</span></span>

<span data-ttu-id="4d48d-117">Объект **Extensions** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4d48d-117">The **Extensions** object has these properties.</span></span>



| <span data-ttu-id="4d48d-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="4d48d-118">Property</span></span>                                           | <span data-ttu-id="4d48d-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="4d48d-119">Access type</span></span>          | <span data-ttu-id="4d48d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="4d48d-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d48d-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="4d48d-121">**\_NewEnum**</span></span>](extensions-newenum.md)<br/> | <span data-ttu-id="4d48d-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4d48d-122">Read-only</span></span><br/> | <span data-ttu-id="4d48d-123">Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="4d48d-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="4d48d-124">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="4d48d-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="4d48d-125">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="4d48d-125">**Count**</span></span>](extensions-count.md)<br/>       | <span data-ttu-id="4d48d-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4d48d-126">Read-only</span></span><br/> | <span data-ttu-id="4d48d-127">Возвращает число объектов [**расширения**](extension.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="4d48d-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="4d48d-128">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4d48d-128">**Item**</span></span>](extensions-item.md)<br/>         | <span data-ttu-id="4d48d-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4d48d-129">Read-only</span></span><br/> | <span data-ttu-id="4d48d-130">Извлекает объект [**расширения**](extension.md) , представляющий индексированное расширение сертификата коллекции.</span><span class="sxs-lookup"><span data-stu-id="4d48d-130">Retrieves the [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span> <span data-ttu-id="4d48d-131">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d48d-131">This is the default property.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="4d48d-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d48d-132">Remarks</span></span>

<span data-ttu-id="4d48d-133">Объект **Extensions** возвращается методом [**Certificate. Extensions**](certificate-extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="4d48d-133">The **Extensions** object is returned by the [**Certificate.Extensions**](certificate-extensions.md) method.</span></span>

<span data-ttu-id="4d48d-134">Не удается создать объект **Extensions** .</span><span class="sxs-lookup"><span data-stu-id="4d48d-134">The **Extensions** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d48d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="4d48d-135">Requirements</span></span>



| <span data-ttu-id="4d48d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="4d48d-136">Requirement</span></span> | <span data-ttu-id="4d48d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="4d48d-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d48d-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4d48d-138">End of client support</span></span><br/> | <span data-ttu-id="4d48d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d48d-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4d48d-140">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4d48d-140">End of server support</span></span><br/> | <span data-ttu-id="4d48d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d48d-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4d48d-142">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="4d48d-142">Redistributable</span></span><br/>       | <span data-ttu-id="4d48d-143">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="4d48d-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4d48d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4d48d-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4d48d-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d48d-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
