---
description: Получает логическое значение, указывающее, задан ли бит ДатаенЦифермент.
ms.assetid: 9b29a76f-1494-4db3-a5d7-69fe631ca1dd
title: Кэйусаже. ИсдатаенЦиферментенаблед, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDataEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aad6cbcd21830ad127b9537749dfb1c05a4c9ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685037"
---
# <a name="keyusageisdataenciphermentenabled-property"></a><span data-ttu-id="19ac1-103">Кэйусаже. ИсдатаенЦиферментенаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="19ac1-103">KeyUsage.IsDataEnciphermentEnabled property</span></span>

<span data-ttu-id="19ac1-104">\[Свойство **исдатаенЦиферментенаблед** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="19ac1-104">\[The **IsDataEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="19ac1-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="19ac1-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="19ac1-106">Свойство **исдатаенЦиферментенаблед** Извлекает логическое значение, указывающее, задан ли бит датаенЦифермент.</span><span class="sxs-lookup"><span data-stu-id="19ac1-106">The **IsDataEnciphermentEnabled** property retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ac1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19ac1-107">Syntax</span></span>


```VB
KeyUsage.IsDataEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="19ac1-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="19ac1-108">Property value</span></span>

<span data-ttu-id="19ac1-109">Если **значение равно true**, бит датаенЦифермент установлен.</span><span class="sxs-lookup"><span data-stu-id="19ac1-109">If **true**, the dataEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ac1-110">Требования</span><span class="sxs-lookup"><span data-stu-id="19ac1-110">Requirements</span></span>



| <span data-ttu-id="19ac1-111">Требование</span><span class="sxs-lookup"><span data-stu-id="19ac1-111">Requirement</span></span> | <span data-ttu-id="19ac1-112">Значение</span><span class="sxs-lookup"><span data-stu-id="19ac1-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19ac1-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="19ac1-113">Redistributable</span></span><br/> | <span data-ttu-id="19ac1-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="19ac1-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="19ac1-115">DLL</span><span class="sxs-lookup"><span data-stu-id="19ac1-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="19ac1-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19ac1-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19ac1-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19ac1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ac1-118">**кэйусаже**</span><span class="sxs-lookup"><span data-stu-id="19ac1-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
