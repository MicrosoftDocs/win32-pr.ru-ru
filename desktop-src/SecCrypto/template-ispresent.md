---
description: Получает логическое значение, указывающее, имеется ли расширение шаблона.
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: Свойство Template. Present
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23dcd8cc5ee92a689300078d439998e43933af93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647943"
---
# <a name="templateispresent-property"></a><span data-ttu-id="7f6eb-103">Свойство Template. Present</span><span class="sxs-lookup"><span data-stu-id="7f6eb-103">Template.IsPresent property</span></span>

<span data-ttu-id="7f6eb-104">\[Свойство **Present** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7f6eb-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для шаблона сертификата для получения шаблона расширения сертификата.\]</span><span class="sxs-lookup"><span data-stu-id="7f6eb-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="7f6eb-106">Свойство **Present** получает логическое значение, указывающее, имеется ли расширение шаблона.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-106">The **IsPresent** property retrieves a Boolean value that indicates whether the template extension is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6eb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f6eb-107">Syntax</span></span>


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="7f6eb-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7f6eb-108">Property value</span></span>

<span data-ttu-id="7f6eb-109">Если **значение равно true**, имеется расширение шаблона.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-109">If **true**, the template extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f6eb-110">Требования</span><span class="sxs-lookup"><span data-stu-id="7f6eb-110">Requirements</span></span>



| <span data-ttu-id="7f6eb-111">Требование</span><span class="sxs-lookup"><span data-stu-id="7f6eb-111">Requirement</span></span> | <span data-ttu-id="7f6eb-112">Значение</span><span class="sxs-lookup"><span data-stu-id="7f6eb-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6eb-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7f6eb-113">Redistributable</span></span><br/> | <span data-ttu-id="7f6eb-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="7f6eb-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7f6eb-115">DLL</span><span class="sxs-lookup"><span data-stu-id="7f6eb-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="7f6eb-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f6eb-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f6eb-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f6eb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f6eb-118">**Шаблон**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
