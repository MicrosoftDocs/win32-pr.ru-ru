---
description: Извлекает коллекцию сертификатов, связанную с объектом Сигнеддата. После извлечения можно перечислить отдельные объекты сертификата в коллекции.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: Сигнеддата. Certificates, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668487"
---
# <a name="signeddatacertificates-property"></a><span data-ttu-id="55f81-104">Сигнеддата. Certificates, свойство</span><span class="sxs-lookup"><span data-stu-id="55f81-104">SignedData.Certificates property</span></span>

<span data-ttu-id="55f81-105">\[Свойство **Certificates** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="55f81-105">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="55f81-106">Вместо этого используйте [**класс SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="55f81-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="55f81-107">Свойство **Certificates** извлекает коллекцию [**сертификатов**](certificates.md) , связанную с объектом [**сигнеддата**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="55f81-107">The **Certificates** property retrieves the [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span> <span data-ttu-id="55f81-108">После извлечения можно перечислить отдельные объекты [**сертификата**](certificate.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="55f81-108">After being retrieved, the individual [**Certificate**](certificate.md) objects in the collection can be enumerated.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f81-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55f81-109">Syntax</span></span>


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="55f81-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="55f81-110">Property value</span></span>

<span data-ttu-id="55f81-111">Коллекция [**сертификатов**](certificates.md) , связанная с объектом [**сигнеддата**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="55f81-111">The [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="55f81-112">Требования</span><span class="sxs-lookup"><span data-stu-id="55f81-112">Requirements</span></span>



| <span data-ttu-id="55f81-113">Требование</span><span class="sxs-lookup"><span data-stu-id="55f81-113">Requirement</span></span> | <span data-ttu-id="55f81-114">Значение</span><span class="sxs-lookup"><span data-stu-id="55f81-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55f81-115">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="55f81-115">Redistributable</span></span><br/> | <span data-ttu-id="55f81-116">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="55f81-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="55f81-117">DLL</span><span class="sxs-lookup"><span data-stu-id="55f81-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="55f81-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55f81-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55f81-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55f81-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f81-120">**сигнеддата**</span><span class="sxs-lookup"><span data-stu-id="55f81-120">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
