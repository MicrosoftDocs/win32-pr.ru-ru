---
description: Возвращает число объектов EKU в коллекции.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: Свойство EKU. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41e77f3803fa65db1573c6619ebf1265b7418924
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648908"
---
# <a name="ekuscount-property"></a><span data-ttu-id="620c3-103">Свойство EKU. Count</span><span class="sxs-lookup"><span data-stu-id="620c3-103">EKUs.Count property</span></span>

<span data-ttu-id="620c3-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="620c3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="620c3-105">Вместо этого используйте [**класс X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="620c3-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="620c3-106">Свойство **Count** извлекает количество объектов [**EKU**](eku.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="620c3-106">The **Count** property retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span>

<span data-ttu-id="620c3-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="620c3-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="620c3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="620c3-108">Syntax</span></span>


```VB
EKUs.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="620c3-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="620c3-109">Property value</span></span>

<span data-ttu-id="620c3-110">Число объектов [**EKU**](eku.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="620c3-110">The number of [**EKU**](eku.md) objects in the collection.</span></span> <span data-ttu-id="620c3-111">Каждый объект **EKU** представляет одно свойство расширенного использования ключа (EKU) сертификата.</span><span class="sxs-lookup"><span data-stu-id="620c3-111">Each **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="620c3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="620c3-112">Remarks</span></span>

<span data-ttu-id="620c3-113">Свойство **Count** можно использовать для указания последнего объекта [**EKU**](eku.md) в коллекции при извлечении определенного объекта **EKU** с помощью свойства [**EKU. Item**](ekus-item.md) .</span><span class="sxs-lookup"><span data-stu-id="620c3-113">The **Count** property can be used to specify the last [**EKU**](eku.md) object in a collection when retrieving a specific **EKU** object using the [**EKUs.Item**](ekus-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="620c3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="620c3-114">Requirements</span></span>



| <span data-ttu-id="620c3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="620c3-115">Requirement</span></span> | <span data-ttu-id="620c3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="620c3-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="620c3-117">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="620c3-117">End of client support</span></span><br/> | <span data-ttu-id="620c3-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="620c3-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="620c3-119">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="620c3-119">End of server support</span></span><br/> | <span data-ttu-id="620c3-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="620c3-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="620c3-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="620c3-121">Redistributable</span></span><br/>       | <span data-ttu-id="620c3-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="620c3-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="620c3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="620c3-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="620c3-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="620c3-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
