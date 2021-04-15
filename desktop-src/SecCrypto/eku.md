---
description: Представляет одно свойство расширенного использования ключа (EKU) сертификата.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: Объект EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff397ae747ecd09dd1292e5c15eb4291692d9651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669121"
---
# <a name="eku-object"></a><span data-ttu-id="85ca1-103">Объект EKU</span><span class="sxs-lookup"><span data-stu-id="85ca1-103">EKU object</span></span>

<span data-ttu-id="85ca1-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="85ca1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="85ca1-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="85ca1-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="85ca1-106">Объект **EKU** представляет одно свойство расширенного использования ключа (EKU) сертификата.</span><span class="sxs-lookup"><span data-stu-id="85ca1-106">The **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="85ca1-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="85ca1-107">Members</span></span>

<span data-ttu-id="85ca1-108">Объект **EKU** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="85ca1-108">The **EKU** object has these types of members:</span></span>

-   [<span data-ttu-id="85ca1-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="85ca1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85ca1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="85ca1-110">Properties</span></span>

<span data-ttu-id="85ca1-111">Объект **EKU** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="85ca1-111">The **EKU** object has these properties.</span></span>



| <span data-ttu-id="85ca1-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="85ca1-112">Property</span></span>                            | <span data-ttu-id="85ca1-113">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="85ca1-113">Access type</span></span>           | <span data-ttu-id="85ca1-114">Описание</span><span class="sxs-lookup"><span data-stu-id="85ca1-114">Description</span></span>                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85ca1-115">**Имя**</span><span class="sxs-lookup"><span data-stu-id="85ca1-115">**Name**</span></span>](eku-name.md)<br/> | <span data-ttu-id="85ca1-116">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="85ca1-116">Read/write</span></span><br/> | <span data-ttu-id="85ca1-117">Задает или получает значение перечисления, которое указывает CAPICOM имя EKU.</span><span class="sxs-lookup"><span data-stu-id="85ca1-117">Sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="85ca1-118">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85ca1-118">This is the default property.</span></span><br/>                                                                                   |
| [<span data-ttu-id="85ca1-119">**КОДА**</span><span class="sxs-lookup"><span data-stu-id="85ca1-119">**OID**</span></span>](eku-oid.md)<br/>   | <span data-ttu-id="85ca1-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="85ca1-120">Read/write</span></span><br/> | <span data-ttu-id="85ca1-121">Задает или получает строку, содержащую значение строки [*идентификатора объекта*](../secgloss/o-gly.md) EKU (OID), определенное в винкрипт. h.</span><span class="sxs-lookup"><span data-stu-id="85ca1-121">Sets or retrieves a string that contains an EKU [*object identifier*](../secgloss/o-gly.md) (OID) string value as defined in Wincrypt.h.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="85ca1-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85ca1-122">Remarks</span></span>

<span data-ttu-id="85ca1-123">Объект **EKU** используется следующей коллекцией и свойством:</span><span class="sxs-lookup"><span data-stu-id="85ca1-123">The **EKU** object is used by the following collection and property:</span></span>

-   <span data-ttu-id="85ca1-124">Коллекция [**EKU**](ekus.md)</span><span class="sxs-lookup"><span data-stu-id="85ca1-124">[**EKUs**](ekus.md) collection</span></span>
-   <span data-ttu-id="85ca1-125">[**Цертификатестатус. EKU,**](certificatestatus-eku.md) свойство</span><span class="sxs-lookup"><span data-stu-id="85ca1-125">[**CertificateStatus.EKU**](certificatestatus-eku.md) property</span></span>

<span data-ttu-id="85ca1-126">Не удается создать объект **EKU** .</span><span class="sxs-lookup"><span data-stu-id="85ca1-126">The **EKU** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="85ca1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="85ca1-127">Requirements</span></span>



| <span data-ttu-id="85ca1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="85ca1-128">Requirement</span></span> | <span data-ttu-id="85ca1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="85ca1-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85ca1-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="85ca1-130">End of client support</span></span><br/> | <span data-ttu-id="85ca1-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85ca1-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="85ca1-132">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="85ca1-132">End of server support</span></span><br/> | <span data-ttu-id="85ca1-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85ca1-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="85ca1-134">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="85ca1-134">Redistributable</span></span><br/>       | <span data-ttu-id="85ca1-135">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="85ca1-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="85ca1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="85ca1-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="85ca1-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85ca1-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
