---
description: Свойство Algorithm извлекает объект OID, определяющий алгоритм, используемый открытым ключом. Это свойство по умолчанию.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: Свойство PublicKey. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668724"
---
# <a name="publickeyalgorithm-property"></a><span data-ttu-id="4eed8-104">Свойство PublicKey. Algorithm</span><span class="sxs-lookup"><span data-stu-id="4eed8-104">PublicKey.Algorithm property</span></span>

<span data-ttu-id="4eed8-105">\[Свойство **Algorithm** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4eed8-105">\[The **Algorithm** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4eed8-106">Вместо этого используйте [**свойство X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4eed8-106">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4eed8-107">Свойство **Algorithm** извлекает объект [**OID**](oid.md) , определяющий алгоритм, используемый открытым ключом.</span><span class="sxs-lookup"><span data-stu-id="4eed8-107">The **Algorithm** property retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="4eed8-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4eed8-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eed8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4eed8-109">Syntax</span></span>


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a><span data-ttu-id="4eed8-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4eed8-110">Property value</span></span>

<span data-ttu-id="4eed8-111">Объект [**OID**](oid.md) , определяющий алгоритм, используемый открытым ключом.</span><span class="sxs-lookup"><span data-stu-id="4eed8-111">The [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eed8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4eed8-112">Requirements</span></span>



| <span data-ttu-id="4eed8-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4eed8-113">Requirement</span></span> | <span data-ttu-id="4eed8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4eed8-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4eed8-115">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="4eed8-115">Redistributable</span></span><br/> | <span data-ttu-id="4eed8-116">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="4eed8-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4eed8-117">DLL</span><span class="sxs-lookup"><span data-stu-id="4eed8-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="4eed8-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4eed8-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eed8-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4eed8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eed8-120">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="4eed8-120">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
