---
description: Представляет коллекцию квалификаторов.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Объект квалификаторов (iAds. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e873019d6fbfb21de8be430d7960f697b39eeca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685380"
---
# <a name="qualifiers-object"></a><span data-ttu-id="b33e4-103">Квалификатор, объект</span><span class="sxs-lookup"><span data-stu-id="b33e4-103">Qualifiers object</span></span>

<span data-ttu-id="b33e4-104">\[Объект **квалификаторов** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b33e4-104">\[The **Qualifiers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b33e4-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="b33e4-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="b33e4-106">Объект **квалификаторов** представляет коллекцию квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="b33e4-106">The **Qualifiers** object represents a collection of qualifiers.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b33e4-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="b33e4-107">When to use</span></span>

<span data-ttu-id="b33e4-108">Объект **квалификаторов** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="b33e4-108">The **Qualifiers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b33e4-109">Получение определенного расширенного свойства из коллекции.</span><span class="sxs-lookup"><span data-stu-id="b33e4-109">Retrieve a specific extended property from the collection.</span></span>
-   <span data-ttu-id="b33e4-110">Получение числа расширенных свойств в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b33e4-110">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="b33e4-111">Выполните итерацию по коллекции.</span><span class="sxs-lookup"><span data-stu-id="b33e4-111">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="b33e4-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="b33e4-112">Members</span></span>

<span data-ttu-id="b33e4-113">Объект **квалификаторов** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b33e4-113">The **Qualifiers** object has these types of members:</span></span>

-   [<span data-ttu-id="b33e4-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="b33e4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b33e4-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="b33e4-115">Properties</span></span>

<span data-ttu-id="b33e4-116">Объект **квалификаторов** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="b33e4-116">The **Qualifiers** object has these properties.</span></span>



| <span data-ttu-id="b33e4-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="b33e4-117">Property</span></span>                                           | <span data-ttu-id="b33e4-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="b33e4-118">Access type</span></span>          | <span data-ttu-id="b33e4-119">Описание</span><span class="sxs-lookup"><span data-stu-id="b33e4-119">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b33e4-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="b33e4-120">**\_NewEnum**</span></span>](qualifiers-newenum.md)<br/> | <span data-ttu-id="b33e4-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b33e4-121">Read-only</span></span><br/> | <span data-ttu-id="b33e4-122">Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="b33e4-122">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="b33e4-123">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="b33e4-123">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="b33e4-124">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="b33e4-124">**Count**</span></span>](qualifiers-count.md)<br/>       | <span data-ttu-id="b33e4-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b33e4-125">Read-only</span></span><br/> | <span data-ttu-id="b33e4-126">Возвращает количество квалификаторов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b33e4-126">Retrieves the number of qualifiers in the collection.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="b33e4-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b33e4-127">**Item**</span></span>](qualifiers-item.md)<br/>         | <span data-ttu-id="b33e4-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b33e4-128">Read-only</span></span><br/> | <span data-ttu-id="b33e4-129">Извлекает объект [**квалификатора**](qualifier.md) , представляющий индексированный квалификатор коллекции.</span><span class="sxs-lookup"><span data-stu-id="b33e4-129">Retrieves a [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span> <span data-ttu-id="b33e4-130">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b33e4-130">This is the default property.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="b33e4-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b33e4-131">Remarks</span></span>

<span data-ttu-id="b33e4-132">Не удается создать объект **квалификаторов** .</span><span class="sxs-lookup"><span data-stu-id="b33e4-132">The **Qualifiers** object cannot be created.</span></span>

<span data-ttu-id="b33e4-133">Свойство CAPICOM объекта [**полициинформатион. квалификаторы**](policyinformation-qualifiers.md) возвращает объект **квалификаторов** .</span><span class="sxs-lookup"><span data-stu-id="b33e4-133">The [**PolicyInformation.Qualifiers**](policyinformation-qualifiers.md) CAPICOM object property returns a **Qualifiers** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b33e4-134">Требования</span><span class="sxs-lookup"><span data-stu-id="b33e4-134">Requirements</span></span>



| <span data-ttu-id="b33e4-135">Требование</span><span class="sxs-lookup"><span data-stu-id="b33e4-135">Requirement</span></span> | <span data-ttu-id="b33e4-136">Значение</span><span class="sxs-lookup"><span data-stu-id="b33e4-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b33e4-137">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b33e4-137">Redistributable</span></span><br/> | <span data-ttu-id="b33e4-138">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="b33e4-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b33e4-139">Header</span><span class="sxs-lookup"><span data-stu-id="b33e4-139">Header</span></span><br/>          | <dl> <span data-ttu-id="b33e4-140"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="b33e4-140"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="b33e4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b33e4-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="b33e4-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b33e4-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
