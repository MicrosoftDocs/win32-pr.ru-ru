---
description: Возвращает число объектов Полициинформатион в коллекции.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: ЦертификатеполиЦиес. Count, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689426"
---
# <a name="certificatepoliciescount-property"></a><span data-ttu-id="770f4-103">ЦертификатеполиЦиес. Count, свойство</span><span class="sxs-lookup"><span data-stu-id="770f4-103">CertificatePolicies.Count property</span></span>

<span data-ttu-id="770f4-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="770f4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="770f4-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для получения политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="770f4-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="770f4-106">Свойство **Count** извлекает количество объектов [**полициинформатион**](policyinformation.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="770f4-106">The **Count** property retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span>

<span data-ttu-id="770f4-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="770f4-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="770f4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="770f4-108">Syntax</span></span>


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="770f4-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="770f4-109">Property value</span></span>

<span data-ttu-id="770f4-110">Число объектов [**полициинформатион**](policyinformation.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="770f4-110">The number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span> <span data-ttu-id="770f4-111">Каждый объект **полициинформатион** представляет одну политику сертификата в коллекции.</span><span class="sxs-lookup"><span data-stu-id="770f4-111">Each **PolicyInformation** object represents a single certificate policy in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="770f4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="770f4-112">Remarks</span></span>

<span data-ttu-id="770f4-113">Свойство **Count** можно использовать для указания последнего объекта [**полициинформатион**](policyinformation.md) в коллекции при извлечении определенного объекта **полициинформатион** с помощью свойства [**цертификатеполиЦиес. Item**](certificatepolicies-item.md) .</span><span class="sxs-lookup"><span data-stu-id="770f4-113">The **Count** property can be used to specify the last [**PolicyInformation**](policyinformation.md) object in the collection when retrieving a specific **PolicyInformation** object using the [**CertificatePolicies.Item**](certificatepolicies-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="770f4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="770f4-114">Requirements</span></span>



| <span data-ttu-id="770f4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="770f4-115">Requirement</span></span> | <span data-ttu-id="770f4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="770f4-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="770f4-117">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="770f4-117">End of client support</span></span><br/> | <span data-ttu-id="770f4-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="770f4-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="770f4-119">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="770f4-119">End of server support</span></span><br/> | <span data-ttu-id="770f4-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="770f4-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="770f4-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="770f4-121">Redistributable</span></span><br/>       | <span data-ttu-id="770f4-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="770f4-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="770f4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="770f4-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="770f4-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="770f4-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
