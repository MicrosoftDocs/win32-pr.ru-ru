---
description: Возвращает логическое значение, указывающее, имеется ли расширение EKU. Это свойство по умолчанию.
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: Екстендедкэйусаже. Present, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 785fa3c973e7f90eeab20bd76826b9e5bf612891
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668869"
---
# <a name="extendedkeyusageispresent-property"></a><span data-ttu-id="7a39f-104">Екстендедкэйусаже. Present, свойство</span><span class="sxs-lookup"><span data-stu-id="7a39f-104">ExtendedKeyUsage.IsPresent property</span></span>

<span data-ttu-id="7a39f-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7a39f-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7a39f-106">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7a39f-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7a39f-107">Свойство **Present** возвращает логическое значение, указывающее, имеется ли расширение EKU.</span><span class="sxs-lookup"><span data-stu-id="7a39f-107">The **IsPresent** property returns a Boolean value that indicates whether the EKU extension is present.</span></span> <span data-ttu-id="7a39f-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a39f-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a39f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a39f-109">Syntax</span></span>


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="7a39f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7a39f-110">Property value</span></span>

<span data-ttu-id="7a39f-111">Если задано **значение true**, расширение EKU имеется.</span><span class="sxs-lookup"><span data-stu-id="7a39f-111">If **true**, the EKU extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a39f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7a39f-112">Requirements</span></span>



| <span data-ttu-id="7a39f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7a39f-113">Requirement</span></span> | <span data-ttu-id="7a39f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7a39f-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a39f-115">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7a39f-115">End of client support</span></span><br/> | <span data-ttu-id="7a39f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a39f-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7a39f-117">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7a39f-117">End of server support</span></span><br/> | <span data-ttu-id="7a39f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a39f-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7a39f-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7a39f-119">Redistributable</span></span><br/>       | <span data-ttu-id="7a39f-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a39f-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7a39f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7a39f-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7a39f-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a39f-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a39f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a39f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a39f-124">**екстендедкэйусаже**</span><span class="sxs-lookup"><span data-stu-id="7a39f-124">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
