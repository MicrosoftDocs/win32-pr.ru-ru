---
description: Возвращает идентификатор объекта политики. Это свойство по умолчанию.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: Полициинформатион. OID, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685141"
---
# <a name="policyinformationoid-property"></a><span data-ttu-id="461d7-104">Полициинформатион. OID, свойство</span><span class="sxs-lookup"><span data-stu-id="461d7-104">PolicyInformation.OID property</span></span>

<span data-ttu-id="461d7-105">\[Свойство **OID** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="461d7-105">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="461d7-106">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="461d7-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="461d7-107">Свойство **OID** получает идентификатор объекта политики.</span><span class="sxs-lookup"><span data-stu-id="461d7-107">The **OID** property retrieves the policy's OID.</span></span> <span data-ttu-id="461d7-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="461d7-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="461d7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="461d7-109">Syntax</span></span>


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="461d7-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="461d7-110">Property value</span></span>

<span data-ttu-id="461d7-111">Идентификатор объекта политики в виде объекта [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="461d7-111">The policy's object identifier as an [**OID**](oid.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="461d7-112">Требования</span><span class="sxs-lookup"><span data-stu-id="461d7-112">Requirements</span></span>



| <span data-ttu-id="461d7-113">Требование</span><span class="sxs-lookup"><span data-stu-id="461d7-113">Requirement</span></span> | <span data-ttu-id="461d7-114">Значение</span><span class="sxs-lookup"><span data-stu-id="461d7-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="461d7-115">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="461d7-115">Redistributable</span></span><br/> | <span data-ttu-id="461d7-116">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="461d7-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="461d7-117">DLL</span><span class="sxs-lookup"><span data-stu-id="461d7-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="461d7-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="461d7-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="461d7-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="461d7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="461d7-120">**полициинформатион**</span><span class="sxs-lookup"><span data-stu-id="461d7-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
