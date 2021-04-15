---
description: Извлекает квалификатор, основанный на указанном индексе.
ms.assetid: 4d54358d-99de-4a1c-b843-41006f47a279
title: Свойство квалификаторов. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 798b1f212aabd5b1ab34a1eefb626be4572b9c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669076"
---
# <a name="qualifiersitem-property"></a><span data-ttu-id="d47e8-103">Свойство квалификаторов. Item</span><span class="sxs-lookup"><span data-stu-id="d47e8-103">Qualifiers.Item property</span></span>

<span data-ttu-id="d47e8-104">\[Свойство **Item** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d47e8-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d47e8-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="d47e8-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="d47e8-106">Свойство **Item** получает квалификатор, основанный на указанном индексе.</span><span class="sxs-lookup"><span data-stu-id="d47e8-106">The **Item** property retrieves a qualifier based on a specified index.</span></span> <span data-ttu-id="d47e8-107">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d47e8-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d47e8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d47e8-108">Syntax</span></span>


```VB
Qualifiers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="d47e8-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d47e8-109">Property value</span></span>

<span data-ttu-id="d47e8-110">Объект [**квалификатора**](qualifier.md) , представляющий индексированный квалификатор коллекции.</span><span class="sxs-lookup"><span data-stu-id="d47e8-110">A [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="d47e8-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d47e8-111">Requirements</span></span>



| <span data-ttu-id="d47e8-112">Требование</span><span class="sxs-lookup"><span data-stu-id="d47e8-112">Requirement</span></span> | <span data-ttu-id="d47e8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d47e8-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d47e8-114">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d47e8-114">Redistributable</span></span><br/> | <span data-ttu-id="d47e8-115">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="d47e8-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d47e8-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d47e8-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="d47e8-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d47e8-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d47e8-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d47e8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47e8-119">**Квалификаторы**</span><span class="sxs-lookup"><span data-stu-id="d47e8-119">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
