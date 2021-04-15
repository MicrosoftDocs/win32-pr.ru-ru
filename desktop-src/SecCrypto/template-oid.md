---
description: Извлекает объект OID, определяющий объект шаблона.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Свойство Template. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648890"
---
# <a name="templateoid-property"></a><span data-ttu-id="0e396-103">Свойство Template. OID</span><span class="sxs-lookup"><span data-stu-id="0e396-103">Template.OID property</span></span>

<span data-ttu-id="0e396-104">\[Свойство **OID** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0e396-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0e396-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для шаблона сертификата для получения шаблона расширения сертификата.\]</span><span class="sxs-lookup"><span data-stu-id="0e396-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="0e396-106">Свойство **OID** извлекает объект [**OID**](oid.md) , определяющий объект [**шаблона**](template.md) .</span><span class="sxs-lookup"><span data-stu-id="0e396-106">The **OID** property retrieves an [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

<span data-ttu-id="0e396-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0e396-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e396-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e396-108">Syntax</span></span>


```VB
Template.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="0e396-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0e396-109">Property value</span></span>

<span data-ttu-id="0e396-110">Объект [**OID**](oid.md) , определяющий объект [**шаблона**](template.md) .</span><span class="sxs-lookup"><span data-stu-id="0e396-110">An [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e396-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0e396-111">Requirements</span></span>



| <span data-ttu-id="0e396-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0e396-112">Requirement</span></span> | <span data-ttu-id="0e396-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0e396-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e396-114">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0e396-114">Redistributable</span></span><br/> | <span data-ttu-id="0e396-115">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0e396-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0e396-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0e396-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="0e396-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e396-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e396-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e396-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e396-119">**Шаблон**</span><span class="sxs-lookup"><span data-stu-id="0e396-119">**Template**</span></span>](template.md)
</dt> </dl>

 

 
