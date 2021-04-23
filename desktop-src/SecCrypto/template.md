---
description: Представляет шаблон расширения сертификата для сертификата.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Объект шаблона
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fedd64979ad74ceac3f6d54af58c57d8d8b2b134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648888"
---
# <a name="template-object"></a><span data-ttu-id="bac2d-103">Объект шаблона</span><span class="sxs-lookup"><span data-stu-id="bac2d-103">Template object</span></span>

<span data-ttu-id="bac2d-104">\[Объект **шаблона** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="bac2d-104">\[The **Template** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bac2d-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для шаблона сертификата для получения шаблона расширения сертификата.\]</span><span class="sxs-lookup"><span data-stu-id="bac2d-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="bac2d-106">Объект **шаблона** представляет шаблон расширения сертификата сертификата.</span><span class="sxs-lookup"><span data-stu-id="bac2d-106">The **Template** object represents the certificate extension template of the certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="bac2d-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="bac2d-107">When to use</span></span>

<span data-ttu-id="bac2d-108">Объект **шаблона** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="bac2d-108">The **Template** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="bac2d-109">Определите, помечен ли шаблон критическим или нет.</span><span class="sxs-lookup"><span data-stu-id="bac2d-109">Determine whether the template is marked critical or present.</span></span>
-   <span data-ttu-id="bac2d-110">Получите [*идентификатор объекта*](../secgloss/o-gly.md) или имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="bac2d-110">Retrieve the [*object identifier*](../secgloss/o-gly.md) (OID) or name of the template.</span></span>
-   <span data-ttu-id="bac2d-111">Получение дополнительной или основной версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="bac2d-111">Retrieve the minor or major version of the template.</span></span>

## <a name="members"></a><span data-ttu-id="bac2d-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="bac2d-112">Members</span></span>

<span data-ttu-id="bac2d-113">Объект **шаблона** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bac2d-113">The **Template** object has these types of members:</span></span>

-   [<span data-ttu-id="bac2d-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="bac2d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bac2d-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="bac2d-115">Properties</span></span>

<span data-ttu-id="bac2d-116">Объект **шаблона** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bac2d-116">The **Template** object has these properties.</span></span>



| <span data-ttu-id="bac2d-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="bac2d-117">Property</span></span>                                                 | <span data-ttu-id="bac2d-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="bac2d-118">Access type</span></span>          | <span data-ttu-id="bac2d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="bac2d-119">Description</span></span>                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bac2d-120">**Критическое**</span><span class="sxs-lookup"><span data-stu-id="bac2d-120">**IsCritical**</span></span>](template-iscritical.md)<br/>     | <span data-ttu-id="bac2d-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bac2d-121">Read-only</span></span><br/> | <span data-ttu-id="bac2d-122">Получает логическое значение, указывающее, помечено ли расширение шаблона как критическое.</span><span class="sxs-lookup"><span data-stu-id="bac2d-122">Retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="bac2d-123">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="bac2d-123">**IsPresent**</span></span>](template-ispresent.md)<br/>       | <span data-ttu-id="bac2d-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bac2d-124">Read-only</span></span><br/> | <span data-ttu-id="bac2d-125">Получает логическое значение, указывающее, имеется ли расширение шаблона.</span><span class="sxs-lookup"><span data-stu-id="bac2d-125">Retrieves a Boolean value that indicates whether the template extension is present.</span></span><br/>         |
| [<span data-ttu-id="bac2d-126">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="bac2d-126">**MajorVersion**</span></span>](template-majorversion.md)<br/> | <span data-ttu-id="bac2d-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bac2d-127">Read-only</span></span><br/> | <span data-ttu-id="bac2d-128">Возвращает основной номер версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="bac2d-128">Retrieves the major version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="bac2d-129">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="bac2d-129">**MinorVersion**</span></span>](template-minorversion.md)<br/> | <span data-ttu-id="bac2d-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bac2d-130">Read-only</span></span><br/> | <span data-ttu-id="bac2d-131">Возвращает дополнительный номер версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="bac2d-131">Retrieves the minor version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="bac2d-132">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bac2d-132">**Name**</span></span>](template-name.md)<br/>                 | <span data-ttu-id="bac2d-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bac2d-133">Read-only</span></span><br/> | <span data-ttu-id="bac2d-134">Извлекает строку, содержащую имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="bac2d-134">Retrieves a string that contains the name of the template.</span></span><br/>                                  |
| [<span data-ttu-id="bac2d-135">**КОДА**</span><span class="sxs-lookup"><span data-stu-id="bac2d-135">**OID**</span></span>](template-oid.md)<br/>                   | <span data-ttu-id="bac2d-136">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bac2d-136">Read-only</span></span><br/> | <span data-ttu-id="bac2d-137">Извлекает объект [**OID**](oid.md) , определяющий объект **шаблона** .</span><span class="sxs-lookup"><span data-stu-id="bac2d-137">Retrieves an [**OID**](oid.md) object that identifies the **Template** object.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="bac2d-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bac2d-138">Remarks</span></span>

