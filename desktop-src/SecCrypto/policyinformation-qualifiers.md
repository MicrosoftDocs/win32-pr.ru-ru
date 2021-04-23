---
description: Извлекает коллекцию квалификаторов политики.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: Свойство Полициинформатион. квалификаторы (iAds. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685140"
---
# <a name="policyinformationqualifiers-property"></a><span data-ttu-id="87994-103">Полициинформатион. квалификаторы, свойство</span><span class="sxs-lookup"><span data-stu-id="87994-103">PolicyInformation.Qualifiers property</span></span>

<span data-ttu-id="87994-104">\[Свойство **Квалификаторы** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="87994-104">\[The **Qualifiers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="87994-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="87994-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="87994-106">Свойство **Квалификаторы** получает коллекцию квалификаторов политики.</span><span class="sxs-lookup"><span data-stu-id="87994-106">The **Qualifiers** property retrieves a collection of the policy's qualifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="87994-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87994-107">Syntax</span></span>


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a><span data-ttu-id="87994-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="87994-108">Property value</span></span>

<span data-ttu-id="87994-109">В качестве [**квалификатора**](qualifiers.md) объекта можно увидеть указатель на политику сертификации (или квалификаторы уведомления пользователя).</span><span class="sxs-lookup"><span data-stu-id="87994-109">The policy's Certification Practice Statement (CPS) pointer or user notice qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="87994-110">Требования</span><span class="sxs-lookup"><span data-stu-id="87994-110">Requirements</span></span>



| <span data-ttu-id="87994-111">Требование</span><span class="sxs-lookup"><span data-stu-id="87994-111">Requirement</span></span> | <span data-ttu-id="87994-112">Значение</span><span class="sxs-lookup"><span data-stu-id="87994-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87994-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="87994-113">Redistributable</span></span><br/> | <span data-ttu-id="87994-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="87994-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="87994-115">Header</span><span class="sxs-lookup"><span data-stu-id="87994-115">Header</span></span><br/>          | <dl> <span data-ttu-id="87994-116"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="87994-116"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="87994-117">DLL</span><span class="sxs-lookup"><span data-stu-id="87994-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="87994-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87994-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87994-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87994-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87994-120">**полициинформатион**</span><span class="sxs-lookup"><span data-stu-id="87994-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
