---
description: Предоставляет доступ к сведениям о политике расширения.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: Объект Полициинформатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665171"
---
# <a name="policyinformation-object"></a><span data-ttu-id="edcca-103">Объект Полициинформатион</span><span class="sxs-lookup"><span data-stu-id="edcca-103">PolicyInformation object</span></span>

<span data-ttu-id="edcca-104">\[Объект **полициинформатион** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="edcca-104">\[The **PolicyInformation** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="edcca-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="edcca-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="edcca-106">Объект **полициинформатион** предоставляет доступ к сведениям о политике расширения.</span><span class="sxs-lookup"><span data-stu-id="edcca-106">The **PolicyInformation** object provides access to the policy information of an extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="edcca-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="edcca-107">When to use</span></span>

<span data-ttu-id="edcca-108">Объект **полициинформатион** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="edcca-108">The **PolicyInformation** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="edcca-109">Получите идентификатор объекта политики.</span><span class="sxs-lookup"><span data-stu-id="edcca-109">Retrieve the policy OID.</span></span>
-   <span data-ttu-id="edcca-110">Получение коллекции квалификаторов политики.</span><span class="sxs-lookup"><span data-stu-id="edcca-110">Retrieve a collection of the policy's qualifiers.</span></span>

## <a name="members"></a><span data-ttu-id="edcca-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="edcca-111">Members</span></span>

<span data-ttu-id="edcca-112">Объект **полициинформатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="edcca-112">The **PolicyInformation** object has these types of members:</span></span>

-   [<span data-ttu-id="edcca-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="edcca-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="edcca-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="edcca-114">Properties</span></span>

<span data-ttu-id="edcca-115">Объект **полициинформатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="edcca-115">The **PolicyInformation** object has these properties.</span></span>



| <span data-ttu-id="edcca-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="edcca-116">Property</span></span>                                                      | <span data-ttu-id="edcca-117">Описание</span><span class="sxs-lookup"><span data-stu-id="edcca-117">Description</span></span>                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edcca-118">**КОДА**</span><span class="sxs-lookup"><span data-stu-id="edcca-118">**OID**</span></span>](policyinformation-oid.md)<br/>               | <span data-ttu-id="edcca-119">Получает OID политики в виде объекта [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="edcca-119">Retrieves the policy's OID, as an [**OID**](oid.md) object.</span></span> <span data-ttu-id="edcca-120">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="edcca-120">This is the default property.</span></span><br/>       |
| [<span data-ttu-id="edcca-121">**Квалификаторы**</span><span class="sxs-lookup"><span data-stu-id="edcca-121">**Qualifiers**</span></span>](policyinformation-qualifiers.md)<br/> | <span data-ttu-id="edcca-122">Извлекает коллекцию квалификаторов политики в виде объекта [**квалификаторов**](qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="edcca-122">Retrieves a collection of the policy's qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="edcca-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="edcca-123">Remarks</span></span>

<span data-ttu-id="edcca-124">Не удается создать объект **полициинформатион** .</span><span class="sxs-lookup"><span data-stu-id="edcca-124">The **PolicyInformation** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="edcca-125">Требования</span><span class="sxs-lookup"><span data-stu-id="edcca-125">Requirements</span></span>



| <span data-ttu-id="edcca-126">Требование</span><span class="sxs-lookup"><span data-stu-id="edcca-126">Requirement</span></span> | <span data-ttu-id="edcca-127">Значение</span><span class="sxs-lookup"><span data-stu-id="edcca-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edcca-128">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="edcca-128">Redistributable</span></span><br/> | <span data-ttu-id="edcca-129">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="edcca-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="edcca-130">DLL</span><span class="sxs-lookup"><span data-stu-id="edcca-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="edcca-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edcca-131"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
