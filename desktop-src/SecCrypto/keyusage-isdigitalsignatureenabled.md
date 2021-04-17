---
description: Получает логическое значение, указывающее, задан ли бит Дигиталсигнатуре.
ms.assetid: 561eea86-ff23-4a26-adf2-b43009566eaa
title: Кэйусаже. Исдигиталсигнатуринаблед, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDigitalSignatureEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b323effebe60597e1d6cf66e75d48c39fcdca4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685036"
---
# <a name="keyusageisdigitalsignatureenabled-property"></a><span data-ttu-id="e3067-103">Кэйусаже. Исдигиталсигнатуринаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="e3067-103">KeyUsage.IsDigitalSignatureEnabled property</span></span>

<span data-ttu-id="e3067-104">\[Свойство **исдигиталсигнатуринаблед** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="e3067-104">\[The **IsDigitalSignatureEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e3067-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e3067-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e3067-106">Свойство **исдигиталсигнатуринаблед** Извлекает логическое значение, указывающее, задан ли бит дигиталсигнатуре.</span><span class="sxs-lookup"><span data-stu-id="e3067-106">The **IsDigitalSignatureEnabled** property retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3067-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3067-107">Syntax</span></span>


```VB
KeyUsage.IsDigitalSignatureEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e3067-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e3067-108">Property value</span></span>

<span data-ttu-id="e3067-109">Если **значение равно true**, бит дигиталсигнатуре установлен.</span><span class="sxs-lookup"><span data-stu-id="e3067-109">If **true**, the digitalSignature bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3067-110">Требования</span><span class="sxs-lookup"><span data-stu-id="e3067-110">Requirements</span></span>



| <span data-ttu-id="e3067-111">Требование</span><span class="sxs-lookup"><span data-stu-id="e3067-111">Requirement</span></span> | <span data-ttu-id="e3067-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e3067-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3067-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e3067-113">Redistributable</span></span><br/> | <span data-ttu-id="e3067-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="e3067-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e3067-115">DLL</span><span class="sxs-lookup"><span data-stu-id="e3067-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="e3067-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3067-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3067-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3067-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3067-118">**кэйусаже**</span><span class="sxs-lookup"><span data-stu-id="e3067-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
