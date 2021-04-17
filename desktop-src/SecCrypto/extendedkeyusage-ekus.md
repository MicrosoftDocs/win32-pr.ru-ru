---
description: Возвращает коллекцию EKU для сертификата.
ms.assetid: 64211a00-7d4d-4381-a134-9cd570ed7dbb
title: Екстендедкэйусаже. EKU, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 24bcf7b4332e75afad0e21415a7dfe8eb690c32b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665089"
---
# <a name="extendedkeyusageekus-property"></a><span data-ttu-id="5a0c3-103">Екстендедкэйусаже. EKU, свойство</span><span class="sxs-lookup"><span data-stu-id="5a0c3-103">ExtendedKeyUsage.EKUs property</span></span>

<span data-ttu-id="5a0c3-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5a0c3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5a0c3-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="5a0c3-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5a0c3-106">Свойство **EKU** Возвращает коллекцию [**EKU**](ekus.md) для сертификата.</span><span class="sxs-lookup"><span data-stu-id="5a0c3-106">The **EKUs** property returns the [**EKUs**](ekus.md) collection for the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a0c3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a0c3-107">Syntax</span></span>


```VB
ExtendedKeyUsage.EKUs As EKUs
```



## <a name="property-value"></a><span data-ttu-id="5a0c3-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5a0c3-108">Property value</span></span>

<span data-ttu-id="5a0c3-109">Коллекция [**EKU**](ekus.md) , содержащая объекты [**EKU**](eku.md) для сертификата.</span><span class="sxs-lookup"><span data-stu-id="5a0c3-109">The [**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a0c3-110">Требования</span><span class="sxs-lookup"><span data-stu-id="5a0c3-110">Requirements</span></span>



| <span data-ttu-id="5a0c3-111">Требование</span><span class="sxs-lookup"><span data-stu-id="5a0c3-111">Requirement</span></span> | <span data-ttu-id="5a0c3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="5a0c3-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a0c3-113">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5a0c3-113">End of client support</span></span><br/> | <span data-ttu-id="5a0c3-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a0c3-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5a0c3-115">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="5a0c3-115">End of server support</span></span><br/> | <span data-ttu-id="5a0c3-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a0c3-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5a0c3-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="5a0c3-117">Redistributable</span></span><br/>       | <span data-ttu-id="5a0c3-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a0c3-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5a0c3-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5a0c3-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5a0c3-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a0c3-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a0c3-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a0c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a0c3-122">**екстендедкэйусаже**</span><span class="sxs-lookup"><span data-stu-id="5a0c3-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
