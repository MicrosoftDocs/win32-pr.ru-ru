---
description: Извлекает коллекцию, содержащую все сертификаты в хранилище.
ms.assetid: 06cfc0e9-8a77-4e10-b559-4d42ac93c01b
title: Свойство Store. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 979cf31c98286ca5bdd2df709176a27a5abb2321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648691"
---
# <a name="storecertificates-property"></a><span data-ttu-id="61ec6-103">Свойство Store. Certificates</span><span class="sxs-lookup"><span data-stu-id="61ec6-103">Store.Certificates property</span></span>

<span data-ttu-id="61ec6-104">\[Свойство **Certificates** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="61ec6-104">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="61ec6-105">Вместо этого используйте [**класс X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="61ec6-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="61ec6-106">Свойство **Certificates** извлекает коллекцию, содержащую все сертификаты в хранилище.</span><span class="sxs-lookup"><span data-stu-id="61ec6-106">The **Certificates** property retrieves the collection that includes all of the certificates in the store.</span></span> <span data-ttu-id="61ec6-107">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61ec6-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ec6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61ec6-108">Syntax</span></span>


```VB
Store.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="61ec6-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="61ec6-109">Property value</span></span>

<span data-ttu-id="61ec6-110">Коллекция сертификатов в хранилище.</span><span class="sxs-lookup"><span data-stu-id="61ec6-110">The collection of certificates in the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="61ec6-111">Требования</span><span class="sxs-lookup"><span data-stu-id="61ec6-111">Requirements</span></span>



| <span data-ttu-id="61ec6-112">Требование</span><span class="sxs-lookup"><span data-stu-id="61ec6-112">Requirement</span></span> | <span data-ttu-id="61ec6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="61ec6-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61ec6-114">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="61ec6-114">Redistributable</span></span><br/> | <span data-ttu-id="61ec6-115">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="61ec6-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="61ec6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="61ec6-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="61ec6-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61ec6-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61ec6-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61ec6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ec6-119">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="61ec6-119">**Store**</span></span>](store.md)
</dt> </dl>

 

 
