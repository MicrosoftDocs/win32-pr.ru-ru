---
description: Получает логическое значение, указывающее, помечено ли расширение Кэйусаже как критическое.
ms.assetid: f7d53570-2b89-40a9-ab56-fcae4e4cb70c
title: Свойство Кэйусаже. Critical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b1829da9c9ddbcf5261f4cc595b72b8596193078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685038"
---
# <a name="keyusageiscritical-property"></a><span data-ttu-id="c4d6b-103">Свойство Кэйусаже. Critical</span><span class="sxs-lookup"><span data-stu-id="c4d6b-103">KeyUsage.IsCritical property</span></span>

<span data-ttu-id="c4d6b-104">\[Свойство « **критическое** » доступно для использования в операционных системах, указанных в разделе «требования».</span><span class="sxs-lookup"><span data-stu-id="c4d6b-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c4d6b-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c4d6b-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c4d6b-106">Свойство « **Critical** » получает логическое значение, указывающее, помечено ли расширение кэйусаже как критическое.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-106">The **IsCritical** property retrieves a Boolean value that indicates whether the KeyUsage extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4d6b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4d6b-107">Syntax</span></span>


```VB
KeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c4d6b-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c4d6b-108">Property value</span></span>

<span data-ttu-id="c4d6b-109">Если **значение — true**, расширение кэйусаже помечено как критическое.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-109">If **true**, the KeyUsage extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4d6b-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c4d6b-110">Requirements</span></span>



| <span data-ttu-id="c4d6b-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c4d6b-111">Requirement</span></span> | <span data-ttu-id="c4d6b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c4d6b-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d6b-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c4d6b-113">Redistributable</span></span><br/> | <span data-ttu-id="c4d6b-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="c4d6b-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c4d6b-115">DLL</span><span class="sxs-lookup"><span data-stu-id="c4d6b-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="c4d6b-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4d6b-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4d6b-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4d6b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d6b-118">**кэйусаже**</span><span class="sxs-lookup"><span data-stu-id="c4d6b-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
