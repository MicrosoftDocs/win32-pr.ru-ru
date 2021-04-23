---
description: Предоставляет доступ только для чтения к свойствам расширенного использования ключа (EKU) сертификата.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Объект Екстендедкэйусаже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648868"
---
# <a name="extendedkeyusage-object"></a><span data-ttu-id="58a2d-103">Объект Екстендедкэйусаже</span><span class="sxs-lookup"><span data-stu-id="58a2d-103">ExtendedKeyUsage object</span></span>

<span data-ttu-id="58a2d-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="58a2d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="58a2d-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="58a2d-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="58a2d-106">Объект **екстендедкэйусаже** предоставляет доступ только для чтения к свойствам расширенного использования ключа (EKU) сертификата.</span><span class="sxs-lookup"><span data-stu-id="58a2d-106">The **ExtendedKeyUsage** object provides read-only access to the extended key usage (EKU) properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="58a2d-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="58a2d-107">Members</span></span>

<span data-ttu-id="58a2d-108">Объект **екстендедкэйусаже** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="58a2d-108">The **ExtendedKeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="58a2d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="58a2d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58a2d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="58a2d-110">Properties</span></span>

<span data-ttu-id="58a2d-111">Объект **екстендедкэйусаже** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="58a2d-111">The **ExtendedKeyUsage** object has these properties.</span></span>



| <span data-ttu-id="58a2d-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="58a2d-112">Property</span></span>                                                     | <span data-ttu-id="58a2d-113">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="58a2d-113">Access type</span></span>          | <span data-ttu-id="58a2d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="58a2d-114">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58a2d-115">**EKU**</span><span class="sxs-lookup"><span data-stu-id="58a2d-115">**EKUs**</span></span>](extendedkeyusage-ekus.md)<br/>             | <span data-ttu-id="58a2d-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a2d-116">Read-only</span></span><br/> | <span data-ttu-id="58a2d-117">Коллекция [**EKU**](ekus.md) , содержащая объекты [**EKU**](eku.md) для сертификата.</span><span class="sxs-lookup"><span data-stu-id="58a2d-117">[**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span><br/>                            |
| [<span data-ttu-id="58a2d-118">**Критическое**</span><span class="sxs-lookup"><span data-stu-id="58a2d-118">**IsCritical**</span></span>](extendedkeyusage-iscritical.md)<br/> | <span data-ttu-id="58a2d-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a2d-119">Read-only</span></span><br/> | <span data-ttu-id="58a2d-120">Получает **логическое** значение, указывающее, помечено ли расширение EKU как критическое.</span><span class="sxs-lookup"><span data-stu-id="58a2d-120">Retrieves a **Boolean** value that indicates whether the EKU extension is marked critical.</span></span><br/>                                   |
| [<span data-ttu-id="58a2d-121">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="58a2d-121">**IsPresent**</span></span>](extendedkeyusage-ispresent.md)<br/>   | <span data-ttu-id="58a2d-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a2d-122">Read-only</span></span><br/> | <span data-ttu-id="58a2d-123">Получает **логическое** значение, указывающее, имеется ли расширение EKU.</span><span class="sxs-lookup"><span data-stu-id="58a2d-123">Retrieves a **Boolean** value that indicates whether the EKU extension is present.</span></span><br/> <span data-ttu-id="58a2d-124">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="58a2d-124">This is the default property.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="58a2d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58a2d-125">Remarks</span></span>

<span data-ttu-id="58a2d-126">Не удается создать объект **екстендедкэйусаже** .</span><span class="sxs-lookup"><span data-stu-id="58a2d-126">The **ExtendedKeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="58a2d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="58a2d-127">Requirements</span></span>



| <span data-ttu-id="58a2d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="58a2d-128">Requirement</span></span> | <span data-ttu-id="58a2d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="58a2d-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58a2d-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="58a2d-130">End of client support</span></span><br/> | <span data-ttu-id="58a2d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58a2d-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="58a2d-132">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="58a2d-132">End of server support</span></span><br/> | <span data-ttu-id="58a2d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58a2d-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="58a2d-134">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="58a2d-134">Redistributable</span></span><br/>       | <span data-ttu-id="58a2d-135">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="58a2d-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="58a2d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="58a2d-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="58a2d-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58a2d-137"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58a2d-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58a2d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58a2d-139">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="58a2d-139">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
