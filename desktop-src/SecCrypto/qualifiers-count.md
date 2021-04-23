---
description: Возвращает количество объектов квалификатора в коллекции.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Свойство квалификаторов. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ffb79941a78602bfda8f5287b0f4df7205d4d86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689436"
---
# <a name="qualifierscount-property"></a><span data-ttu-id="9a291-103">Свойство квалификаторов. Count</span><span class="sxs-lookup"><span data-stu-id="9a291-103">Qualifiers.Count property</span></span>

<span data-ttu-id="9a291-104">\[Свойство **Count** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9a291-104">\[The **Count** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9a291-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="9a291-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="9a291-106">Свойство **Count** извлекает количество объектов [**квалификатора**](qualifier.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="9a291-106">The **Count** property retrieves the number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a291-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a291-107">Syntax</span></span>


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="9a291-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9a291-108">Property value</span></span>

<span data-ttu-id="9a291-109">Количество объектов [**квалификатора**](qualifier.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="9a291-109">Number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a291-110">Требования</span><span class="sxs-lookup"><span data-stu-id="9a291-110">Requirements</span></span>



| <span data-ttu-id="9a291-111">Требование</span><span class="sxs-lookup"><span data-stu-id="9a291-111">Requirement</span></span> | <span data-ttu-id="9a291-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9a291-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a291-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9a291-113">Redistributable</span></span><br/> | <span data-ttu-id="9a291-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a291-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9a291-115">DLL</span><span class="sxs-lookup"><span data-stu-id="9a291-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="9a291-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a291-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a291-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a291-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a291-118">**Квалификаторы**</span><span class="sxs-lookup"><span data-stu-id="9a291-118">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
