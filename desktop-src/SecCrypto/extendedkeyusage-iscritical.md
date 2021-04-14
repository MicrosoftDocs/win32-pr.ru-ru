---
description: Возвращает логическое значение, указывающее, помечено ли расширение EKU как критическое.
ms.assetid: f6d2a2e0-512b-44f2-a7d9-9ad661398aa8
title: Свойство Екстендедкэйусаже. Critical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5331922567af3b9a34517ab5059fa03ad9904270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648127"
---
# <a name="extendedkeyusageiscritical-property"></a><span data-ttu-id="47a9e-103">Свойство Екстендедкэйусаже. Critical</span><span class="sxs-lookup"><span data-stu-id="47a9e-103">ExtendedKeyUsage.IsCritical property</span></span>

<span data-ttu-id="47a9e-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47a9e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="47a9e-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="47a9e-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="47a9e-106">Свойство « **Critical** » возвращает логическое значение, указывающее, помечено ли расширение EKU как критическое.</span><span class="sxs-lookup"><span data-stu-id="47a9e-106">The **IsCritical** property returns a Boolean value that indicates whether the EKU extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="47a9e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47a9e-107">Syntax</span></span>


```VB
ExtendedKeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="47a9e-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="47a9e-108">Property value</span></span>

<span data-ttu-id="47a9e-109">Если **значение — true**, расширение EKU помечено как критическое.</span><span class="sxs-lookup"><span data-stu-id="47a9e-109">If **true**, the EKU extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="47a9e-110">Требования</span><span class="sxs-lookup"><span data-stu-id="47a9e-110">Requirements</span></span>



| <span data-ttu-id="47a9e-111">Требование</span><span class="sxs-lookup"><span data-stu-id="47a9e-111">Requirement</span></span> | <span data-ttu-id="47a9e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="47a9e-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47a9e-113">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="47a9e-113">End of client support</span></span><br/> | <span data-ttu-id="47a9e-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47a9e-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="47a9e-115">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="47a9e-115">End of server support</span></span><br/> | <span data-ttu-id="47a9e-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47a9e-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="47a9e-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="47a9e-117">Redistributable</span></span><br/>       | <span data-ttu-id="47a9e-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="47a9e-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="47a9e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="47a9e-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="47a9e-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47a9e-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47a9e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47a9e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a9e-122">**екстендедкэйусаже**</span><span class="sxs-lookup"><span data-stu-id="47a9e-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
