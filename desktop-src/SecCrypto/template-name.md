---
description: Извлекает имя шаблона.
ms.assetid: f92346bc-89b6-4063-aa66-85e2fb88d67d
title: Template.Name, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 005a9cc961b1d7be0ebda0b8e76307b95d92a6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668971"
---
# <a name="templatename-property"></a><span data-ttu-id="c5103-103">Template.Name, свойство</span><span class="sxs-lookup"><span data-stu-id="c5103-103">Template.Name property</span></span>

<span data-ttu-id="c5103-104">\[Свойство **Name** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="c5103-104">\[The **Name** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c5103-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для шаблона сертификата для получения шаблона расширения сертификата.\]</span><span class="sxs-lookup"><span data-stu-id="c5103-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="c5103-106">Свойство **Name** извлекает имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="c5103-106">The **Name** property retrieves the name of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5103-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5103-107">Syntax</span></span>


```VB
Template.Name As String
```



## <a name="property-value"></a><span data-ttu-id="c5103-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c5103-108">Property value</span></span>

<span data-ttu-id="c5103-109">Имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="c5103-109">The name of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5103-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c5103-110">Requirements</span></span>



| <span data-ttu-id="c5103-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c5103-111">Requirement</span></span> | <span data-ttu-id="c5103-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c5103-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5103-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c5103-113">Redistributable</span></span><br/> | <span data-ttu-id="c5103-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5103-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c5103-115">DLL</span><span class="sxs-lookup"><span data-stu-id="c5103-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="c5103-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5103-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5103-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5103-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5103-118">**Шаблон**</span><span class="sxs-lookup"><span data-stu-id="c5103-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
