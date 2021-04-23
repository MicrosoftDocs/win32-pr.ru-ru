---
description: Получает логическое значение, указывающее, помечено ли расширение шаблона как критическое.
ms.assetid: 37e2000a-d3c8-46b5-84e5-a3904fdbaeea
title: Свойство Template. «Critical»
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66f9dc90828cd474497478872f154adbd3fcd12a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648767"
---
# <a name="templateiscritical-property"></a><span data-ttu-id="8c56f-103">Свойство Template. «Critical»</span><span class="sxs-lookup"><span data-stu-id="8c56f-103">Template.IsCritical property</span></span>

<span data-ttu-id="8c56f-104">\[Свойство « **критическое** » доступно для использования в операционных системах, указанных в разделе «требования».</span><span class="sxs-lookup"><span data-stu-id="8c56f-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8c56f-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для шаблона сертификата для получения шаблона расширения сертификата.\]</span><span class="sxs-lookup"><span data-stu-id="8c56f-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="8c56f-106">Свойство « **Critical** » получает логическое значение, указывающее, помечено ли расширение шаблона как критическое.</span><span class="sxs-lookup"><span data-stu-id="8c56f-106">The **IsCritical** property retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c56f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c56f-107">Syntax</span></span>


```VB
Template.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8c56f-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8c56f-108">Property value</span></span>

<span data-ttu-id="8c56f-109">Если **значение равно true**, расширение шаблона помечено как критическое.</span><span class="sxs-lookup"><span data-stu-id="8c56f-109">If **true**, the template extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c56f-110">Требования</span><span class="sxs-lookup"><span data-stu-id="8c56f-110">Requirements</span></span>



| <span data-ttu-id="8c56f-111">Требование</span><span class="sxs-lookup"><span data-stu-id="8c56f-111">Requirement</span></span> | <span data-ttu-id="8c56f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8c56f-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c56f-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8c56f-113">Redistributable</span></span><br/> | <span data-ttu-id="8c56f-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c56f-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8c56f-115">DLL</span><span class="sxs-lookup"><span data-stu-id="8c56f-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="8c56f-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c56f-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c56f-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c56f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c56f-118">**Шаблон**</span><span class="sxs-lookup"><span data-stu-id="8c56f-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
