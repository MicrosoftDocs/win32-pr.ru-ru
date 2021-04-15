---
description: Возвращает идентификатор объекта квалификатора.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Свойство квалификатора. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a86aaf7b60b98811e2d1fbef79c520448f1d47f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688928"
---
# <a name="qualifieroid-property"></a><span data-ttu-id="66caf-103">Свойство квалификатора. OID</span><span class="sxs-lookup"><span data-stu-id="66caf-103">Qualifier.OID property</span></span>

<span data-ttu-id="66caf-104">\[Свойство **OID** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="66caf-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="66caf-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="66caf-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="66caf-106">Свойство **OID** получает идентификатор объекта квалификатора.</span><span class="sxs-lookup"><span data-stu-id="66caf-106">The **OID** property retrieves the object ID of the qualifier.</span></span> <span data-ttu-id="66caf-107">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66caf-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="66caf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66caf-108">Syntax</span></span>


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="66caf-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="66caf-109">Property value</span></span>

<span data-ttu-id="66caf-110">Объект [**OID**](oid.md) , определяющий квалификатор.</span><span class="sxs-lookup"><span data-stu-id="66caf-110">An [**OID**](oid.md) object that identifies the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="66caf-111">Требования</span><span class="sxs-lookup"><span data-stu-id="66caf-111">Requirements</span></span>



| <span data-ttu-id="66caf-112">Требование</span><span class="sxs-lookup"><span data-stu-id="66caf-112">Requirement</span></span> | <span data-ttu-id="66caf-113">Значение</span><span class="sxs-lookup"><span data-stu-id="66caf-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66caf-114">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="66caf-114">Redistributable</span></span><br/> | <span data-ttu-id="66caf-115">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="66caf-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="66caf-116">DLL</span><span class="sxs-lookup"><span data-stu-id="66caf-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="66caf-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66caf-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66caf-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66caf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66caf-119">**Квалификатор**</span><span class="sxs-lookup"><span data-stu-id="66caf-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