<span data-ttu-id="bac2d-139">Не удается создать объект **шаблона** .</span><span class="sxs-lookup"><span data-stu-id="bac2d-139">The **Template** object cannot be created.</span></span>

<span data-ttu-id="bac2d-140">Объект **шаблона** возвращается методом [**Certificate. Template**](certificate-template.md) .</span><span class="sxs-lookup"><span data-stu-id="bac2d-140">A **Template** object is returned by the [**Certificate.Template**](certificate-template.md) method.</span></span>

<span data-ttu-id="bac2d-141">CAPICOM использует две разные версии шаблонов сертификатов.</span><span class="sxs-lookup"><span data-stu-id="bac2d-141">CAPICOM uses two different versions of certificate templates.</span></span> <span data-ttu-id="bac2d-142">В следующей таблице показаны имя и идентификатор объекта для каждой версии шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="bac2d-142">The following table shows the name and OID for each certificate template version.</span></span>



| <span data-ttu-id="bac2d-143">Версия</span><span class="sxs-lookup"><span data-stu-id="bac2d-143">Version</span></span> | <span data-ttu-id="bac2d-144">Имя</span><span class="sxs-lookup"><span data-stu-id="bac2d-144">Name</span></span>                               | <span data-ttu-id="bac2d-145">OID</span><span class="sxs-lookup"><span data-stu-id="bac2d-145">OID</span></span>                    |
|---------|------------------------------------|------------------------|
| <span data-ttu-id="bac2d-146">V1</span><span class="sxs-lookup"><span data-stu-id="bac2d-146">V1</span></span>      | <span data-ttu-id="bac2d-147">Сзоид \_ Регистрация \_ \_ расширения типом</span><span class="sxs-lookup"><span data-stu-id="bac2d-147">szOID\_ENROLL\_CERTTYPE\_EXTENSION</span></span> | <span data-ttu-id="bac2d-148">"1.3.6.1.4.1.311.20.2"</span><span class="sxs-lookup"><span data-stu-id="bac2d-148">"1.3.6.1.4.1.311.20.2"</span></span> |
| <span data-ttu-id="bac2d-149">V2</span><span class="sxs-lookup"><span data-stu-id="bac2d-149">V2</span></span>      | <span data-ttu-id="bac2d-150">\_шаблон сертификата \_ сзоид</span><span class="sxs-lookup"><span data-stu-id="bac2d-150">szOID\_CERTIFICATE\_TEMPLATE</span></span>       | <span data-ttu-id="bac2d-151">"1.3.6.1.4.1.311.21.7"</span><span class="sxs-lookup"><span data-stu-id="bac2d-151">"1.3.6.1.4.1.311.21.7"</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="bac2d-152">Требования</span><span class="sxs-lookup"><span data-stu-id="bac2d-152">Requirements</span></span>



| <span data-ttu-id="bac2d-153">Требование</span><span class="sxs-lookup"><span data-stu-id="bac2d-153">Requirement</span></span> | <span data-ttu-id="bac2d-154">Значение</span><span class="sxs-lookup"><span data-stu-id="bac2d-154">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bac2d-155">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="bac2d-155">Redistributable</span></span><br/> | <span data-ttu-id="bac2d-156">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="bac2d-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bac2d-157">DLL</span><span class="sxs-lookup"><span data-stu-id="bac2d-157">DLL</span></span><br/>             | <dl> <span data-ttu-id="bac2d-158"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bac2d-158"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
