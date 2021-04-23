---
description: Возвращает дополнительный номер версии шаблона.
ms.assetid: 3fc51d43-9113-4b4b-88ab-27cf6e5c4fa0
title: Свойство Template. MinorVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MinorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a1de0beb41cbe87ca86b443c5cc2145c2058073
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648891"
---
# <a name="templateminorversion-property"></a><span data-ttu-id="b82af-103">Свойство Template. MinorVersion</span><span class="sxs-lookup"><span data-stu-id="b82af-103">Template.MinorVersion property</span></span>

<span data-ttu-id="b82af-104">\[Свойство **minorversion** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b82af-104">\[The **MinorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b82af-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для шаблона сертификата для получения шаблона расширения сертификата.\]</span><span class="sxs-lookup"><span data-stu-id="b82af-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="b82af-106">Свойство **minorversion** извлекает дополнительный номер версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="b82af-106">The **MinorVersion** property retrieves the minor version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="b82af-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b82af-107">Syntax</span></span>


```VB
Template.MinorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="b82af-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b82af-108">Property value</span></span>

<span data-ttu-id="b82af-109">Дополнительный номер версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="b82af-109">The minor version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="b82af-110">Требования</span><span class="sxs-lookup"><span data-stu-id="b82af-110">Requirements</span></span>



| <span data-ttu-id="b82af-111">Требование</span><span class="sxs-lookup"><span data-stu-id="b82af-111">Requirement</span></span> | <span data-ttu-id="b82af-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b82af-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b82af-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b82af-113">Redistributable</span></span><br/> | <span data-ttu-id="b82af-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="b82af-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b82af-115">DLL</span><span class="sxs-lookup"><span data-stu-id="b82af-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="b82af-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b82af-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b82af-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b82af-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b82af-118">**Шаблон**</span><span class="sxs-lookup"><span data-stu-id="b82af-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
