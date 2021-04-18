---
description: Возвращает основной номер версии шаблона.
ms.assetid: efde3a7c-48e0-4bfe-9118-3098c7ef8771
title: Свойство Template. MajorVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MajorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a193a36ed7e914d1ed45d26c21008a7e59a5b8a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668972"
---
# <a name="templatemajorversion-property"></a><span data-ttu-id="6c8be-103">Свойство Template. MajorVersion</span><span class="sxs-lookup"><span data-stu-id="6c8be-103">Template.MajorVersion property</span></span>

<span data-ttu-id="6c8be-104">\[Свойство **majorversion** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="6c8be-104">\[The **MajorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6c8be-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для шаблона сертификата для получения шаблона расширения сертификата.\]</span><span class="sxs-lookup"><span data-stu-id="6c8be-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="6c8be-106">Свойство **majorversion** извлекает основной номер версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="6c8be-106">The **MajorVersion** property retrieves the major version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c8be-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c8be-107">Syntax</span></span>


```VB
Template.MajorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="6c8be-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6c8be-108">Property value</span></span>

<span data-ttu-id="6c8be-109">Основной номер версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="6c8be-109">The major version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8be-110">Требования</span><span class="sxs-lookup"><span data-stu-id="6c8be-110">Requirements</span></span>



| <span data-ttu-id="6c8be-111">Требование</span><span class="sxs-lookup"><span data-stu-id="6c8be-111">Requirement</span></span> | <span data-ttu-id="6c8be-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6c8be-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8be-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6c8be-113">Redistributable</span></span><br/> | <span data-ttu-id="6c8be-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c8be-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6c8be-115">DLL</span><span class="sxs-lookup"><span data-stu-id="6c8be-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="6c8be-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c8be-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c8be-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c8be-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8be-118">**Шаблон**</span><span class="sxs-lookup"><span data-stu-id="6c8be-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
