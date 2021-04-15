---
description: Представляет указатель на инструкцию по сертификации (CPS) или квалификатор уведомления пользователя.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Объект квалификатора
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648775"
---
# <a name="qualifier-object"></a><span data-ttu-id="2325b-103">Объект квалификатора</span><span class="sxs-lookup"><span data-stu-id="2325b-103">Qualifier object</span></span>

<span data-ttu-id="2325b-104">\[Объект **квалификатора** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="2325b-104">\[The **Qualifier** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2325b-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="2325b-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="2325b-106">Объект **квалификатора** представляет собой указатель на инструкцию по сертификации (CPS) или квалификатор уведомления пользователя.</span><span class="sxs-lookup"><span data-stu-id="2325b-106">The **Qualifier** object represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2325b-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="2325b-107">When to use</span></span>

<span data-ttu-id="2325b-108">Объект **квалификатора** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="2325b-108">The **Qualifier** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="2325b-109">Получите идентификатор объекта квалификатора.</span><span class="sxs-lookup"><span data-stu-id="2325b-109">Retrieve the object identifier of the qualifier.</span></span>
-   <span data-ttu-id="2325b-110">Получите универсальный код ресурса (URI), указывающий на сервер публикаций Contribute, опубликованный [*центром сертификации*](../secgloss/c-gly.md) (ЦС).</span><span class="sxs-lookup"><span data-stu-id="2325b-110">Retrieve the Uniform Resource Identifier (URI) that points to a CPS published by the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>
-   <span data-ttu-id="2325b-111">Получите имя Организации, связанной с квалификатором.</span><span class="sxs-lookup"><span data-stu-id="2325b-111">Retrieve the name of the organization associated with the qualifier.</span></span>
-   <span data-ttu-id="2325b-112">Получение имени и содержимого уведомления пользователя.</span><span class="sxs-lookup"><span data-stu-id="2325b-112">Retrieve the name and content of a user notice.</span></span>

## <a name="members"></a><span data-ttu-id="2325b-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="2325b-113">Members</span></span>

<span data-ttu-id="2325b-114">Объект **квалификатора** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2325b-114">The **Qualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="2325b-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="2325b-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2325b-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="2325b-116">Properties</span></span>

<span data-ttu-id="2325b-117">Объект **квалификатора** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2325b-117">The **Qualifier** object has these properties.</span></span>



| <span data-ttu-id="2325b-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="2325b-118">Property</span></span>                                                          | <span data-ttu-id="2325b-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="2325b-119">Access type</span></span>          | <span data-ttu-id="2325b-120">Описание</span><span class="sxs-lookup"><span data-stu-id="2325b-120">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2325b-121">**кпспоинтер**</span><span class="sxs-lookup"><span data-stu-id="2325b-121">**CPSPointer**</span></span>](qualifier-cpspointer.md)<br/>             | <span data-ttu-id="2325b-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2325b-122">Read-only</span></span><br/> | <span data-ttu-id="2325b-123">Извлекает строку, содержащую URI, указывающий на сервер публикаций Contribute, опубликованный центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="2325b-123">Retrieves a string that contains the URI that points to a CPS published by the CA.</span></span><br/>                                       |
| [<span data-ttu-id="2325b-124">**експлиЦиттекст**</span><span class="sxs-lookup"><span data-stu-id="2325b-124">**ExplicitText**</span></span>](qualifier-explicittext.md)<br/>         | <span data-ttu-id="2325b-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2325b-125">Read-only</span></span><br/> | <span data-ttu-id="2325b-126">Извлекает строку, содержащую содержимое уведомления пользователя.</span><span class="sxs-lookup"><span data-stu-id="2325b-126">Retrieves a string that contains the content of the user notice.</span></span> <span data-ttu-id="2325b-127">Это свойство может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="2325b-127">This property may be empty.</span></span><br/>                             |
| [<span data-ttu-id="2325b-128">**нотиценумберс**</span><span class="sxs-lookup"><span data-stu-id="2325b-128">**NoticeNumbers**</span></span>](qualifier-noticenumbers.md)<br/>       | <span data-ttu-id="2325b-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2325b-129">Read-only</span></span><br/> | <span data-ttu-id="2325b-130">Извлекает объект **нотиценумберс** , содержащий коллекцию номеров пользовательских уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2325b-130">Retrieves a **NoticeNumbers** object that contains the collection of user notice numbers.</span></span> <span data-ttu-id="2325b-131">Это свойство может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="2325b-131">This property may be empty.</span></span><br/>    |
| [<span data-ttu-id="2325b-132">**КОДА**</span><span class="sxs-lookup"><span data-stu-id="2325b-132">**OID**</span></span>](qualifier-oid.md)<br/>                           | <span data-ttu-id="2325b-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2325b-133">Read-only</span></span><br/> | <span data-ttu-id="2325b-134">Извлекает объект [**OID**](oid.md) , определяющий квалификатор.</span><span class="sxs-lookup"><span data-stu-id="2325b-134">Retrieves an [**OID**](oid.md) object that identifies the qualifier.</span></span> <span data-ttu-id="2325b-135">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2325b-135">This is the default property.</span></span><br/>                      |
| [<span data-ttu-id="2325b-136">**OrganizationName**</span><span class="sxs-lookup"><span data-stu-id="2325b-136">**OrganizationName**</span></span>](qualifier-organizationname.md)<br/> | <span data-ttu-id="2325b-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2325b-137">Read-only</span></span><br/> | <span data-ttu-id="2325b-138">Извлекает строку, содержащую имя Организации, связанной с квалификатором.</span><span class="sxs-lookup"><span data-stu-id="2325b-138">Retrieves a string that contains the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="2325b-139">Это свойство может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="2325b-139">This property may be empty.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2325b-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2325b-140">Remarks</span></span>

<span data-ttu-id="2325b-141">Не удается создать объект **квалификатора** .</span><span class="sxs-lookup"><span data-stu-id="2325b-141">The **Qualifier** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="2325b-142">Требования</span><span class="sxs-lookup"><span data-stu-id="2325b-142">Requirements</span></span>



| <span data-ttu-id="2325b-143">Требование</span><span class="sxs-lookup"><span data-stu-id="2325b-143">Requirement</span></span> | <span data-ttu-id="2325b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="2325b-144">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2325b-145">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="2325b-145">Redistributable</span></span><br/> | <span data-ttu-id="2325b-146">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="2325b-146">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2325b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="2325b-147">DLL</span></span><br/>             | <dl> <span data-ttu-id="2325b-148"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2325b-148"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
