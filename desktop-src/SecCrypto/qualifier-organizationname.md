---
description: Возвращает имя Организации, связанной с квалификатором.
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: Свойство квалификатора. название_организации
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1e1ebb2b948d5a933b59e86c8753b6b68a3a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648791"
---
# <a name="qualifierorganizationname-property"></a><span data-ttu-id="253b4-103">Свойство квалификатора. название_организации</span><span class="sxs-lookup"><span data-stu-id="253b4-103">Qualifier.OrganizationName property</span></span>

<span data-ttu-id="253b4-104">\[Свойство **название_организации** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="253b4-104">\[The **OrganizationName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="253b4-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="253b4-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="253b4-106">Свойство **название_организации** извлекает имя Организации, связанной с квалификатором.</span><span class="sxs-lookup"><span data-stu-id="253b4-106">The **OrganizationName** property retrieves the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="253b4-107">Это свойство может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="253b4-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="253b4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="253b4-108">Syntax</span></span>


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a><span data-ttu-id="253b4-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="253b4-109">Property value</span></span>

<span data-ttu-id="253b4-110">Имя Организации, связанной с квалификатором.</span><span class="sxs-lookup"><span data-stu-id="253b4-110">The name of the organization associated with the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="253b4-111">Требования</span><span class="sxs-lookup"><span data-stu-id="253b4-111">Requirements</span></span>



| <span data-ttu-id="253b4-112">Требование</span><span class="sxs-lookup"><span data-stu-id="253b4-112">Requirement</span></span> | <span data-ttu-id="253b4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="253b4-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="253b4-114">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="253b4-114">Redistributable</span></span><br/> | <span data-ttu-id="253b4-115">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="253b4-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="253b4-116">DLL</span><span class="sxs-lookup"><span data-stu-id="253b4-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="253b4-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="253b4-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="253b4-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="253b4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="253b4-119">**Квалификатор**</span><span class="sxs-lookup"><span data-stu-id="253b4-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
