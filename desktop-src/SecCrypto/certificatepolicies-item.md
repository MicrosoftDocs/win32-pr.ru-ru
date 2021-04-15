---
description: Извлекает объект Полициинформатион, представляющий индексированную политику. Это свойство по умолчанию.
ms.assetid: 0143629a-97cf-43f4-8f96-774f0f5cfeca
title: ЦертификатеполиЦиес. Item, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a41cfb88f5f3ad59a8dbf62c85eca2a13c69f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689382"
---
# <a name="certificatepoliciesitem-property"></a><span data-ttu-id="8f3fb-104">ЦертификатеполиЦиес. Item, свойство</span><span class="sxs-lookup"><span data-stu-id="8f3fb-104">CertificatePolicies.Item property</span></span>

<span data-ttu-id="8f3fb-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8f3fb-106">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для получения политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="8f3fb-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="8f3fb-107">Свойство **Item** извлекает объект [**полициинформатион**](policyinformation.md) , представляющий индексированную политику.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-107">The **Item** property retrieves the [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span> <span data-ttu-id="8f3fb-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-108">This is the default property.</span></span>

<span data-ttu-id="8f3fb-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3fb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f3fb-110">Syntax</span></span>


```VB
CertificatePolicies.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="8f3fb-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8f3fb-111">Property value</span></span>

<span data-ttu-id="8f3fb-112">Объект [**полициинформатион**](policyinformation.md) , представляющий индексированную политику.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-112">A [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f3fb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8f3fb-113">Requirements</span></span>



| <span data-ttu-id="8f3fb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8f3fb-114">Requirement</span></span> | <span data-ttu-id="8f3fb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8f3fb-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3fb-116">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8f3fb-116">End of client support</span></span><br/> | <span data-ttu-id="8f3fb-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f3fb-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8f3fb-118">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8f3fb-118">End of server support</span></span><br/> | <span data-ttu-id="8f3fb-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f3fb-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8f3fb-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8f3fb-120">Redistributable</span></span><br/>       | <span data-ttu-id="8f3fb-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f3fb-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8f3fb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8f3fb-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8f3fb-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f3fb-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
