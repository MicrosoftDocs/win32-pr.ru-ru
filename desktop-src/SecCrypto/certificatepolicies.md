---
description: Коллекция объектов Полициинформатион.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Объект ЦертификатеполиЦиес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688814"
---
# <a name="certificatepolicies-object"></a><span data-ttu-id="65e26-103">Объект ЦертификатеполиЦиес</span><span class="sxs-lookup"><span data-stu-id="65e26-103">CertificatePolicies object</span></span>

<span data-ttu-id="65e26-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="65e26-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="65e26-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для получения политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="65e26-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="65e26-106">Объект **цертификатеполиЦиес** представляет коллекцию объектов [**полициинформатион**](policyinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="65e26-106">The **CertificatePolicies** object represents a collection of [**PolicyInformation**](policyinformation.md) objects.</span></span> <span data-ttu-id="65e26-107">Каждый объект [**полициинформатион**](policyinformation.md) представляет одну политику сертификата.</span><span class="sxs-lookup"><span data-stu-id="65e26-107">Each [**PolicyInformation**](policyinformation.md) object represents a single certificate policy.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="65e26-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="65e26-108">When to use</span></span>

<span data-ttu-id="65e26-109">Объект **цертификатеполиЦиес** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="65e26-109">The **CertificatePolicies** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="65e26-110">Получите количество политик сертификатов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="65e26-110">Retrieve the number of certificate policies in the collection.</span></span>
-   <span data-ttu-id="65e26-111">Извлечение конкретного объекта [**полициинформатион**](policyinformation.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="65e26-111">Retrieve a specific [**PolicyInformation**](policyinformation.md) object from the collection.</span></span>
-   <span data-ttu-id="65e26-112">Выполните итерацию по коллекции.</span><span class="sxs-lookup"><span data-stu-id="65e26-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="65e26-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="65e26-113">Members</span></span>

<span data-ttu-id="65e26-114">Объект **цертификатеполиЦиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="65e26-114">The **CertificatePolicies** object has these types of members:</span></span>

-   [<span data-ttu-id="65e26-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="65e26-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65e26-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="65e26-116">Properties</span></span>

<span data-ttu-id="65e26-117">Объект **цертификатеполиЦиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="65e26-117">The **CertificatePolicies** object has these properties.</span></span>



| <span data-ttu-id="65e26-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="65e26-118">Property</span></span>                                                    | <span data-ttu-id="65e26-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="65e26-119">Access type</span></span>          | <span data-ttu-id="65e26-120">Описание</span><span class="sxs-lookup"><span data-stu-id="65e26-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65e26-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="65e26-121">**\_NewEnum**</span></span>](certificatepolicies-newenum.md)<br/> | <span data-ttu-id="65e26-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="65e26-122">Read-only</span></span><br/> | <span data-ttu-id="65e26-123">Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="65e26-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="65e26-124">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="65e26-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="65e26-125">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="65e26-125">**Count**</span></span>](certificatepolicies-count.md)<br/>       | <span data-ttu-id="65e26-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="65e26-126">Read-only</span></span><br/> | <span data-ttu-id="65e26-127">Возвращает число объектов [**полициинформатион**](policyinformation.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="65e26-127">Retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="65e26-128">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="65e26-128">**Item**</span></span>](certificatepolicies-item.md)<br/>         | <span data-ttu-id="65e26-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="65e26-129">Read-only</span></span><br/> | <span data-ttu-id="65e26-130">Извлекает объект [**полициинформатион**](policyinformation.md) , представляющий политику индексированных сертификатов коллекции.</span><span class="sxs-lookup"><span data-stu-id="65e26-130">Retrieves a [**PolicyInformation**](policyinformation.md) object that represents the indexed certificate policy of the collection.</span></span> <span data-ttu-id="65e26-131">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="65e26-131">This is the default property.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="65e26-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65e26-132">Remarks</span></span>

<span data-ttu-id="65e26-133">Не удается создать объект **цертификатеполиЦиес** .</span><span class="sxs-lookup"><span data-stu-id="65e26-133">The **CertificatePolicies** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="65e26-134">Требования</span><span class="sxs-lookup"><span data-stu-id="65e26-134">Requirements</span></span>



| <span data-ttu-id="65e26-135">Требование</span><span class="sxs-lookup"><span data-stu-id="65e26-135">Requirement</span></span> | <span data-ttu-id="65e26-136">Значение</span><span class="sxs-lookup"><span data-stu-id="65e26-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65e26-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="65e26-137">End of client support</span></span><br/> | <span data-ttu-id="65e26-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65e26-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="65e26-139">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="65e26-139">End of server support</span></span><br/> | <span data-ttu-id="65e26-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65e26-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="65e26-141">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="65e26-141">Redistributable</span></span><br/>       | <span data-ttu-id="65e26-142">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="65e26-142">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="65e26-143">DLL</span><span class="sxs-lookup"><span data-stu-id="65e26-143">DLL</span></span><br/>                   | <dl> <span data-ttu-id="65e26-144"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65e26-144"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
