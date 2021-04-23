---
description: Представляет одно расширение сертификата.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Объект расширения (Ммкобж. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685328"
---
# <a name="extension-object"></a><span data-ttu-id="7d3d3-103">Объект расширения</span><span class="sxs-lookup"><span data-stu-id="7d3d3-103">Extension object</span></span>

<span data-ttu-id="7d3d3-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7d3d3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7d3d3-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7d3d3-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7d3d3-106">Объект **расширения** представляет одно расширение сертификата.</span><span class="sxs-lookup"><span data-stu-id="7d3d3-106">The **Extension** object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7d3d3-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="7d3d3-107">When to use</span></span>

<span data-ttu-id="7d3d3-108">Объект **расширения** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="7d3d3-108">The **Extension** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="7d3d3-109">Получите идентификатор объекта для расширения сертификата.</span><span class="sxs-lookup"><span data-stu-id="7d3d3-109">Retrieve the OID of the certificate extension.</span></span>
-   <span data-ttu-id="7d3d3-110">Получите данные о расширении сертификата, представленные объектом [**енкодеддата**](encodeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="7d3d3-110">Retrieve the certificate extension data represented by an [**EncodedData**](encodeddata.md) object.</span></span>
-   <span data-ttu-id="7d3d3-111">Определите, помечено ли расширение сертификата как критическое.</span><span class="sxs-lookup"><span data-stu-id="7d3d3-111">Determine whether the certificate extension is marked as critical.</span></span>

## <a name="members"></a><span data-ttu-id="7d3d3-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="7d3d3-112">Members</span></span>

<span data-ttu-id="7d3d3-113">Объект **расширения** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7d3d3-113">The **Extension** object has these types of members:</span></span>

-   [<span data-ttu-id="7d3d3-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="7d3d3-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d3d3-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="7d3d3-115">Properties</span></span>

<span data-ttu-id="7d3d3-116">Объект **расширения** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7d3d3-116">The **Extension** object has these properties.</span></span>



| <span data-ttu-id="7d3d3-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="7d3d3-117">Property</span></span>                                                | <span data-ttu-id="7d3d3-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="7d3d3-118">Access type</span></span>          | <span data-ttu-id="7d3d3-119">Описание</span><span class="sxs-lookup"><span data-stu-id="7d3d3-119">Description</span></span>                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d3d3-120">**енкодеддата**</span><span class="sxs-lookup"><span data-stu-id="7d3d3-120">**EncodedData**</span></span>](extension-encodeddata.md)<br/> | <span data-ttu-id="7d3d3-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d3d3-121">Read-only</span></span><br/> | <span data-ttu-id="7d3d3-122">Извлекает закодированные данные для расширения.</span><span class="sxs-lookup"><span data-stu-id="7d3d3-122">Retrieves the encoded data for the extension.</span></span><br/>                                      |
| [<span data-ttu-id="7d3d3-123">**Критическое**</span><span class="sxs-lookup"><span data-stu-id="7d3d3-123">**IsCritical**</span></span>](extension-iscritical.md)<br/>   | <span data-ttu-id="7d3d3-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d3d3-124">Read-only</span></span><br/> | <span data-ttu-id="7d3d3-125">Получает логическое значение, указывающее, помечено ли расширение как критическое.</span><span class="sxs-lookup"><span data-stu-id="7d3d3-125">Retrieves a Boolean value that indicates whether the extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="7d3d3-126">**КОДА**</span><span class="sxs-lookup"><span data-stu-id="7d3d3-126">**OID**</span></span>](extension-oid.md)<br/>                 | <span data-ttu-id="7d3d3-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d3d3-127">Read-only</span></span><br/> | <span data-ttu-id="7d3d3-128">Возвращает идентификатор объекта для расширения.</span><span class="sxs-lookup"><span data-stu-id="7d3d3-128">Retrieves the object identifier for the extension.</span></span> <span data-ttu-id="7d3d3-129">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7d3d3-129">This is the default property.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="7d3d3-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d3d3-130">Remarks</span></span>

<span data-ttu-id="7d3d3-131">Не удается создать объект **расширения** .</span><span class="sxs-lookup"><span data-stu-id="7d3d3-131">The **Extension** object cannot be created.</span></span>

<span data-ttu-id="7d3d3-132">Объект **расширения** используется объектом коллекции [**Extensions**](extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="7d3d3-132">The **Extension** object is used by the [**Extensions**](extensions.md) collection object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d3d3-133">Требования</span><span class="sxs-lookup"><span data-stu-id="7d3d3-133">Requirements</span></span>



| <span data-ttu-id="7d3d3-134">Требование</span><span class="sxs-lookup"><span data-stu-id="7d3d3-134">Requirement</span></span> | <span data-ttu-id="7d3d3-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7d3d3-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d3d3-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7d3d3-136">End of client support</span></span><br/> | <span data-ttu-id="7d3d3-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d3d3-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7d3d3-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7d3d3-138">End of server support</span></span><br/> | <span data-ttu-id="7d3d3-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d3d3-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7d3d3-140">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7d3d3-140">Redistributable</span></span><br/>       | <span data-ttu-id="7d3d3-141">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="7d3d3-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7d3d3-142">Header</span><span class="sxs-lookup"><span data-stu-id="7d3d3-142">Header</span></span><br/>                | <dl> <span data-ttu-id="7d3d3-143"><dt>Ммкобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d3d3-143"><dt>Mmcobj.h</dt></span></span> </dl>    |
| <span data-ttu-id="7d3d3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7d3d3-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7d3d3-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d3d3-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
