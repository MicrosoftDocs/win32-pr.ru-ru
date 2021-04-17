---
description: Получает логическое значение, указывающее, задан ли бит Кэйцертсигн.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: Кэйусаже. Искэйцертсигненаблед, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyCertSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d475565896910f76211e3843526e9a889586efa0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685027"
---
# <a name="keyusageiskeycertsignenabled-property"></a><span data-ttu-id="6ef0a-103">Кэйусаже. Искэйцертсигненаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="6ef0a-103">KeyUsage.IsKeyCertSignEnabled property</span></span>

<span data-ttu-id="6ef0a-104">\[Свойство **искэйцертсигненаблед** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="6ef0a-104">\[The **IsKeyCertSignEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6ef0a-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6ef0a-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6ef0a-106">Свойство **искэйцертсигненаблед** Извлекает логическое значение, указывающее, задан ли бит кэйцертсигн.</span><span class="sxs-lookup"><span data-stu-id="6ef0a-106">The **IsKeyCertSignEnabled** property retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef0a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ef0a-107">Syntax</span></span>


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6ef0a-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6ef0a-108">Property value</span></span>

<span data-ttu-id="6ef0a-109">Если **значение равно true**, бит кэйцертсигн установлен.</span><span class="sxs-lookup"><span data-stu-id="6ef0a-109">If **true**, the keyCertSign bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef0a-110">Требования</span><span class="sxs-lookup"><span data-stu-id="6ef0a-110">Requirements</span></span>



| <span data-ttu-id="6ef0a-111">Требование</span><span class="sxs-lookup"><span data-stu-id="6ef0a-111">Requirement</span></span> | <span data-ttu-id="6ef0a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6ef0a-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef0a-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6ef0a-113">Redistributable</span></span><br/> | <span data-ttu-id="6ef0a-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ef0a-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6ef0a-115">DLL</span><span class="sxs-lookup"><span data-stu-id="6ef0a-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="6ef0a-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ef0a-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ef0a-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ef0a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef0a-118">**кэйусаже**</span><span class="sxs-lookup"><span data-stu-id="6ef0a-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
